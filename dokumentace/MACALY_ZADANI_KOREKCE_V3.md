# Zadání pro Macaly: korekce po posledním náhledu (AILadies)

**Stránka:** [ailadies.cz](https://www.ailadies.cz/)  
**Typ dokumentu:** samostatné doplňující zadání  
**Navazuje na:** `MACALY_ZADANI_HERO_REDESIGN.md` a `MACALY_ZADANI_SEKCE_UPRAVY_V2.md`  

---

## Cíl

Tento dokument obsahuje pouze finální korekce po posledním náhledu, aby šly realizovat samostatně bez hledání v předchozích poznámkách.

---

## 1) Sekce O mně – vrátit portrétní layout

### Co je špatně teď
- Fotka je vložená jako široký banner a nevychází ořez (není vidět hlava).

### Co má být nově
- Rozložení vrátit do původní podoby:
  - **fotka vlevo**
  - **text vpravo**
- Fotka musí být **portrét na výšku**, ne landscape banner.
- Ořez nastavit tak, aby byl vidět celý obličej (v Macaly použít ekvivalent `object-position: center top`).
- Zaoblení rohů zachovat.

### Přesný soubor
- Použít: `01_PROJEKTY/AILadies/assets/petra_o_mne_fotka_portrait_667x1000.png`
- Referenční formát: **667 × 1000 px** (portrét), tento poměr zachovat.

---

## 2) Sekce O mně – ponechat jen LinkedIn dole

- Blok odrážek s hvězdičkami (Fandi mámám, Moderování, AI vzdělávání, Podcast, Mediální tréninky) **zůstává smazaný**.
- Ve spodní části sekce nechat pouze:
  - `→ LinkedIn profil`
  - odkaz: `https://www.linkedin.com/in/petra-kv%C4%9Btov%C3%A1-p%C5%A1eni%C4%8Dn%C3%A1/`

---

## 3) Sekce „Získej svůj osobní AI plán“ – kartička vpravo

### Důležitá korekce obsahu kartičky
- Kartička nesmí vypadat jako „10 promptů“.
- Musí odpovídat tématu **Osobní AI plán**.
- Do kartičky **nedávat jméno Petra Květová Pšeničná**.

### Doporučený text přímo na kartičce

```
OSOBNÍ AI PLÁN · PDF

Tvůj plán na míru
kde začít s AI
a co řešit jako
první krok

stručně a prakticky
bez technického
balastu
```

### Vizuál kartičky
- Styl ponechat hravý (nakloněná kartička, jemný stín).
- Na hover se může narovnat (pokud to Macaly umí).

---

## 4) Potvrzení, co se nemění

- Hero korekce z předchozích dokumentů platí beze změny.
- Ceny a úspory balíčků platí beze změny.
- Ostatní texty na stránce se nyní neupravují.

---

## Krátký checklist

- [ ] O mně: portrét vlevo + text vpravo (ne banner).
- [ ] O mně: použita fotka `petra_o_mne_fotka_portrait_667x1000.png`.
- [ ] O mně: hlava není oříznutá.
- [ ] O mně: zůstává jen LinkedIn odkaz.
- [ ] AI plán kartička: text je o osobním AI plánu, ne o promptech.
- [ ] AI plán kartička: bez jména.
