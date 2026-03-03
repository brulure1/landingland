# landingland

Landing pages statiques déployées sur Vercel. Générées par IA via l'API Cursor Cloud Agents.

## Structure

```
├── .cursor/rules/          → Cursor Rules (lues auto par les Cloud Agents)
├── landings/
│   ├── free/               → Exemples par type (lecture seule)
│   │   ├── ecommerce/      → _type.css + exemple
│   │   ├── saas/
│   │   ├── event/
│   │   └── freestyle/
│   └── {bu}/               → BU client (1 par utilisateur/équipe)
├── shared/base.css          → CSS partagé
├── prompt-templates/        → Référence des prompts
└── vercel.json              → Rewrites URL plates
```

## URLs

Chaque landing a une URL plate : `https://domain/{slug}`
Le mapping est dans `vercel.json` (rewrites). Pas de BU/type visible dans l'URL.

## Types

| Type | Description |
|------|-------------|
| `ecommerce` | Vente produit : prix, avis, FAQ, urgence |
| `saas` | App/SaaS : features, pricing, démo |
| `event` | Événement : countdown, speakers, agenda |
| `freestyle` | Aucune contrainte CSS |

## Déploiement

Push sur `main` → Vercel déploie automatiquement.
