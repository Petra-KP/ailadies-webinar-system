# AILadies – Cookie lišta: co připravit a jak nastavit

> Krátký návod pro web ailadies.cz (Macaly nebo jiný builder). Právní rámec: **GDPR** + **ePrivacy** (směrnice o soukromí v elektronických komunikacích) – u **neesenciálních** cookies (analytika, marketing) je potřeba **předchozí souhlas**; technicky nezbytné cookies mohou běžet bez souhlasu.

---

## 1. Co máš mít připavené **před** zapnutím lišty

| Položka | Účel |
|--------|------|
| **Odkaz na Zásady ochrany osobních údajů** | Lišta musí odkazovat na stránku s informací o zpracování (máš v `AILadies_obchodni_podminky_DRAFT.md` část II, nebo samostatná URL). |
| **Odkaz na Obchodní podmínky** | Doporučené u e-shopu/plateb; u čistě informačního webu stačí v patičce. |
| **Seznam cookies / technologií podle kategorií** | Nutné vs. analytické vs. případně marketing. Níže návrh pro AILadies. |
| **Rozhodnutí, co přesně na webu používáš** | Např. jen Google Analytics 4? Hotjar? Pixel? Embedy? – **bez toho nejde** lištu správně nastavit. |

---

## 2. Kategorie cookies (logika lišty)

### A) Nezbytné (vždy zapnuté, bez souhlasu)

- Session / bezpečnost (např. přihlášení, košík, CSRF) – pokud Macaly něco takového používá.
- Uložení **volby v cookie liště** (aby se uživateli znovu neukazovala po každém kliknutí).
- Technické cookies poskytovatele hostingu.

**Text do lišty (stručně):**  
„Nezbytné cookies zajišťují základní funkce webu a nemohou být vypnuty.“

### B) Analytické (vyžadují souhlas před načtením skriptu)

Typicky:

- **Google Analytics 4** (`_ga`, `_gid`, …) – pokud ho na web vložíš.
- Případně **Hotjar**, **Plausible** (některé režimy) – dle dokumentace nástroje.

**Důležité:** Skript GA4 **nesmí** běžet dřív, než uživatel souhlasí s analytikou (nebo dokud nezvolí „Přijmout vše“ podle tvého nastavení). Macaly nebo cookie nástroj musí **blokovat** načítání, dokud není souhlas.

### C) Marketing / reklamní (souhlas)

- Meta Pixel, Google Ads remarketing, LinkedIn Insight – **jen pokud** někdy přidáš.

---

## 3. Návrh obsahu pro **AILadies** (co doplnit do Macaly / CMP)

### Krátký úvodní text (cookie banner)

> Tento web používá cookies a podobné technologie. Některé jsou nezbytné pro fungování stránky, jiné nám pomáhají analyzovat návštěvnost a zlepšovat služby. Podrobnosti najdete v [Zásadách ochrany osobních údajů](#).

*(Odkaz nahraď skutečnou URL stránky se zásadami.)*

### Tlačítka (minimálně)

- **„Pouze nezbytné“** – odmítnout vše kromě nutných.
- **„Přizpůsobit“** (volitelné) – rozbalí kategorie.
- **„Přijmout vše“** – souhlas s analytikou (a marketingem, pokud ho máš).

Doporučení: mít **stejně výrazné** „Odmítnout“ / „Pouze nezbytné“ jako „Přijmout vše“ (doporučení ÚOOÚ a praxe).

### Dlouhá verze – sekce „Cookies“ ve zásadách (doplň do části II OP)

Připrav tabulku nebo seznam:

| Název / nástroj | Účel | Typ | Doba platnosti |
|-----------------|------|-----|----------------|
| [cookie lišty] | Uložení preferencí | Nezbytné | 12 měsíců |
| _ga (Google) | Měření návštěvnosti | Analytické | dle Google |
| _gid (Google) | Měření návštěvnosti | Analytické | dle Google |

**Pozn.:** Pokud použiješ jen Macaly vestavěnou analytiku bez GA, přečti si jejich dokumentaci – některé nástroje jsou **first-party** a stále mohou vyžadovat informování.

---

## 4. Co **konkrétně** připravit jako soubory / texty

1. **Jedna stránka „Zásady ochrany osobních údajů“** na webu  
   - Obsah z části II dokumentu `AILadies_obchodni_podminky_DRAFT.md` + sekce **Cookies** s tabulkou výše.

2. **Jedna stránka „Cookies“** (volitelně samostatná)  
   - Nebo jen kotva `#cookies` na stejné stránce jako zásady.

3. **Cookie lišta v Macaly**  
   - Zapnout vestavěnou cookie lištu / integraci (např. Google Consent Mode v2, pokud používáš GA4).  
   - Zkontrolovat v dokumentaci Macaly: [Cookie consent / GDPR](https://www.macaly.com/) – aktuální postup se mění.

4. **Google Analytics 4 (pokud ho používáš)**  
   - V GA4 zapnout **souhlas** (Consent Mode v2): měření před souhlasem omezené / anonymní podle nastavení.  
   - Připravit **GTM** nebo vložení skriptu **až po** souhlasu.

5. **„Cookie policy“ export** – některé nástroje (Cookiebot, CookieYes, …) generují seznam – u jednoduchého webu stačí ručně udržovaná tabulka.

---

## 5. Checklist před spuštěním webu

- [ ] Víš přesně, které skripty (GA, Hotjar, chat…) běží na doméně.
- [ ] Neesenciální skripty se **nenačítají** bez souhlasu.
- [ ] Lišta má odkaz na **zásady** a jasnou volbu **odmítnout** nepodstatné.
- [ ] Uložení preference funguje (cookie / localStorage).
- [ ] V zásadách je popsané **kdo** je správce, **účel** cookies, **doba** uchování.
- [ ] Po změně nástrojů (nový Pixel) aktualizovat tabulku a lištu.

---

## 6. Texty „copy-paste“ pro lištu (krátké varianty)

**Varianta A – jeden odstavec**

> Používáme cookies. Nezbytné cookies jsou nutné pro funkci webu. Analytické cookies nám pomáhají pochopit, jak web používáte – zapíší se jen s vaším souhlasem. Více informací v zásadách ochrany osobních údajů.

**Varianta B – ještě kratší**

> Respektujeme vaše soukromí. Nastavte cookies podle svých preferencí. Podrobnosti v zásadách ochrany osobních údajů.

---

## 7. Kde to v projektu doplnit

- Po dokončení webu: stejný obsah **zkopírovat** do Macaly (cookie banner + stránka se zásadami).
- Tento soubor `AILadies_cookie_lista_navod.md` drž jako **interní checklist**; při změně nástrojů ho aktualizuj.

---

*Poslední aktualizace: březen 2026. Právní vývoj (Consent Mode, ePrivacy Regulation) sleduj u ÚOOÚ a u poskytovatele analytiky.*
