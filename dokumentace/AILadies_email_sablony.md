# AILadies – E-mailové šablony

> Šablony pro Google Workspace (kalendář, fakturace), Macaly a ruční odeslání.  
> U každé části jsou **dvě verze** – **vykání** (formálnější) a **tykání** (osobnější). Vyber si, co sedí.

---

## 0. Potvrzení poptávky „Hledáš jiný formát?" (formulář Poptat nabídku)

> Automatický e-mail odesílaný po odeslání formuláře „Poptat nabídku" (blok „Hledáš jiný formát?" v sekci Nabídka).
> Odesílatel: mentorka@ailadies.cz. Tykání.

### 0a – Auto-response klientce (tykání)

**Předmět:** Díky za poptávku – AILadies

---

Ahoj [OSLOVENÍ],

díky, že ses ozvala – tvoje poptávka mi právě dorazila.

Brzy se ti ozvu s návrhem spolupráce na míru.

Těším se!
Petra
AILadies · ailadies.cz · mentorka@ailadies.cz

---

> **Poznámka k poli [OSLOVENÍ]:** Propojit s polem formuláře „Jak tě mám oslovit?" (5. pád). Pokud je prázdné, fallback na pole „Jméno" v základním tvaru.

### 0b – Notifikace Petře (kopie poptávky)

**Komu:** mentorka@ailadies.cz
**Předmět:** Nová poptávka – [TYP POPTÁVKY] – [JMÉNO] [PŘÍJMENÍ]

---

Nová poptávka přes web AILadies:

Jméno: [JMÉNO] [PŘÍJMENÍ]
E-mail: [EMAIL]
Typ poptávky: [TYP POPTÁVKY]
Zpráva: [ZPRÁVA]

Poptávka je uložena v admin panelu Macaly.

---

## 1. Potvrzení odeslání poptávky (formulář / Macaly)

> Po odeslání poptávky. **Ne** slibovat potvrzení termínu do 1–2 dnů – klientka si termín vybírá sama v rezervačním kalendáři.

### 1a – Vykání

**Předmět:** Děkujeme za poptávku – AILadies

---

Dobrý den, paní [PŘÍJMENÍ] / [JMÉNO],

děkujeme za váš zájem o osobní AI mentoring. Vaše poptávka nám dorazila.

Na adresu **[E-MAIL]** jsme vám právě poslali potvrzovací e-mail. Pokud ho nevidíte, zkontrolujte prosím složku Nevyžádaná.

**Další krok:**  
Vyberte si prosím vhodný termín a počet hodin v **rezervačním kalendáři**:  
[ODKAZ NA KALENDÁŘ / BOOKING]

Jakmile si termín zarezervujete, obdržíte potvrzení rezervace a den před sezením automatickou připomínku z Google kalendáře.

---

**INDIVIDUÁLNÍ NABÍDKA**

Připravím pro vás individuální nabídku na míru. Ozvu se vám do **1–2 pracovních dnů** s přesnou cenou, rozsahem a platebními pokyny.

Faktura vám přijde e-mailem po potvrzení programu (nebo po domluvě podle vašeho procesu).

---

S pozdravem  
Petra Květová Pšeničná  
AILadies · ailadies.cz · hello@ailadies.cz

---

### 1b – Tykání

**Předmět:** Díky za poptávku! AILadies

---

Ahoj [JMÉNO],

díky, že ses ozvala – tvoje poptávka mi právě dorazila.

Na **[E-MAIL]** jsem ti poslala potvrzovací e-mail. Kdyby nepřišel, koukni do spamu.

**Co dál:**  
Vyber si prosím termín a počet hodin v **rezervačním kalendáři**:  
[ODKAZ NA KALENDÁŘ]

Jakmile si termín zarezervuješ, přijde ti potvrzení rezervace a den před mentoringem ti Google pošle automatickou připomínku.

---

**INDIVIDUÁLNÍ NABÍDKA**

