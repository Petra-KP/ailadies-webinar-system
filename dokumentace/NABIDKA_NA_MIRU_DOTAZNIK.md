# AILadies – nabídka na míru (krátký dotazník + návod na vyhodnocení)

> ⚠️ **ARCHIV — v1.3.** Aktuální finální metodika (v2.0) je v [`METODIKA_AI_PLAN_NA_MIRU.md`](METODIKA_AI_PLAN_NA_MIRU.md). Tento dokument slouží jen jako historie předchozí verze.

**Účel:** Druhý, krátký formulář na [ailadies.cz](https://www.ailadies.cz/) vedle stávajícího dlouhého onboardingu. Slouží ženám, které chtějí **nejprve písemnou nabídku** a krátké „zasazení“, než se objednají na konzultaci.

**Platforma:** Formulář se vkládá a data ukládají v **Macaly** — níže je obsah připravený ke zkopírování do editoru.

**Tón:** tykání, podpora, bez technického žargonu (stejně jako zbytek webu AILadies).

---

## 1. Text nad formulářem (návrh pro web)

**Nadpis (H2):**  
Nabídka na míru

**Perex (1–2 věty):**  
Pár minut a pár otázek – a já ti připravím návrh, co by pro tebe mohlo dávat smysl: v čem vidím potenciál, co bych doporučila jako první krok a jestli dává smysl začít jednou hodinou nebo rovnou delším mentoringem (vždycky **jedna ku jedné**, podle tebe). Nic tě k ničemu nezavazuje.

**Podnadpis pod formulářem (drobný text):**  
Vyplnění zabere asi **8–12 minut**. **Hned po odeslání** ti na e-mail přijde **automatické potvrzení**, že formulář dorazil a že na nabídce pracuji. Osobní odpověď s návrhem ti pošlu co nejdřív.

---

## 2. Struktura dotazníku (pole pro Macaly)

Interní ID v závorkách jsou návrhy pro pojmenování polí v exportu / CRM; uprav podle konvence Macaly.

### Blok A – Kontakt

| Interní ID | Typ | Povinné | Text pro uživatele |
|------------|-----|---------|---------------------|
| `email` | e-mail | ano | E-mail (na něj ti pošlu návrh nabídky) |
| `jmeno` | krátký text | ne | Jak ti mám říkat? (jméno nebo přezdívka) |

### Blok B – Kde jsi teď s AI

| Interní ID | Typ | Povinné | Text / možnosti |
|------------|-----|---------|-----------------|
| `uroven_ai` | výběr jedné odpovědi (radio) | ano | **Kde teď jsi s AI?** |
| | | | • Úplně na začátku – zatím spíš zkouším, co to umí |
| | | | • Občas použiju chatbota, ale nemám v tom systém |
| | | | • Už AI používám pravidelně a chtěla bych to posunout dál |
| | | | • AI je součást mojí práce – řeším konkrétní nástroje nebo postupy |

**Poznámka k implementaci:** ikony (klíček, lupa, blesk, raketa) jsou volitelné — pokud Macaly umožňuje, vizuálně sjednotit se stávajícím dotazníkem.

### Blok C – Co tě nejvíc zajímá (zaměření)

| Interní ID | Typ | Povinné | Text / možnosti |
|------------|-----|---------|-----------------|
| `oblasti` | výběr více možností (checkbox) | ano, min. 1 | **Co bys chtěla s AI spíš řešit?** (zaškrtni vše, co sedí) |
| | | | • Texty a dokumenty (e-maily, smlouvy, podklady) |
| | | | • Prezentace, shrnutí, struktura myšlenek |
| | | | • Plánování, organizace, úkoly |
| | | | • Komunikace s lidmi (tým, klienti) |
| | | | • Osobní projekty nebo podnikání |
| | | | • Učení se novým věcem rychleji |
| | | | • Jiné (upřesním níže) |
| `oblasti_jine` | dlouhý text, řádky 2 | ne | Pokud jsi zaškrtla „Jiné“ – napiš stručně co |

### Blok D – Tvoje práce (kontext)

*(Aby šlo nabídku navázat na reálný den, ne jen na „AI obecně“.)*

| Interní ID | Typ | Povinné | Text / omezení |
|------------|-----|---------|----------------|
| `pracovni_role` | krátký text | ano | **Jaká je tvoje pracovní role nebo pozice?** (např. koordinátorka projektů, podnikatelka, specialistka v týmu…) |
| `co_delas` | dlouhý text, řádky 2–3 | ano | **Čemu se v práci nejvíc věnuješ?** Stačí jedna nebo dvě věty – o čem tvoje práce ve skutečnosti je. |
| `opakujici_ukoly` | dlouhý text | ano | **Co se u tebe v práci opakuje nejčastěji?** (např. e-maily, zápisy, reporty, příprava podkladů…) Klidně odrážky – jde mi o opakující se úkoly, ne o jednorázové projekty. |
| `co_te_bavi` | dlouhý text, řádky 2–3 | ano | **Co tě v práci baví nejvíc?** (klidně pár slov – ať vím, co ti drží energii.) |
| `co_te_nebavi` | dlouhý text, řádky 2–3 | ano | **Co tě v práci naopak nejvíc štve nebo vyčerpává?** |
| `v_cem_jsi_silna` | dlouhý text, řádky 2 | ano | **V čem jsi silná?** (dovednosti, zkušenosti – klidně i mimo AI.) |
| `jake_nastroje_pouzivas` | dlouhý text | ano | **Jaké nástroje s AI teď používáš?** (např. ChatGPT, Copilot, Claude, Gemini, něco jiného – napiš, co reálně otevíráš.) |
| `nastroje_free_nebo_placene` | výběr jedné | ano | **Tyhle nástroje máš spíš…** |
| | | | • většinou zdarma (free účty) |
| | | | • mix – něco free, něco placené |
| | | | • mám placené předplatné u jednoho nebo víc nástrojů |
| | | | • zatím skoro nic / nevím přesně |
| `ochota_investovat_nastroje` | výběr jedné | ano | **Kdyby ti konkrétní placený nástroj výrazně ulehčil práci – jsi ochotná do toho jít?** |
| | | | • ano, když uvidím smysl a cenu |
| | | | • radši zůstat u free variant |
| | | | • zatím nevím – záleží na situaci |

### Blok E – Cíl a překážky

| Interní ID | Typ | Povinné | Text / omezení |
|------------|-----|---------|----------------|
| `cil_1_mesic` | dlouhý text | ano | **Co by pro tebe bylo za měsíc úspěch v souvislosti s AI?** Stačí jedna věta nebo krátký odstavec – co bys chtěla stihnout nebo změnit. (doporučeno max. 500 znaků) |
| `prekazky_ai` | výběr více možností (checkbox) | ano, min. 1 | **Co ti teď nejvíc stojí v cestě k tomu, aby sis AI v práci osvojila – tak, aby ti opravdu pomáhala?** *(Zaškrtni vše, co na tebe sedí.)* |
| | | | • Nemám v klidu čas to zkoušet |
| | | | • Nevím, kde přesně začít – je toho moc |
| | | | • Bojím se chyby nebo „nejistého“ výstupu |
| | | | • Nástroje a nastavení mi připadají složité |
| | | | • Chybí mi někdo, kdo mi to ukáže v mém kontextu (ne obecné rady) |
| | | | • Jiné (upřesním níže) |
| `prekazky_jine` | krátký text | ne | Upřesnění u „Jiné“ |

### Blok F – Jedna otázka navíc (volitelná, „těžší“)

| Interní ID | Typ | Povinné | Text |
|------------|-----|---------|------|
| `zamysleni_navic` | dlouhý text | ne | **Kdybys měla AI použít jen na jednu konkrétní věc z tvé práce příští týden – co by to bylo a proč?** (Nepovinné; pomůže mi líp trefit první krok.) |

### Blok G – Čas a tempo

| Interní ID | Typ | Povinné | Text / možnosti |
|------------|-----|---------|-----------------|
| `cas_tydne` | výběr jedné | ano | **Kolik času týdně reálně můžeš dát práci s AI (učení, zkoušení)?** |
| | | | • Do 30 minut |
| | | | • Cca 30–60 minut |
| | | | • 1–2 hodiny |
| | | | • Víc než 2 hodiny – chci intenzivněji |
| `tempo` | výběr jedné | ano | **Jak ti vyhovuje tempo?** |
| | | | • Radši krátké kroky a vidět pokrok postupně |
| | | | • Radši větší soustředěné bloky občas |
| | | | • Nevím – potřebuju doporučit |

### Blok H – Otevřená poznámka

| Interní ID | Typ | Povinné | Text |
|------------|-----|---------|------|
| `poznamka` | dlouhý text | ne | **Je něco, co bych měla vědět, než ti napíšu nabídku?** (volitelné) |

### Blok I – Souhlas

| Interní ID | Typ | Povinné | Text |
|------------|-----|---------|------|
| `souhlas_gdpr` | checkbox | ano | Souhlasím se zpracováním osobních údajů za účelem přípravy nabídky a kontaktování ohledně služeb AILadies. [Odkaz na zásady zpracování osobních údajů] |

*(URL zásad doplň stejně jako u hlavního formuláře na webu.)*

---

## 3. Text po odeslání (děkovací stránka v Macaly)

**Nadpis:** Děkuju, zprávu mám

**Text:**  
Mrknu na tvé odpovědi a napíšu ti, co by podle mě dávalo smysl – včetně toho, jestli začít jednou hodinou nebo rovnou balíčkem sezení. Odpověď ti pošlu na e-mail, který jsi zadala. *(Automatické potvrzení o přijetí už máš v schránce.)*

---

## 3a. Automatický e-mail hned po odeslání (nastavit v Macaly)

Tento mail musí odejít **okamžitě** po odeslání formuláře (autoresponder / potvrzení příjmu).

**Předmět (návrh):** AILadies – mám tvůj dotazník, pracuji na nabídce

**Tělo (návrh):**

```
Ahoj [jméno, pokud vyplněno / „ahoj“],

díky za vyplnění dotazníku „Nabídka na míru“ – právě mi dorazil a začnu na něm pracovat.

Jakmile budu mít hotové, pošlu ti osobní odpověď s návrhem.

Kdyby ti mezitím něco napadlo, klidně odpověz na tenhle e-mail.

Těším se na spolupráci a na to, jaký posun spolu dokážeme udělat – nejen v AI, ale i v tom, jak ti práce bude líp sedět.

Petra
AILadies
```

*(V Macaly napoj na stejný e-mail odesílatele jako u ostatních automatických mailů z webu.)*

---

## 4. Předmět / štítek pro interní notifikaci

Aby šly odpovědi odlišit od hlavního dlouhého dotazníku:

- **Předmět e-mailu (návrh):** `[AILadies] Nabídka na míru – nový dotaz`
- Nebo štítek v Macaly: `nabidka_na_miru`

---

## 5. Návod na vyhodnocení (pro tebe)

Tenhle dotazník **nehodnotí „skóre“** a není psychotest. Slouží k tomu, abys rychle viděla **kontext, motivaci a kapacitu** – a mohla napsat **konkrétní, lidskou nabídku**.

### 5.1 Co si přečíst jako první

1. **`pracovni_role`, `co_delas`, `opakujici_ukoly`** – reálný kontext; tady ukotříš nabídku v jejím dni, ne v obecné teorii.
2. **`co_te_bavi`, `co_te_nebavi`, `v_cem_jsi_silna`** (pokud vyplněno) – tón, motivace, kde ji můžeš pochválit a kde šetřit čas.
3. **`jake_nastroje_pouzivas`, `nastroje_free_nebo_placene`, `ochota_investovat_nastroje`** – neslibovat placené nástroje, pokud nechce investovat; naopak otevřít placené varianty, když dávají smysl a je ochotná.
4. **`cil_1_mesic`** – co chce stihnout za měsíc; zrcadlení a návrh prvních kroků.
5. **`zamysleni_navic`** (pokud vyplněno) – často nejlepší háček na konkrétní první mentoringový úkol.
6. **`uroven_ai` + `oblasti`** – tón (začátečnice vs. pokročilá) a příklady nástrojů.
7. **`prekazky_ai`** – co ji brzdí → jak mluvit o bezpečí, krocích, času.
8. **`cas_tydne` + `tempo`** – realistický rozsah nabídky (jedna hodina vs. balíček; mentoring vždy 1:1).

### 5.2 Jak u `uroven_ai` uvažovat o rozsahu (hodina vs. balíček)

| Odpověď | Obecný signál | Směr doporučení |
|---------|----------------|-----------------|
| Úplně na začátku | Vysoká potřeba struktury a důvěry | Často sedí **úvodní konzultace zdarma** nebo **1× hodina** jako první krok; balíček až když sedne chemie. |
| Občas, bez systému | Chce návyk a konkrétní postupy | **Hodinový mentoring** nebo **krátký balíček (3×)** – důraz na opakovatelné rutiny. |
| Pravidelně, chci dál | Už ví, že to má smysl | **Balíček** (5× nebo 10×) nebo specializace podle `oblasti`. |
| Součást práce, nástroje | Často konkrétní workflow | Konkrétní nástroje + možná hlubší série; v textu ukázat, že rozumíš její roli. |

Tohle nejsou pevná pravidla – jen **heuristika**, než si přečteš celý text.

### 5.3a Nástroje a ochota investovat

- **`jake_nastroje_pouzivas`** – ověř si, že nenavrhneš nástroj, který už aktivně používá (nebo naopak navrhni upgrade, když free nestačí).
- **`nastroje_free_nebo_placene` + `ochota_investovat_nastroje`** – když je ochota investovat nízká, drž doporučení u free vrstev nebo nástrojů, které už platí; když je ochota vysoká, můžeš otevřít placené varianty s jasným „proč se to vyplatí“.

### 5.3b Překážky (`prekazky_ai`) → tón odpovědi

| Zaškrtnutá možnost | Co pomůže v nabídce |
|--------------------|---------------------|
| Nemám v klidu čas | Malé kroky, jeden konkrétní úkol z první hodiny; mentoring jako investice času, která se vrátí. |
| Nevím kde začít | Jedna **jasná dráha** (první, druhý krok), ne katalog nástrojů. |
| Bojím se chyby / nejistého výstupu | Bezpečný prostor, kontrolní otázky k výstupu, že „nejde o známku“. |
| Nástroje složité | Bez žargonu; začít od toho, co už má v počítači. |
| Chybí kontext učitele | Zdůrazni **1:1** a že se budeš dívat na *její* úkoly z `opakujici_ukoly`. |
| Jiné (`prekazky_jine`) | Číst doslova a odpovědět na to, co napsala. |

### 5.4 Čas a tempo → velikost nabídky

- **Do 30 min / krátké kroky** → spíš **1× hodina** nebo **Start (3×)** s jasným plánem mezi sezeními.
- **1–2 h nebo víc** → **balíčky** dávají smysl; u „intenzivněji“ můžeš nabídnout kratší interval sezení nebo domácí úkoly.
- **„Nevím – potřebuju doporučit“** → v e-mailu krátce **rozhodni ty** (např. „navrhuju začít jednou hodinou a podle toho…“).

### 5.5 Šablona odpovědi klientce (e-mail)

*(Uprav vždy podle `pracovni_role`, `co_delas`, `opakujici_ukoly`, `co_te_bavi` / `co_te_nebavi` / `v_cem_jsi_silna`, `jake_nastroje_pouzivas`, `cil_1_mesic`, `zamysleni_navic`, `poznamka`.)*

```
Předmět: AILadies – návrh pro tebe (podle tvého dotazníku)

Ahoj [jméno / Jak ti mám říkat],

díky za vyplnění – mám z toho dobrý obrázek o tom, kde jsi a co by pro tebe teď dávalo smysl.

[1 odstavec: zrcadlení role + čeho se dotýká její práce – z co_delas / opakujici_ukoly]

[volitelně: věta, co ji baví vs. co nebaví – z co_te_bavi / co_te_nebavi; pochvala silné stránky – z v_cem_jsi_silna]

[1 krátký odstavec: její cíl za měsíc – z cil_1_mesic]

Co vidím jako potenciál:
• [1–2 body – konkrétně k oblastem a úrovni AI]

Co bych doporučila jako první krok:
• [konkrétní – např. jedna oblast nástrojů nebo jeden typ úkolu]

Mentoring je vždycky jedna ku jedné – tady navrhni **rozsah**:
[1× 60 min / balíček Start (3×) nebo Rozjezd (5×) nebo … – podle webu – a krátce proč]

(Dřívější úvodní konzultaci zdarma zmiň jen když to dává smysl z kontextu.)

Další krok:
[odkaz na rezervaci / nabídka odpovědi na otázky / cena, pokud už dáváš konkrétní částku]

Těším se,
Petra
```

### 5.6 Kdy zvážit osobní poznámku

- Pokud je v `poznamka` nebo `prekazky_jine` něco citlivého (zdraví, velký stres v práci), odpověz **empaticky** a případně navrhni nejdřív krátký hovor místo dlouhého plánu.
- Pokud cíl není s AI úplně jasný, jedna věta typu: „Můžeme na prvním setkání nejdřív ujasnit, jestli je AI u toho vůbec ten hlavní nástroj.“

### 5.7 List k zamyšlení (úkol pro mentoring – ne do formuláře)

Tenhle blok **není** pole ve formuláři. Je to **příloha pro tebe**: můžeš vybrat 1–2 otázky a poslat je klientce **e-mailem po první konzultaci** nebo **jako domácí úkol před druhým sezením** – aby se nad svou prací a AI zastavila víc, než stihne v rychlém dotazníku.

**List (kopírovatelné):**

1. Když se podíváš na svůj minulý týden v práci: které **tři činnosti** ti sebraly nejvíc času bez toho, že by tě naplňovaly?
2. Který **jeden opakující se úkol** by ti přišel nejdřív na řadu k vyzkoušení s AI – a proč právě ten?
3. Co by se muselo stát, aby ses za měsíc na svou práci s AI dívala **o něco spokojeněji**? (jedna věta)
4. Kdy ti AI **nesedí** – protože výsledek, protože proces, nebo protože nevíš, jak zadat zadání?
5. Kdo v tvém okolí (v práci nebo doma) by z tvého lepšího používání AI měl **nejvíc užitek** – a jak by to u něj vypadalo?
6. Pokud bys měla vynechat jednu věc, kterou děláš „protože to tak má být“, ale ve skutečnosti je to zbytečné – co by to bylo?

*(Otázky můžeš zkrátit, přeskupit nebo doplnit o vlastní – podle toho, co z dotazníku už víš.)*

---

## 6. Verze dokumentu

| Verze | Datum | Poznámka |
|-------|--------|----------|
| 1.0 | 2026-04-15 | První verze obsahu + návod; platforma Macaly |
| 1.1 | 2026-04-15 | Rychlejší SLA + okamžitý mail; cíl za 1 měsíc; práce/kontext; překážky přeformulované; volitelné `zamysleni_navic`; příloha „list k zamyšlení“; přejmenování `bariera` → `prekazky_ai` |
| 1.2 | 2026-04-15 | Bavi/nebavi/silné stránky; nástroje + free/placené + investice; bez „formátu spolupráce“ a bez lhůty 24 h; bez odkazu na konzultaci na děkovné stránce; autoresponder s těšením na spolupráci a posun nejen v AI |
| 1.3 | 2026-04-15 | List k zamyšlení: „sežraly“ → „sebraly“; kompletní zadání pro Macaly v `MACALY_ZADANI_FORMULAR_NABIDKA_NA_MIRU.md` |

**Zadání pro implementaci ve Macaly (jeden soubor):** [`MACALY_ZADANI_FORMULAR_NABIDKA_NA_MIRU.md`](MACALY_ZADANI_FORMULAR_NABIDKA_NA_MIRU.md)

**Agent pro vyhodnocení odpovědí (Cursor):** [`../../../08_Agenti/agent_ailadies_nabidka_na_miru.md`](../../../08_Agenti/agent_ailadies_nabidka_na_miru.md)
