# Zadání pro Macaly: sekce FAQ (rozklikávací akordeon) – AILadies

**Stránka:** [ailadies.cz](https://www.ailadies.cz/)  
**Typ úpravy:** přidat samostatnou sekci FAQ  
**Forma:** rozklikávací akordeon (otázka → klik → zobrazí se odpověď)

---

## 1) Cíl sekce

Přidat na web přehlednou sekci nejčastějších otázek, která:
- snižuje obavy před objednáním mentoringu,
- vysvětluje rozdíl mezi mentoringem a kurzy,
- podporuje rozhodnutí „jít do toho“.

Sekce má být čitelná, stručná a mobilně přívětivá.

---

## 2) Umístění sekce

Požadované umístění:
- **hned pod sekci `Začít`**,
- **nad sekci `Doporuč dál`**.

Pořadí na stránce má být:
1. `Začít`
2. `FAQ (Časté otázky)`
3. `Doporuč dál`

---

## 2b) FAQ odkaz v horní navigaci

Ano, přidat FAQ i do horní lišty.

Požadované umístění v menu:
- **za položku `O mně`**
- před CTA tlačítky (`AI plán`, `Začít`)

Doporučené pořadí menu:
`Pro koho | Jak to funguje | Co dostaneš | Nabídka | O mně | FAQ | AI plán | Začít`

Klik na `FAQ` má scrollovat na FAQ sekci (anchor link).

---

## 3) Název sekce (nahradit stávající text)

Aktuální text:
- `Časté otázky`
- `Ještě váháš? Tady jsou odpovědi.`

Nahradit tímto:

**Varianta A (doporučená):**
- Eyebrow: `Časté otázky`
- Hlavní titulek: `Co tě možná napadá před začátkem`


---

## 4) UX chování akordeonu

- Každá položka = 1 otázka (klikací řádek) + odpověď (skrytá/rozbalená).
- Ikona vpravo: `+` (zavřeno), po rozbalení `×` nebo otočené `+`.
- Animace rozbalení jemná (cca 200–300 ms).
- Na desktopu může být otevřená vždy jen 1 otázka (doporučeno).
- Na mobilu musí být klikací plocha přes celou šířku řádku.
- **Výchozí stav po načtení: všechny otázky zavřené** (žádná předem rozbalená).

---

## 5) Finální obsah FAQ (copy-paste)

### 1. Co když s AI neumím vůbec nic?
Nemusíš nic umět. Začneme u toho, co reálně děláš v práci, a ukážu ti, kde ti AI pomůže od prvního dne.

### 2. Čím se AI Ladies mentoring liší od kurzů nebo videí na YouTube?
Kurzy a videa ukazují obecné příklady. V mentoringu řešíme přímo tvou práci, tvé cíle a tvůj způsob fungování. Odcházíš s konkrétními výstupy, které hned použiješ.

### 3. AI změní práci. Co to znamená konkrétně pro mě? Mám se bát?
Nemusíš se bát. AI je nástroj, který ti může ušetřit čas, zjednodušit rutinu a dát větší jistotu v práci. A platí jednoduchá věc: kdo se s AI naučí pracovat, má výhodu a je napřed.

### 4. Jaký nástroj budeme používat?
Na první setkání nepotřebuješ nic placeného. Vyzkoušíme základní nástroje jako ChatGPT, Gemini, NotebookLM nebo Claude. Každý se hodí na něco jiného a já ti pomůžu vybrat, co má smysl pro tvou práci.

### 5. Kdy a kde probíhají setkání?
Online přes Google Meet, v čase, který si vybereš v mém kalendáři. Pokud máš zájem o osobní setkání, domluvíme se individuálně.

### 6. Co když nestíhám pracovat mezi sezeními?
Nic se neděje. Tempo mentoringu přizpůsobíme tvému životu, ne naopak.

### 7. Proč si vybrat mentoring právě ode mě?
Mám zkušenosti z médií, nezisku i AI prostředí a právě ta kombinace je důvod, proč mentoring funguje prakticky a bez zbytečné teorie.  
Jako moderátorka a novinářka umím klást správné otázky, rychle se dostat k podstatě a vysvětlit složité věci jednoduše, srozumitelně a bez technického žargonu. Díky tomu neřešíme obecné návody, ale to, co opravdu potřebuješ ty.  
Spoluzaložila jsem neziskovku Fandi mámám, takže rozumím realitě každodenního provozu, vedení týmu i tomu, jak náročné je zavádět změny do praxe, když je málo času a energie.  
Zkušenost z AI-first firmy Aibility mi zase dala pohled zevnitř na to, jak rychle se AI posouvá, kde má největší dopad a jak ji využít v různých typech práce.  
A protože sama nejsem technický typ, vím, kde se můžeš zaseknout — často dřív, než se to stane — a pomůžu ti najít cestu, která bude dávat smysl právě tobě.

---

## 6) Vizuální styl

- Zachovat aktuální brand (barvy, typografie, spacing).
- Otázky tučnější/kontrastnější než odpovědi.
- Odpovědi max-width pro dobrou čitelnost.
- Jemné oddělovače mezi položkami (1 px, světlá linka).

---

## 7) Kontrola po nasazení

- [ ] Sekce je opravdu rozklikávací (akordeon), ne statický text.
- [ ] Funguje na mobilu i desktopu.
- [ ] Texty jsou přesně podle zadání (včetně diakritiky).
- [ ] U otázky „AI změní práci…“ je zachovaný závěr: „kdo se s AI naučí pracovat, má výhodu a je napřed.“
- [ ] Nadpis sekce je nahrazen novou variantou (A/B/C).
- [ ] Po načtení FAQ jsou všechny položky zavřené.
- [ ] V horním menu je položka `FAQ` umístěná za `O mně` a odkazuje na FAQ sekci.
