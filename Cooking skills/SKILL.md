---
name: heti-menu-tervezo
description: >
  Családi heti ebéd és vacsora menüterv készítése bevásárlólistával, receptekkel és tápanyag-információval.
  Használd ezt a skill-t, amikor a felhasználó heti menüt, étkezési tervet, ebéd- vagy vacsoratervet kér,
  bevásárlólistát szeretne, receptötleteket keres a hétre, vagy bármilyen családi étkezés-tervezésről van szó.
  Akkor is triggerelődj, ha a felhasználó azt mondja: "mit főzzek", "mit együnk", "tervezd meg a hetet",
  "bevásárlólista", "heti kaja", "menüterv", vagy hasonló. Még akkor is használd, ha nem mondja ki
  kifejezetten hogy "menüterv" — ha étkezés-tervezésről van szó, ez a skill kell.
---

# Családi Heti Menütervező

Segíts a családnak megtervezni a heti ebéd és vacsora menüt! A család 2 felnőttből és 3 gyerekből áll (7, 5 és 3 évesek).

## Alapelvek

### Receptek használata
**MINDIG a `receptek/` mappában lévő receptfájlok alapján tervezz.** Ne találj ki új receptet — csak olyat tervezz, ami dokumentálva van. Ha a felhasználó mégis új ételt szeretne, jegyezd meg, de javasold hogy azt is dokumentálják.

### Gyerekbarát szemlélet
Minden receptfájl tartalmaz egy "Gyerekek" szekciót — ez az irányadó:
- 🟢 = az adott gyerek eszik belőle
- 🟡 = vegyesen, alkalmanként eszi
- 🔴 = nem eszi

Ha egy ételt valamelyik gyerek nem eszik, gondoskodj alternatíváról (pl. egy egyszerűbb köret vagy a másik szülő feladata lesz az alternatíva).

### Változatosság
- Egy héten belül ne ismétlődjön ugyanaz az étel vagy ugyanaz a fehérjeforrás túl sűrűn
- Váltogasd a fehérjeforrásokat: csirke, sertés, marha, hal, tojás, hüvelyesek
- Legyen legalább 1 húsmentes nap a héten
- Váltakozzanak a levesek, főételek, főzelékek, könnyű fogások

### Praktikusság
- Hétköznap gyors ételeket tervezz (max. 30-45 perc — az elkészítési idő minden receptfájlban szerepel)
- Hétvégén megengedhető a hosszabb főzés
- Gondolj a maradék-újrahasznosításra (pl. bolognai ragu → másnap lasagna)
- Ebédre mindig tervezz levest ÉS főételt (leves + második fogás)

---

## Munkafolyamat

### 0. lépés: Receptek beolvasása

Mielőtt tervezel, olvasd be:
1. `receptek.md` — az összes elérhető étel áttekintése
2. `kedvencek.md` — a kedvencek listája
3. Az adott hétre tervezett receptek fájljait a `receptek/` mappából
4. **A legutóbbi ~3 hét menütervét** (`heti-menu-*.md`) — kiindulásként, hogy lásd, mi szerepelt nemrég. ⚠️ De ezek csak terv-szintűek; a tényleges étkezéseket **a felhasználótól kérdezd meg** (lásd 1. lépés, 0. kérdés), és azt vedd alapul a **Gyakoriság** címke betartásához (ne ismételj a megadott időköznél sűrűbben; csirkepaprikás max 3 hetente egyszer).

### 1. lépés: Információgyűjtés

**MINDIG egyezz meg a főzési kapacitásban, MIELŐTT tervet készítenél.** Kérdezd meg:

0. **Mit ettetek / főztetek VALÓJÁBAN az elmúlt héten?** A mentett menütervek gyakran NEM tükrözik a valóságot (a család sokszor változtat). Ezért a Gyakoriság-ellenőrzéshez (mit ne ismételj) ne csak a `heti-menu-*.md` fájlokra hagyatkozz — **kérdezd meg a felhasználót, mi készült el ténylegesen**, és azt vedd alapul.
1. **Mely napokra kell terv?** Melyik napokon főzünk, és melyik napokon eszünk maradékot / rendelünk? (Nem mindig kell mind a 7 napra terv.)
2. **Az egyes főzős napokon mennyi idő / mikor lesz a főzésre?** Pl. melyik napon van csak rövid idő (gyors étel kell), melyiken lehet ráérősen főzni, és van-e nap amikor előző este lehet előkészíteni.
3. Van-e speciális alkalom a héten? (vendégek, születésnap, kirándulás, elfoglalt napok)
4. Van valami amit mindenképpen szeretnének/nem szeretnének ezen a héten?

