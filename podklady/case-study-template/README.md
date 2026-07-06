# Case study — sablona a generovanie

Tento priecinok definuje **presnu strukturu case study** SCR a sluzi na
generovanie novych case studies cez Claude Code.

- `travitor-vzor.html` — REFERENCNA case study (Travitor). Je to etalon aj
  sablona zaroven. Otvor ju dvojklikom v prehliadaci (ziadny server, ziadna
  appka) a vidis presne ako ma case study vyzerat.
- `assets/` — obrazky, screenshoty a video. Uz su tu **realne Travitor assety**
  (hero-video.mp4, 6 screenshotov, logo), takze vzor sa zobrazi kompletny.
  Pre novu case study sem das media klienta a v HTML prepises cesty.

> Vzor zodpoveda case study na webe (scrweb appka, stranka Travitor). Bloky su
> 1:1 ako komponenty webu — takze obsah sa neskor cisto preklopi do realneho
> webu. Finalny vizual doladi Figma; tu ide o strukturu a obsah.

---

## Ako vygenerovat novu case study (workflow pre Matu)

1. Daj do `inputs/` (alebo do tohto priecinka) zdroj — Word, PDF, poznamky,
   cisla, citacie od klienta/PM.
2. V Claude Code napis napr.:
   *"Vygeneruj case study pre projekt <KLIENT> podla case-study-template/
   travitor-vzor.html. Zdroj je inputs/<subor>. Uloz ako
   case-study-template/<klient>.html."*
3. Claude skopiruje vzor, blok po bloku nahradi obsah zo zdroja a ulozi novy
   HTML. Otvoris ho v prehliadaci a skontrolujes.
4. Obrazky/screenshoty/video dohodis do `assets/` a v HTML nahradis placeholdery
   (bloky s prerusovanou ciarou a popisom `assets/...`).

---

## Struktura case study — 12 blokov (poradie ako vo vzore)

| # | Blok | Co obsahuje | Povinny |
|---|------|-------------|---------|
| 1 | Hero | tagy (odvetvie · riesenie · krajina), headline, podtitulok, 3-4 hlavne cisla | ano |
| 2 | Intro (O projekte) | 2 odstavce o projekte + meta (klient, odvetvie, trh, nasa rola, partneri, infra) | ano |
| 3 | Video | ukazkove video platformy | nie (vynechaj ak nie je) |
| 4 | Challenge (Vyzva) | 4-5 painpointov klienta + zvyrazneny citat | ano |
| 5 | Approach (Pristup) | 3 karty (01 analyza, 02 dizajn, 03 architektura) + zaverecna veta | ano |
| 6 | Image grid (Galeria) | 6 screenshotov platformy | nie (vynechaj ak nie su) |
| 7 | Solution (Riesenie) | feature list + moduly + integracie + 3 showcase ukazky | ano |
| 8 | Tech stack (Technologia) | 4 technologicke piliere + 3 bloky (standardy, bezpecnost, open-source) | nie |
| 9 | Impact (Vysledky) | 4 velke cisla s popisom | ano |
| 10 | Testimonials | 1-3 citacie pouzivatelov/klienta | nie |
| 11 | Partnership (Nas prinos) | text + timeline milnikov | ano |
| 12 | CTA | zaverecna vyzva na akciu | ano |

> Volitelne bloky (video, galeria, tech, testimonials) jednoducho vymaz z HTML,
> ak pre dany projekt nemas obsah. Zuba (druha hotova case study na webe) napr.
> nema video ani galeriu — a je to v poriadku.

---

## Z coho sa plnia bloky (mapovanie zdroj -> case study)

- **Cisla a citacie** ber primarne z `../03_referencie.md` (kniznica referencii)
  alebo z toho, co je v zdrojovom subore. Nevymyslaj cisla.
- **Painpointy a prinos** — ak ich zdroj nema, inspiruj sa painpointmi/prinosom
  produktu v `../02_produkty_podklady.md` (podla typu riesenia projektu).
- **Tagy v Hero** (odvetvie + riesenie) ber LEN z ciselnika — slovenske nazvy
  produktov a odvetvi su v `../04_kanaly_a_formaty.md` (mapovanie SK/EN/slug).
  Nikdy vymyslene labely.

---

## Pravidla

- **Jazyk:** case study je verejny obsah -> pis SO SPRAVNOU DIAKRITIKOU.
- **Ton:** partner, nie dodavatel; civilne a konkretne (cisla, fakty), ziadna vata.
- **Citlive veci** (konkretne cisla klienta, mena, NDA) over s Lubosom pred publikovanim.

### Akcentova farba per klient
Vzor pouziva oranzovu (Travitor). Pre iny projekt staci v HTML hore v sekcii
`.cs-page { ... }` prepisat 7 premennych `--accent*` (napr. na firemnu farbu
klienta). Cely vizual sa prefarbi automaticky.

### Obrazky a video (assets/)
- Placeholdery vo vzore (prerusovana ciara s popisom `assets/...`) ukazuju, kam
  pride ake medium.
- Realny obrazok: nahrad placeholder za `<img src="assets/screen-1.png" alt="...">`.
- Realne video: `<video controls poster="assets/poster.jpg"><source src="assets/video.mp4" type="video/mp4"></video>`.
- Konvencia: vsetky media pre danu case study daj do `assets/` (idealne s nazvom klienta v subore).
