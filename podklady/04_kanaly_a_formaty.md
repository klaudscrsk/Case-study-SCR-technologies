# Kanaly, web a formaty

Kde a v akom tvare publikujeme. Konkretne ucty a pristupy ti da Lubos/marketing.

## Kanaly
- **Web SCR** (scrtechnologies.sk) — hlavny kanal. Prechadza redizajnom 2026
  (shift z "software house" na strategickeho partnera). Detail nizsie.
- **LinkedIn** — hlavny B2B kanal (firemny profil + profily ludi z leadershipu).
- **Clutch** — referencie a hodnotenia (B2B recenzny portal, mame 5.0).
- **Blog** — odborny obsah, novinky (sekcia na webe).
- **Ponuky a decky** — case studies a proof-pointy sa pouzivaju aj v predaji.

---

## Web SCR — struktura a sitemap

> Pozn.: nizsie je struktura podla noveho webu (Vue appka, `_apps/web`).
> Web je v slovencine. URL adresy (slug) su bez diakritiky.

### Sitemap (verejne stranky)
```
/                                       Domov
/riesenia                               Riesenia a sluzby (rozcestnik)
   /riesenia/podnikovy-operacny-system  Podnikovy operacny system
   /riesenia/b2b-b2c-portal             Digitalny B2B a B2C portal
   /riesenia/digitalne-kanaly           Digitalne kanaly
   /riesenia/enterprise-ecommerce       Enterprise ecommerce platforma
   /riesenia/digitalne-produkty         Digitalne produkty a aplikacie
   /riesenia/ai-riesenia                AI riesenia
   /riesenia/digitalna-transformacna-strategia  Digitalna transformacna strategia
   /riesenia/cx-transformacia           Customer eXperience transformacia
   /riesenia/outsourcing-it             Outsourcing IT specialistov
/odvetvia                               Odvetvia (rozcestnik)
   /odvetvia/zdravotnictvo              Zdravotnictvo a HealthTech
   /odvetvia/banky                      Banky a Poistovnictvo
   /odvetvia/obchod                     Obchod a E-commerce
   /odvetvia/vyroba                     Vyroba a Priemysel
   /odvetvia/it                         IT a Technologie
   /odvetvia/energia                    Energia a Telco
   /odvetvia/verejny-sektor             Verejny Sektor
/expertiza/:slug                        Expertiza (technologicke kompetencie)
   ai-first · digitalna-automatizacia · digitalne-kanaly-portaly ·
   enterprise-architektura · vyvoj-aplikacii · cx-ux-dizajn ·
   devops-cloud · qa-testovanie
/case-studies                           Case studies (rozcestnik)
   /case-studies/odvetvie/:slug         filter podla odvetvia
   /case-studies/riesenie/:slug         filter podla riesenia
   /case-studies/travitor               hotova case study
   /case-studies/zuba                   hotova case study
/o-nas                                  O nas
   /o-nas/profil · /o-nas/kariera · /o-nas/preco-spolupracovat
/blog                                   Blog
/kontakt                                Kontakt
/sitemap                                Mapa stranky
```

### Hlavne menu (mega menu) — 4 sekcie
1. **Riesenia** — zoradene podla cielovej skupiny:
   - 01 Male a stredne firmy — digitalizacia procesov a predaja s AI
     (Podnikovy operacny system, Digitalny B2B a B2C portal, AI riesenia)
   - 02 Velke firmy a korporacie — enterprise ekosystemy a AI
     (Digitalne kanaly, Enterprise ecommerce, Digitalne produkty a aplikacie,
     AI riesenia, Digitalna transformacna strategia, CX transformacia)
   - 03 IT firmy a partneri — kapacity a expertiza
     (AI riesenia, Digitalna transformacna strategia, Outsourcing IT specialistov)
   - 04 Podla expertizy — technologicke kompetencie (8 expertiznych stranok)
2. **Produkty** — vlastne pomenovane platformy (brandy). Pozri poznamku nizsie.
3. **Odvetvia** — 7 odvetvi, kazde ma priradene odporucane riesenia.
4. **Case studies** — podla riesenia / podla odvetvia + vybrane hotove referencie.

> **Poznamka k brandom:** web ma v menu sekciu "Produkty" s vlastnymi nazvami
> platform (SynCore = Podnikovy operacny system, B2Base = Digitalny B2B a B2C
> portal, The Blueprint Strategy = Digitalna transformacna strategia). V tychto
> podkladoch brandy zamerne nepouzivame — drz sa popisnych nazvov. Brandy len
> aby si vedela, ze su to tie iste produkty, ak ich na webe uvidis.