**A főzési kapacitást kösd össze az előkészíthetőség címkével:**
- **Zsúfolt nap / kevés idő:** 🟢 (előző nap elkészítve) vagy 🟡 (előre előkészítve) ételeket időzíts ide, illetve gyors (≤30 perc) fogásokat.
- **Ráérős nap:** ide kerülhetnek a 🔴 (frissen készítendő) és a hosszabb elkészítési idejű ételek.
- Ha egy napon előző este van idő előkészíteni, használd ki (pác, szósz, püré, tészta előre).

### 2. lépés: Menüterv összeállítása

Készíts egy markdown fájlt az alábbi struktúrával. A fájl neve: `heti-menu-YYYY-WNN.md`.

```markdown
# 🍽️ Heti Menüterv — [dátum hétfőtől vasárnapig]

## Heti áttekintés

| Nap | Ebéd (leves + főétel) | Vacsora |
|-----|------------------------|---------|
| Hétfő | ... + ... | ... |
| Kedd | ... | ... |
| Szerda | ... | ... |
| Csütörtök | ... | ... |
| Péntek | ... | ... |
| Szombat | ... | ... |
| Vasárnap | ... | ... |

---

## Hétfő

### 🥣 Ebéd: [leves neve] + [főétel neve]

**Leves:** [leves neve]
**Elkészítési idő:** X perc | **Kalória:** ~XXX kcal/felnőtt | ~XXX kcal/gyerek
**Recept:** `receptek/[fajlnev].md`

**Főétel:** [főétel neve]
**Elkészítési idő:** X perc | **Kalória:** ~XXX kcal/felnőtt | ~XXX kcal/gyerek
**Recept:** `receptek/[fajlnev].md`

**Gyerekek:** [ki eszi, ki nem — a receptfájl alapján]

**💡 Tipp:** [praktikus megjegyzés, pl. előkészítés, tálalás gyerekeknek]

### 🍲 Vacsora: [étel neve]
[ugyanez a struktúra]

---

[... további napok ...]

---

## 🛒 Bevásárlólista

> Az összetevők a receptfájlokban szereplő pontos hozzávalók alapján, 5 főre összesítve.

### 🥩 Hús, hal
- [ ] ...

### 🥛 Tejtermékek, tojás
- [ ] ...

### 🥦 Zöldség, gyümölcs
- [ ] ...

### 🫙 Szárazáru, tartósáru
- [ ] ...

### 🌿 Fűszerek
- [ ] ...

### 🍞 Pékáru
- [ ] ...

### 🛒 Egyéb
- [ ] ...

---

## 📊 Heti tápanyag-összesítő

| Nap | Ebéd kcal | Vacsora kcal | Összesen |
|-----|-----------|-------------|----------|
| Hétfő | ... | ... | ... |
| **Heti átlag** | **...** | **...** | **...** |

> Becsült értékek, felnőtt adagokra. Gyerekadagok: 7 éves ~70%, 5 éves ~60%, 3 éves ~50%.
```

### 3. lépés: Bevásárlólista összeállítása

- Olvasd be minden tervezett receptfájlt
- Összesítsd az összetevőket (ne legyen duplikáció)
- Ellenőrizd minden receptfájl **"Bevásárlólista megjegyzés"** szekcióját — ha van ilyen, azokat a tételeket is add hozzá (pl. csilis babhoz automatikusan szalsza hozzávalók is kellenek)
- Kategorizáld bolt-barát sorrendben

**Beszerzési időzítés (mindig tervezd meg):**
- Minden hozzávaló **legkésőbb 1 nappal a főzés napja előtt** legyen otthon — ne a főzés napján kelljen vásárolni.
- Ha egy ételt előző nap készítünk el vagy este előkészítünk (🟢/🟡 címke, pl. pác), akkor a hozzávaló az **előkészítés napjára** kell — vagyis a beszerzési határidő még 1 nappal korábbra csúszik (gyakorlatilag 2 nappal az evés napja előtt).
- A bevásárlólistához készíts egy rövid **„Beszerzési ütemezés"** szakaszt: a fő bevásárlás legkésőbbi napja, és ha kell, melyik tételt mikorra kell beszerezni.
- Gyorsan romló tételeknél (friss hal, friss zöldfűszer, pékáru) jelezd, hogy a felhasználás napjához közel, de még a határidőn belül érdemes venni.

### 4. lépés: Kedvencek / receptek frissítése

Ha az interakció során új étel kerül szóba, javasold a `receptek/` mappába való felvételét.

---

## Kimenet

A végső kimenet egyetlen markdown fájl:
1. Heti áttekintő táblázat
2. Napi bontás (minden napra ebéd + vacsora, receptfájlra hivatkozással)
3. Összesített bevásárlólista (receptfájlok hozzávalói alapján)
4. Tápanyag-összesítő táblázat

A fájlt mentsd a munkakönyvtárba `heti-menu-YYYY-WNN.md` néven.
