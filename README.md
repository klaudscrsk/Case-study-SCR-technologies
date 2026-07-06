# Case study — SCR technologies

Repozitár na tvorbu case studies (a produktových stránok) SCR technologies
v jednotnom vizuálnom štýle 1:1 podľa vzoru.

## Štruktúra

Každý projekt = **vlastný priečinok** s `input/` (podklady) a `output/` (hotové HTML).
Priečinok `podklady/` je spoločný pre všetky projekty (vzory + kontext o SCR).

```
.
├── GALIA-case-study/        ← jeden projekt = jeden priečinok
│   ├── input/               ← SEM podklady (brief, screenshoty, logo, čísla, citácie)
│   └── output/              ← SEM hotové HTML (otvoriteľné dvojklikom v prehliadači)
├── <DALSI-PROJEKT>/         ← ďalšie case studies rovnako (input/ + output/)
└── podklady/    ← spoločný „onboarding pack" — kontext o SCR + záväzné HTML vzory (needitovať)
    ├── CLAUDE.md                     → pravidlá a workflow (mozog)
    ├── 01_firma_a_positioning.md     → kto je SCR: positioning, claim, čísla, klienti, leadership
    ├── 02_produkty_podklady.md       → 9 produktov: tagline, painpointy, prínos, kľúčové slová, klienti
    ├── 03_referencie.md              → knižnica referencií: plné popisy projektov, čísla, citácie
    ├── 04_kanaly_a_formaty.md        → sitemap webu, mapovanie SK/EN názvov, formáty a dĺžky
    ├── case-study-template/
    │   ├── travitor-vzor.html        → ZÁVÄZNÝ vzor case study (12 blokov)
    │   └── README.md                 → štruktúra 12 blokov + čo do ktorého
    └── product-page-template/
        ├── pos-vzor.html             → ZÁVÄZNÝ vzor produktovej stránky (10 blokov)
        └── README.md                 → štruktúra blokov + čo do ktorého
```

## Ako to funguje

1. **Podklady** k novej case study (brief, screenshot vzoru, čísla, citácie) daj do
   `<PROJEKT>/input/`.
2. Povedz napr.: *„Vygeneruj case study pre GALIA, podklady sú v GALIA-case-study/input/"*.
3. Hotové HTML sa uloží do `<PROJEKT>/output/` ako `<projekt>.html`.

## Záväzné pravidlá (zhrnutie z `podklady/CLAUDE.md`)

- **Vernosť predlohe pred kreativitou** — vzor (`travitor-vzor.html` / `pos-vzor.html`)
  je záväzná dizajnová šablóna. Zachovaj poradie a počet sekcií, rozloženie, počty
  boxov/kariet/citácií/čísel a približné dĺžky textov.
- **Brand identita = vždy SCR.** Case study je marketingová stránka SCR (klient je len jej
  téma). Akcentová farba ostáva **oranžová ako v Travitor vzore** — `--accent*` premenné
  NEPREFARBUJEME podľa klienta. Logo a prvky klienta sa umiestňujú **presne ako v Travitore**
  (napr. logo klienta v hero na tmavom pozadí).
- **Diakritika zapnutá** — verejný obsah so správnou slovenčinou.
- **Čísla a citácie len z podkladov** (`03_referencie.md` alebo zdroj v `input/`). Nevymýšľať.
- **Názvy produktov konzistentne** podľa `02_produkty_podklady.md` a `04_kanaly_a_formaty.md`.
- **Positioning = strategický partner**, nie dodávateľ.
- **Firemné údaje** (IČO, adresa, presný názov) overovať na https://finstat.sk/47203811.