Připravím pro tebe individuální nabídku na míru. Ozvu se ti do **1–2 pracovních dnů** s přesnou cenou, rozsahem a platebními pokyny.

Fakturu ti pošlu e-mailem po potvrzení programu (nebo po domluvě).

---

Těším se!  
Petra  
AILadies · ailadies.cz

---

## 2. Potvrzení po výběru termínu (Google Kalendář – automatický e-mail)

> Odesílá se ve chvíli, kdy si klientka zarezervuje slot. Lze napojit na „Potvrzení rezervace“ v Google Calendar nebo na vlastní šablonu z Apps Scriptu.

### 2a – Vykání

**Předmět:** Potvrzení rezervace – AI mentoring AILadies

---

Dobrý den, [JMÉNO],

děkujeme, že jste si vybrala termín osobního AI mentoringu.

**Rezervace:** [DATUM] v [ČAS]  
**Délka:** 60 minut  
**Spojení:** online přes **Google Meet** (odkaz najdete v pozvánce v kalendáři a v připomínce).

Den před sezením vám přijde **automatická připomínka** z Google účtu – s časem a odkazem na Meet.

Na setkání budu připravená podle informací, které jste mi poslala v poptávce. Pokud budete mít jakýkoli dotaz předem, napište mi prosím na hello@ailadies.cz.

Těším se na setkání.

S pozdravem  
Petra Květová Pšeničná  
AILadies

---

### 2b – Tykání

**Předmět:** Máš rezervovaný termín – AILadies

---

Ahoj [JMÉNO],

díky, že sis vybrala termín mentoringu – máme ho zarezervovaný.

**Kdy:** [DATUM] v [ČAS]  
**Délka:** 60 minut  
**Kde:** online přes **Google Meet** – odkaz je v kalendářové pozvánce a přijde i v připomínce.

Den předem ti Google pošle **automatickou připomínku**, ať na nic nezapomeneš.

Budu připravená podle toho, co jsi mi napsala v poptávce. Kdybys měla jakýkoli dotaz, ozvi se na hello@ailadies.cz.

Těším se!

Petra  
AILadies

---

## 3. Faktura zaplacená (platební / fakturační automatizace)

> Krátký e-mail po připsání platby (Google Workspace + Apps Script nebo ručně). Pokud ještě **nemá** zarezervovaný termín, přidej odstavec s kalendářem.

### 3a – Vykání (termín už má zarezervovaný)

**Předmět:** Platba přijata – děkuji, AILadies

---

Dobrý den, [JMÉNO],

děkuji za úhradu faktury **[ČÍSLO FAKTURY]**. Platba mi dorazila – **váš mentoring je uhrazený** a já se moc těším na naši spolupráci.

Vše je v pořádku. Setkání máte v kalendáři na **[DATUM A ČAS]**; den předem přijde připomínka s odkazem na Google Meet.

V případě dotazů jsem k dispozici na hello@ailadies.cz.

S pozdravem  
Petra Květová Pšeničná  
AILadies

---

### 3b – Vykání (termín ještě nemá – má si vybrat)

**Předmět:** Platba přijata – rezervace termínu

---

Dobrý den, [JMÉNO],

děkuji za úhradu faktury **[ČÍSLO FAKTURY]**. Platba mi dorazila – **váš mentoring je uhrazený**.

Pokud jste si ještě **nevybrala termín** ani počet hodin, udělejte tak prosím v rezervačním kalendáři:  
[ODKAZ NA KALENDÁŘ]

Tam zvolíte **počet hodin**, které chcete využít, a vhodný termín. Po rezervaci obdržíte potvrzení a den před sezením automatickou připomínku.

Děkuji a těším se na setkání.

S pozdravem  
Petra Květová Pšeničná  
AILadies

---

### 3c – Tykání (termín už má)

**Předmět:** Platba dorazila – díky!

---

Ahoj [JMÉNO],

