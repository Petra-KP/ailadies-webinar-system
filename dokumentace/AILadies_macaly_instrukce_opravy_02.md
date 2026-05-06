# AILadies – Opravy a upřesnění instrukcí (kolo 3)

> Tento dokument **doplňuje** původní instrukce (`AILadies_macaly_instrukce_2026.md`) a opravy kola 2 (`AILadies_macaly_instrukce_opravy_01.md`).
> Kde se tento dokument liší od předchozích, platí tento dokument.
>
> **Kontakt pro dotazy:** mentorka@ailadies.cz

---

## Přehled oprav

| # | Kde na webu | Co se opravuje |
|---|---|---|
| A | Cookie lišta | Kontrola nastavení z hlediska GDPR a platné legislativy ČR/EU |
| B | Formulář „Osobní AI plán" | Opravit nefunkční odkaz na Ochranu osobních údajů |
| C | Odpovědní e-mail „Osobní AI plán" | Opravit překlep „vyplníla" → „vyplnila" |
| D | Odpovědní e-mail „Poptávka" | Odstranit časový údaj z věty o ozvání |
| E | Přepínač jazyka (EN) | Přesunout úplně vpravo za „Začít" + vizuálně utlumit |
| F | Anglická verze webu | Audit překladů — všechny sekce, formuláře, balíčky, patička, cookie lišta |

---

## A. Cookie lišta — kontrola nastavení (GDPR + ČR/EU)

### Právní rámec

Web ailadies.cz podléhá:
- **GDPR** (nařízení EU 2016/679) — zpracování osobních údajů
- **ePrivacy směrnice** (2002/58/ES, implementována v ČR zákonem č. 127/2005 Sb., o elektronických komunikacích) — cookies a sledovací technologie
- Doporučením **ÚOOÚ** (Úřad pro ochranu osobních údajů, uoou.cz)

### Co zkontrolovat v Macaly — bezpečnostní a právní checklist

**1) Zobrazení při první návštěvě**
- [ ] Banner se zobrazí **před načtením jakýchkoli neesenciálních skriptů** (analytika, tracking)
- [ ] Analytické skripty (GA4 apod.) **nejsou** aktivní dříve, než uživatel klikne „Přijmout vše"
- [ ] Testovat v anonymním okně + v síťovém panelu prohlížeče (F12 → Network) — při první návštěvě bez souhlasu **nesmí** letět požadavky na `google-analytics.com`

**2) Tlačítka — symetrie odmítnutí a přijetí**
- [ ] Tlačítko **„Pouze nezbytné"** nebo **„Odmítnout"** musí být **stejně viditelné** jako „Přijmout vše" — neschované v submenu, ne šedé na šedém pozadí
- [ ] Obojí musí být **na první pohled**, bez nutnosti klikat na „Další nastavení" jen proto, aby šlo odmítnout
- [ ] Doporučení ÚOOÚ a evropská praxe: odmítnutí = stejně snadné jako přijetí

**3) Obsah lišty**
- [ ] Text lišty stručně vysvětluje, **k čemu** cookies slouží (neesenciální = analytika/marketing)
- [ ] Odkaz na **Zásady ochrany osobních údajů**: `https://www.ailadies.cz/ochrana-osobnich-udaju`
- [ ] Odkaz na **Obchodní podmínky**: `https://www.ailadies.cz/obchodni-podminky`
- [ ] Oba odkazy **fungují a vedou na správné stránky** (otestovat kliknutím)

**4) Uložení a respektování volby**
- [ ] Po kliknutí na libovolné tlačítko se banner **schová** a **nezobrazí** při dalším načtení stránky ve stejném prohlížeči
- [ ] Pokud uživatel zvolil „Pouze nezbytné", i po zavření a opětovném otevření prohlížeče (ve stejné session) se banner **nezobrazuje** zbytečně znovu
- [ ] V patičce nebo někde na webu je odkaz **„Nastavení cookies"** nebo možnost volbu **změnit** (výzva ÚOOÚ: umožnit kdykoli odvolat souhlas stejně snadno, jak byl udělen)

