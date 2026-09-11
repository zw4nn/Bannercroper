# Redacted BannerLab

**Redacted BannerLab** est une application Android pensée pour accompagner les agents Ingress dans la préparation et le suivi de leurs opérations, bannières et outils de terrain.

> Version stable actuelle : **1.1.0**

## Le Lab

L'application est organisée comme un laboratoire à plusieurs étages. Chaque espace regroupe une famille d'outils afin d'éviter de transformer l'écran d'accueil en tableau de bord d'avion.

### IGOR — IITC Gateway for Operations & Routing

IGOR assure le lien avec IITC et les outils de préparation :

- gestion et synchronisation des missions ;
- suivi des clés et de l'inventaire lorsque les données sont disponibles ;
- captures uniques ;
- outils de parcours et de préparation ;
- modules activables ou mis en veille ;
- panneau compact/minimisable ;
- retour permanent vers le panneau principal IGOR.

IGOR fonctionne avec des données explicitement fournies ou synchronisées par l'utilisateur. Redacted BannerLab n'a pas vocation à scraper silencieusement la carte Ingress.

### LEON

LEON s'occupe des calculs et du temps :

- calcul AP exact ;
- calculs AP Pile / Tout Pile ;
- timers personnalisés ;
- timer Drone avec apparence ENL ou RES ;
- timers de hack/portail ;
- prise en compte des Heat Sinks et Multi-Hacks et de leur rareté ;
- calcul du cooldown et du nombre de hacks avant burnout ;
- vérification des événements Ingress susceptibles de modifier temporairement ces règles ;
- timers flottants Android déplaçables, réductibles et persistants ;
- notifications de fin.

### MILO

MILO regroupe les fonctions de publication et les échanges associés au Publisher, avec vérification d'intégrité et gestion du stockage Android.

### RITA — Robot d’Investigation, de Transmission et d’Analyse

RITA accompagne l'application et intervient notamment pour les informations système et les mises à jour.

Au lancement, Redacted BannerLab peut vérifier si une nouvelle version stable est disponible. Lorsqu'une mise à jour est détectée, RITA présente les informations de version avant téléchargement et installation.

## Intégration avec Ingress Prime

La version stable reste volontairement prudente.

Elle propose uniquement un **cadre néon passif** optionnel autour de Prime :

- vert pour ENL ;
- bleu pour RES ;
- entièrement traversant afin de ne pas bloquer les interactions avec le jeu.

Les expérimentations de HUD interactif, capteurs et éléments naviguants ne font pas partie de la version stable 1.1.0.

Les timers flottants de LEON sont indépendants de ce HUD expérimental et restent disponibles.

## Langues

Redacted BannerLab dispose d'une interface multilingue. Les principales zones du Lab sont traduites et l'anglais sert de langue de repli lorsqu'une chaîne n'est pas encore disponible dans la langue choisie.

L'arabe bénéficie d'une prise en charge RTL.

## Éléments saisonniers

Certains éléments du Lab sont saisonniers et peuvent n'apparaître que pendant la période concernée. Ils ne sont volontairement pas documentés ici en détail.

## Mise à jour Android

Les mises à jour stables conservent :

- le package Android de production `com.bannerforge.mobile` ;
- la même clé de signature Android ;
- une vérification de l'intégrité SHA-256 ;
- une vérification du package, de la signature et du `versionCode` avant installation.

La confirmation finale d'installation reste gérée par Android.

## Compilation

Le dépôt contient le workflow GitHub Actions de production :

`.github/workflows/build-redacted-bannerlab-prod.yml`

Le workflow :

1. extrait `Redacted_BannerLab_Source.zip` ;
2. installe les dépendances ;
3. compile l'application web ;
4. génère le projet Android Capacitor ;
5. applique les ressources et patches Android ;
6. compile l'APK Release ;
7. signe l'APK avec la clé de production fournie exclusivement par GitHub Actions Secrets ;
8. vérifie la signature finale ;
9. génère le SHA-256 et les métadonnées de mise à jour ;
10. peut publier la GitHub Release.

Aucun keystore ni mot de passe de signature ne doit être ajouté au dépôt.

## Sécurité et confidentialité

Le projet est conçu pour rester auditable :

- aucune clé de signature dans les sources ;
- pas de collecte cachée destinée au suivi des utilisateurs ;
- pas de scraping silencieux de la carte Ingress ;
- contrôles d'intégrité lors des mises à jour ;
- trafic HTTP non chiffré interdit dans la configuration Android de production.

## Avertissement

Redacted BannerLab est un projet indépendant destiné à la communauté.

Il n'est ni développé, ni approuvé, ni sponsorisé par Niantic ou Scopely. **Ingress** et les éléments associés restent la propriété de leurs détenteurs respectifs.

Les licences et mentions des composants tiers utilisés par le projet sont détaillées dans `THIRD_PARTY_NOTICES.md`.
