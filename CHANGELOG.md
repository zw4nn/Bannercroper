# Changelog — Redacted BannerLab

Ce fichier suit les versions stables publiques de Redacted BannerLab. Les builds expérimentaux internes ne sont volontairement pas détaillés ici.

---

## 1.1.0

Première version de la branche **1.1.x** et évolution majeure du Lab depuis la 1.0.18.

### Le Lab

- Refonte de l'organisation générale autour d'un véritable système d'ascenseur et d'étages.
- Navigation entre les espaces du Lab revue.
- Amélioration des retours Android et des transitions entre les différentes zones.
- Tutoriels adaptés à l'organisation par étages.
- Nombreuses corrections d'interface et améliorations mobiles.

### LEON

- Ajout et consolidation de l'espace LEON.
- Calcul AP exact.
- Outils AP Pile / Tout Pile.
- Nouvelle salle Timers.
- Timers personnalisés.
- Timer Drone avec sélection ENL / RES.
- Timers hack/portail.
- Sélection des Heat Sinks et Multi-Hacks et de leur rareté.
- Calcul du cooldown applicable.
- Calcul du nombre de hacks disponibles avant burnout.
- Vérification des événements Ingress susceptibles de modifier temporairement :
  - le cooldown Drone ;
  - le cooldown de hack ;
  - le nombre de hacks avant burnout.
- Overlays Timers Android conservés :
  - déplacement ;
  - réduction/agrandissement ;
  - persistance ;
  - notifications de fin ;
  - affichage permanent ou limité à Ingress Prime selon le réglage.

### IGOR

- IGOR devient le panneau central des outils IITC du Lab.
- Panneau réductible/minimisable.
- Retour cohérent vers IGOR depuis ses différents modules.
- Activation et mise en veille des modules améliorées.
- Synchronisations Android/IITC renforcées.
- Améliorations de la gestion des missions.
- Améliorations des Clés et de l'Inventaire.
- Améliorations des Captures uniques.
- Correctifs de recherche, d'export et de persistance locale.

### MILO

- Consolidation du Publisher.
- Amélioration de la gestion du stockage Android.
- Vérifications d'intégrité renforcées entre les différents composants de publication.

### RITA et mises à jour

- Vérification des nouvelles versions stables au lancement lorsque l'option est activée.
- RITA présente une fenêtre dédiée lorsqu'une mise à jour est disponible.
- Affichage des informations de version avant installation.
- Vérification SHA-256 de l'APK téléchargé.
- Vérification du package Android, de la signature et du `versionCode`.
- Conservation de la confirmation d'installation Android.

### Ingress Prime

- Conservation d'un cadre néon passif optionnel autour de Prime.
- Choix ENL vert ou RES bleu.
- Le cadre reste traversant et ne bloque pas les interactions.
- Retrait de la PROD des expérimentations de HUD interactif, capteurs et éléments naviguants.
- Les overlays Timers de LEON restent disponibles indépendamment de ce retrait.

### Internationalisation

- Mise à jour et harmonisation des traductions des principales zones du Lab.
- Anglais utilisé comme fallback lorsqu'une traduction manque.
- Conservation du support RTL pour l'arabe.
- Formats de dates adaptés à la locale lorsque disponibles.

### Saisonnier

- Le système saisonnier reste intégré.
- Les options concernées ne deviennent visibles que pendant leur période prévue.
- Les contenus surprises ne sont volontairement pas détaillés dans le changelog public.

### Technique et sécurité

- Passage à la série 1.1.x.
- Package de production conservé : `com.bannerforge.mobile`.
- Conservation de la clé de signature Android stable.
- Renforcement du bridge entre l'application et ses composants.
- Amélioration de la persistance locale et des deep links.
- Clés et secrets de signature maintenus hors du dépôt.
- Workflow GitHub Actions PROD consolidé.
- Nettoyage des ressources et fichiers historiques inutiles dans l'archive de production.

---

## 1.0.18

Dernière version stable de référence avant la refonte 1.1.0.

Pour l'historique détaillé des développements antérieurs, consulter les Releases GitHub correspondantes.