---

## Mapovanie nazvov — produkty (SK / EN / web slug)

> Web a workspace pouzivaju **slovenske** nazvy. Intro deck a medzinarodny
> marketing pouzivaju **anglicke** nazvy. Su to tie iste produkty — paruj podla
> tabulky, nemiesaj varianty v ramci jedneho textu.

| # | SK nazov (web + workspace) | EN nazov (deck / intl) | Web URL (slug) |
|---|---|---|---|
| 1 | Podnikovy operacny system | Enterprise Operating System | /riesenia/podnikovy-operacny-system |
| 2 | Digitalny B2B a B2C portal | Digital B2B & B2C Portal | /riesenia/b2b-b2c-portal |
| 3 | Digitalne kanaly | Digital Channels | /riesenia/digitalne-kanaly |
| 4 | Enterprise ecommerce platforma | Enterprise Ecommerce Platform | /riesenia/enterprise-ecommerce |
| 5 | Digitalne produkty a aplikacie | Digital Products & Applications | /riesenia/digitalne-produkty |
| 6 | AI riesenia | AI Solutions | /riesenia/ai-riesenia |
| 7 | Digitalna transformacna strategia | Digital Transformation Strategy | /riesenia/digitalna-transformacna-strategia |
| 8 | Customer eXperience transformacia | Customer eXperience Transformation | /riesenia/cx-transformacia |
| 9 | Outsourcing IT specialistov | Outsourcing IT Specialists | /riesenia/outsourcing-it |

## Mapovanie nazvov — odvetvia (SK / EN / web slug)

| SK nazov (web + workspace) | EN nazov (deck / intl) | Web URL (slug) |
|---|---|---|
| Zdravotnictvo a HealthTech | Healthcare & Healthtech | /odvetvia/zdravotnictvo |
| Banky a Poistovnictvo | Banking & Insurance | /odvetvia/banky |
| Obchod a E-commerce | E-commerce & Retail | /odvetvia/obchod |
| Vyroba a Priemysel | Manufacturing & Industry | /odvetvia/vyroba |
| IT a Technologie | IT & Technology | /odvetvia/it |
| Energia a Telco | Energy & Telco | /odvetvia/energia |
| Verejny Sektor | Public Sector | /odvetvia/verejny-sektor |

---

## Formaty a dlzky (orientacne)
- **LinkedIn post:** 1 myslienka, 600-1300 znakov. Silny prvy riadok (hook),
  potom konkretika, na konci jemna vyzva. Bez hashtagovej spuste (3-5 staci).
- **Produktova stranka (/riesenia/...):** co to riesi -> komu -> co prinasa ->
  proof (cisla, referencie) -> CTA. Podklady v `02_produkty_podklady.md`.
- **Odvetvova stranka (/odvetvia/...):** painpointy odvetvia -> odporucane
  riesenia pre dane odvetvie -> referencie z odvetvia.
- **Expertizna stranka (/expertiza/...):** technologicka kompetencia, pre koho,
  ako ju pouzivame.
- **Case study (web):** pribeh klienta s cislami (kontext -> co sme spravili ->
  vysledok). Hotove vzory na webe: Travitor, Zuba. Fakty a cisla z `03_referencie.md`.
  Vizual a struktura sablony case study sa este pripravuju zvlast.
- **Kratky popis referencie:** max ~250 znakov, bez technologii (`03_referencie.md`).

## Vizualny styl
- Positioning = partner, nie dodavatel — vizual cisty, sebavedomy, biznisovy.
- Konkretny dizajn (logo, farby, fonty, komponenty) je vo Figme — vyziadaj si
  pristup / brand manual od marketingu. Tento balik je o obsahu, nie o grafickom
  manuali.

## Workflow s Claude Code (tip)
- Vlastne podklady (brief od klienta, poznamky, fotky, cisla) si daj do
  `inputs/` a v zadani na ne odkaz.
- Pytaj si viac variantov ("daj 3 verzie hooku") a vyber.
- Po sebe si vystup precitaj: sedi ton (partner, nie dodavatel)? su cisla
  z podkladov (`03_referencie.md`)? su nazvy produktov presne podla `02`
  a v spravnom jazyku (SK na web, EN na medzinarodny obsah)?
