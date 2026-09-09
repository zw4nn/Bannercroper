# 🧪 Redacted BannerLab

**Version : 1.0.17 · build 11700**  
**Personnel du Lab : REDACTED · IGOR 0.6.17 · MILO 0.5.2 · RITA · OSCAR · LEON 0.1.0**

Redacted BannerLab est un outil mobile-first communautaire pour préparer des fresques Ingress, organiser leurs missions et faciliter le travail entre le Lab, IITC et Mission Authoring Tool.

## 🧮 LEON 0.1.0

LEON rejoint officiellement le personnel du Lab : **Leveling & Exact Operations Navigator**.

Il peut notamment :

- lire un nombre d’AP ou le texte « Partager les statistiques » du Scanner ;
- choisir un objectif de niveau ou un objectif personnalisé ;
- tenir compte des bonus AP détectés ;
- rechercher une combinaison exacte pour atteindre l’objectif **TOUT PILE**.

LEON est également présenté dans **Réglages & infos** avec son rôle et sa version.

## 🗺️ IGOR 0.6.17

**IGOR = IITC Gateway for Operations & Routing.**

Il assure la passerelle entre Redacted BannerLab et IITC pour préparer les parcours, actions portail et synchronisations nécessaires au travail sur une bannière.

Le bridge utilise désormais une authentification HMAC-SHA256 avec timestamp court et nonce anti-rejeu.

## 📤 MILO 0.5.2

MILO accompagne la préparation et la publication des missions dans Mission Authoring Tool depuis Chrome ou Firefox.

La configuration navigateur utilise une clé de setup éphémère et les URI de retour ne transportent plus de secret réutilisable.

## 🤖 RITA et les mises à jour intégrées

Depuis plusieurs versions, Redacted BannerLab peut rechercher et installer ses mises à jour directement depuis **Réglages & infos**.

À partir de la 1.0.17, **RITA vous guide** dans ce parcours : vérification de la version disponible, téléchargement de l’APK et confirmation d’installation Android.

Le `versionCode` Android reste utilisé en interne pour déterminer l’ordre des versions et vérifier les APK, mais sa longue valeur numérique n’est plus affichée dans l’interface.

## 🖼️ Interface et navigation

La 1.0.17 consolide également plusieurs améliorations de l’éditeur et de la navigation : aperçu Prime plein écran, comportement d’OSCAR, interactions de REDACTED et diverses corrections de présentation.

## 📦 Source propre

Le ZIP source de la version courante ne conserve plus les anciens README, changelogs et notes de versions historiques. La documentation embarquée correspond uniquement à la release courante.

## 🔐 Sécurité

Les clés de signature Android, mots de passe et tokens ne doivent jamais être stockés dans le dépôt source. Ils restent injectés lors du build via les secrets GitHub Actions.

> Ingress et Ingress Prime sont des marques de Niantic. Redacted BannerLab est un projet communautaire indépendant, non affilié et non approuvé par Niantic.
