# AILadies – Onboarding proces a CRM

---

## Onboarding klientky – checklist

### Před prvním sezením

- [ ] Přišel vyplněný formulář z webu (notifikace na hello@ailadies.cz)
- [ ] Přečíst formulář – zapsat si klíčové body
- [ ] Pokud nahrála hlasovou zprávu – poslechnout a poznamenat
- [ ] Odpovědět do 24 hodin:
  - Poděkovat za zprávu
  - Navrhnout 2–3 termíny (sdílet volné sloty z Google Calendar)
- [ ] Klientka potvrdí termín → vytvořit událost v Google Calendar s Google Meet odkazem
- [ ] Vytvořit Google Drive složku: `AILadies/Klientky/[Jmeno_Prijmeni]/`
- [ ] Přidat klientku do Google Sheets (CRM)
- [ ] Připravit se na sezení (15–20 min):
  - Jaké nástroje jí doporučit?
  - Jaký prompt / šablona jí pomůže nejvíc?
  - Jaký je realistický výstup z první hodiny?

### Během sezení (60 min)

- [ ] Na začátku informovat o nahrávání a získat souhlas
- [ ] Zapnout nahrávání
- [ ] Představení (5 min) – ověřit info z formuláře
- [ ] Hlavní blok (45 min) – pracovat na konkrétním problému
- [ ] Shrnutí a další kroky (10 min)
- [ ] Poznamenat si klíčové body do CRM (hned po sezení)

### Po sezení (do 2 hodin)

- [ ] Zpracovat nahrávku v Cursoru → připravit materiály a prezentaci
- [ ] Nahrát prezentaci na GitHub Pages (za heslem)
- [ ] Odeslat e-mail "Souhrn po sezení" s odkazem a heslem
- [ ] Nahrát materiály do Google Drive složky klientky
- [ ] Vystavit fakturu (Google Sheets → Apps Script → PDF → e-mail)
- [ ] Aktualizovat CRM v Google Sheets

### Follow-up (3 dny po sezení)

- [ ] Odeslat follow-up e-mail
- [ ] Pokud klientka odpovídá – reagovat a nabídnout další sezení

### Po 2–3 sezeních

- [ ] Požádat o referenci/testimonial
- [ ] Smazat nahrávky starší než 30 dnů

---

## CRM – Google Sheets

### List 1: Klientky

| Sloupec | Popis |
|---|---|
| ID | K001, K002... |
| Jméno | Celé jméno |
| E-mail | Kontakt |
| Role / Obor | Co dělá |
| AI úroveň | Začátečnice / Zkusila / Občas / Pravidelně |
| Zdroj | Odkud přišla (web, LinkedIn, Aibility, doporučení...) |
| Datum prvního kontaktu | Kdy vyplnila formulář |
| Stav | Nová / Domluvená / Aktivní / Ukončená / Neodpověděla |
| Počet sezení | Celkem hodin |
| Poslední sezení | Datum |
| Další sezení | Datum |
| Celkem fakturováno | Kč |
| Testimonial | Ano/Ne |
| Poznámky | Cokoliv důležitého |

### List 2: Sezení (log)

| Sloupec | Popis |
|---|---|
| Datum | Datum a čas |
| ID klientky | K001... |
| Téma | Co jsme řešily (1–2 věty) |
| Výstupy | Prompt, šablona, nastavení... |
| Další kroky | Co si má vyzkoušet |
| Číslo faktury | Odkaz na list Fakturace |
| Stav platby | Zaplacena / Nezaplacena |
| Odkaz na materiály | GitHub Pages URL |

---

## Google Drive – Struktura složek

```
AILadies/
  Klientky/
    Jana_Novakova/
      01_vstupni_formular.pdf
      02_sezeni_2026-04-15/
        souhrn.md
        prompty.md
        sablona_tydenni_plan.md
      03_sezeni_2026-04-29/
        ...
    Marie_Kralova/
      ...
  Sablony/
    prompt_zasobnik.md
    sablona_souhrn_sezeni.md
  Reference/
    testimonial_jana_n.txt
  Fakturace/
    Faktury_2026/
      2026001_Jana_Novakova.pdf
    Sablona_faktury (Google Docs)
```

---

## Automatizace (přes Apps Script, postupně)

1. **Formulář → CRM:** Nový řádek v Sheets po vyplnění formuláře na webu (přes webhook/Macaly)
2. **Po sezení:** Připomínka v kalendáři "Odeslat souhrn [jméno]"
3. **Fakturace:** Generování a odeslání faktury z Sheets (viz AILadies_fakturacni_system.md)
4. **Follow-up:** Připomínka 3 dny po sezení
5. **Splatnost:** Denní kontrola nezaplacených faktur
