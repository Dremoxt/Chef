# CLAUDE.md

## Projekt leírás

Ez egy családi heti menütervező projekt. A cél, hogy minden héten könnyen és gyorsan összeállítsuk az ebéd és vacsora menüt az egész családnak, bevásárlólistával, receptekkel és tápanyag-információval együtt.

## Családi kontextus

### Családtagok
- **Apa** — felnőtt, normál adag
- **Anya** — felnőtt, normál adag
- **Nagygyerek** — 7 éves, kb. 70%-os felnőtt adag
- **Középső** — 5 éves, kb. 60%-os felnőtt adag
- **Kicsi** — 3 éves, kb. 50%-os felnőtt adag

### Étrendi korlátozások
- Nincs allergia, intoleranicia vagy egyéb korlátozás

### Étkezési szokások
- **Ebéd:** könnyedebb, de tápláló (a gyerekek napközben aktívak)
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
- **Csak vacsora:** Virsli, Gofri

## Fájlstruktúra

```
.
├── CLAUDE.md                  # Ez a fájl — projekt kontextus
├── kedvencek.md               # Család kedvenc ételei
├── receptek.md                # Receptlista index (kategóriák, gyerekjelölések, időigény)
├── szoszok.md                 # Szósz receptek és párosítások
├── receptek/                  # Részletes receptfájlok (egy étel = egy fájl)
│   ├── csilis-bab.md
│   ├── bolognai-ragu.md
│   ├── lasagna.md
│   ├── csirkepaprikas.md
│   ├── galuska.md
│   ├── paprikas-krumpli.md
│   ├── fuszeres-csirkemell-csikok.md
│   ├── caciki.md
│   ├── palacsinta.md
│   ├── husleves.md
│   ├── kaposztaleves-husos.md
│   ├── kaposztaleves-vegetarian.md
│   ├── brokkoli-kremleves.md
│   ├── karfiol-kremleves.md
│   ├── cukkini-kremleves.md
│   ├── savanyú-krumplileves.md
│   ├── spenótos-tejszínes-csirkemell.md
│   ├── sertes-szuzerme-krumplipurevel.md
│   └── pasztorpite.md
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

- A menütervet KIZÁRÓLAG a `receptek/` mappában lévő receptek alapján kell összeállítani
- A bevásárlólista az egyes receptfájlokban szereplő pontos hozzávalók alapján készül
- A bevásárlólista legyen összesített (ne legyen 3x csirkemell külön-külön)
- A bevásárlólista checkbox formátumú (`- [ ]`)
- Minden receptfájl "Bevásárlólista megjegyzés" szekciójában szereplő extra tételek is kerüljenek a listára
- A gyerekek étkezési preferenciái receptenként eltérnek — mindig az adott receptfájl "Gyerekek" szekciója az irányadó
- A tápanyag-összesítő becsült kalória értékeket tartalmazzon felnőtt és gyerek adagra
- A kimenet nyelve mindig magyar
