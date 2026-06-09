# CLAUDE.md

## Projekt leírás

Családi heti menütervező — ebéd és vacsora tervezés 5 főre (2 felnőtt + 3 gyerek), bevásárlólistával és receptekkel.

## Kontextus
### Étrendi korlátozások
- Nincs allergia, intoleranicia vagy egyéb korlátozás

### Étkezési szokások
- **Ebéd:** mindig leves + főétel (könnyedebb, de tápláló — a gyerekek napközben aktívak)
- **Vacsora:** tartalmasabb főétkezés, a család együtt eszik
- **Hétköznap:** max 30-45 perc főzési idő, gyors és egyszerű
- **Hétvégén:** lehet igényesebb, hosszabb elkészítési idejű étel is
- A gyerekek iskolás/óvodás korúak, fontos a rendszeres étkezés

### Konyha stílus preferenciák
1. **Magyar/hagyományos** — gulyás, pörkölt, rántott húsok, levesek, tésztaételek
2. **Gyors/egyszerű** — egyedényes ételek, tészták, szendvicsek, omlettek
3. **Egészségtudatos** — sok zöldség, teljes kiőrlés, kevesebb cukor, de gyerekbarát ízek
4. **Nemzetközi** — pizza, pasta, wok, enyhe curry, burrito — gyerekek is szeretik

### Fontos szempontok
- A gyerekek nem szeretik a túl fűszeres/csípős ételeket
- Új ételeket óvatosan, kis adagban vezessünk be
- Maradék-újrahasznosítás: ha vasárnap sült csirke van, hétfőn legyen csirkés saláta/szendvics
- Heti legalább 1 húsmentes nap
- Fehérjeforrások rotálása: csirke, sertés, marha, hal, tojás, hüvelyesek
- A bevásárlólista legyen bolt-barát: kategóriákba rendezve

### Étkezés-típus kötések (melyik étel mikor szerepelhet)
- **Csak ebéd:** Csirkepaprikás, Sertés szűzérme krumplipürével, Pásztorpite
- **Csak vacsora:** Virsli, Gofri, Tejbegríz, Palacsinta

### Előkészíthetőség címke (minden receptfájl fejlécében)
Minden receptfájl tartalmaz egy **Előkészíthetőség** mezőt, ami megmondja, mennyire lehet előre dolgozni vele:
- 🟢 **Előző nap elkészíthető** — nyugodtan elkészíthető előre, felmelegítve is jó (sokszor finomabb)
- 🟡 **Részben előkészíthető** — egyes elemek előre mehetnek (pác, szósz, tészta, püré), a befejezés frissen
- 🔴 **Frissen, aznap készítendő** — frissen az igazi, nem érdemes előre csinálni

Tervezésnél használd ezt: zsúfolt napokra a 🟢/🟡 ételeket időzítsd (előző nap előkészítve), a 🔴 ételeket ráérős napokra.

### Gyakoriság címke (minden receptfájl fejlécében)
Minden receptfájl tartalmaz egy **Gyakoriság** mezőt, ami megmondja, milyen sűrűn szerepelhet az étel a menüben:
- 🔁 **Heti 1-2×** — gyors kedvencek (virsli, meleg szendvics)
- 🔁 **~Hetente 1×** — pl. húsleves, édes fogások (gofri, palacsinta, tejbegríz), pizza
- 🔁 **~2 hetente 1×** — a legtöbb leves és gyors főétel
- 🔁 **~3 hetente 1×** — laktató/munkásabb ételek (lasagna, csilis bab tartomány) és a **csirkepaprikás (legfeljebb 3 hetente egyszer)**
- 🔁 **Igény szerint** — köretek/kísérők (galuska, caciki)

**Tervezésnél kötelező:** nézd meg a legutóbbi ~3 hét menütervét (`heti-menu-*.md`), és ne sértsd meg a gyakoriságot — ami nemrég szerepelt, azt a megadott időközön belül ne tervezd újra. **Csirkepaprikás: max 3 hetente egyszer.**

### Szezonalitás címke (minden receptfájl fejlécében)
Minden receptfájl tartalmaz egy **Szezonalitás** mezőt, ami megmondja, melyik évszakhoz illik leginkább:
- ☀️ **Nyár** — könnyű, friss zöldséges fogások (cukkini krémleves, caciki)
- 🌱 **Tavasz** / 🍂 **Ősz** — szezonális zöldségek (brokkoli, spenót)
- 🍂❄️ **Ősz–tél** — laktató, lassú, melegítő ételek (húsleves, lasagna, rakott krumpli, karfiol/káposztaleves)
- 🗓️ **Egész évben** — kamra-/hús-alapú, szezonfüggetlen ételek

