# autoservis-kral

Ukázkový web pro fiktivní autoservis — **Autoservis Král**.

## Status

Hotové a nasazené. Repo: [adam-kriz/autoservis-kral](https://github.com/adam-kriz/autoservis-kral).
Živý web: **https://adam-kriz.github.io/autoservis-kral/**

## Brief

Portfolio/ukázkový web ve stylu, který má zaujmout **autoservisy, pneuservisy,
autolakovny a podobné "akční" obory** — třetí vzorek stylu do oslovovacích
mailů kampaně `kampan-weby/` (viz `kampan-weby/CLAUDE.md`, sekce „Ukázkové
weby v mailu"), vedle `malejpodnik/` (kavárenský styl) a `remeslna-dilna/`
(dílenský/industriální styl pro klasické řemeslníky).

**Autoservis Král je fiktivní firma** — žádná konkrétní firma z
`pribram-web-leady.pdf`. Text (příběh, zakázky, kontakty) je smyšlený tak,
aby web působil jako reálný menší autoservis v Příbrami.

## Design — druhá verze (po zamítnutí první)

První verze (brutalistní styl s tlustými černými obrysy, tvrdými stíny
a ručně kreslenými SVG ikonami — v podstatě jen přebarvená `remeslna-dilna`)
byla **zamítnuta**: uživatel chtěl něco, co nepůsobí "kresleně", a má
skutečný náboj pro lidi kolem aut. Aktuální verze je proto **úplně jiný
vizuální jazyk**:

- Tmavý, fotkami řízený design (ne světlá "papírová" paleta jako u ostatních
  dvou vzorků) — asfaltově černé pozadí (`--bg`), tlumené tmavě šedé karty
  (`--surface`)
- Skutečné fotky (viz `img/`, zdroj Pexels, volná licence) místo kreslených
  ikon — mechanik v dílně, detail kola/brzdy, auto za tmy
- Gradientní červeno-oranžový akcent (`--red` → `--red-2`) používaný na
  tlačítkách, nadpisech (text s gradientem) a "glow" stínech — žádné tlusté
  černé obrysy ani skloněné (skew) prvky z první verze
- Editorial/premium mřížka služeb s tenkými linkami místo kartiček s
  ikonami v rámečku
- Marquee pruh se scrollujícím textem (CSS animace) pro pocit pohybu
- Font **Anton** (masivní, blokový verzálkový display font) pro nadpisy —
  jiný než Oswald (`remeslna-dilna`) i Bebas Neue (zavržená první verze),
  + Inter pro běžný text

## Stack

Statický web, jeden soubor `index.html` (inline CSS, bez build stepu) +
složka `img/` se staženými fotkami.

- Fonty: Google Fonts – Anton (nadpisy, verzálky), Inter (běžný text)
- Barevná paleta (CSS proměnné v `:root`): `--bg`/`--surface` (tmavé pozadí
  a karty), `--red`/`--red-2` (gradientní červeno-oranžový akcent), `--text`/
  `--text-soft` (světlý text na tmavém pozadí), `--line` (jemné 1px
  oddělovače místo silných obrysů)
- Fotky v `img/` (stažené z pexels.com, licence Pexels — volné k použití,
  bez nutnosti kreditovat): `hero.jpg`, `about.jpg`, `detail.jpg`,
  `wheel.jpg`, `contact-bg.jpg`

## Konvence

Řídí se konvencemi z kořenového [`CLAUDE.md`](../CLAUDE.md) — vlastní GitHub
repo `autoservis-kral`, nezávislé na kořenovém repu workspace.

## Lokální náhled

`.claude/launch.json` v kořeni workspace obsahuje konfiguraci `autoservis-kral`
(Python `http.server` na portu 8126).
