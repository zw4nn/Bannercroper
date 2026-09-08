# Redacted BannerLab

**Éditeur mobile-first non officiel pour créer, préparer et publier des bannières Ingress Prime.**

> Version stable : **1.0.15**  
> IGOR : **0.6.10** · MILO : **0.5.1**

Redacted BannerLab regroupe dans une seule application le travail de préparation d’une bannière : découpe de la fresque, organisation des missions, préparation du parcours, suivi dans IITC et assistance à la publication dans Mission Authoring Tool.

Le projet est indépendant et **n’est ni affilié, ni approuvé, ni sponsorisé par Niantic**.

## Ce que fait Redacted BannerLab

- création d’une fresque à partir d’une image et découpe en missions ;
- édition mobile des missions, titres, descriptions et paramètres ;
- placement et organisation des portails ;
- aperçu de la bannière et export des visuels ;
- recherche et consultation de bannières Bannergress ;
- préparation et suivi du parcours avec **IGOR**, le companion IITC ;
- assistance à la publication avec **MILO**, sans automatiser le clic final de soumission ;
- sauvegarde locale des projets et outils d’export / restauration ;
- interface multilingue avec détection automatique de la langue et anglais en fallback.

## Les assistants du Lab

### IGOR

**IITC Gateway for Operations & Routing**

IGOR accompagne la préparation et le suivi des missions dans IITC : parcours, portails, progression et synchronisation volontaire avec Redacted BannerLab.

### MILO

**Mission Import & Launch Operator**

MILO accompagne la publication dans Mission Authoring Tool. Il prépare les données de mission et guide l’Agent dans Chrome ou Firefox.

**Le bouton final Submit reste toujours sous le contrôle de l’Agent.**

### RITA

**Redacted Information & Telegram Assistant**

RITA est le bot Telegram du Lab pour le support, les informations et les échanges liés au projet.

## Installation Android

1. Ouvrir la section **Releases** de ce dépôt.
2. Télécharger l’APK de la dernière version stable.
3. Autoriser l’installation depuis cette source si Android le demande.
4. Installer l’APK sans désinstaller une version officielle précédente de Redacted BannerLab.

Les versions officielles utilisent la **même clé de signature Android**, afin que les mises à jour puissent s’installer par-dessus les versions précédentes.

[➡️ Télécharger la dernière release](https://github.com/zw4nn/Redacted-Banner-Lab/releases/latest)

## Code source et builds

Le dépôt reste volontairement simple :

- `Redacted_BannerLab_Source.zip` contient le code source utilisé pour le build ;
- `.github/workflows/` contient le workflow GitHub Actions de compilation et de publication ;
- `README.md` décrit toujours la **dernière version de production**.

Lors d’un build, GitHub Actions :

1. vérifie puis extrait le ZIP source ;
2. installe les dépendances ;
3. compile l’application web ;
4. génère le projet Android ;
5. applique les ressources et correctifs Android du projet ;
6. vérifie la version ;
7. signe l’APK avec la clé officielle injectée via **GitHub Actions Secrets** ;
8. vérifie la signature et produit le SHA-256 ;
9. publie les fichiers de release lorsque la publication est demandée.

La clé de signature Android et ses mots de passe **ne sont pas présents dans le dépôt ni dans le ZIP source**.

## Vie privée

Redacted BannerLab est conçu avec une approche locale :

- pas de compte Redacted BannerLab ;
- pas de publicité ;
- pas de télémétrie cachée ;
- pas de collecte silencieuse de données de jeu ;
- les projets restent locaux tant que l’utilisateur ne déclenche pas volontairement une action d’export, de partage, de synchronisation ou de publication.

Certaines fonctions utilisent naturellement des services externes lorsque l’Agent les demande, notamment GitHub, Bannergress, OpenStreetMap / Valhalla, IITC, Mission Authoring Tool et Telegram.

## Transparence

Le dépôt public permet d’inspecter le code livré dans le ZIP source et le processus de build GitHub Actions.

Les garde-fous du build vérifient notamment :

- l’absence de clé de signature dans le ZIP ;
- la cohérence entre version web et version Android ;
- le certificat utilisé pour signer l’APK ;
- le SHA-256 des APK publiés.

## Versions de test

Les builds intermédiaires et versions de test peuvent évoluer rapidement. **Ce README n’est volontairement pas modifié pour chaque build de test.**

Il est mis à jour uniquement lorsqu’une version est réellement passée en **production / GitHub Release**. Cela évite que la page d’accueil du dépôt présente une fonction expérimentale comme déjà disponible au public, concept étonnamment raisonnable pour Internet.

## Communauté

Redacted BannerLab est un projet communautaire créé pour faciliter la conception et le suivi des bannières Ingress.

Retours, bugs et idées peuvent être transmis via les accès Support / Telegram intégrés à l’application.

---

© 2026 Zw4nn · Redacted BannerLab  
Projet communautaire non officiel pour Ingress Prime.