díky, platba za fakturu **[ČÍSLO FAKTURY]** mi přišla – **mentoring máš zaplacený** a já se moc těším.

Máme domluvené sezení na **[DATUM A ČAS]**; den předem ti přijde připomínka s Meetem.

Kdybys cokoli potřebovala, napiš na hello@ailadies.cz.

Petra  
AILadies

---

### 3d – Tykání (termín ještě nemá)

**Předmět:** Platba dorazila – ještě si vyber termín

---

Ahoj [JMÉNO],

díky, platba mi přišla – **mentoring máš zaplacený**.

Pokud sis ještě **nevybrala termín** nebo **počet hodin**, udělej to prosím tady:  
[ODKAZ NA KALENDÁŘ]

V kalendáři nastavíš, kolik hodin chceš využít, a vybereš si čas. Pak ti přijde potvrzení a den předem připomínka.

Těším se!

Petra  
AILadies

---

## 4. Připomínka před sezením (1 den předem)

> Může zůstat ruční nebo se částečně překrývat s automatickou připomínkou Google Calendar. Níže plná verze s nahráváním (jako dřív).

### 4a – Tykání (plná verze)

**Předmět:** Zítra se potkáme! Pár tipů na přípravu

---

Ahoj [JMÉNO],

jen krátká připomínka, že se zítra potkáme na AI mentoringu.

**Kdy:** [DATUM A ČAS]  
**Kde:** online – odkaz na Google Meet: [ODKAZ]  
**Délka:** 60 minut

**Aby ses z toho dostala maximum:**

- Přines si konkrétní úkol nebo problém, na kterém chceš pracovat  
- Mít otevřený počítač (budeme společně zkoušet nástroje)  
- Klidně si připrav otázky, které tě napadly  

Žádná příprava není povinná – prostě přijď tak, jak jsi.

**Nahrávání:**  
Sezení nahrávám, abych ti pak mohla připravit materiály – souhrn, prompty, šablony a prezentaci. Nahrávku zpracuji pomocí AI nástrojů (Cursor/Claude, ChatGPT) – všechny mám nastavené tak, že tvoje data nepoužívají k trénování. Materiály ti zpřístupním na zabezpečené stránce chráněné heslem; nahrávka se smaže do 30 dnů.  
Pokud ti nahrávání nevyhovuje, dej mi vědět – budu dělat pouze písemné poznámky.

Těším se!  
Petra

---

### 4b – Vykání (plná verze)

**Předmět:** Zítra – AI mentoring AILadies

---

Dobrý den, [JMÉNO],

připomínám zítřejší osobní AI mentoring.

**Termín:** [DATUM A ČAS]  
**Spojení:** online přes Google Meet – [ODKAZ]  
**Délka:** 60 minut

Doporučuji mít připravený konkrétní úkol nebo otázku z vaší praxe a otevřený počítač. Příprava není povinná.

**Nahrávání:**  
Sezení nahrávám za účelem přípravy materiálů pro vás (souhrn, prompty, šablony). Zpracování probíhá v nástrojích s vypnutým trénováním na datech; materiály obdržíte na zabezpečené stránce. Nahrávka je uchována nejdéle 30 dnů.  
Pokud s nahráváním nesouhlasíte, dejte mi prosím vědět – budu vést pouze písemné poznámky.

S pozdravem  
Petra Květová Pšeničná  
AILadies

---

## 5. Souhrn po sezení + materiály

> Stejný obsah jako dřív; přidávám stručnou vykací variantu nadpisu a úvodu.

### 5a – Tykání

**Předmět:** Shrnutí dnešního sezení + materiály pro tebe

---

Ahoj [JMÉNO],

díky za dnešní sezení! Tady je shrnutí toho, co jsme spolu prošly.

**Co jsme řešily:**  
[2–3 věty]

**Co jsme vytvořily / nastavily:**  
- [výstup 1]  
- [výstup 2]  
- [výstup 3]  

