# Cavarè Clothing — Shopify Website Project

## Project
Premium menswear webshop voor **Cavarè Clothing**.

- **Store:** ywyp1c-k2.myshopify.com
- **GitHub:** https://github.com/Mimoun078/cavare-theme
- **Domein:** www.cavareclothing.nl
- **Platform:** Shopify — eigen thema op basis van Dawn

---

## Hoe aanpassingen werken

```
Ik pas bestanden aan → git push naar GitHub → Shopify pikt het automatisch op
```

### Commando's (ik doe dit, niet de gebruiker)
```bash
git add <bestanden>
git commit -m "Omschrijving"
git push
```

### Shopify CLI (alleen voor noodgevallen)
```bash
shopify auth login
shopify theme push --store ywyp1c-k2.myshopify.com --unpublished --path .
shopify theme list
```

---

## Merkidentiteit

| Wat | Waarde |
|-----|--------|
| Primaire kleur | Cavarè Brown `#2A1B0F` |
| Donkere kleur | Deep Charcoal `#231F20` |
| Achtergrond | Soft Cream `#FEFEFE` |
| Licht beige | `#F5F0EB` |
| Tekst licht | `#7A6E65` |
| Heading font | Cinzel (serif) — via Google Fonts |
| Body font | Inter (sans-serif) — via Google Fonts |
| Logo | CAVARÈ wordmark (spaced caps) |

**Stijl:** Minimalistisch, luxe, veel witruimte, subtiele hover animaties, 0px border-radius op knoppen

---

## Thema structuur

Alle CSS staat inline in de sections (via `<style>` tags) zodat er geen conflicten zijn met Dawn's eigen CSS. Dawn's core JS en checkout blijven intact.

| Bestand | Wat het doet |
|---------|-------------|
| `layout/theme.liquid` | Dawn's origineel + cavare.css link + Google Fonts |
| `assets/cavare.css` | Globale Cavarè stijl (fallback / gedeelde stijlen) |
| `sections/header.liquid` | Navigatie — CAVARÈ logo, menu, cart icoon |
| `sections/footer.liquid` | Footer — links, social, copyright |
| `sections/hero-banner.liquid` | Homepage hero met foto + tekst overlay |
| `sections/featured-collection.liquid` | Productgrid — toont echte producten of placeholder foto's |
| `sections/brand-story.liquid` | Split sectie — foto links, tekst rechts op donker |
| `sections/main-product.liquid` | Productpagina |
| `sections/main-collection.liquid` | Shop/collectie pagina |
| `sections/main-cart.liquid` | Winkelwagen pagina |
| `sections/page-about.liquid` | Over ons pagina |
| `sections/page-contact.liquid` | Contact pagina |

---

## Foto's in assets

| Bestandsnaam | Gebruik |
|-------------|---------|
| `cavare-model.jpeg` | Hero banner (homepage) |
| `cavare-tshirts.jpeg` | Product kaart 1 |
| `cavare-tshirt-red.jpeg` | Product kaart 2 |
| `cavare-jas-brown.jpeg` | Product kaart 3 + merkverhaal |
| `cavare-bodywarmer.jpeg` | Product kaart 4 |
| `cavare-broek.jpeg` | Beschikbaar voor shop pagina |
| `cavare-product.jpeg` | Beschikbaar voor extra gebruik |
| `cavare-logo.png` | Logo (bruin achtergrond versie) |

---

## Pagina's en templates

| Pagina | Template bestand | Section |
|--------|-----------------|---------|
| Homepage | `templates/index.json` | hero-banner, featured-collection, brand-story |
| Shop | `templates/collection.json` | main-collection |
| Product | `templates/product.json` | main-product |
| Winkelwagen | `templates/cart.json` | main-cart |
| Over ons | `templates/page.about.json` | page-about |
| Contact | `templates/page.contact.json` | page-contact |

---

## Aanpak regels (BELANGRIJK)

1. **Alle styling inline in sections** via `<style>` tags — geen externe CSS klassen gebruiken
2. **Nooit Dawn's core bestanden aanpassen** behalve `layout/theme.liquid`
3. **Altijd eigen prefix** gebruiken: `.cavare-` voor CSS klassen
4. **Altijd alles in één commit** — niet stap voor stap pushen
5. **Foto's gaan in `/assets/`** — gebruik `{{ 'bestandsnaam' | asset_url }}` in Liquid
6. **Taal:** Nederlands in de UI, code in het Engels

---

## Wat de gebruiker nog zelf moet doen in Shopify

- [ ] Logo uploaden: Shopify editor → Header → Logo → Select
- [ ] Producten aanmaken: Shopify Admin → Products → Add product
- [ ] Collectie aanmaken en koppelen aan "Uitgelichte Collectie" sectie
- [ ] iDEAL / PayPal instellen: Shopify Admin → Settings → Payments
- [ ] Domein koppelen: cavareclothing.nl → Shopify Admin → Settings → Domains
- [ ] Thema publiceren: Shopify Admin → Online Store → Themes → Publish

---

## Nog te bouwen (volgende sessies)

- [ ] Footer verbeteren (Instagram link, betaalmethode icoontjes)
- [ ] Productpagina testen met echte producten
- [ ] Over ons pagina met model foto
- [ ] Contact pagina
- [ ] Announcement bar (bijv. "Gratis verzending boven €75")
- [ ] Mobiel testen en finetunen
- [ ] NL/EN taalswitch activeren via Shopify Markets
