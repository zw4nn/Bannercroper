# Redacted BannerLab

**Version 1.0.16 · build 11600**

Redacted BannerLab est un outil mobile-first non officiel pour préparer, organiser, jouer et publier des fresques de missions **Ingress Prime**.

Le Lab regroupe dans une seule application la création de bannière, la préparation des missions, le travail avec IITC, la publication vers Mission Authoring Tool et le suivi d'une fresque en jeu.

> Projet communautaire indépendant. Redacted BannerLab n'est ni développé, ni approuvé, ni affilié à Niantic.

---

## 🧪 Les assistants du Lab

### IGOR 0.6.10

**IITC Gateway for Operations & Routing**

IGOR accompagne la préparation du parcours dans IITC :

- récupération des portails ;
- construction mission par mission ;
- actions et passphrases ;
- reprise du dernier portail entre deux missions ;
- statistiques et estimation piétonne via OpenStreetMap / Valhalla ;
- sauvegarde locale de la progression ;
- synchronisation manuelle authentifiée avec Redacted BannerLab.

### MILO 0.5.1

**Mission Import & Launch Operator**

MILO accompagne la publication dans **Mission Authoring Tool** :

- installation guidée dans Chrome Android ;
- assistant pas à pas avec de vraies captures Chrome ;
- chargement d'une bannière préparée par le Lab ;
- préparation des missions, portails, actions, passphrases et images ;
- reprise de la session de publication ;
- gestion claire des fichiers et de la mémoire locale.

Les fichiers actuels sont :

- `MILO.user.js`
- `MILO_CurrentBanner.json`
- `MILO_Launch.txt`

La compatibilité avec les anciens fichiers Publisher est conservée pendant la migration.

**MILO prépare. L'Agent reste toujours seul à valider `Submit`.**

---

## 🎨 Création de fresques

- import d'une image de fond ;
- découpage en missions ;
- éditeur multi-calques ;
- textes et images superposables ;
- calques globaux ou liés à certaines missions ;
- cadrage individuel des cases ;
- historique Annuler / Rétablir ;
- aperçu et Studio plein écran ;
- export du projet et sauvegarde complète ;
- reprise automatique du travail local.

---

## 🗺️ Missions et parcours

- Mission Planner mobile ;
- portails et coordonnées ;
- actions Hack, Mod, Capture/Upgrade, Link, Field et Passphrase ;
- minimum de portails contrôlé avant publication ;
- titres et descriptions par mission ;
- description commune de bannière ;
- reprise facultative du dernier portail d'une mission ;
- recherche Bannergress par nom, ville, auteur ou proximité ;
- favoris et reprise d'une fresque en cours.

### Distances piétonnes

Le Lab utilise **OpenStreetMap / Valhalla** pour estimer les trajets à pied entre les portails.

La valeur « Valhalla brut » correspond à la réponse directe du moteur de routage. Le Lab contrôle ensuite les tronçons manifestement aberrants afin de produire une estimation piétonne plus exploitable.

---

## 🎮 Jouer une fresque

L'overlay Android permet de suivre une fresque sans perdre le fil :

- vraie tête de Redacted ;
- panneau compact ;
- navigation `<` / `>` ;
- ouverture de la mission courante ;
- bouton **Mission terminée** ;
- réduction en bulle ;
- déplacement et fermeture de l'overlay ;
- progression conservée localement.

À la fin d'une fresque, le Lab déclenche une célébration renforcée avec feux d'artifice et messages de **Redacted, IGOR et MILO**.

L'overlay ne contrôle pas l'interface Ingress et n'effectue aucune action dans le jeu à la place de l'Agent.

---

## 🌍 Langues

Redacted BannerLab prend en charge 20 langues avec détection automatique au premier lancement et sélection manuelle dans les réglages.

Les chaînes encore non traduites utilisent l'anglais comme langue de secours. L'arabe active l'affichage RTL.

---

## 🔄 Mises à jour Android

Le Lab intègre son propre mécanisme de mise à jour :

1. détection d'une version plus récente ;
2. téléchargement volontaire de l'APK ;
3. vérification SHA-256, package, signature et `versionCode` ;
4. installation uniquement après action explicite de l'utilisateur et confirmation Android.

La même clé de signature Android est conservée entre les versions officielles afin de permettre les mises à jour sans désinstallation.

---

## 🔐 Confidentialité et sécurité

Redacted BannerLab est conçu sans compte RBL, publicité ni télémétrie cachée.

Les projets et images restent localement sur l'appareil sauf action volontaire d'export, de partage ou de publication.

Certaines fonctions communiquent volontairement avec des services externes lorsqu'elles sont utilisées :

- GitHub pour les mises à jour ;
- Bannergress pour la recherche de bannières ;
- OpenStreetMap / Valhalla pour le routage ;
- Mission Authoring Tool pour la publication ;
- Telegram pour le support et les informations communautaires.

Le pont Redacted BannerLab ↔ IGOR est authentifié par un jeton local aléatoire. MILO est vérifié par SHA-256 avant son utilisation.

Les clés de signature Android et les secrets de build ne sont jamais stockés dans le dépôt source.

---

## 🛠️ Développement

### Prérequis

- Node.js 22
- Java 21
- Android SDK / build-tools

### Build web

```bash
npm install
npm run build
```

### Synchronisation Android

```bash
npx cap add android
npx cap sync android
```

Le build officiel Android est ensuite généré et signé par GitHub Actions avec les secrets de signature conservés hors du dépôt.

### Versions embarquées

- Redacted BannerLab : **1.0.16**
- Android `versionCode` : **11600**
- IGOR : **0.6.10**
- MILO : **0.5.1**
- Capacitor : **8.5.1**
- Vite : **7.3.6**
- Leaflet : **1.9.4**

---

## 📦 v1.0.16

Cette version finalise notamment :

- l'intégration officielle de MILO ;
- le tutoriel Chrome guidé ;
- les nouveaux fichiers MILO ;
- l'affichage des versions IGOR et MILO dans les réglages ;
- le nouvel overlay Redacted plus compact ;
- la navigation plus claire ;
- la célébration de fin de fresque renforcée.

Les notes détaillées de version sont disponibles dans `CHANGELOG_v1.0.16.md`.

---

© 2026 Zw4nn · Redacted BannerLab

Fait pour la communauté Ingress. Pensé d'abord côté Enlightened, mais ouvert à tous les Agents. 💚💙
