<div align="center">
# 🌋 OVPF — Piton de la Fournaise

**Dashboard interactif de surveillance sismique et volcanique (2013-2026)**

[![Live Demo](https://img.shields.io/badge/🌐_Live_Demo-gunout.github.io/Fournaise-ff6b00)](https://gunout.github.io/Fournaise/)
[![GitHub Pages](https://img.shields.io/badge/Hosted_on-GitHub_Pages-181717?logo=github)](https://pages.github.com/)
[![License](https://img.shields.io/badge/License-MIT-blue)](LICENSE)

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/docs/Web/JavaScript)
[![MapLibre](https://img.shields.io/badge/MapLibre_GL-4.7.1-396CB2)](https://maplibre.org/)
[![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?logo=chart.js&logoColor=white)](https://www.chartjs.org/)

[![Séismes](https://img.shields.io/badge/Séismes-3017-ff6b00)](#)
[![Webcams](https://img.shields.io/badge/Webcams-9-00ffff)](#)
[![Période](https://img.shields.io/badge/Période-2013--2026-00ff00)](#)

</div>

---

## 📖 À propos

**OVPF — Piton de la Fournaise** est un tableau de bord interactif qui visualise **3 017 séismes** enregistrés par l'Observatoire Volcanologique du Piton de la Fournaise (OVPF-IPGP) entre **mars 2013 et octobre 2026**.

L'application combine une **carte 3D interactive**, des **graphiques statistiques**, des **filtres dynamiques** et un accès aux **webcams en direct** du volcan.

> 🌋 Le Piton de la Fournaise est l'un des volcans les plus actifs au monde. Ce dashboard permet d'explorer plus d'une décennie de son activité sismique.

---

## ✨ Fonctionnalités

### 🗺️ Carte 3D interactive
- Rendu MapLibre GL avec terrain 3D AWS
- Clustering intelligent des 3 017 marqueurs
- Clic sur cluster → zoom automatique
- Clic sur point → popup détaillé
- Shift + glisser → sélection rectangle

### 📊 4 graphiques interactifs
- Événements par année (VT vs REG)
- Distribution des magnitudes
- Distribution des profondeurs
- Répartition VT / Régionaux
- Histogrammes cliquables → filtres appliqués

### 🎛️ Filtres avancés
- 📅 Plage temporelle (2013 → 2026)
- 📊 Magnitude (min / max)
- ⬇️ Profondeur (min / max)
- 🌋 Catégorie (VT / REG / Forts)
- Combinaison de tous les filtres

### 🎬 Visualisation dynamique
- 🔥 Heatmap de densité
- ▶️ Timeline animée (2013 → 2026)
- 🔝 Top 10 des séismes les plus forts
- 📥 Export CSV des événements filtrés
- ☀️ Mode clair / sombre

### 📹 9 webcams en direct
HUBERT DELISLE, PITON DE BERT, CASCADES, CRATERE FONTAINE, BORY, DOLOMIEU EST, BASALTE, PARC, ENCLOS.

Actualisation manuelle ou auto (5 min).

---

## 🛠️ Stack technique

- **Carte 3D** : MapLibre GL JS 4.7.1
- **Terrain 3D** : AWS Terrain Tiles
- **Fond de carte** : OpenStreetMap
- **Graphiques** : Chart.js
- **Hébergement** : GitHub Pages
- **Proxy CORS** : Cloudflare Workers
- **Données** : OVPF-IPGP / FDSN

---

## 🚀 Installation locale

### Cloner le dépôt

Ouvrez un terminal et tapez :

    git clone https://github.com/gunout/Fournaise.git
    cd Fournaise

### Lancer un serveur local

Tapez dans le terminal :

    python3 -m http.server 8000

Puis ouvrez : http://localhost:8000

---

## 📁 Structure du projet

    Fournaise/
    ├── index.html              # Dashboard complet
    ├── catalogue.json          # 3 017 séismes (OVPF)
    ├── worker.js               # Cloudflare Worker (proxy CORS)
    ├── README.md               # Ce fichier
    └── LICENSE                 # Licence MIT

---

## 🌐 Déploiement

### GitHub Pages

1. Poussez le dépôt sur GitHub
2. Settings → Pages
3. Source : `Deploy from a branch`
4. Branch : `main` + `/ (root)`
5. Save → en ligne sous 2 minutes

### Cloudflare Worker (webcams)

Le Worker `ipgp-cams.gunout.workers.dev` fait office de proxy CORS pour les webcams IPGP.

---

## 📊 Source des données

- **OVPF-IPGP** : https://www.ipgp.fr/observatoire-volcanologique-du-piton-de-la-fournaise/
- **FDSN Web Services** : http://ws.ipgp.fr/fdsnws/event/1
- **Webcams OVPF** : https://www.ipgp.fr/volcanoweb/reunion/
- **OpenStreetMap** : https://www.openstreetmap.org/

---

## 🎯 Utilisation

### Carte interactive

| Action | Résultat |
|--------|----------|
| Clic sur un point | Popup avec détails |
| Clic sur un cluster | Zoom automatique |
| Shift + glisser | Sélection rectangle |
| Molette | Zoom |
| Clic droit + glisser | Pivoter la vue 3D |

### Actions spéciales

| Bouton | Action |
|--------|--------|
| 🔥 Heatmap | Vue densité |
| ▶ Lire timeline | Animation 2013 → 2026 |
| 📥 Export CSV | Télécharge les événements |
| 🔄 Reset tout | Réinitialise les filtres |
| ☀️ Mode clair | Bascule le thème |

---

## 📈 Statistiques

| Métrique | Valeur |
|----------|--------|
| Total séismes | 3 017 |
| VT sommitaux | 1 933 |
| Régionaux | 1 084 |
| Magnitude max | 4.34 |
| Profondeur max | 56.47 km |
| Période | 24/03/2013 → 08/10/2026 |
| Webcams | 9 |

---

## 🤝 Contribution

1. Forkez le projet
2. Créez une branche
3. Committez vos changements
4. Poussez la branche
5. Ouvrez une Pull Request

---

## 📜 Licence

Ce projet est distribué sous licence **MIT**. Voir [LICENSE](LICENSE).

Les **données sismiques** proviennent de l'**OVPF-IPGP**. Les **webcams** restent la propriété de l'IPGP.

---

## 🙏 Remerciements

- 🌋 OVPF-IPGP pour les données et les webcams
- 🗺️ OpenStreetMap contributors
- 🎨 MapLibre et Chart.js
- ☁️ Cloudflare Workers

---
<div align="center">
## 🌋 Réalisé par Gleaphe — 2026


**⭐ Si ce projet vous plaît, n'hésitez pas à lui donner une étoile ! ⭐**
</div>

---
