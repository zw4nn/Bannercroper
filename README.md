# Redacted BannerLab

**Redacted BannerLab** est une application Android conçue pour accompagner les agents Ingress dans la préparation, l'organisation et le suivi de leurs opérations et missions.

**Version stable actuelle : 1.1.0**

## Le Lab

Redacted BannerLab est organisé comme un laboratoire à plusieurs étages. L'ascenseur permet d'accéder aux différents assistants et à leurs outils.

### IGOR — IITC Gateway for Operations & Routing

IGOR est l'assistant IITC du Lab.

Il regroupe notamment :
- la gestion et la synchronisation des missions ;
- les outils liés aux clés et à l'inventaire lorsque les données sont disponibles ;
- les captures uniques ;
- les outils de parcours et de préparation ;
- les modules activables ou mis en veille ;
- un panneau compact et minimisable ;
- une navigation cohérente entre ses différents modules.

IGOR travaille avec les données explicitement fournies ou synchronisées par l'utilisateur. Redacted BannerLab n'a pas vocation à scraper silencieusement la carte Ingress.

### LEON — Level Expert and Operation Navigator

LEON s'occupe des calculs et du temps.

Son étage regroupe notamment :
- le calcul AP exact ;
- les outils AP Pile / Tout Pile ;
- les timers personnalisés ;
- le timer Drone avec sélection ENL ou RES ;
- les timers de hack et de portail ;
- la sélection des Heat Sinks et Multi-Hacks et de leur rareté ;
- le calcul du cooldown ;
- le calcul du nombre de hacks avant burnout ;
- la prise en compte des événements Ingress susceptibles de modifier temporairement ces règles.

Les timers de LEON peuvent fonctionner sous forme d'overlays Android flottants, être déplacés, réduits et continuer à fonctionner en arrière-plan jusqu'à leur notification de fin.

### MILO — Mission Interface and Logistics Operator

MILO regroupe les fonctions liées au Publisher et aux échanges nécessaires à la préparation et à la publication.

Il assure notamment :
- les échanges avec le Publisher ;
- la gestion du stockage Android associé ;
- la sélection et la mémorisation des emplacements utiles ;
- les contrôles d'intégrité entre les différents composants concernés.

### RITA — Redacted Information & Telegram Assistant

RITA est l'assistante d'information et de communication de Redacted BannerLab.

Elle intervient notamment pour :
- les informations importantes du Lab ;
- les annonces ;
- Telegram ;
- les informations liées aux nouvelles versions ;
- la présentation des mises à jour disponibles.

Au lancement, Redacted BannerLab peut vérifier si une nouvelle version stable est disponible. Lorsqu'une mise à jour est détectée, RITA présente les informations correspondantes avant le téléchargement et l'installation.

## Intégration avec Ingress Prime

La version stable 1.1.0 reste volontairement prudente concernant les éléments affichés au-dessus d'Ingress Prime.

Elle conserve un **cadre néon passif optionnel** :
- vert pour ENL ;
- bleu pour RES ;
- entièrement traversant afin de ne pas bloquer les interactions avec Prime.

Les expérimentations de HUD interactif, capteurs, personnages et éléments naviguants ne font pas partie de la version stable 1.1.0.

Les overlays Timers de LEON sont indépendants de ce HUD expérimental et restent disponibles.

## Langues

Redacted BannerLab propose une interface multilingue avec détection de la langue du téléphone au premier lancement et sélection manuelle dans les réglages.

Les principales zones de l'application sont localisées. L'anglais sert de fallback lorsqu'une traduction n'est pas encore disponible.

L'arabe bénéficie d'une prise en charge RTL et les formats de date utilisent la locale appropriée lorsque cela est possible.

## Éléments saisonniers

Certains éléments du Lab sont saisonniers et ne deviennent accessibles ou visibles que pendant leur période prévue.

Leur contenu n'est volontairement pas détaillé dans la documentation publique afin de préserver leur découverte dans l'application.

## Mises à jour Android

Les versions stables conservent :
- le package Android de production `com.bannerforge.mobile` ;
- la même clé de signature Android entre les versions ;
- une vérification SHA-256 de l'APK ;
- une vérification du package ;
- une vérification de la signature ;
- une vérification du `versionCode`.

La confirmation finale de l'installation reste gérée par Android.

## Compilation

Le workflow GitHub Actions de production est situé dans :

`.github/workflows/build-redacted-bannerlab-prod.yml`

Il assure notamment :
1. l'extraction de l'archive source ;
2. l'installation des dépendances ;
3. la compilation de l'application web ;
4. la génération du projet Android Capacitor ;
5. l'application des ressources et patches Android ;
6. la compilation de l'APK Release ;
7. la signature avec la clé PROD fournie par GitHub Actions Secrets ;
8. la vérification de la signature finale ;
9. la génération du SHA-256 et des métadonnées de mise à jour ;
10. la publication facultative de la GitHub Release.

Aucun keystore, mot de passe de signature ou secret ne doit être ajouté au dépôt.

## Sécurité et confidentialité

Le projet vise à rester auditable :
- aucune clé de signature n'est incluse dans les sources ;
- pas de collecte cachée destinée au suivi des utilisateurs ;
- pas de scraping silencieux de la carte Ingress ;
- contrôles d'intégrité des mises à jour ;
- trafic HTTP non chiffré interdit dans la configuration Android de production.

## Avertissement

Redacted BannerLab est un projet indépendant destiné à la communauté.

Il n'est ni développé, ni approuvé, ni sponsorisé par Niantic ou Scopely. **Ingress** et les éléments associés restent la propriété de leurs détenteurs respectifs.

Les licences et mentions des composants tiers utilisés par le projet sont détaillées dans `THIRD_PARTY_NOTICES.md`.
