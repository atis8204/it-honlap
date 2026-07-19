---
layout: ../../layouts/BlogPost.astro
title: "Skálázható vagy csak túlméretezett? Hogyan tervezz IT-infrastruktúrát egy növekvő cégnek"
description: "A jó IT-tervezés nem arról szól, hogy a legnagyobbat vedd. 20 év tapasztalat alapján hogyan találd meg az egyensúlyt a mai igény és a jövőbeli növekedés között."
date: "2026. július 19."
tag: "IT Üzemeltetés"
slug: "skalazhato-vagy-tulmeretezett"
readTime: 6
---

Van egy hiba, amit sok cég elkövet, amikor IT-infrastruktúrát vásárol: vagy túl kicsit vesz, és fél év múlva már fuldoklik, vagy túl nagyot, és évekig fizet olyan kapacitásért, amit soha nem használ ki.

A jó tervezés valahol a kettő között van. És ez nem szerencse kérdése — ez mérnöki munka. Húsz év alatt épp elég rendszerbővítést és hardvercserét láttam ahhoz, hogy tudjam: a legtöbb probléma abból ered, hogy valaki vagy alul-, vagy túllőtte a méretezést. Ebben a cikkben leírom, hogyan érdemes ezt átgondolni — hogyan kerüld el a túlméretezést úgy, hogy közben nem fejlődsz bele a rendszerbe fél év alatt.

---

## A két rossz véglet

**Az alultervezés** a látványosabb probléma. Megveszed a legolcsóbb megoldást, ami „most éppen elég", aztán jön két új kolléga, elindul egy új rendszer, és hirtelen minden lassú. A szerver zihál, a hálózat akadozik, és vészhelyzetben kell bővíteni — ami mindig drágább és stresszesebb, mint ha előre terveztél volna.

**A túltervezés** csendesebb, de ugyanúgy pénzbe kerül. Megveszed a nagyvállalati szintű megoldást egy öt fős cégnek, mert „legyen benne tartalék". Aztán három év múlva lecseréled, és soha nem használtad ki a felét sem. A pénz, amit a felesleges kapacitásra költöttél, ott ült kihasználatlanul.

A cél nem az, hogy elkerüld mindkettőt teljesen — hanem hogy tudatosan dönts arról, hol húzod meg a határt.

---

## 1. Először a mai igényt mérd fel, ne a jövőt

A tervezés mindig a jelennel kezdődik. Mielőtt bármit veszel, tudnod kell, mit csinál a rendszer *most*:

- Hány felhasználó dolgozik egyszerre?
- Milyen alkalmazások futnak, és mennyire erőforrás-igényesek?
- Mennyi adat keletkezik havonta?
- Mikor van a csúcsterhelés — és mekkora?

Ez a kiindulópont. Ha ezt nem méred fel, akkor nem tervezel, hanem tippelsz — és a tippelés vagy alul-, vagy túllövéshez vezet.

---

## 2. A növekedést becsüld meg, de reálisan

Most jön a kulcskérdés: mennyivel nőttök? Itt a legtöbben elrontják — vagy egyáltalán nem gondolnak rá, vagy irreálisan nagyot álmodnak.

A jó becslés reális és időhöz kötött. Nem az a kérdés, hogy „mi lesz, ha tízszeresére nőünk", hanem hogy **„mi a valószínű méret 2-3 év múlva?"** Egy cég, ami évi 15-20%-kal nő, három év alatt nagyjából másfélszeresére hízik — nem tízszeresére.

A tervezésnek erre a reális horizontra kell szólnia. Túl messzire tervezni ugyanolyan pazarlás, mint egyáltalán nem tervezni.

---

## 3. Válaszd szét, mi drága bővíteni és mi olcsó

Ez a mérnöki tervezés lényege, és itt dől el, hogy okosan költesz-e.

Nem minden komponenst kell előre túlméretezni — csak azt, amit **később drága vagy fájdalmas bővíteni**. A logika egyszerű:

**Amit olcsó és gyors később bővíteni**, azt vedd a mai igényre méretezve. Például a memória (RAM) egy szerverben általában könnyen bővíthető — nem kell előre teletömni. A tárhely sok rendszerben szintén bővíthető utólag.

**Amit drága vagy nehéz később cserélni**, ott érdemes tartalékot hagyni. Például az alapinfrastruktúra — a hálózati gerinc, a switchek portszáma, a szerver alaplapja, ami meghatározza, meddig bővíthető egyáltalán. Ha itt spórolsz, később az egészet cserélheted.

Ez a szétválasztás a különbség a mérnök és a szerelő között: nem mindent méretezel túl, csak azt, aminek a bővítése később aránytalanul fájna.

---

## 4. Gondolkodj modulokban, ne monolitban

A skálázható rendszer titka, hogy **darabonként bővíthető**. Ha úgy tervezel, hogy minden egy nagy, összefüggő egység, akkor bővítéskor az egészet kell megfognod. Ha modulárisan tervezel, akkor csak azt a darabot fejleszted, ahol a szűk keresztmetszet van.

Egy példa: ahelyett, hogy egyetlen óriási szervert vennél, ami mindent csinál, sokszor jobb két-három kisebb, célzott egység — így ha egy funkció nő ki magát, csak azt bővíted, nem az egészet. Ráadásul, ha egy komponens meghibásodik, nem áll le az egész rendszer.

---

## 5. A tartalék nem pazarlás — a puffer az része a tervnek

Van egy fontos különbség a túlméretezés és a **tudatos tartalék** között.

A túlméretezés az, amikor kétszer akkorát veszel, mint amire valaha szükség lesz. A tudatos tartalék az, amikor tudod, hogy a rendszernek nem szabad 100%-on futnia — mert akkor nincs hova nőni a csúcsterhelésnek, és az első nagyobb igény megakasztja.

Egy jól tervezett rendszer általában 60-70%-os normál kihasználtságon fut, hogy legyen hova mennie a terhelésnek. Ez nem pazarlás — ez a stabilitás ára. A gép, ami folyamatosan a határon üzemel, előbb-utóbb bedől.

---

## Összefoglalva

A skálázható infrastruktúra nem a legnagyobb, hanem a **legokosabban tervezett** rendszer. A recept:

1. **Mérd fel a mai igényt** pontosan, ne tippelj.
2. **Becsüld meg a növekedést** reálisan, 2-3 éves horizonton.
3. **Válaszd szét**, mit olcsó és mit drága később bővíteni — és csak az utóbbinál hagyj tartalékot.
4. **Tervezz modulárisan**, hogy darabonként bővíthess.
5. **Hagyj tudatos puffert**, mert a 100%-on futó rendszer nem stabil.

A túlméretezés pénzbe kerül. Az alultervezés stresszbe és vészhelyzetbe. A jó tervezés a kettő között van — és ez az, ami megkülönbözteti azt, aki csak beállítja a rendszert, attól, aki előre is gondolkodik.
