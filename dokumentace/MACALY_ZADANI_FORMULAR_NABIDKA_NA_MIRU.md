# Zadání pro Macaly: formulář „AI plán na míru“ (AILadies)

**Účel tohoto dokumentu:** finální implementační zadání pro Macaly na [ailadies.cz](https://www.ailadies.cz/). Jde o druhou, samostatnou cestu vedle stávajícího dlouhého dotazníku. **Stávající formulář se nemění.**

**Značka:** AILadies  
**Tón:** tykání, podpora, bez technického žargonu  
**Délka vyplnění:** cca 8 minut

**Zdroj pravdy (metodika):** [`METODIKA_AI_PLAN_NA_MIRU.md`](METODIKA_AI_PLAN_NA_MIRU.md)  
**Zpracování odpovědí v Cursoru (agent):** [`../../../08_Agenti/agent_ailadies_nabidka_na_miru.md`](../../../08_Agenti/agent_ailadies_nabidka_na_miru.md)

---

## 1. Co má formulář dělat

- Uložit odpovědi v Macaly.
- Poslat **Petře** notifikační e-mail se všemi odpověďmi ve strukturovaném formátu (sekce 5).
- Poslat vyplňující okamžitě **autoresponder** (sekce 6).
- Po odeslání zobrazit **děkovací obrazovku** (sekce 7).
- Použít přesně interní názvy polí (slugy) z tohoto dokumentu.
- Pole a pořadí odpovídají metodice v2.1.
- Ukládat odpovědi v adminu samostatně v přehledu / záložce **AI plán** (v profilu, kam máš přístup).
- Umožnit párování záznamu AI plán s objednávkou mentoringu (primárně podle e-mailu).
- Umožnit interní stavovou evidenci zpracování (`nové`, `zpracovávám`, `odesláno`, `spárováno s objednávkou`).

---

## 2. Umístění na webu a CTA text

Formulář „AI plán na míru“ má být jako paralelní cesta pod/vedle stávající nabídky konzultace.

**Doporučený CTA text:**
- `Získej svůj osobní AI plán`
- Doplňková věta: `Vyplň krátký dotazník a dostaneš doporučení, kde začít a co ti přinese největší posun.`

### 2.1 UX chování na webu (důležité)

Dotazník nemá být po načtení stránky rozbalený jako velký blok.

Požadované chování:

- **Default stav:** zobrazená je jen úvodní sekce (nadpis + krátký text + CTA tlačítko).
- **První krok:** uživatelka klikne na CTA (např. `Získat osobní plán` / `Vyplnit formulář`).
- **Až poté:** otevře se formulář (krok 1), ideálně plynulým rozbalením nebo přechodem na formulářový blok.
- **Na mobilech:** po kliknutí na CTA automaticky scrollnout na začátek formuláře.
- **Volitelně:** u rozbaleného formuláře zobrazit malé tlačítko `Skrýt formulář`.

### 2.2 Layout formuláře (viz základní dotazník)

Formulář nemá být přes celou šířku stránky. Má vizuálně odpovídat základnímu dotazníku:

- Formulář je v **centrovaném card/bloku**.
- Doporučená šířka: max. cca **780–860 px** na desktopu.
- Po stranách má mít dost prostoru (nelepí se na okraje stránky).
- Na mobilu je šířka 100 % s běžným vnitřním odsazením.
- Vizuálně má působit jako „kompaktní průvodce kroky“, ne jako dlouhá celostránková stěna.

### 2.3 Chování po odeslání (ukotvení)

Po kliknutí na odeslání:

- stránka se má **ukotvit/scrollnout na potvrzovací blok** (stejné místo, kde se zobrazuje hláška po odeslání),
- uživatelka má ihned vidět potvrzení bez nutnosti ručního scrollování,
- doporučení: potvrzovací blok mít vlastní kotvu/ID (např. `#ai-plan-sent`) a po submitu na ni přeskočit.

Preferovaná implementace:

- Accordion / collapsible sekce ve stejné stránce.
- Pokud to v Macaly nejde, alternativa je mezikrok s CTA a otevření formuláře na samostatné podstránce.

---

## 3. Texty nad formulářem

### 3.0 Přesný popisek sekce „Osobní AI plán“ (COPY BEZ ÚPRAV)

Použít přesně tento text (beze změny slov, interpunkce a pomlčky):

**Nadpis (H2):**  
Získej svůj osobní AI plán

**Perex:**  
Odpověz na pár otázek o tom, jak pracuješ a kde s AI jsi. Připravím ti konkrétní doporučení – kde začít, na čem pracovat a jak by mohl vypadat mentoring přesně pro tebe. Vyplnění tě k ničemu nezavazuje.

---

**Nadpis (H2):**  
Získej svůj osobní AI plán

**Perex:**  
Odpověz na pár otázek o tom, jak pracuješ a kde s AI jsi. Připravím ti konkrétní doporučení – kde začít, na čem pracovat a jak by mohl vypadat mentoring přesně pro tebe. Vyplnění tě k ničemu nezavazuje.

**Podnadpis (drobný text nad prvním polem):**  
Vyplnění zabere asi 8 minut. Po odeslání hned uvidíš potvrzení, že dotazník byl úspěšně odeslán. Tvůj AI plán ti pošlu co nejdřív.

---

## 4. Pole formuláře (finální specifikace)

> Důležité: držet pořadí kroků a interní názvy polí přesně podle tabulek.

### KROK 1 — Kontakt

| Interní název | Typ | Povinné | Label / text pro uživatelku |
|---|---|---|---|
| `jmeno` | krátký text | ano | Jméno a příjmení |
| `email` | e-mail | ano | E-mail |
| `firma_projekt` | krátký text | ne | Firma nebo projekt |
| `web_linkedin` | krátký text | ne | Web nebo LinkedIn (volitelné) |

### KROK 2 — Vztah k AI

| Interní název | Typ | Povinné | Label / možnosti |
|---|---|---|---|
| `uroven_ai` | jedna možnost (radio) | ano | Jak bys popsala svůj aktuální vztah s AI? |
|  |  |  | Úplně na začátku – zatím spíš zkouším, co to umí |
|  |  |  | Občas použiju chatbota, ale nemám v tom systém |
|  |  |  | Už AI používám pravidelně a chtěla bych to posunout dál |
|  |  |  | AI je součást mojí práce – řeším konkrétní nástroje nebo postupy |

### KROK 3 — Tvoje práce

| Interní název | Typ | Povinné | Label / možnosti |
|---|---|---|---|
| `pracovni_role` | jedna možnost (radio) | ano | Jaká je tvoje pracovní role? |
|  |  |  | Freelancerka / OSVČ |
|  |  |  | Podnikatelka / majitelka firmy |
|  |  |  | Manažerka / vedoucí týmu |
|  |  |  | Koordinátorka / projektová manažerka |
|  |  |  | Specialistka (marketing, HR, finance, právo…) |
|  |  |  | Asistentka / office manager |
|  |  |  | Učitelka / lektorka / koučka |
|  |  |  | Pracuji v neziskovém sektoru |
|  |  |  | Jiné |
| `pracovni_role_jine` | krátký text | ne | Pokud Jiné, upřesni |
| `kontext_pouziti` | jedna možnost (radio) | ano | Používáš AI primárně pro: |
|  |  |  | Svoji práci / podnikání |
|  |  |  | Práci ve firmě nebo organizaci |
|  |  |  | Osobní věci / organizaci života |
|  |  |  | Kombinaci |
| `cinnosti` | více možností (checkbox, max 3) | ano | Čemu se v práci nejvíc věnuješ? |
|  |  |  | Komunikace a e-maily |
|  |  |  | Tvorba obsahu (texty, sociální sítě, newslettery) |
|  |  |  | Administrativa a organizace |
|  |  |  | Práce s lidmi (tým, klienti, zákazníci) |
|  |  |  | Vzdělávání nebo předávání znalostí |
|  |  |  | Projekty a jejich řízení |
|  |  |  | Obchod, nabídky, smlouvy |
|  |  |  | Kreativní nebo vizuální tvorba |
|  |  |  | Jiné |
| `cinnosti_jine` | krátký text | ne | Pokud Jiné, upřesni |
| `co_te_vycerpava` | dlouhý text | ano | Co tě v práci nejvíc vyčerpává nebo zdržuje? |
| `opakujici_ukol` | střední / dlouhý text | ano | Popiš jednu konkrétní opakující se věc, která tě stojí nejvíc času nebo energie |
| `co_te_bavi_silne_stranky` | dlouhý text | ne | Co tě v práci baví nejvíc? V čem jsi silná? (volitelné) |

### KROK 4 — Přístup a zkušenosti

| Interní název | Typ | Povinné | Label / možnosti |
|---|---|---|---|
| `vztah_technologie` | jedna možnost (radio) | ano | Jak bys popsala svůj vztah k technologiím obecně? |
|  |  |  | Nové věci zkouším ráda – technologie mě baví |
|  |  |  | Zvládnu to, když vím proč – ale nechci trávit čas nastavováním |
|  |  |  | Raději mám věci jednoduché – čím méně aplikací, tím líp |
|  |  |  | Technologie mi dělají stres, ale vím, že to potřebuju překonat |
| `predchozi_vzdelavani` | jedna možnost (radio) | ano | Prošla jsi už nějakým kurzem nebo vzděláváním zaměřeným na AI? |
|  |  |  | Ne, zatím nic |
|  |  |  | Koukla jsem na pár videí nebo webinářů zdarma |
|  |  |  | Byla jsem na placeném kurzu – ale moc mi to nepomohlo |
|  |  |  | Byla jsem na kurzu a něco jsem si odnesla, ale chybí mi praxe |
|  |  |  | Vzdělávám se průběžně sama – čtu, zkouším, testuji |
| `reakce_na_spatny_vystup` | jedna možnost (radio) | ano | Když jsi AI zkusila a výsledek nebyl dobrý – co jsi udělala? |
|  |  |  | Zkusila jsem to znovu, upravila zadání |
|  |  |  | Vzdala jsem to a vrátila se ke starému způsobu |
|  |  |  | Nevěděla jsem, co s tím – výsledek jsem nepoužila |
|  |  |  | Zatím jsem to moc nezkoušela |
| `styl_uceni` | jedna možnost (radio) | ano | Jak pracuješ, když se učíš něco nového? |
|  |  |  | Zkouším hned v praxi – učím se za pochodu |
|  |  |  | Potřebuji nejdřív pochopit princip, pak teprve zkouším |
|  |  |  | Nejlépe se učím, když mi někdo ukáže postup krok za krokem |
|  |  |  | Kombinuji – trochu teorie, trochu praxe |

### KROK 5 — Co chceš s AI řešit

| Interní název | Typ | Povinné | Label / možnosti |
|---|---|---|---|
| `use_case` | více možností (checkbox, max 3) | ano | Na co bys AI nejvíc chtěla využít? |
|  |  |  | Psaní a úprava textů (e-maily, nabídky, posty) |
|  |  |  | Shrnutí a strukturování informací |
|  |  |  | Příprava prezentací nebo podkladů |
|  |  |  | Plánování a organizace práce |
|  |  |  | Komunikace s klienty nebo týmem |
|  |  |  | Brainstorming a hledání nápadů |
|  |  |  | Rychlejší učení se novým věcem |
|  |  |  | Automatizace opakujících se úkolů |
|  |  |  | Jiné |
| `use_case_jine` | krátký text | ne | Pokud Jiné, upřesni |

### KROK 6 — Nástroje

| Interní název | Typ | Povinné | Label / možnosti |
|---|---|---|---|
| `nastroje` | více možností (checkbox) | ano | Které AI nástroje už používáš nebo jsi zkoušela? |
|  |  |  | ChatGPT (OpenAI) |
|  |  |  | Claude (Anthropic) |
|  |  |  | Gemini (Google) |
|  |  |  | Copilot (Microsoft) |
|  |  |  | Perplexity |
|  |  |  | Midjourney / DALL-E / jiný obrazový AI |
|  |  |  | Notion AI |
|  |  |  | Canva AI |
|  |  |  | Otter.ai nebo jiný nástroj na přepis |
|  |  |  | Make / Zapier (automatizace) |
|  |  |  | Jiné |
|  |  |  | Zatím žádný |
| `nastroje_jine` | krátký text | ne | Pokud Jiné, upřesni |
| `zpusob_pouziti` | jedna možnost (radio) | ano | Jak AI ve své práci dnes nejčastěji používáš? *(Bez názvů úrovní typu Citizen/Power user.)* |
|  |  |  | Používám AI občas na jednotlivé úkoly |
|  |  |  | Používám AI pravidelně, ale zatím bez jasného postupu |
|  |  |  | Mám vlastní postupy a používám AI systematicky |
|  |  |  | Zatím AI nepoužívám, chci začít |
| `nastaveni_nastroju` | jedna možnost (radio) | ano | Jak máš nástroje nastavené? |
|  |  |  | Většinou zdarma |
|  |  |  | Mix free a placené |
|  |  |  | Placené předplatné |
|  |  |  | Nevím přesně |
| `ochota_investovat` | jedna možnost (radio) | ano | Kdyby ti konkrétní placený nástroj výrazně ulehčil práci – jsi ochotná do toho jít? |
|  |  |  | Ano, když uvidím smysl a cenu |
|  |  |  | Radši zůstat u free variant |
|  |  |  | Zatím nevím – záleží na situaci |

### KROK 7 — Cíl, bariéry, urgence

| Interní název | Typ | Povinné | Label / možnosti |
|---|---|---|---|
| `cil_1_mesic` | dlouhý text | ano | Co by pro tebe bylo za měsíc úspěch v souvislosti s AI? |
| `bariera` | více možností (checkbox) | ano | Co ti teď nejvíc stojí v cestě? |
|  |  |  | Nemám v klidu čas to zkoušet |
|  |  |  | Nevím, kde přesně začít – je toho moc |
|  |  |  | Bojím se chyby nebo nejistého výstupu |
|  |  |  | Nástroje a nastavení mi připadají složité |
|  |  |  | Nevím, jak to použít přímo ve své práci |
|  |  |  | Chybí mi někdo, kdo mi to ukáže v mém kontextu |
|  |  |  | Jiné |
| `bariera_jine` | krátký text | ne | Pokud Jiné, upřesni |
| `urgence` | jedna možnost (radio) | ano | Jak moc to teď řešíš? |
|  |  |  | Chci to rozjet hned / v nejbližších dnech |
|  |  |  | Chtěla bych začít do měsíce |
|  |  |  | Mapuji si možnosti, nechci tlačit |
|  |  |  | Zatím se jen rozhlížím |

### KROK 8 — Jak spolupracovat

| Interní název | Typ | Povinné | Label / možnosti |
|---|---|---|---|
| `cas_tydne` | jedna možnost (radio) | ano | Kolik času týdně reálně můžeš dát práci s AI? |
|  |  |  | Do 30 minut |
|  |  |  | Cca 30–60 minut |
|  |  |  | 1–2 hodiny |
|  |  |  | Víc než 2 hodiny – chci intenzivněji |
| `tempo` | jedna možnost (radio) | ano | Jak ti vyhovuje tempo? |
|  |  |  | Radši krátké kroky a vidět pokrok postupně |
|  |  |  | Radši větší soustředěné bloky občas |
|  |  |  | Nevím – potřebuju doporučit |
| `rozsah` | jedna možnost (radio) | ano | Co by ti teď dávalo největší smysl? *(Jde o počet mentoringových setkání 1:1.)* |
|  |  |  | 1 setkání (60 min) – chci rychlý směr a konkrétní první krok |
|  |  |  | 2–3 setkání – chci nastavit základy a začít je používat v praxi |
|  |  |  | 5+ setkání – chci hlubší systém a dlouhodobější podporu |
|  |  |  | Nejsem si jistá – doporuč mi vhodnou variantu |
| `jedna_vec_pristi_tyden` | dlouhý text | ne | Kdybys měla AI použít jen na jednu věc příští týden – co by to bylo a proč? |
| `poznamka` | dlouhý text | ne | Je něco, co bych měla vědět, než ti napíšu doporučení? |
| `souhlas_gdpr` | checkbox | ano | Souhlasím se zpracováním osobních údajů za účelem přípravy doporučení a kontaktování ohledně služeb AILadies. [odkaz na zásady] |

**Text tlačítka odeslání:**  
Pošli mi AI plán na mail

---

## 5. Notifikační e-mail pro Petru (strukturovaný formát)

**Předmět (pevně):**  
`[AILadies] AI plán na míru | Nová odpověď`

**Tělo e-mailu (každé pole na vlastní řádek):**

```text
Formulář: AI plán na míru
Odesláno: [datum a čas z Macaly]

jmeno: [hodnota]
email: [hodnota]
firma_projekt: [hodnota]
web_linkedin: [hodnota]
uroven_ai: [hodnota]
pracovni_role: [hodnota]
pracovni_role_jine: [hodnota]
kontext_pouziti: [hodnota]
cinnosti: [hodnoty]
cinnosti_jine: [hodnota]
co_te_vycerpava: [hodnota]
opakujici_ukol: [hodnota]
co_te_bavi_silne_stranky: [hodnota]
vztah_technologie: [hodnota]
predchozi_vzdelavani: [hodnota]
reakce_na_spatny_vystup: [hodnota]
styl_uceni: [hodnota]
use_case: [hodnoty]
use_case_jine: [hodnota]
nastroje: [hodnoty]
nastroje_jine: [hodnota]
zpusob_pouziti: [hodnota]
nastaveni_nastroju: [hodnota]
ochota_investovat: [hodnota]
cil_1_mesic: [hodnota]
bariera: [hodnoty]
bariera_jine: [hodnota]
urgence: [hodnota]
cas_tydne: [hodnota]
tempo: [hodnota]
rozsah: [hodnota]
jedna_vec_pristi_tyden: [hodnota]
poznamka: [hodnota]
souhlas_gdpr: [ano/ne]
```

**Poznámka:** pokud Macaly umožní, přidat i export CSV jako přílohu. Textová verze výše je povinné minimum.

---

## 6. Automatický e-mail pro vyplňující (autoresponder)

**Předmět:**  
AILadies – mám tvůj dotazník, díky

**Tělo:**

```text
Ahoj [jmeno nebo "Ahoj"],

díky za vyplnění dotazníku AI plán na míru – právě mi dorazil.

Tvůj AI plán ti pošlu na mail co nejdřív.

Těším se, až se společně pustíme na tvé objevování AI.

Petra
AILadies
```

---

## 7. Děkovací obrazovka po odeslání

**Nadpis:**  
Dotazník se úspěšně odeslal.

**Text:**  
Tvůj AI plán ti pošlu na mail co nejdřív. Hned teď ti na mail přišlo potvrzení o odeslání dotazníku. Těším se, až se společně pustíme na tvé objevování AI.

**Tlačítko:**  
Pošli mi AI plán na mail

---

## 8. Důležitá poznámka k objednávkovému formuláři na webu

Na stránce s objednávkou mentoringu doplnit viditelnou poznámku:

> Pokud jsi už vyplnila dotazník AI plán na míru, ve formuláři objednávky stačí vyplnit jen základní údaje (jméno, e-mail, fakturační údaje). Vstupní část není potřeba vyplňovat znovu.

Tato poznámka má být přímo u objednávkového formuláře.

---

### 8.1 Admin profil (Market) – evidence a párování

V adminu Macaly (profil Market) nastavit samostatnou evidenci odpovědí:

- Samostatná záložka / přehled s názvem **AI plán**.
- V seznamu zobrazit minimálně: datum, jméno, e-mail, stav, vazba na objednávku.
- Detail záznamu musí obsahovat všechna pole z formuláře (sekce 4).

**Stav zpracování (ručně přepínatelný):**

- `nové`
- `zpracovávám`
- `odesláno` (výsledkový e-mail klientce je odeslaný)
- `spárováno s objednávkou`

**Párování s objednávkou:**

- Primární klíč: `email`.
- Sekundární kontrola: `jmeno` + časové okno odeslání.
- Pokud existuje objednávka se stejným e-mailem, u záznamu AI plánu zobrazit vazbu na objednávku (ID/odkaz v adminu).
- Cíl: v adminu rychle poznat, zda už klientka po AI plánu přešla do objednávky.

---

## 9. Volitelná věta o metodice (attribution)

Tuto větu používat pouze v **e-mailu s výsledky AI plánu** (ne na webu, ne v autoresponderu).

### Vybraná formulace (default)

> Tento AI plán je zpracovaný podle metodiky AILadies, kterou jsem navrhla s podporou AI nástrojů.

### Další možné varianty

1. *Tvůj AI plán vychází z metodiky AILadies, kterou jsem sestavila s podporou AI.*
2. *Doporučení je připravené podle metodiky AI plán na míru od AILadies, kterou jsem vytvořila s pomocí AI.*
3. *Výsledky vychází z metodiky AILadies „AI plán na míru“, sestavené mnou s podporou AI.*
4. *Tvůj výstup je připraven podle metodiky AILadies, kterou jsem vytvořila pro mentoring 1:1 s využitím AI.*

**Umístění v e-mailu:** do závěru (podpis nebo P.S.), jednou větou, bez dalšího vysvětlování.

---

## 10. Kontrolní checklist pro Macaly / Petru po nasazení

- [ ] Formulář je nasazen jako paralelní cesta vedle stávajícího formuláře.
- [ ] Formulář není defaultně rozbalený; nejdřív je vidět jen intro + CTA.
- [ ] Po kliknutí na CTA se otevře formulář (krok 1) a na mobilu se správně posune viewport.
- [ ] Formulář není přes celou stránku; je v centrovaném bloku jako základní dotazník.
- [ ] Po odeslání se viewport ukotví na potvrzovací blok (`Dotazník se úspěšně odeslal.`).
- [ ] Pole a slugy odpovídají přesně sekci 4.
- [ ] Předmět notifikace je `[AILadies] AI plán na míru | Nová odpověď`.
- [ ] Notifikační e-mail obsahuje všechna pole ve strukturovaném formátu ze sekce 5.
- [ ] Autoresponder odchází okamžitě po odeslání.
- [ ] Děkovací obrazovka obsahuje finální text ze sekce 7.
- [ ] GDPR odkaz je funkční.
- [ ] U objednávkového formuláře je viditelná poznámka o přeskočení vstupní části.
- [ ] V adminu je samostatná záložka **AI plán** se seznamem odeslaných formulářů.
- [ ] U každého záznamu lze přepnout stav (`nové` / `zpracovávám` / `odesláno` / `spárováno s objednávkou`).
- [ ] Párování AI plán ↔ objednávka funguje minimálně podle e-mailu.
- [ ] Proběhlo testovací odeslání (Petra + testovací e-mail klientky).

---

## 11. Verze zadání

| Verze | Datum | Poznámka |
|---|---|---|
| 2.0 | 2026-04-18 | Finální zadání podle metodiky `METODIKA_AI_PLAN_NA_MIRU.md` v2.1 (8 kroků, nové slugy, urgence, nový text závěrečné obrazovky, notifikace pro Petru, autoresponder, poznámka k objednávce) |
| 2.1 | 2026-04-18 | Attribution přesunuto výhradně do e-mailu s výsledky; doplněno 5 alternativ formulace |
| 2.2 | 2026-04-18 | Nastavena vybraná defaultní attribution formulace pro výsledkový e-mail |
| 2.3 | 2026-04-18 | Doplněny požadavky na admin workflow v Macaly: záložka AI plán, stavy zpracování, párování s objednávkou |
| 2.4 | 2026-04-18 | Doplněn UX požadavek: formulář defaultně sbalený, otevření až po kliknutí na CTA (+ mobilní scroll) |
| 2.5 | 2026-04-18 | Upraveny formulace u `zpusob_pouziti` (bez Citizen/Power user) a `rozsah` (srozumitelnější varianty včetně počtu setkání) |
| 2.6 | 2026-04-18 | Doplněn požadavek na kompaktní layout (ne přes celou stránku), ukotvení po odeslání na potvrzovací blok a nová textace „Dotazník se úspěšně odeslal.“ |
| 2.7 | 2026-04-18 | Doplněn explicitní blok COPY BEZ ÚPRAV pro sekci „Osobní AI plán“ (nadpis + perex) |