**5) Technické blokování (Consent Mode)**
- [ ] Pokud je na webu Google Analytics 4, musí být nakonfigurován **Consent Mode v2** — analytika při odmítnutí buď **nefunguje**, nebo sbírá anonymizovaná ping data bez cookies (dle zvoleného nastavení)
- [ ] Pokud je použit Google Tag Manager (GTM), šablony tagů musí mít nastavenu podmínku spuštění **závislou na souhlasu**
- [ ] Ověřit v Macaly dokumentaci: jak builder řeší Consent Mode — pokud nepodporuje, zvážit přidání externího CMP (Cookiebot, CookieYes apod.)

**6) Dokumentace cookies**
- [ ] Na stránce Ochrana osobních údajů (`/ochrana-osobnich-udaju`) je **sekce Cookies** s tabulkou: název cookie, účel, typ (nezbytné/analytické), platnost
- [ ] Při přidání nového nástroje (pixel, chat, embed) **aktualizovat tabulku** a případně aktualizovat lištu

> **Shrnutí:** Právně nejrizikovější je situace, kdy analytické skripty jedou bez souhlasu. To je nejdůležitější věc k ověření.

---

## B. Formulář „Osobní AI plán" — opravit odkaz

### Kde v Macaly
Formulář (nebo potvrzovací/GDPR text pod formulářem) v sekci **„Získej svůj osobní AI plán"** — obsahuje odkaz na zásady ochrany soukromí / osobních údajů.

### Problém
Odkaz na Ochranu osobních údajů **nefunguje** (vede na neexistující URL nebo je prázdný).

### Oprava
Nastavit odkaz na:
```
https://www.ailadies.cz/ochrana-osobnich-udaju
```

Text odkazu ponechat tak, jak je (např. „Zásady ochrany osobních údajů" nebo „ochranu soukromí") — měnit pouze cílovou URL.

Po opravě **otestovat kliknutím** — stránka musí načíst správně.

---

## C. Odpovědní e-mail „Osobní AI plán" — opravit překlep

### Problém
V automatickém e-mailu odesílaném po vyplnění formuláře „Osobní AI plán" je překlep:

> ~~Brzy ti pošlu konkrétní doporučení, která navážou na to, co jsi vyplníla...~~

Slovo **„vyplníla"** je chybně — obsahuje **dlouhé í** navíc.

### Oprava
Nahradit za:
```
vyplnila
```

Celá věta po opravě:
```
Brzy ti pošlu konkrétní doporučení, která navážou na to, co jsi vyplnila,
a pomůžou ti posunout práci s AI dál.
```

---

## D. Odpovědní e-mail „Poptávka" — odstranit časový údaj

