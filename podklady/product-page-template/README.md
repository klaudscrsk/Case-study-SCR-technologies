# Produktova stranka — sablona a generovanie

Definuje **presnu strukturu produktovej stranky** SCR (riesenia) a sluzi na
generovanie novych produktovych stranok cez Claude Code.

- `pos-vzor.html` — REFERENCNA produktova stranka (Podnikovy operacny system).
  Etalon aj sablona. Otvor dvojklikom v prehliadaci (ziadny server, ziadna appka).
- `assets/` — obrazky/screenshoty produktu. Uz su tu realne SynCore screenshoty,
  takze vzor sa zobrazi kompletny.

> Vzor zodpoveda produktovej stranke na webe (scrweb appka, `ProduktPage.vue`).
> Bloky su 1:1 ako komponenty webu — obsah sa neskor cisto preklopi do realneho
> webu. Finalny vizual doladi Figma; tu ide o strukturu a obsah.

---

## Ako vygenerovat novu produktovu stranku (workflow pre Matu)

1. Daj do `inputs/` zdroj — popis produktu, painpointy, hodnoty, moduly,
   referencie, screenshoty.
2. V Claude Code napis napr.:
   *"Vygeneruj produktovu stranku pre <PRODUKT> podla
   product-page-template/pos-vzor.html. Zdroj je inputs/<subor>. Uloz ako
   product-page-template/<produkt>.html."*
3. Claude skopiruje vzor, blok po bloku nahradi obsah a ulozi novy HTML.
4. Screenshoty produktu dohodis do `assets/` a v HTML nahradis cesty.

---

## Struktura stranky — bloky (poradie ako vo vzore)

| # | Blok | Co obsahuje | Povinny |
|---|------|-------------|---------|
| — | Bocna navigacia | plavajuce menu sekcii vlavo (auto, zobrazi sa po hero) | ano |
| 1 | Hero | brand, breadcrumb, headline, podtitulok, CTA, 4 metriky, 2 screenshoty | ano |
| 2 | Vyzvy | preco platforma — 4 karty s painpointmi + "Z praxe" | ano |
| — | Logo strip | "Doveruju nam" — loga klientov | nie |
| 3 | Hodnoty | 8 kariet "co platforma riesi" (grid) | ano |
| 4 | Ukazky | screenshot slider (2 viditelne) | nie (vynechaj ak nie su) |
| 5 | Moduly | 3 stlpce: Core / Konfigurovatelne / Odvetvie-specific | ano |
| 6 | Projekty | slider referencnych pribehov (3 viditelne) | ano |
| 7 | Pristup | tmava sekcia + horizontalna timeline (5 krokov) | nie |
| 8 | Referencie | 1-3 citacie klientov | nie |
| 9 | Technologie | 6 kariet principov + zaverecna veta | ano |
| 10 | CTA | zaverecna vyzva | ano |

> Volitelne bloky (ukazky, pristup, referencie, logo strip) jednoducho vymaz
> z HTML, ak pre dany produkt nemas obsah. B2B portal napr. ma rovnaku strukturu,
> ina sada dat.

---

## Z coho sa plnia bloky (mapovanie zdroj -> stranka)

- **Painpointy, hodnoty, moduly, prinos** — primarne z `../02_produkty_podklady.md`
  (sekcia daneho produktu) + zo zdroja.
- **Referencne pribehy a citacie** — z `../03_referencie.md` (kniznica referencii).
- **Nazvy, brand, tagline** — z `../04_kanaly_a_formaty.md` (mapovanie SK/EN nazvov).
  Brand badge v hero (napr. "SynCore") je na webe pouzity — v textovom obsahu inde
  drz popisny nazov.

---

## Pravidla

- **Jazyk:** produktova stranka je verejny obsah -> pis SO SPRAVNOU DIAKRITIKOU.
- **Ton:** partner, nie dodavatel; civilne a konkretne, ziadna vata.
- **Citlive veci** (konkretne cisla klienta, mena, NDA) over s Lubosom.

### Akcentova farba
Vzor pouziva oranzovu (SCR). Pre iny produkt staci v HTML hore v `.cs-page { ... }`
prepisat premenne `--accent*`.

### Interaktivne bloky
- **Ukazky** (screenshot slider) a **Projekty** (slider pribehov) maju prev/next
  tlacidla + bodky (vanilla JS dole v subore). Funguju z `file://` bez servera.
- **Bocna navigacia** sa zobrazi po odrolovani za hero a zvyrazni aktivnu sekciu.
- **Moduly** maju hover tooltip s popisom (Core a Konfigurovatelne stlpce).

### Obrazky (assets/)
- Hero: 2 screenshoty (`imgMain`, `imgSecondary`).
- Ukazky slider: N screenshotov.
- Projekty: 1 screenshot per pribeh (volitelne).
- Realny obrazok: `<img src="assets/nazov.png" alt="..." loading="lazy">`.
- Konvencia: vsetky media daj do `assets/` (idealne s nazvom produktu/klienta).