**Doporučení na vyzkoušení:**  
- [úkol 1]  
- [úkol 2]  

**Materiály:**  
[ODKAZ] · heslo: [HESLO]

---

Zkus si s tím pohrát a dej mi vědět, jak ti to šlo. Pokud chceš další termín, napiš nebo použij rezervační kalendář: [ODKAZ].

Petra

---

### 5b – Vykání

**Předmět:** Souhrn po mentoringu + materiály – AILadies

---

Dobrý den, [JMÉNO],

děkuji za dnešní sezení. Posílám stručný souhrn a materiály.

**Téma:**  
[2–3 věty]

**Výstupy:**  
- [výstup 1]  
- [výstup 2]  

**Doporučené kroky:**  
- [úkol 1]  

**Materiály:**  
[ODKAZ] · heslo: [HESLO]

V případě dotazů pište prosím na hello@ailadies.cz. Další termín si můžete vybrat zde: [ODKAZ NA KALENDÁŘ].

S pozdravem  
Petra Květová Pšeničná  
AILadies

---

## 6. Follow-up (3 dny po sezení)

### 6a – Tykání

**Předmět:** Jak ti to šlo s AI?

---

Ahoj [JMÉNO],

je to pár dní od našeho sezení – jak ti to šlo? Podařilo se ti vyzkoušet [KONKRÉTNÍ VĚC]?

Kdybys narazila na cokoli, napiš. A pokud chceš pokračovat, stačí rezervační kalendář nebo odpověď na tento e-mail.

Petra

---

### 6b – Vykání

**Předmět:** Krátká zpětná vazba – AILadies

---

Dobrý den, [JMÉNO],

ráda bych se zeptala, jak se vám daří aplikovat to z posledního sezení – zejména [KONKRÉTNÍ VĚC].

V případě dotazů jsem k dispozici na hello@ailadies.cz. Další termín si můžete vybrat v rezervačním kalendáři.

S pozdravem  
Petra Květová Pšeničná

---

## 7. Žádost o referenci (po 2–3 sezeních)

*(Obě verze – uprav podle zvoleného tykání/vykání v komunikaci.)*

**Předmět (tykání):** Malá prosba – tvoje zkušenost  
**Předmět (vykání):** Ráda bych vás požádala o krátkou referenci

---

[Tykání:] Ahoj [JMÉNO], moc si vážím naší spolupráce…  
[Vykání:] Dobrý den, [JMÉNO], vážím si naší spolupráce…

Mohla byste mi prosím napsat 2–3 věty – jak vám mentoring pomohl, co se změnilo, komu byste službu doporučila?  
Formální ani dlouhé to být nemusí.

Děkuji!  
Petra

---

## 8. Welcome – newsletter / webinář

*(Ponecháno; při potřebě doplň vykací variantu stejně jako u bodů výše.)*

---

## 9. Později – automatizace (připomínka, souhrn jako u Sonji)

> Sem doplníme šablony po odladění procesu:  
> - plná automatická připomínka (jen Meet + čas vs. rozšířená s nahráváním),  
> - případně přesný text „jako u Sonji“ pro souhrn po první hodině.

**Placeholder:** `[Sem vložit odkaz na vzorový e-mail / Sonja – po doplnění]`

---

## Poznámky k použití

- **Macaly / web:** sekce 1 – potvrzení poptávky + individuální nabídka (bez slibu „potvrdím termín za vás“).  
- **Google Calendar:** sekce 2 – po rezervaci slotu.  
- **Platba:** sekce 3 – po připsání platby; pokud platba přijde před výběrem termínu, použij 3b nebo 3d.  
- **Před sezením:** sekce 4 – buď jen Google reminder, nebo tento delší e-mail.  
- Placeholdery: `[JMÉNO]`, `[E-MAIL]`, `[ODKAZ NA KALENDÁŘ]`, `[ČÍSLO FAKTURY]`, `[ODKAZ MEET]`, `[HESLO]`.
