# AILadies – AI plán na míru (finální metodika v2)

> **Účel dokumentu:** Jeden zdroj pravdy pro **diagnostický dotazník** a **vyhodnocování odpovědí** v AILadies. Z tohoto dokumentu se odvíjí (1) zadání pro Macaly a (2) agent v Cursoru pro zpracování odpovědí.
>
> **Sjednocuje tři dřívější zdroje:**
>
> - `AILadies_Dotaznik_Metodika.md` (princip AI plán, 4 osy, šablony A/B/C, lead scoring, prompt pro automatizaci)
> - `ai_ladies_metodika.md` (typy klientek, urgence)
> - `NABIDKA_NA_MIRU_DOTAZNIK.md` (bavi/nebavi/silné stránky, list k zamyšlení, tón mentoring 1:1)
>
> **Další kroky po této metodice:** Macaly zadání (nový formulář) → úprava agenta v Cursoru → automatizace. Tento dokument pokrývá **jen metodiku**.

---

## OBSAH

1. [Cíl a princip „AI plán"](#1-cíl-a-princip-ai-plán)
2. [Finální podoba dotazníku](#2-finální-podoba-dotazníku)
3. [Metodika vyhodnocování – 4 osy](#3-metodika-vyhodnocování--4-osy)
4. [Typ klientky (praktická pomůcka)](#4-typ-klientky)
5. [Lead scoring a urgence](#5-lead-scoring-a-urgence)
6. [Struktura výstupního e-mailu](#6-struktura-výstupního-e-mailu)
7. [Šablony e-mailů podle úrovně](#7-šablony-e-mailů-podle-úrovně)
8. [Tipy podle oblasti zájmu](#8-tipy-podle-oblasti-zájmu)
9. [Interní záznam pro Petru](#9-interní-záznam-pro-petru)
10. [Prompt pro agenta / automatizaci](#10-prompt-pro-agenta)
11. [List k zamyšlení (volitelná nadstavba po konzultaci)](#11-list-k-zamyšlení)

---

## 1. Cíl a princip „AI plán"

### Co má dotazník udělat

- **Pro klientku:** Dát jí pocit, že vyplnění mělo smysl – že se nad svojí prací zamyslela a získala konkrétní hodnotu i bez objednání mentoringu.
- **Pro Petru:** Získat dost informací k tomu, aby mohla připravit personalizované doporučení a rozhodnout se, jak velký prostor klientce věnovat.
- **Pro byznys:** Přirozeně dovést klientku k objednání mentoringu – ne tlakem, ale logikou.

### Princip „AI plán"

Místo „vyhodnocení testu" pracujeme s konceptem **AI plánu** – směru posunu, ne charakteristiky.

Každá žena dostane do e-mailu obraz ve formátu:

> **Kde teď jsi → Kde máš největší potenciál → Co by byl první smysluplný krok**

### Co dotazník NENÍ

- ❌ Psychotest nebo skórovací tabulka pro klientku (bodování je **interní**, klientka ho nevidí).
- ❌ Assessment v duchu SP™ / Ability (AILadies je samostatný projekt, nemíchat s jinými metodikami Aibility).
- ❌ Místo pro prodejní tlak (ani v e-mailu).

### Tón

- Tykání, lidské, ženské, bez klišé.
- Mentoring je **vždy 1:1** – toto se nikdy neuvádí jako otázka („formát spolupráce 1:1"), ale jako **fakt** v nabídce. Otázka na formát se ptá jen na **rozsah** (jednorázové vs. balíček vs. intenzivnější).
- Žádné pevné sliby typu „odpovím do 24 hodin" – raději „pošlu co nejdřív" nebo „obvykle do 48 hodin".

---

## 2. Finální podoba dotazníku

> Formulář má **8 kroků**, vyplnění ~8 minut. Všechna interní ID (v závorkách / kurzívou) se použijí jako názvy polí v Macaly a jako klíče pro agenta.

### ÚVODNÍ OBRAZOVKA

**Nadpis:**
Chceš vědět, kde začít? Vyplň formulář a dostaneš AI plán přímo pro tebe.

**Text:**
Odpověz na pár otázek o tom, jak pracuješ a kde s AI jsi. Připravím ti konkrétní doporučení – kde začít, na čem pracovat a jak by mohl vypadat mentoring přesně pro tebe. Vyplnění tě k ničemu nezavazuje. Zabere to asi 8 minut.

**Tlačítko:** Začít

---

### KROK 1 — Kontakt

**Nadpis:** Jak se jmenuješ a kam ti mám AI plán poslat?


| Interní ID      | Typ         | Povinné | Label / popisek                                                 |
| --------------- | ----------- | ------- | --------------------------------------------------------------- |
| `jmeno`         | krátký text | ✅       | Jméno a příjmení                                                |
| `email`         | e-mail      | ✅       | E-mail                                                          |
| `firma_projekt` | krátký text | ❌       | Firma nebo projekt – např. název firmy, značky nebo projektu    |
| `web_linkedin`  | krátký text | ❌       | Web nebo LinkedIn – pomůže mi se připravit, klidně nech prázdné |


---

### KROK 2 — Vztah k AI

**Nadpis:** Jak bys popsala svůj aktuální vztah s AI?
**Typ:** výběr jedné možnosti · `uroven_ai`

- 🌱 Úplně na začátku – zatím spíš zkouším, co to umí
- 🔍 Občas použiju chatbota, ale nemám v tom systém
- ⚡ Už AI používám pravidelně a chtěla bych to posunout dál
- 🚀 AI je součást mojí práce – řeším konkrétní nástroje nebo postupy

---

### KROK 3 — Tvoje práce

**Nadpis:** Řekni mi víc o tom, co děláš

**3.1 Jaká je tvoje pracovní role?** · `pracovni_role`
*Výběr jedné možnosti + „Jiné"*

- Freelancerka / OSVČ
- Podnikatelka / majitelka firmy
- Manažerka / vedoucí týmu
- Koordinátorka / projektová manažerka
- Specialistka (marketing, HR, finance, právo…)
- Asistentka / office manager
- Učitelka / lektorka / koučka
- Pracuji v neziskovém sektoru
- Jiné: ______ · `pracovni_role_jine`

**3.2 Používáš AI primárně pro:** · `kontext_pouziti`
*Výběr jedné možnosti*

- Svoji práci / podnikání
- Práci ve firmě nebo organizaci
- Osobní věci / organizaci života
- Kombinaci

**3.3 Čemu se v práci nejvíc věnuješ?** · `cinnosti`
*Výběr více možností (max. 3) + „Jiné"*

- Komunikace a e-maily
- Tvorba obsahu (texty, sociální sítě, newslettery)
- Administrativa a organizace
- Práce s lidmi (tým, klienti, zákazníci)
- Vzdělávání nebo předávání znalostí
- Projekty a jejich řízení
- Obchod, nabídky, smlouvy
- Kreativní nebo vizuální tvorba
- Jiné: ______ · `cinnosti_jine`

**3.4 Co tě v práci nejvíc vyčerpává nebo zdržuje?** · `co_te_vycerpava`
*Dlouhý text — povinné* ✅

**3.5 Popiš jednu konkrétní věc, kterou děláš v práci opakovaně a která tě stojí nejvíc času nebo energie.** · `opakujici_ukol`
*Krátký až střední text — povinné* ✅
*Popisek:* Klidně jen jedna věta – třeba „každý týden píšu nabídky klientům" nebo „po každé schůzce přepisuji poznámky do e-mailu."

**3.6 Co tě v práci naopak baví nejvíc? V čem jsi silná?** · `co_te_bavi_silne_stranky`
*Dlouhý text — nepovinné*
*Popisek:* Ať v AI plánu zrcadlím i tvoje silné stránky, ne jen to, co chceš zautomatizovat.

---

### KROK 4 — Tvůj přístup a zkušenosti

**Nadpis:** Jak přistupuješ k novým věcem

**4.1 Jak bys popsala svůj vztah k technologiím obecně?** · `vztah_technologie`
*Výběr jedné možnosti*

- Nové věci zkouším ráda – technologie mě baví
- Zvládnu to, když vím proč – ale nechci trávit čas nastavováním
- Raději mám věci jednoduché – čím méně aplikací, tím líp
- Technologie mi dělají stres, ale vím, že to potřebuju překonat

**4.2 Prošla jsi už nějakým kurzem nebo vzděláváním zaměřeným na AI?** · `predchozi_vzdelavani`
*Výběr jedné možnosti*

- Ne, zatím nic
- Koukla jsem na pár videí nebo webinářů zdarma
- Byla jsem na placeném kurzu – ale moc mi to nepomohlo
- Byla jsem na kurzu a něco jsem si odnesla, ale chybí mi praxe
- Vzdělávám se průběžně sama – čtu, zkouším, testuji

**4.3 Když jsi AI zkusila a výsledek nebyl dobrý – co jsi udělala?** · `reakce_na_spatny_vystup`
*Výběr jedné možnosti*

- Zkusila jsem to znovu, upravila zadání
- Vzdala jsem to a vrátila se ke starému způsobu
- Nevěděla jsem, co s tím – výsledek jsem nepoužila
- Zatím jsem to moc nezkoušela

**4.4 Jak pracuješ, když se učíš něco nového?** · `styl_uceni`
*Výběr jedné možnosti*

- Zkouším hned v praxi – učím se za pochodu
- Potřebuji nejdřív pochopit princip, pak teprve zkouším
- Nejlépe se učím, když mi někdo ukáže postup krok za krokem
- Kombinuji – trochu teorie, trochu praxe

---

### KROK 5 — Co chceš s AI řešit

**Nadpis:** Na co bys AI nejvíc chtěla využít? · `use_case`
*Výběr více možností (max. 3) + „Jiné"*

- Psaní a úprava textů (e-maily, nabídky, posty)
- Shrnutí a strukturování informací
- Příprava prezentací nebo podkladů
- Plánování a organizace práce
- Komunikace s klienty nebo týmem
- Brainstorming a hledání nápadů
- Rychlejší učení se novým věcem
- Automatizace opakujících se úkolů
- Jiné: ______ · `use_case_jine`

---

### KROK 6 — Nástroje

**Nadpis:** V čem se orientuješ a co používáš?

**6.1 Které AI nástroje už používáš nebo jsi zkoušela?** · `nastroje`
*Výběr více možností + „Jiné" + „Zatím žádný"*

- ChatGPT (OpenAI)
- Claude (Anthropic)
- Gemini (Google)
- Copilot (Microsoft)
- Perplexity
- Midjourney / DALL-E / jiný obrazový AI
- Notion AI
- Canva AI
- Otter.ai nebo jiný nástroj na přepis
- Make / Zapier (automatizace)
- Jiné: ______ · `nastroje_jine`
- Zatím žádný

**6.2 Jak AI aktuálně používáš?** · `zpusob_pouziti`
*Výběr jedné možnosti*

- Nárazově podle potřeby
- Pravidelně, ale bez systému
- Systematicky – mám nějaké workflow

**6.3 Jak máš nástroje nastavené?** · `nastaveni_nastroju`
*Výběr jedné možnosti*

- Většinou zdarma
- Mix free a placené
- Placené předplatné
- Nevím přesně

**6.4 Kdyby ti konkrétní placený nástroj výrazně ulehčil práci – jsi ochotná do toho jít?** · `ochota_investovat`
*Výběr jedné možnosti*

- Ano, když uvidím smysl a cenu
- Radši zůstat u free variant
- Zatím nevím – záleží na situaci

---

### KROK 7 — Cíl, bariéry a urgence

**Nadpis:** Kam chceš dojít a co ti teď stojí v cestě?

**7.1 Co by pro tebe bylo za měsíc úspěch v souvislosti s AI?** · `cil_1_mesic`
*Dlouhý text — povinné* ✅

**7.2 Co ti teď nejvíc stojí v cestě?** · `bariera`
*Výběr více možností + „Jiné"*

- Nemám v klidu čas to zkoušet
- Nevím, kde přesně začít – je toho moc
- Bojím se chyby nebo nejistého výstupu
- Nástroje a nastavení mi připadají složité
- Nevím, jak to použít přímo ve své práci
- Chybí mi někdo, kdo mi to ukáže v mém kontextu
- Jiné: ______ · `bariera_jine`

**7.3 Jak moc to teď řešíš?** · `urgence`
*Výběr jedné možnosti*
*(Pomáhá mi poznat, jestli hledáš rychlý start, nebo se zatím jen rozhlížíš.)*

- Chci to rozjet hned / v nejbližších dnech
- Chtěla bych začít do měsíce
- Mapuji si možnosti, nechci tlačit
- Zatím se jen rozhlížím

---

### KROK 8 — Jak spolupracovat

**Nadpis:** Poslední otázky a odeslání

**8.1 Kolik času týdně reálně můžeš dát práci s AI?** · `cas_tydne`
*Výběr jedné možnosti*

- Do 30 minut
- Cca 30–60 minut
- 1–2 hodiny
- Víc než 2 hodiny – chci intenzivněji

**8.2 Jak ti vyhovuje tempo?** · `tempo`
*Výběr jedné možnosti*

- Radši krátké kroky a vidět pokrok postupně
- Radši větší soustředěné bloky občas
- Nevím – potřebuju doporučit

**8.3 Jaký rozsah spolupráce by ti nejlíp sedl?** · `rozsah`
*Výběr jedné možnosti*
*(Mentoring je vždycky jedna ku jedné – jde jen o to, jestli chceš jednorázově, nebo navazující sezení.)*

- Jednorázové setkání – chci rychlý náhled a konkrétní tip
- Několik setkání – chci se v tom postupně zorientovat
- Intenzivnější spolupráce – chci to pořádně rozjet
- Zatím nevím – poraď mi

**8.4 Kdybys měla AI použít jen na jednu věc příští týden – co by to bylo a proč?** · `jedna_vec_pristi_tyden`
*Dlouhý text — nepovinné*

**8.5 Je něco, co bych měla vědět, než ti napíšu doporučení?** · `poznamka`
*Dlouhý text — nepovinné*

**8.6 Souhlas se zpracováním osobních údajů** · `souhlas_gdpr`
*Checkbox — povinné* ✅
Souhlasím se zpracováním osobních údajů za účelem přípravy doporučení a kontaktování ohledně služeb AILadies. [odkaz na zásady]

---

### ZÁVĚREČNÁ OBRAZOVKA

**Nadpis:** Hotovo – díky!

**Text:** Tvůj AI plán ti pošlu na mail co nejdřív. Hned teď ti na mail přišlo potvrzení, že mi dotazník dorazil. Těším se, až se společně pustíme na tvé objevování AI.

**Tlačítko odeslání:** Pošli mi AI plán na mail

---

## 3. Metodika vyhodnocování – 4 osy

Každou respondentku hodnotíme podle **4 os**. Osy se vyhodnocují **interně** (klientka je nevidí), slouží agentovi a Petře k přípravě personalizovaného výstupu.

### OSA 1 — Úroveň práce s AI

Kombinace `uroven_ai` + `zpusob_pouziti` + `nastroje`.


| Úroveň             | Signály                                                                | Co klientka potřebuje              |
| ------------------ | ---------------------------------------------------------------------- | ---------------------------------- |
| **1 — Start**      | „Úplně na začátku" + žádné nebo jeden nástroj + „nárazově"             | Jistota, první krok, žádný tlak    |
| **2 — Objevování** | „Občas chatbot, bez systému" + 1–2 nástroje + „nárazově / bez systému" | Systém, rutina, konkrétní postupy  |
| **3 — Praxe**      | „Používám pravidelně" + více nástrojů + „pravidelně bez systému"       | Workflow, kvalita výstupů, šablony |
| **4 — Systém**     | „AI je součást práce" + nástroje vč. automatizace + „mám workflow"     | Procesy, automatizace, další posun |


### OSA 2 — Hlavní fokus

Z `cinnosti` + `use_case` + `opakujici_ukol`. **Vždy jen 1 hlavní fokus** (méně je víc).


| Fokus                    | Kdy přidělit                            | Směr doporučení                      |
| ------------------------ | --------------------------------------- | ------------------------------------ |
| **Texty a komunikace**   | tvorba obsahu, e-maily, nabídky         | psaní, šablony, tón, revize          |
| **Organizace a přehled** | administrativa, plánování, zahlcení     | shrnutí, prioritizace, meeting notes |
| **Obsah a vzdělávání**   | lektorství, vzdělávání, tvorba podkladů | osnovy, posty, scénáře               |
| **Práce s lidmi**        | tým, klienti, koordinace                | příprava odpovědí, struktura schůzek |
| **Automatizace**         | opakující se úkoly, Make/Zapier         | workflow, automatizace               |
| **Strategický posun**    | chce AI zavést systémově                | roadmapa, prioritizace, systém       |


### OSA 3 — Typ osobnosti a přístup k učení

Z `vztah_technologie` + `styl_uceni` + `reakce_na_spatny_vystup`.


| Typ             | Signály                                                               | Jak s ní komunikovat                         |
| --------------- | --------------------------------------------------------------------- | -------------------------------------------- |
| **Průzkumnice** | „Technologie mě baví" + „Zkouším hned v praxi" + „Zkusila jsem znovu" | Stručně, akčně, hodně samostatnosti          |
| **Praktická**   | „Zvládnu, když vím proč" + „Krok za krokem"                           | Jasné postupy, vysvětlit smysl               |
| **Opatrná**     | „Raději jednoduché" + „Pochopit princip" + „Nevěděla, co s tím"       | Trpělivost, méně nástrojů, hlubší vysvětlení |
| **Nejistá**     | „Stres" + „Vzdala jsem to"                                            | Velká bezpečnost, malé kroky, podpora        |


### OSA 4 — Hlavní bariéra

Z `bariera` – pokud zaškrtne víc, vybrat 1 primární podle `co_te_vycerpava` a `cil_1_mesic`.


| Bariéra                           | Tón reakce v e-mailu                                        |
| --------------------------------- | ----------------------------------------------------------- |
| Nemám čas                         | „Nepotřebuješ začínat velkoryse – stačí 1–2 situace týdně." |
| Nevím, kde začít                  | „Začneme na tvých reálných úkolech, ne na teorii."          |
| Bojím se chyb                     | „Ukážu ti, jak si výstupy hlídat a kde AI nepřeceňovat."    |
| Nástroje jsou složité             | „Vybereme minimum nástrojů, ne deset nových aplikací."      |
| Nevím, jak to použít ve své práci | „Doporučení postavím přímo na tvém kontextu."               |
| Chybí mi někdo, kdo mi to ukáže   | „Právě v tom mentoring dává největší smysl."                |


---

## 4. Typ klientky

Pomocná kategorizace pro **první pohled** na lead – shrne osy 1 a 4 do 1 slova.


| Typ             | Kdy přidělit                                                            | Přístup v nabídce                                                            |
| --------------- | ----------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| **Hledající**   | Úroveň 1–2 + bariéra „nevím kde začít"                                  | Jednoduchý start, 1 konkrétní krok, úvodní konzultace zdarma nebo 1× setkání |
| **Přetížená**   | Úroveň 1–3 + bariéra „čas" nebo „složitost" + chaos v `co_te_vycerpava` | Zjednodušení, radikální fokus na 1 use case, 2–3 sezení na nastavení rutiny  |
| **Praktická**   | Úroveň 2–3 + ochota investovat + chce konkrétní výsledky                | Mentoring balíček, konkrétní workflow pro 2–3 opakující úkoly                |
| **Strategická** | Úroveň 3–4 + „zavést systémově" + cíl za měsíc = systém / automatizace  | Intenzivnější spolupráce, roadmapa, napojení nástrojů                        |


*(Typ klientky se v e-mailu přímo nezmiňuje – slouží Petře a agentovi k volbě šablony a rozsahu.)*

### Doporučený rozsah spolupráce

Kombinace **typu klientky + `cas_tydne` + `tempo` + `rozsah` + `urgence`**.


| Situace                                              | Doporučený rozsah                           | Pozn.                                            |
| ---------------------------------------------------- | ------------------------------------------- | ------------------------------------------------ |
| Hledající, málo času, nejistota                      | Úvodní konzultace zdarma nebo 1× setkání    | Zmínit zdarma konzultaci, jen když to dává smysl |
| Občas používá, chce systém (Přetížená / Hledající 2) | 2–3 navazující setkání                      | Start balíček                                    |
| Pravidelně + chce výsledky (Praktická)               | Mentoring balíček (5×)                      |                                                  |
| Workflow / automatizace (Strategická)                | Intenzivnější spolupráce (10× nebo na míru) |                                                  |


---

## 5. Lead scoring a urgence

Aby Petra rychle poznala, komu psát **osobně a rychle** a komu stačí automatizovaný e-mail.

### Bodování (0–10)


| Signál                                                                                     | Body |
| ------------------------------------------------------------------------------------------ | ---- |
| `urgence` = „chci hned" nebo „do měsíce"                                                   | 3    |
| `zpusob_pouziti` = „systematicky" nebo úroveň 3–4                                          | 2    |
| `ochota_investovat` = „ano, když uvidím smysl"                                             | 2    |
| `use_case` obsahuje „automatizace" nebo „workflow"                                         | 2    |
| `cil_1_mesic` je konkrétní (ne „chci se zlepšit")                                          | 1    |
| Vyplní nepovinné otázky (`jedna_vec_pristi_tyden`, `poznamka`, `co_te_bavi_silne_stranky`) | 1    |


### Výklad

- **0–3 body** → nurture, pošli e-mail, nečekej aktivní reakci.
- **4–6 bodů** → zajímavý lead, sleduj reakci, po 3 dnech zvaž krátký follow-up.
- **7+ bodů** → **napiš osobně**, nabídni konzultaci přímo s konkrétním termínem.

---

## 6. Struktura výstupního e-mailu

Každý e-mail má **5 částí**. Max 350 slov. Tykání, bez klišé.

### 1. Zrcadlo

*Ukáže, že jsi ji četla. Jedna věta, která pojmenuje, kde je.*

### 2. Její AI plán v kostce

*Konkrétní obraz ve formátu:*

- **Kde teď jsi:** …
- **Kde máš největší potenciál:** …
- **Co by byl první smysluplný krok:** …

### 3. Tři otázky k zamyšlení

*Hodnota zdarma – malý coaching moment. Tři otázky nad čím přemýšlet.*

### 4. Jeden konkrétní tip (akce + nástroj)

Dvě části dohromady, ne odděleně:

- **Akce:** Co konkrétně udělat (viz sekce 8 – Tipy podle oblasti / `use_case`).
- **Nástroj:** Pokud klientka uvedla konkrétní nástroje (`nastroje`), vazba tipu na nástroj, který **už zná** – ne nový. Pokud neuvedla žádný, nástroj se nezmiňuje vůbec.

*Příklad: „Zkus v ChatGPT (nebo Claudi – vím, že ho máš) zadat přesně tenhle prompt: …"*

### 5. Pozvání k dalšímu kroku

Jeden CTA bez tlaku. Klientku odkazujeme přímo na ailadies.cz, kde si vybere konkrétní formu mentoringu. **Nerozpisujeme formáty v e-mailu** – web to udělá za nás.

**Důležité:** Na webu je objednávkový formulář, který normálně zahrnuje i vstupní dotazník. Klientce, která **už vyplnila tento diagnostický formulář**, stačí ve formuláři objednávky vyplnit jen základní údaje (jméno, e-mail, fakturační údaje) – vstupní dotazník není potřeba opakovat. Toto musí být na webu u objednávkového formuláře viditelně vyznačeno (např. „Pokud jsi vyplnila AI plán dotazník, přeskočte úvodní část – stačí základní údaje.").

*Tón CTA: přátelský, jeden krok, bez tlaku.*

---

## 7. Šablony e-mailů podle úrovně

*(Placeholder `[jméno]`, `[konkrétní oblast]`, `[tip]` – agent nebo Petra dovyplní.)*

### ŠABLONA A — Úroveň 1 (Start) / typ Hledající

**Předmět:** Tvůj AI plán – tady je

Ahoj [jméno],

děkuju za vyplnění formuláře. Z toho, co jsi napsala, vidím, že jsi zatím spíš na začátku – a to je přesně ta fáze, kde má smysl začít správně, ne rychle.

**Tvůj AI plán v kostce:**

- **Kde teď jsi:** Vnímáš, že AI by ti mohla pomoct, ale zatím jsi nenašla cestu, jak ji do své práce přirozeně zapojit.
- **Kde máš největší potenciál:** [konkrétní oblast podle `cinnosti` / `use_case`] – tady AI šetří nejvíc energie hned od začátku.
- **Co by byl první smysluplný krok:** Vybrat jeden opakující se úkol a zkusit ho zadat AI přesně tak, jak bys to popsala kolegyni.

**Než začneš s AI naplno, stojí za to si odpovědět na tři otázky:**

1. **Co mi v práci opravdu bere nejvíc energie?** Ne co by mělo – co reálně cítíš jako zátěž každý týden.
2. **Kde chci být za 3 měsíce?** Konkrétně: co chci dělat jinak, rychleji nebo vůbec nedělat?
3. **Co jsem ochotná zkusit, i když to hned nebude dokonalé?** AI vyžaduje trochu trpělivosti na začátku.

**Tip, který můžeš vyzkoušet ještě dnes:**
[Konkrétní tip podle `use_case` – sekce 8]
[+ pokud klientka uvedla nástroj: „Zkus to přímo v [nástroji, který používá] – vím, že ho znáš."]

**Co dál:**
Jestli chceš udělat první krok se mnou, podívej se na ailadies.cz, kde najdeš různé formy mentoringu 1:1 – vyber si tu, která ti nejlíp sedí. Pokud jsi tenhle dotazník vyplnila, ve formuláři objednávky přeskočíš vstupní část a vyplníš jen základní údaje. [odkaz]

*Těším se,*
Petra

---

### ŠABLONA B — Úroveň 2 (Objevování) / typ Přetížená nebo Hledající 2

**Předmět:** Tvůj AI plán – tady je

Ahoj [jméno],

děkuju za vyplnění formuláře. Z tvých odpovědí je vidět, že AI už používáš – ale zatím spíš po jednotlivých krocích a bez většího systému. To je velmi častá fáze a zároveň ta, kde bývá **největší prostor pro rychlý posun**.

**Tvůj AI plán v kostce:**

- **Kde teď jsi:** Máš základ – víš, jak AI zhruba funguje. Jen ti chybí převést ji do tvého konkrétního pracovního kontextu.
- **Kde máš největší potenciál:** [konkrétní oblast] – tady má smysl nastavit pár opakovatelných postupů, které ti začnou šetřit čas hned.
- **Co by byl první smysluplný krok:** Vytipovat 2–3 úkoly, které řešíš pořád dokola, a pro každý si připravit jednoduchý postup.

**Tři otázky k zamyšlení:**

1. **Co mi v práci opravdu bere nejvíc energie?**
2. **Kde chci být za 3 měsíce?** Konkrétně: co chci dělat jinak, rychleji nebo vůbec nedělat?
3. **Co jsem ochotná zkusit, i když to hned nebude dokonalé?**

**Tip, který můžeš vyzkoušet ještě dnes:**
[Konkrétní tip podle `use_case`]
[+ pokud klientka uvedla nástroj: „Zkus to přímo v [nástroji, který používá] – vím, že ho znáš."]

**Co dál:**
Na ailadies.cz najdeš různé formy mentoringu 1:1 – vyber si tu, která ti nejlíp sedí. Protože jsi tenhle dotazník vyplnila, ve formuláři objednávky přeskočíš vstupní část a vyplníš jen základní údaje. [odkaz]

*Těším se,*
Petra

---

### ŠABLONA C — Úroveň 3–4 (Praxe a systém) / typ Praktická nebo Strategická

**Předmět:** Tvůj AI plán – tady je

Ahoj [jméno],

děkuju za vyplnění formuláře. Z tvých odpovědí je vidět, že AI ve své práci aktivně používáš – a teď hledáš **další posun**. Ne začátek, ale větší efekt, lepší systém a výsledky, které jsou konzistentní.

**Tvůj AI plán v kostce:**

- **Kde teď jsi:** Máš zkušenost a pracovní kontext. AI ti už pomáhá, ale ne vždy dává konzistentní výsledky.
- **Kde máš největší potenciál:** [konkrétní oblast] – tady má smysl nastavit konkrétní workflow nebo šablonu, aby AI fungovala pro tebe systematicky.
- **Co by byl první smysluplný krok:** Vybrat 1–2 oblasti, kde výsledky AI nejsou konzistentní, a zmapovat, kde to vázne.

**Tři otázky k zamyšlení:**

1. **Co mi v práci opravdu bere nejvíc energie?**
2. **Kde chci být za 3 měsíce?**
3. **Mám správné nástroje, nebo se rozptyluju?** Někdy jeden dobrý placený nástroj nahradí tři free.

**Tip, který můžeš vyzkoušet ještě dnes:**
[Konkrétní tip podle `use_case`]
[+ pokud klientka uvedla nástroj: „Zkus to přímo v [nástroji, který používá] – vím, že ho znáš."]

**Co dál:**
Na ailadies.cz najdeš různé formy mentoringu 1:1 – vyber si tu, která ti nejlíp sedí. Protože jsi tenhle dotazník vyplnila, ve formuláři objednávky přeskočíš vstupní část a vyplníš jen základní údaje. [odkaz]

*Těším se,*
Petra

---

## 8. Tipy podle oblasti zájmu

Každý tip v e-mailu má **dvě části**: (1) **akce** – co konkrétně udělat, a (2) **nástroj** – jak to navázat na to, co klientka už používá (`nastroje`). Pokud klientka neuvedla žádný nástroj, nástroj se nezmiňuje.

**Pravidlo pro výběr nástroje:** ChatGPT a Claude jsou vhodné pro texty, strukturování, komunikaci a brainstorming. Gemini pro věci napojené na Google Workspace. Otter.ai / přepis pro schůzky. Make / Zapier pro automatizaci. Canva AI / Midjourney pro vizuály. Pokud má klientka mix, volíme ten, který nejlépe sedí k danému use case.


| Oblast (`use_case`)               | Akce                                                                                                                | Nástroj (podle `nastroje`)                                            |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| Texty a e-maily                   | Napiš AI: *„Pomoz mi napsat e-mail [komu] o [čem] – chci znít [jak]."* A koukni, co dostaneš.                       | ChatGPT nebo Claude – oba umí psaní dobře, Claude je přesnější v tónu |
| Shrnutí a strukturování           | Dej AI delší text nebo zápisky: *„Shrň to do 5 bodů a označ, co je důležité, co jen doplňkové."*                    | ChatGPT nebo Claude; Otter.ai pokud jde o zápis ze schůzky            |
| Příprava prezentací               | Dej AI svůj draft: *„Najdi v tom hlavní myšlenku a navrhni 5 slidů, které ji vystihnou."*                           | ChatGPT / Claude na osnovu; Canva AI na vizuální zpracování           |
| Plánování a organizace            | Jednou týdně dej AI seznam úkolů a zeptej se: *„Co z toho je nejdůležitější a co bys udělala jako první?"*          | ChatGPT nebo Gemini (pokud pracuje v Google Workspace)                |
| Komunikace s klienty / týmem      | Popiš AI situaci s klientem a zeptej se: *„Jak bys tuto situaci komunikovala profesionálně a empaticky?"*           | Claude – přirozenější v empatickém tónu                               |
| Brainstorming                     | Napiš AI: *„Brainstormuj se mnou 10 nápadů na [téma]. Buď konkrétní a klidně i bláznivá."*                          | ChatGPT nebo Claude – oba fungují                                     |
| Rychlejší učení                   | Požádej AI: *„Vysvětli mi [téma] tak, jako bys to vysvětlovala kamarádce u kávy."*                                  | ChatGPT nebo Gemini; Perplexity pokud chce zdroje                     |
| Automatizace opakujících se úkolů | Jeden den si zapiš všechny opakující se úkoly. Pak vyber jeden – a zamysli se, jestli by ho mohla AI dělat za tebe. | Make / Zapier (pokud ho má); ChatGPT na analýzu úkolů                 |
| Obsah a vzdělávání                | Požádej AI o osnovu tématu, které připravuješ – a pak ji uprav podle sebe.                                          | ChatGPT nebo Claude; Canva AI pokud potřebuje i vizuál                |


---

## 9. Interní záznam pro Petru

Pro každou respondentku zapsat do interní tabulky (např. Google Sheet nebo Notion):


| Pole                             | Obsah                                                 |
| -------------------------------- | ----------------------------------------------------- |
| Jméno                            | `jmeno`                                               |
| E-mail                           | `email`                                               |
| Firma / projekt                  | `firma_projekt`                                       |
| LinkedIn / web                   | `web_linkedin`                                        |
| **Úroveň AI**                    | 1 – Start / 2 – Objevování / 3 – Praxe / 4 – Systém   |
| **Hlavní fokus**                 | jedna kategorie (z osy 2)                             |
| **Typ osobnosti**                | Průzkumnice / Praktická / Opatrná / Nejistá (z osy 3) |
| **Typ klientky**                 | Hledající / Přetížená / Praktická / Strategická       |
| **Bariéra**                      | hlavní problém                                        |
| **Doporučený rozsah**            | konzultace / 1× / 2–3 setkání / balíček / intenzivní  |
| **Doporučený nástroj (interně)** | jen pro Petru – co navrhnout na prvním setkání        |
| **Konkrétní use case**           | `opakujici_ukol`                                      |
| **Ochota investovat**            | ano / free / nevím                                    |
| **Urgence**                      | hned / do měsíce / mapuji / rozhlížím                 |
| **Lead score**                   | 0–10                                                  |
| **Odeslaná odpověď**             | text e-mailu                                          |
| **Stav**                         | nový / odpovězeno / domluvená konzultace / klientka   |
| **Poznámka**                     | co Petra z formuláře vyčetla navíc                    |


---

## 10. Prompt pro agenta

Tento prompt použije **agent v Cursoru** (nebo Make / Zapier s napojením na LLM) pro generování odpovědi z dat.

```
Vyhodnoť odpovědi z diagnostického formuláře AILadies a vytvoř personalizovaný AI plán.

KROK 1 — URČI OSY A TYP

Na základě odpovědí urči:

1. Úroveň práce s AI (1 – Start / 2 – Objevování / 3 – Praxe / 4 – Systém)
   podle uroven_ai + zpusob_pouziti + nastroje
2. Hlavní fokus (Texty a komunikace / Organizace a přehled / Obsah a vzdělávání /
   Práce s lidmi / Automatizace / Strategický posun)
   podle cinnosti + use_case + opakujici_ukol – vyber JEDEN hlavní
3. Typ osobnosti (Průzkumnice / Praktická / Opatrná / Nejistá)
   podle vztah_technologie + styl_uceni + reakce_na_spatny_vystup
4. Typ klientky (Hledající / Přetížená / Praktická / Strategická)
   podle úrovně, bariéry a cíle
5. Hlavní bariéra (1 primární)
6. Lead score (0–10) podle bodovací tabulky v metodice
7. Doporučený rozsah (konzultace zdarma / 1× setkání / 2–3 setkání / balíček / intenzivní)

KROK 2 — NAPIŠ PERSONALIZOVANÝ E-MAIL

Vyber šablonu podle úrovně:
- Úroveň 1 → Šablona A
- Úroveň 2 → Šablona B
- Úroveň 3–4 → Šablona C

Vyplň placeholdery [jméno], [konkrétní oblast], [tip] konkrétními údaji z odpovědí.

Struktura e-mailu (5 částí, max 350 slov):

ČÁST 1 — Zrcadlo (1 věta, která pojmenuje, kde klientka je – použij její vlastní
          slovník z co_te_vycerpava nebo opakujici_ukol)
ČÁST 2 — AI plán v kostce (Kde teď → Kde máš potenciál → První krok)
          — konkrétní oblast vyjmenovat podle hlavního fokusu
ČÁST 3 — Tři otázky k zamyšlení (podle šablony pro danou úroveň)
ČÁST 4 — Jeden konkrétní tip (akce + nástroj):
          a) Akce: vyber z tabulky tipů v sekci 8 metodiky podle hlavního fokusu
          b) Nástroj: pokud klientka uvedla nástroje v `nastroje`, navaz tip na
             nástroj, který už zná (viz sloupec „Nástroj" v tabulce tipů).
             Pokud neuvedla žádný, část b) vynech.
          Formulace: „Zkus to přímo v [nástroji] – vím, že ho znáš."
ČÁST 5 — Pozvání k dalšímu kroku:
          Odkazujeme na ailadies.cz bez výčtu formátů v e-mailu.
          Zmínit: protože vyplnila tento dotazník, ve formuláři objednávky
          přeskočí vstupní část a vyplní jen základní údaje.
          Jeden CTA, bez tlaku. Tón: přátelský, ne prodejní.

TÓN:
- přátelský, lidský, tykací, ženský
- bez klišé a prodejního tlaku
- konkrétní a srozumitelný
- mentoring je VŽDY 1:1 – nikdy to neprezentuj jako volbu
- nezmiňuj "úvodní konzultaci zdarma" automaticky – jen když to dává smysl
  (typicky u úrovně 1 / typu Hledající)
- neslibuj fixní lhůty typu "do 24 hodin"

KROK 3 — VYPLŇ INTERNÍ ZÁZNAM

Kromě e-mailu vygeneruj interní záznam pro Petru (sekce 9 metodiky) –
všechna pole vyplněná.

KROK 4 — OZNAČ ÚROVEŇ POZORNOSTI

Na začátek výstupu napiš:

PRIORITA: [VYSOKÁ (lead score 7+) / STŘEDNÍ (4–6) / NÍZKÁ (0–3)]
DOPORUČENÁ REAKCE: [osobní e-mail / standardní e-mail / nurture]

---

ODPOVĚDI Z FORMULÁŘE:

{{ všechna pole z dotazníku s hodnotami }}
```

---

## 11. List k zamyšlení

*(Volitelná nadstavba pro mentoring – **ne** součást dotazníku.)*

Petra může vybrat 1–2 otázky a poslat je klientce **po první konzultaci** nebo **jako domácí úkol před druhým sezením** – pro hlubší zamyšlení mimo rychlý dotazník.

1. Když se podíváš na svůj minulý týden v práci: které **tři činnosti** ti sebraly nejvíc času bez toho, že by tě naplňovaly?
2. Který **jeden opakující se úkol** by ti přišel nejdřív na řadu k vyzkoušení s AI – a proč právě ten?
3. Co by se muselo stát, aby ses za měsíc na svou práci s AI dívala **o něco spokojeněji**? (jedna věta)
4. Kdy ti AI **nesedí** – protože výsledek, protože proces, nebo protože nevíš, jak zadat zadání?
5. Kdo v tvém okolí (v práci nebo doma) by z tvého lepšího používání AI měl **nejvíc užitek** – a jak by to u něj vypadalo?
6. Pokud bys měla vynechat jednu věc, kterou děláš „protože to tak má být", ale ve skutečnosti je to zbytečné – co by to bylo?

---

## 12. Attribution – jak uvádět zdroj AI plánu

Každý odeslaný e-mail s AI plánem (nebo HTML nabídka) může obsahovat nenápadnou větu v patičce, která:

1. **Buduje důvěru** – klientka ví, že plán není nahodilý, ale vychází z promyšlené metodiky.
2. **Posiluje brand** – AILadies jako autorita, která kombinuje lidský přístup a AI.
3. **Je transparentní** – nepředstíráme, že Petra vše napsala ručně; AI pomáhá, Petra přebírá odpovědnost.

### Navrhovaná formulace (v patičce e-mailu nebo HTML stránky)

> *Tento AI plán byl zpracován na základě metodiky AI plán na míru, kterou jsem vytvořila pro AILadies. Metodiku jsem sestavila s pomocí AI – za obsah a doporučení ručím já.*

**Nebo kratší varianta:**

> *AI plán vychází z metodiky AILadies, sestavené Petrou Pšeničnou s podporou AI.*

**Nebo jako součást podpisu e-mailu:**

> *P.S. Tvůj AI plán vychází z metodiky, kterou jsem pro AILadies sestavila – s pomocí AI, ale s mým přemýšlením za tím.*

### Kde attribution uvádět


| Kde                                       | Forma                                    | Povinné?   |
| ----------------------------------------- | ---------------------------------------- | ---------- |
| E-mail s AI plánem                        | Patička, malé písmo nebo P.S.            | Doporučeno |
| HTML stránka s nabídkou                   | Patička stránky                          | Doporučeno |
| Web ailadies.cz (popis formuláře)         | Jedna věta u perexu                      | Volitelné  |
| Macaly autoresponder (potvrzovací e-mail) | Neuvádět – to je jen technické potvrzení | Ne         |


---

## 13. Co přijde po této metodice

Tento dokument je **zdroj pravdy**. Z něj se odvíjí:

1. **Zadání pro Macaly** → aktualizace `[MACALY_ZADANI_FORMULAR_NABIDKA_NA_MIRU.md](MACALY_ZADANI_FORMULAR_NABIDKA_NA_MIRU.md)` podle nové struktury dotazníku (8 kroků místo stávajících polí).
2. **Agent v Cursoru** → aktualizace `[../../../08_Agenti/agent_ailadies_nabidka_na_miru.md](../../../08_Agenti/agent_ailadies_nabidka_na_miru.md)` tak, aby aplikoval 4 osy + typy + lead scoring a používal šablony A/B/C.
3. **Automatizace** → Make / Zapier napojení Macaly ↔ Gmail ↔ LLM podle promptu v sekci 10.

Tyto kroky **nejsou** součástí tohoto dokumentu – budou se dělat postupně.

---

## 13. Verze dokumentu


| Verze | Datum      | Poznámka                                                                                                                                                                                                                                              |
| ----- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2.0   | 2026-04-18 | První verze sjednocené finální metodiky; sloučení 3 zdrojů (AILadies_Dotaznik_Metodika.md, ai_ladies_metodika.md, NABIDKA_NA_MIRU_DOTAZNIK.md); přidána urgence, typy klientek, lead scoring, 4 osy, šablony A/B/C, prompt pro agenta                 |
| 2.1   | 2026-04-18 | Závěrečná obrazovka bez časové lhůty; tip v e-mailu rozšířen o nástroj klientky; CTA unifikováno na odkaz na web (bez výčtu formátů); přidána sekce Attribution (12); sekce 5 e-mailu doplněna o info o přeskočení vstupního dotazníku při objednávce |


