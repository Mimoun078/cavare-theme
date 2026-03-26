# Cavarè Clothing — Shopify Website Project

## Project
Premium menswear webshop voor **Cavarè Clothing**.

- **Store:** ywyp1c-k2.myshopify.com
- **GitHub:** https://github.com/Mimoun078/Test (wordt hernoemd naar cavare-theme)
- **Domein:** www.cavareclothing.nl
- **Platform:** Shopify (Dawn thema als basis, aangepast met Cavarè stijl)

---

## Hoe aanpassingen doorsturen werken

```
Ik pas bestanden aan → git push naar GitHub → Shopify update automatisch
```

### Handige commando's
```bash
shopify theme dev --store ywyp1c-k2.myshopify.com   # Live preview op je computer
shopify theme push --unpublished                      # Naar Shopify sturen (nog niet live)
shopify theme push --theme <id>                       # Naar specifiek thema sturen
shopify theme list                                    # Bekijk alle thema's in je winkel
```

> Vereist: Node.js 18+ en Shopify CLI (al geïnstalleerd)

---

## Merkidentiteit

| Wat | Waarde |
|-----|--------|
| Primaire kleur | Cavarè Brown `#2A1B0F` |
| Donkere kleur | Deep Charcoal `#231F20` |
| Achtergrond | Soft Cream `#FEFEFE` |
| Heading font | Cinzel (serif) |
| Body font | Inter (sans-serif) |
| Logo | CAVARÈ wordmark (spaced caps) + CV monogram |

**Stijl:** Minimalistisch, luxe, veel witruimte, subtiele animaties

---

## Thema structuur

Dawn levert de basis (cart, checkout, Liquid logica). Wij passen alleen de visuele laag aan via bestanden die beginnen met `cavare-`.

| Bestand | Wat het doet |
|---------|-------------|
| `assets/cavare.css` | Alle Cavarè stijl (kleuren, fonts, layout) |
| `layout/theme.liquid` | Hoofd HTML, navigatie, cart drawer |
| `sections/header.liquid` | Navigatiebalk bovenaan |
| `sections/footer.liquid` | Footer onderaan |
| `sections/hero-banner.liquid` | Grote foto sectie op homepage |
| `sections/featured-collection.liquid` | Productgrid op homepage |
| `sections/brand-story.liquid` | Merkverhaal sectie |
| `sections/main-product.liquid` | Productpagina |
| `sections/main-collection.liquid` | Shop / collectie pagina |

---

## Pagina's

- **Homepage** — Hero + uitgelichte producten + merkverhaal
- **Shop** — Productgrid met filter
- **Productpagina** — Foto's, maten, add to cart, maattabel
- **Over ons** — Merkverhaal, visie
- **Contact** — Formulier + Instagram
- **Cart / Checkout** — Shopify standaard, Cavarè stijl

---

## Talen
- Hoofdtaal: Nederlands
- Tweede taal: Engels
- Taalswitch zichtbaar in navigatie (NL / EN)

---

## Producten (fase 1)
- T-shirts (beschikbaar)
- Hoodies, broeken, accessoires (later)

## Betaalmethoden
- iDEAL, creditcard, PayPal

---

## Nog te doen
- [ ] GitHub repo hernoemen naar `cavare-theme`
- [ ] Logo bestanden toevoegen (PNG/SVG)
- [ ] Productfoto's toevoegen
- [ ] Shopify GitHub koppeling activeren
- [ ] Producten aanmaken in Shopify admin
- [ ] Betaalmethoden instellen
- [ ] Domein koppelen (cavareclothing.nl)
