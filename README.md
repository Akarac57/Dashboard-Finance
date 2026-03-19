[README.md](https://github.com/user-attachments/files/26127003/README.md)
# 🌊 MonHub — Dashboard Personnel

> Dashboard personnel en temps réel, hébergé sur GitHub Pages. Aucun serveur, aucune installation — un seul fichier HTML.

![Dashboard MonHub](https://img.shields.io/badge/status-live-14b8a6?style=flat-square) ![HTML](https://img.shields.io/badge/HTML-single--file-0ea5e9?style=flat-square) ![License](https://img.shields.io/badge/license-MIT-6366f1?style=flat-square)

---

## ✨ Fonctionnalités

### 🌤 Météo
- Température, conditions, ressentis, vent, humidité, pression, visibilité
- **Sélecteur de ville** parmi 19 villes françaises et européennes
- Prévisions sur 6 jours avec probabilité de pluie
- **Vigilance MétéoFrance** en temps réel pour la région Grand-Est (vert / jaune / orange / rouge), mise à jour toutes les 6h
- 🌅 Lever et coucher du soleil (données réelles selon la ville)
- 🌕 Phase de la lune calculée avec icône et nom en français

### 📈 Bourse
- Liste d'actions entièrement personnalisable (AAPL, BNP.PA, ^FCHI…)
- Ajout / suppression à la volée
- Prix et variation en % depuis la clôture précédente
- Mise à jour automatique toutes les 10 minutes
- Sauvegarde de la liste entre les sessions

### 🪙 Crypto
- Liste de cryptomonnaies personnalisable (BTC, ETH, SOL, XRP…)
- Variation 24h en temps réel via CoinGecko
- Ajout par symbole ou nom complet

### 📊 Indices mondiaux
- Liste entièrement personnalisable avec **autocomplete**
- Catalogue de 17 indices (S&P 500, CAC 40, DAX, Nikkei, Hang Seng, VIX…)
- Ajout de n'importe quel indice Yahoo Finance

### 🛢 Matières premières & Forex
- Liste personnalisable avec **autocomplete** par catégorie
- **Matières** : Or, Argent, Pétrole WTI/Brent, Gaz, Blé, Maïs, Café, Cacao, Cuivre, Platine…
- **Forex** : EUR/USD, GBP/USD, USD/JPY, USD/CHF, AUD/USD, CNY, BRL, INR…

### 📰 Actualités
- Filtres par catégorie : Économie, Tech, Monde, Sport, Politique
- Affichage en grille 3 colonnes

### 🔮 Polymarket
- Recherche de marchés de prédiction en temps réel
- Épinglage de marchés favoris avec barres de probabilité (Oui / Non / Multi-outcomes)
- Rafraîchissement automatique des probabilités épinglées
- Sauvegarde des marchés épinglés

### ⚠️ Alertes personnalisées
- Ajout libre de notes d'alerte (ex : "BTC > 90 000", "TSLA < 250")
- Indicateurs colorés
- Sauvegarde persistante

### 🎛 Interface
- **Redimensionnement de chaque widget** à la souris (poignée en bas à droite)
- Taille des widgets sauvegardée entre les sessions
- Double-clic sur la poignée pour réinitialiser la taille
- Design **Ocean Slate** sombre et coloré
- Animations fluides au chargement

---

## 🔌 APIs utilisées

| Service | Usage | Clé requise |
|---|---|---|
| [Open-Meteo](https://open-meteo.com) | Météo & prévisions | ❌ Gratuit |
| [OpenDataSoft / MétéoFrance](https://public.opendatasoft.com) | Vigilance météo | ❌ Gratuit |
| [Yahoo Finance](https://finance.yahoo.com) | Bourse, indices, forex, matières | ❌ (via proxy) |
| [CoinGecko](https://coingecko.com) | Cryptomonnaies | ❌ Gratuit |
| [Polymarket Gamma API](https://gamma-api.polymarket.com) | Marchés de prédiction | ❌ Gratuit |

> Toutes les APIs sont publiques et gratuites. Aucune clé API n'est nécessaire.

---

## 🚀 Déploiement sur GitHub Pages

1. Fork ce dépôt ou crée-en un nouveau
2. Upload `index.html` à la racine
3. Va dans **Settings → Pages**
4. Source : **Deploy from a branch** → `main` / `/ (root)`
5. Ton dashboard est disponible sur `https://[pseudo].github.io/[repo]/`

---

## 💾 Données locales

Toutes les préférences sont sauvegardées dans le `localStorage` du navigateur :

| Clé | Contenu |
|---|---|
| `mh4Stocks` | Liste des actions suivies |
| `mh4Cryptos` | Liste des cryptos suivies |
| `mh4Idx` | Liste des indices suivis |
| `mh4Raw` | Liste des matières/forex suivies |
| `mh4Alerts` | Alertes personnalisées |
| `mh4Poly` | Marchés Polymarket épinglés |
| `mh4Sizes` | Tailles des widgets |

---

## 🛠 Personnalisation

Le dashboard est un fichier HTML autonome. Pour modifier :

- **Ville par défaut** : changer la valeur initiale dans `S.city` dans le JS
- **Symboles par défaut** : modifier les tableaux `DEFAULT_IDX`, `DEFAULT_RAW` et les valeurs initiales de `S.stocks`, `S.cryptos`
- **Couleurs** : modifier les variables CSS dans `:root` en haut du fichier
- **Nouvelles villes** : ajouter une entrée dans le tableau `CITIES` avec `name`, `lat`, `lon`
- **Nouveaux instruments** : ajouter une entrée dans `CATALOGUE` avec le symbole Yahoo Finance

---

## 📁 Structure

```
monhub/
├── index.html     # Le dashboard complet (fichier unique)
└── README.md      # Ce fichier
```

---

## 📄 Licence

MIT — libre d'utilisation, modification et distribution.
