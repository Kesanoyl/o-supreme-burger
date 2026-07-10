# O Suprême Burger — Site Click & Collect

## Résumé
Site de commande en ligne pour **O Suprême Burger** (Besançon, 25000). Fast-food — Burgers maison, menus deals (S1–S12), tex mex, desserts. 100% halal. Commande + paiement en ligne + compte client.

Dupliqué depuis le site **Bikers Food** (même moteur), avec carte, coordonnées et textes adaptés à O Suprême Burger. Le "Composer" de tacos est retiré (carte à base de menus fixes).

## Stack
- **Backend** : Node.js + Express (`server.js`), ES modules
- **Base de données** : PostgreSQL (Neon) via `DATABASE_URL`. Fallback `data.json` sans DB.
- **Paiement** : Stripe Checkout (clés **test** par défaut)
- **Frontend** : HTML/CSS/JS pur dans `public/` — mobile-first
- **Carte** : définie en dur dans `public/app.js` (const `MENU`), 6 catégories / ~55 produits. Images produits réutilisées de Bikers Food dans `public/img/menu/`.

## Design tokens (palette héritée de Bikers Food)
- `--rojo: #A83A4C` (bordeaux/vin) — accent principal
- `--fuego: #C56A3A` (brique) — accent secondaire
- `--oro: #D8BE8A` (crème/doré) — premium
- `--bg: #141210` (charbon profond) — fond
- Polices : Playfair Display (headings) + Inter (body) + Bebas Neue (logo)

## Coordonnées (site vitrine)
- Adresse : 24 rue d'Arènes, 25000 Besançon
- Téléphone : 03 81 58 18 89
- Horaires : Lun–Jeu 11h30–14h00 & 18h00–23h00 · Ven–Sam 18h00–00h00 · Dim 18h00–22h00

## Lancer en local
```bash
npm install
npm start        # http://localhost:3000
npm run dev      # avec --watch
```

## Variables d'environnement (.env)
```
STRIPE_SECRET_KEY=sk_test_...
STRIPE_WEBHOOK_SECRET=whsec_...
DATABASE_URL=postgresql://...   # optionnel, fallback data.json
PUBLIC_URL=http://localhost:3000
PORT=3000
```