### Kde v Macaly
Automatický e-mail odesílaný po odeslání **poptávkového formuláře** (hlavního i formuláře „Hledáš jiný formát?").

### Problém
E-mail aktuálně obsahuje větu s konkrétním časovým údajem:

> ~~Ozvu se ti co nejdříve – obvykle do 1–2 pracovních dní.~~

Časový údaj **„obvykle do 1–2 pracovních dní"** tam nesmí být — žádný konkrétní termín se nikde neuvádí.

### Oprava
Nahradit větu za:
```
Ozvu se ti co nejdřív.
```

Tato úprava se týká **všech odpovědních e-mailů** kde se tato věta (nebo její varianta s časovým údajem) vyskytuje — projít všechny e-mailové šablony v Macaly a odstranit jakýkoli konkrétní časový příslib.

---

## E. Přepínač jazyka (EN) — pozice a vzhled

### Umístění v horní liště

**Požadavek:** Tlačítko / odkaz **„EN"** musí být **úplně vpravo** v navigaci — **až za** primárním tlačítkem **„Začít"**.

**Správné pořadí prvků v hlavičce (zleva doprava):**
```
[Logo AILadies]  [Pro koho] [Jak to funguje] [Co dostaneš] [Nabídka] [O mně] [FAQ …]  [Začít]  [EN]
```

Na mobilním menu stejná logika: „EN" jako **poslední položka** pod hlavním CTA, ne uprostřed mezi navigačními odkazy.

### Vizuální styl — méně výrazné než nyní

**Cíl:** Přepínač jazyka nesmí konkurovat tlačítku „Začít" ani hlavní navigaci.

Doporučené nastavení v Macaly:
- **Ne** plné zlaté / terracotta pill tlačítko (jako je teď)
- Použít **textový odkaz** nebo **ghost** styl: malé písmo (o 1–2 stupně menší než nav položky), barva tlumená — jemná zlatá s nižší saturací nebo šedá v tónu stránky
- **Bez** plného pozadí — případně jen velmi jemný `1px border` nebo úplně bez rámečku
- Hover: lehké zesvětlení nebo podtržení, nic agresivního

**Přístupnost:** Text „EN" musí zůstat čitelný (dostatečný kontrast dle WCAG), jen vizuálně méně dominantní.

---

## F. Anglická verze webu — audit překladů

Po každé úpravě českého obsahu vždy zkontrolovat anglickou verzi. Níže je checklist všech míst.

### Navigace a patička

- [ ] Všechny položky menu přeloženy
- [ ] Patička — navigace, slogan, kontakt, právní řádek
- [ ] Odkaz na „Privacy Policy" / „Terms" — pokud stránky existují jen v češtině, v EN verzi uvést „Czech only" nebo odkaz s vysvětlením

### Hlavní sekce stránky

- [ ] Hero — label, H1, perex, všechna tlačítka (Konzultace zdarma / Jak mentoring probíhá / Chci osobní AI plán)
- [ ] Sekce „Poznáváš se?"
- [ ] Sekce „Jak AI používám já" — všechny 4 karty (titulky + texty)
- [ ] Sekce „Jak to funguje" — H2, perex, callout o ChatGPT / Copilot
- [ ] Sekce „Co dostaneš" — všechny 4 karty
- [ ] Sekce „Nabídka":
  - nadpis a perex
  - úvodní konzultace zdarma
  - jednorázové setkání
  - **názvy balíčků** (Start / Rozjezd / Proměna) a jejich podtitulky
  - ceny a texty o úspoře
  - text pod balíčky o e-mailové podpoře
- [ ] Sekce „Hledáš jiný formát?" — nadpis, obě položky, tlačítko „Poptat nabídku"
- [ ] Sekce „Osobní AI plán" — nadpis, perex, tlačítko
- [ ] FAQ — všechny otázky i odpovědi
- [ ] Sekce „O mně" — bio, bullet pointy
- [ ] Sekce „Začít" / závěrečné CTA

### Formuláře

- [ ] Hlavní poptávkový formulář — názvy polí, placeholdery, GDPR text + odkaz na Privacy Policy
- [ ] Formulář „Poptat nabídku" — všechna pole, výběr typu poptávky, tlačítko odeslání
- [ ] Formulář „Osobní AI plán" — všechna pole, GDPR text + odkaz
- [ ] Potvrzovací / chybové hlášky po odeslání každého formuláře
- [ ] Texty tlačítek rezervace kalendáře (pokud jsou lokalizovatelné)

### Cookie lišta v EN

- [ ] Text banneru přeložen
- [ ] Tlačítka (Accept all / Necessary only / Settings)
- [ ] Oba odkazy vedou na správné stránky (i když jsou zatím v češtině — přidat poznámku „Czech only", pokud překlad neexistuje)

### Postup testu

1. Otevřít web v **anonymním okně**, přepnout na **EN**
2. Projít stránku **odshora dolů** — vše musí být v angličtině (vlastní názvy jako „AILadies" nepřekládat)
3. Odeslat **testovací vyplnění** každého formuláře v EN režimu — ověřit hlášky a odpovědní e-mail
4. Po každé budoucí změně českého textu **zopakovat kontrolu EN verze**

---

## Checklist oprav (kolo 3)

- [ ] Cookie lišta — projít checklist v sekci A, ověřit blokování neesenciálních skriptů před souhlasem
- [ ] Formulář AI plán — odkaz na `https://www.ailadies.cz/ochrana-osobnich-udaju` funguje
- [ ] Odpovědní e-mail AI plán — opraveno „vyplnila" (krátké i)
- [ ] Odpovědní e-maily — odstraněn veškerý konkrétní časový údaj, zůstává jen „Ozvu se ti co nejdřív."
- [ ] Přepínač „EN" — úplně vpravo za „Začít", vizuálně utlumený
- [ ] Anglická verze — audit podle checklistu v sekci F
- [ ] Po všech úpravách publikovat a otestovat v anonymním okně

---

*Opravy kolo 3 · květen 2026 · mentorka@ailadies.cz*
