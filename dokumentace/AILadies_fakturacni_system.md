# AILadies – Fakturační systém (Google Workspace + Apps Script)

> Vlastní fakturační systém bez externích nástrojů. Vše běží v Google Workspace.

---

## Přehled systému

```
Google Sheets (databáze)     →  Apps Script (automatizace)  →  Google Docs (šablona faktury)
     ↓                              ↓                              ↓
Evidence klientek            Generuje fakturu              PDF faktura
Evidence sezení              Odesílá e-mail                Uložena na Drive
Přehled plateb               Sleduje splatnost             Příloha e-mailu
```

---

## Komponenty

### 1. Google Sheets – "AILadies Fakturace"

**List 1: Klientky**

| Sloupec | Popis | Příklad |
|---|---|---|
| ID klientky | Automatické (K001, K002...) | K001 |
| Jméno | Celé jméno | Jana Nováková |
| E-mail | Kontaktní e-mail | jana@example.cz |
| Firma / IČO | Pokud fakturuje na firmu | - |
| Adresa | Fakturační adresa | Praha 5, Smíchov |
| Poznámky | Cokoliv | Founding member |

**List 2: Sezení & Faktury**

| Sloupec | Popis | Příklad |
|---|---|---|
| Datum sezení | Kdy proběhlo | 2026-04-15 |
| ID klientky | Odkaz na list Klientky | K001 |
| Jméno | Auto-vyplní z Klientky | Jana Nováková |
| Délka (min) | Délka sezení | 60 |
| Cena | Cena za sezení | 3 000 |
| Číslo faktury | Auto-generované | 2026001 |
| Datum vystavení | Datum faktury | 2026-04-15 |
| Datum splatnosti | +14 dní | 2026-04-29 |
| Stav | Vystavena / Zaplacena / Po splatnosti | Vystavena |
| Datum platby | Kdy přišla platba | 2026-04-22 |
| PDF odkaz | Link na vygenerovanou fakturu | [odkaz] |
| E-mail odeslán | Ano / Ne | Ano |

**List 3: Nastavení**

| Parametr | Hodnota |
|---|---|
| Jméno poskytovatele | Petra Květová Pšeničná |
| IČO | [DOPLNIT] |
| Sídlo | [DOPLNIT] |
| Bankovní účet | [DOPLNIT] |
| Kód banky | [DOPLNIT] |
| E-mail | hello@ailadies.cz |
| Web | ailadies.cz |
| Prefix faktur | 2026 |
| Poslední číslo | 0 (auto-inkrementuje) |
| Splatnost (dní) | 14 |
| Text na faktuře | "Poskytovatel není plátcem DPH." |

**List 4: Dashboard**

| Metrika | Vzorec (příklad) |
|---|---|
| Příjem tento měsíc | =SUMIFS(Cena; Datum; ">="&EOMONTH(TODAY();-1)+1) |
| Příjem celkem | =SUM(Cena) |
| Nezaplacené faktury | =COUNTIF(Stav;"Vystavena") |
| Suma nezaplacených | =SUMIF(Stav;"Vystavena";Cena) |
| Po splatnosti | =COUNTIFS(Stav;"Vystavena";Splatnost;"<"&TODAY()) |
| Počet klientek celkem | =COUNTA(ID klientky) |
| Hodin tento měsíc | =SUMIFS(Délka;...)/60 |

---

### 2. Google Docs – Šablona faktury

Vytvořit šablonu faktury v Google Docs s placeholdery:

```
═══════════════════════════════════════════
                   FAKTURA
═══════════════════════════════════════════

Číslo faktury:    {{CISLO_FAKTURY}}
Datum vystavení:  {{DATUM_VYSTAVENI}}
Datum splatnosti: {{DATUM_SPLATNOSTI}}

───────────────────────────────────────────
DODAVATEL                    ODBĚRATEL
───────────────────────────────────────────
Petra Květová Pšeničná       {{JMENO_KLIENTKY}}
IČO: {{ICO}}                {{ADRESA_KLIENTKY}}
{{SIDLO}}                   {{ICO_KLIENTKY}}
{{EMAIL}}

───────────────────────────────────────────
POPIS SLUŽBY               ČÁSTKA
───────────────────────────────────────────
Osobní AI mentoring         {{CENA}} Kč
({{DELKA}} min, {{DATUM_SEZENI}})

───────────────────────────────────────────
CELKEM K ÚHRADĚ:           {{CENA}} Kč

Poskytovatel není plátcem DPH.

───────────────────────────────────────────
PLATEBNÍ ÚDAJE
───────────────────────────────────────────
Bankovní účet: {{UCET}} / {{KOD_BANKY}}
VS: {{VARIABILNI_SYMBOL}}

Prosím uhraďte do {{DATUM_SPLATNOSTI}}.
Děkuji za spolupráci.

                              Petra Květová Pšeničná
                              AILadies · ailadies.cz
═══════════════════════════════════════════
```