**Tervezésnél vedd figyelembe az aktuális hónapot:** lehetőleg szezonális fogásokat válassz (nyáron könnyű/zöldséges, télen laktató/melegítő). Az „Egész évben" ételek bármikor mehetnek.

## Fájlstruktúra

```
.
├── CLAUDE.md                  # Ez a fájl — projekt kontextus
├── kedvencek.md               # Család kedvenc ételei
├── receptek.md                # Receptlista index (kategóriák, gyerekjelölések, időigény)
├── szoszok.md                 # Szósz receptek és párosítások
├── receptek/                  # Részletes receptfájlok (egy étel = egy fájl)
│   ├── bolognai-ragu.md
│   ├── brokkoli-kremleves.md
│   ├── caciki.md
│   ├── csilis-bab.md
│   ├── csirkepaprikas.md
│   ├── cukkini-kremleves.md
│   ├── fuszeres-csirkemell-csikok.md
│   ├── galuska.md
│   ├── gofri.md
│   ├── husleves.md
│   ├── instant-ramen.md
│   ├── kaposztaleves-husos.md
│   ├── kaposztaleves-vegetarian.md
│   ├── karfiol-kremleves.md
│   ├── lasagna.md
│   ├── meleg-szendvics.md
│   ├── omlett.md
│   ├── palacsinta.md
│   ├── paprikas-krumpli.md
│   ├── pasztorpite.md
│   ├── pizza-rendeles.md
│   ├── rakott-krumpli.md
│   ├── savanyú-krumplileves.md
│   ├── sertes-szuzerme-krumplipurevel.md
│   ├── spenótos-tejszínes-csirkemell.md
│   ├── tejbegriz.md
│   ├── tojas-krem.md
│   ├── tonhalas-paradicsomos-teszta.md
│   └── virsli.md
├── heti-menu-YYYY-WNN.md      # Generált heti menütervek (pl. heti-menu-2026-W09.md)
└── Cooking skills/
    └── SKILL.md               # A menütervező skill
```

## Parancsok / Gyakori kérések

| Mit mondj | Mit csinál |
|-----------|-----------|
| `"Tervezd meg a jövő heti menüt"` | Teljes heti menüterv generálás |
| `"Mit főzzünk ezen a héten?"` | Ugyanaz, kicsit lazább formában |
| `"Gyors vacsorák kellenek a hétre"` | Hétköznapi gyors receptekre fókuszál |
| `"Frissítsd a kedvenceket"` | kedvencek.md frissítése |
| `"Szombaton vendégek jönnek, 8 fő"` | Adott napra speciális tervezés |
| `"Mutasd a múlt heti menüt"` | Korábbi menüterv megnyitása |

## Minőségi elvárások

- **Tervezés előtt MINDIG egyezz meg a főzési kapacitásban:** mely napokon főzünk (vs. maradék/rendelés), és az egyes főzős napokon mennyi idő / mikor lesz a főzésre. Ez alapján időzítsd az ételeket az előkészíthetőség címke szerint (zsúfolt nap → 🟢/🟡 + gyors fogás; ráérős nap → 🔴 + hosszabb ételek).
- A menütervet KIZÁRÓLAG a `receptek/` mappában lévő receptek alapján kell összeállítani
- **Tervezés előtt MINDIG kérdezd meg, mit ettek/főztek VALÓJÁBAN az elmúlt héten** — a mentett menütervek gyakran nem tükrözik a valóságot (a család sokszor változtat). A tényleges étkezéseket vedd alapul, ne csak a `heti-menu-*.md` fájlokat.
- **Tartsd be a receptek Gyakoriság címkéjét:** a tényleges (megkérdezett) elmúlt heti étkezések + a legutóbbi ~3 hét menüi alapján ne ismételj a megadott időköznél sűrűbben (csirkepaprikás max 3 hetente egyszer)
- A bevásárlólista az egyes receptfájlokban szereplő pontos hozzávalók alapján készül
- A bevásárlólista legyen összesített (ne legyen 3x csirkemell külön-külön)
- A bevásárlást is tervezd meg időben: minden hozzávaló **legkésőbb 1 nappal a főzés (vagy az előző esti előkészítés) napja előtt** legyen otthon. A bevásárlólista tartalmazzon egy rövid „Beszerzési ütemezés" szakaszt a legkésőbbi beszerzési nappal/napokkal.
- A bevásárlólista checkbox formátumú (`- [ ]`)
- Minden receptfájl "Bevásárlólista megjegyzés" szekciójában szereplő extra tételek is kerüljenek a listára
- A gyerekek étkezési preferenciái receptenként eltérnek — mindig az adott receptfájl "Gyerekek" szekciója az irányadó
- A tápanyag-összesítő becsült kalória értékeket tartalmazzon felnőtt és gyerek adagra
- A kimenet nyelve mindig magyar
