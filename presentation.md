# RealEstate Pro – Page des Annonces Immobilières

**Phase 1 : Maquettage & Conception**

**Présenté par :** Essamrachi Ali
**Encadré par :** Mr. ESSARRAJ FOUAD

---

## Travail à Faire

L’objectif de cette phase est de concevoir une **page de listing des biens immobiliers** permettant aux utilisateurs de parcourir, filtrer et accéder rapidement aux annonces disponibles.

* **Cible :** Page `Properties` (Liste des biens à vendre et à louer)
* **Workflow :** Git / GitHub Flow
* **Technologies UI :** HTML5, Tailwind CSS
* **Contexte :** Projet *RealEstate Pro*

---

## Livrables Attendus

À la fin de cette étape, les éléments suivants sont réalisés :

* **Conception UI :** Maquette haute fidélité de la page `Properties`
* **Analyse Fonctionnelle :** Définition des filtres et parcours utilisateur
* **Navigation :** Accès fluide vers la page `Property_details`
* **Préparation Backend :** Structure prête pour intégration Laravel

---

## Perspective Utilisateur

### Cas d’Utilisation Principal

Le système permet à l’utilisateur de :

* Parcourir une liste de biens immobiliers (vente & location)
* Filtrer les annonces par :

  * Localisation
  * Type de bien
  * Prix minimum / maximum
* Visualiser les informations clés d’un bien :

  * Prix
  * Type
  * Localisation
  * Chambres / Salles de bain
* Accéder à la page de détails d’un bien

---

## Maquette (UI Design)

La page **Properties** est structurée en trois zones principales :

1. **Header Public**

   * Navigation claire (Home, Properties, About, Contact)
   * Accès authentification

2. **Barre de Filtres Sticky**

   * Recherche rapide et intuitive
   * Améliore l’expérience utilisateur lors du scroll

3. **Grille des Annonces**

   * Cards modernes et homogènes
   * Mise en avant visuelle des biens
   * Bouton **View Details** pour conversion

---

## Fonctionnalités Clés

La page repose sur des principes UX modernes :

1. **Recherche Avancée**

   * Filtres combinables (lieu, type, prix)

2. **Lisibilité Maximale**

   * Informations essentielles visibles immédiatement
   * Hiérarchie visuelle claire

3. **Navigation Fluide**

   * Pagination intégrée
   * Breadcrumb implicite via menu

4. **Design Responsive**

   * Optimisé mobile, tablette et desktop

---

## Structure Technique (Frontend)

* **Framework CSS :** Tailwind CSS
* **Composants UI :**

  * Cards immobilières réutilisables
  * Badges (For Sale, For Rent, New)
  * Pagination standard
* **SEO Ready :**

  * Meta tags
  * Open Graph
  * Structure sémantique HTML5

---

## Évolution Prévue

Cette page servira de base pour :

* Connexion avec la base de données (Laravel + MySQL)
* Filtres dynamiques (AJAX)
* Sauvegarde des favoris
* Tri avancé (prix, date, popularité)

---

## Conclusion

La page **Properties** constitue le **cœur fonctionnel** de la plateforme *RealEstate Pro*.
Elle offre une expérience claire, moderne et scalable, prête pour une intégration backend complète.

---

## Merci pour votre attention !

**Questions ?**
