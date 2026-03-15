# 🍽️ Heti Menütervező Skill — Claude Code

## Telepítés

### 1. Másold a skill mappát a Claude Code skills könyvtárba:

```bash
# Ha a projekted gyökerében vagy:
mkdir -p .claude/skills
cp -r heti-menu-tervezo .claude/skills/
```

### 2. Hozd létre a kedvencek fájlt a projekted gyökerében:

```bash
cp .claude/skills/heti-menu-tervezo/kedvencek-template.md kedvencek.md
```

Ezután töltsd ki a `kedvencek.md` fájlt a családod kedvenc ételeivel!

## Használat

Indítsd el a Claude Code-ot és írd be bármelyiket:

- `"Tervezd meg a jövő heti menüt"`
- `"Mit főzzünk ezen a héten?"`
- `"Készíts heti bevásárlólistát"`
- `"Gyors vacsoraötletek kellenek a hétre"`
- `"Heti menüterv kell ebédre és vacsorára"`

### Speciális kérések

- `"Ezen a héten sok zöldséget szeretnénk enni"`
- `"Szombaton vendégek jönnek, 8 főre tervezz"`
- `"Gyors ételek kellenek, max 30 perc főzés"`
- `"A gyerekeknek bevált a mac and cheese, add hozzá a kedvencekhez"`

## Kimenetek

A skill egy markdown fájlt generál (`heti-menu-YYYY-WNN.md`), ami tartalmazza:

1. **Heti áttekintő táblázat** — gyors összefoglaló
2. **Napi bontás** — minden napra ebéd + vacsora recept
3. **Bevásárlólista** — kategóriákba rendezve, checkbox-okkal
4. **Tápanyag-összesítő** — becsült kalória értékek

## Kedvencek kezelése

A `kedvencek.md` fájlban tarthatod nyilván, mit szeret a család. A skill minden tervezésnél figyelembe veszi ezt a fájlt, és ha új kedvenc derül ki, felajánlja a frissítését.

## Tippek

- Hétvégén kérd meg, hogy a jövő hétre tervezzen
- Ha valami nagyon bejött, mondd hogy "ez kedvenc lett" és frissíti a listát
- Kérhetsz tematikus heteket is (pl. "olasz hét", "könnyű nyári ételek")
- A bevásárlólista kinyomtatható vagy telefonon is használható
