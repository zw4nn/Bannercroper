# Changelog — Redacted BannerLab

Ce fichier suit les versions stables publiques de Redacted BannerLab. Les builds TEST internes ne sont volontairement pas détaillés.

## 1.1.0

Évolution majeure du Lab depuis la version stable 1.0.18 et première version de la branche 1.1.x.

### Le Lab
- Refonte de l'organisation autour du système d'ascenseur et des différents étages.
- Navigation, transitions et retours Android améliorés.
- Tutoriels adaptés à l'organisation par étages.
- Nombreuses améliorations d'interface et d'utilisation mobile.

### IGOR — IITC Gateway for Operations & Routing
- Panneau central IGOR amélioré.
- Réduction et minimisation du panneau.
- Retour cohérent vers IGOR depuis ses différents modules.
- Activation et mise en veille des modules améliorées.
- Synchronisations Android/IITC renforcées.
- Amélioration des Missions, Clés, Inventaire et Captures uniques.
- Correctifs de recherche, d'export et de persistance locale.

### LEON — Level Expert and Operation Navigator
- Nouvel espace LEON consacré aux calculs et aux timers.
- Calcul AP exact.
- AP Pile / Tout Pile.
- Timers personnalisés.
- Timer Drone avec sélection ENL / RES.
- Timers de hack et de portail.
- Gestion des Heat Sinks et Multi-Hacks avec leur rareté.
- Calcul du cooldown applicable.
- Calcul du nombre de hacks avant burnout.
- Vérification des événements Ingress susceptibles de modifier temporairement :
  - le cooldown Drone ;
  - le cooldown de hack ;
  - le nombre de hacks avant burnout.
- Overlays Timers Android avec déplacement, réduction/agrandissement, persistance et notifications de fin.
- Possibilité de choisir le comportement d'affichage des timers selon le contexte.

### MILO — Mission Interface and Logistics Operator
- Consolidation du Publisher et de ses échanges.
- Amélioration de la gestion du stockage Android.
- Sélection et mémorisation des emplacements utiles.
- Contrôles d'intégrité renforcés entre les composants concernés.

### RITA — Redacted Information & Telegram Assistant
- Intégration renforcée de RITA pour les informations et annonces du Lab.
- Vérification des nouvelles versions stables au lancement lorsque l'option est activée.
- Popup RITA lorsqu'une mise à jour est disponible.
- Présentation des informations de version avant installation.
- Vérification SHA-256 de l'APK téléchargé.
- Vérification du package Android, de la signature et du `versionCode`.
- Conservation de la confirmation finale d'installation par Android.

### Ingress Prime
- Cadre néon passif optionnel conservé.
- Vert ENL ou bleu RES.
- Cadre entièrement traversant afin de ne pas bloquer Prime.
- Retrait de la PROD des expérimentations de HUD interactif, capteurs, personnages et éléments naviguants.
- Les overlays Timers de LEON restent disponibles indépendamment de ce retrait.

### Internationalisation
- Mise à jour et harmonisation des traductions des principales zones du Lab.
- Anglais utilisé comme fallback lorsqu'une traduction manque.
- Support RTL conservé pour l'arabe.
- Formats de date adaptés à la locale lorsque disponibles.

### Saisonnier
- Système saisonnier conservé.
- Les réglages concernés ne deviennent visibles que pendant leur période prévue.
- Les contenus surprises ne sont volontairement pas détaillés dans le changelog public.

### Technique et sécurité
- Passage à la série 1.1.x.
- Package PROD conservé : `com.bannerforge.mobile`.
- Conservation de la clé de signature Android stable.
- Renforcement des échanges entre l'application et ses composants.
- Amélioration de la persistance locale et des deep links.
- Secrets et clés de signature maintenus hors du dépôt.
- Workflow GitHub Actions PROD consolidé.
- Nettoyage des ressources et fichiers historiques inutiles dans l'archive de production.

## 1.0.18

Dernière version stable de référence avant la refonte 1.1.0.

Pour l'historique antérieur, consulter les Releases GitHub correspondantes.