---

### 3. Google Drive – Struktura složek

```
AILadies/
  Fakturace/
    Faktury_2026/
      2026001_Jana_Novakova.pdf
      2026002_Marie_Kralova.pdf
    Sablona_faktury (Google Docs)
  Klientky/
    Jana_Novakova/
      materialy/
    Marie_Kralova/
      materialy/
```

---

### 4. Apps Script – Automatizace

**Co skript dělá:**

1. **Generuje fakturu:** Vezme data z Google Sheets → zkopíruje šablonu → nahradí placeholdery → exportuje jako PDF → uloží na Drive
2. **Odesílá e-mail:** Připojí PDF jako přílohu → odešle klientce
3. **Sleduje splatnost:** Denně kontroluje nezaplacené faktury po splatnosti → upozorní Petru e-mailem
4. **Auto-číslování:** Automaticky generuje číslo faktury (rok + pořadí)

**Funkce skriptu:**

```
generujFakturu(radek)
  → zkopíruje šablonu Google Docs
  → nahradí placeholdery daty z Sheets
  → exportuje jako PDF
  → uloží do složky Faktury_2026/
  → zapíše odkaz na PDF do Sheets

odesliEmail(radek)
  → vezme PDF z Drive
  → odešle e-mail klientce s přílohou
  → zapíše "Ano" do sloupce "E-mail odeslán"

kontrolujSplatnost()
  → projde všechny faktury se stavem "Vystavena"
  → pokud je datum splatnosti < dnes → pošle upozornění Petře
  → spouští se automaticky denně (trigger)

oznacZaplacenou(radek)
  → změní stav na "Zaplacena"
  → zapíše datum platby
```

**Spouštění:**

- **Generování faktury:** Tlačítko v Google Sheets ("Vystavit fakturu") nebo automaticky po vyplnění řádku
- **Odeslání e-mailu:** Tlačítko ("Odeslat klientce") nebo automaticky po generování
- **Kontrola splatnosti:** Denní trigger (každé ráno v 8:00)

---

## Jak to nastavit – krok za krokem

### Krok 1: Vytvořit Google Sheets
- [ ] Vytvořit nový spreadsheet "AILadies Fakturace"
- [ ] Vytvořit 4 listy (Klientky, Sezení & Faktury, Nastavení, Dashboard)
- [ ] Nastavit sloupce podle struktury výše
- [ ] Vyplnit list Nastavení (IČO, adresa, účet...)

### Krok 2: Vytvořit šablonu faktury
- [ ] Vytvořit Google Docs s šablonou (viz výše)
- [ ] Přidat logo AILadies
- [ ] Vložit placeholdery ve formátu {{PLACEHOLDER}}
- [ ] Naformátovat – čistý, profesionální design

### Krok 3: Vytvořit složkovou strukturu na Drive
- [ ] Vytvořit složku AILadies/Fakturace/Faktury_2026/
- [ ] Vytvořit složku AILadies/Klientky/

### Krok 4: Napsat Apps Script
- [ ] V Google Sheets: Rozšíření → Apps Script
- [ ] Napsat funkce (generujFakturu, odesliEmail, kontrolujSplatnost)
- [ ] Přidat tlačítko do Sheets ("Vystavit fakturu", "Odeslat klientce")
- [ ] Nastavit denní trigger pro kontrolu splatnosti

### Krok 5: Otestovat
- [ ] Vytvořit testovací klientku
- [ ] Vygenerovat testovací fakturu
- [ ] Ověřit, že PDF vypadá správně
- [ ] Ověřit, že e-mail se odešle s přílohou
- [ ] Ověřit, že kontrola splatnosti funguje

---

## Rozšíření (později)

- **QR platba:** Do faktury přidat QR kód pro platbu (Apps Script může generovat QR přes Google Charts API)
- **Automatická detekce platby:** Propojit s bankovním API (FIO, mBank) – kontrolovat příchozí platby a automaticky označit jako zaplacené
- **Měsíční report:** Automaticky generovat měsíční přehled příjmů a odeslat na e-mail
- **Připomínka nezaplacené faktury:** Automaticky odeslat klientce připomínku 3 dny po splatnosti

---

## Výhody tohoto řešení

- Žádné měsíční poplatky (vše v rámci Google Workspace, který už máš)
- Plná kontrola nad daty a formátem faktur
- Automatizace šetří čas (po nastavení stačí vyplnit řádek v Sheets)
- Vše na jednom místě (klientky, sezení, faktury, materiály)
- Snadno rozšiřitelné přes Apps Script
