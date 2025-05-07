# 📟 Rapport d’intervention – Optimisation du site de Nina Carducci

**Client** : Nina Carducci
**Site** : [https://nina-carducci.github.io](https://nina-carducci.github.io)
**Date d’intervention** : 15 avril 2025
**Développeur** : Lou Pankion

---

## 🌟 1. Objectifs de la mission

* Améliorer les performances générales du site.
* Optimiser le référencement naturel (SEO) et le référencement local via Schema.org.
* Ajouter les balises sociales (Open Graph, Twitter Cards).
* Améliorer l’accessibilité du site (Wave & Lighthouse).
* Corriger les bugs de la galerie (navigation et filtre actif).
* Produire un rapport d’intervention clair avec un cahier de recette.
* Obtenir un score Lighthouse ≥ 90 sur **Performances**, **Accessibilité** et **SEO**.

---

## 📊 2. Résultats Lighthouse (avant / après)

Audit réalisé avec Google Lighthouse (Chrome DevTools, mode Mobile, 4G simulée).

| Axe           | Score avant | Score après |
| ------------- | ----------- | ----------- |
| Performances  | 61          | ✅ **92**    |
| Accessibilité | 78          | ✅ **100**   |
| SEO           | 67          | ✅ **98**    |

✅ Tous les indicateurs sont passés **au vert** (score ≥ 90), validant les optimisations réalisées.

## 📸 Annexe – Rapport Lighthouse : Accessibilité

Voici le rapport Lighthouse accessibilité, démontrant une note de **100/100** :

![Capture Lighthouse Accessibilité](/img-rapport/nina-lalala.PNG)

---

## 🔧 3. Modifications effectuées

### 🚀 Performances

* Compression et conversion des images en WebP.
* Lazy loading (`loading="lazy"`) sur toutes les images.
* Suppression de jQuery et Bootstrap (remplacés par JavaScript natif et CSS custom).
* Minification des fichiers CSS et JS.
* Ajout d’attributs `width` et `height` pour les images afin de limiter les décalages de mise en page (CLS).

### 📈 SEO

* Ajout des balises `meta title`, `meta description`.
* Intégration des balises Open Graph (`og:title`, `og:description`, `og:image`, `og:url`) et Twitter Cards.
* Mise en place du balisage `Schema.org` en JSON-LD pour entreprise locale :

```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "Nina Carducci",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "68 avenue Alsace-Lorraine",
    "addressLocality": "Bordeaux",
    "postalCode": "33200",
    "addressCountry": "FR"
  },
  "telephone": "05 56 67 78 89",
  "openingHours": "Mo-Fr 10:00-19:00"
}
```

### 🧟‍ Accessibilité

* Ajout d’attributs `alt` **descriptifs** pour toutes les images (fin du `alt="Photo"`).
* Contrastes texte/fond corrigés.
* Structure sémantique des titres (`h1 > h2 > h3`) respectée (aucun niveau sauté).
* Navigation clavier testée avec focus visible.

---

### 🐛 4. Cahier de recette – Correctifs appliqués

| Action                                  | Résultat initial                                            | Résultat après résolution                                     | Statut   | Commentaire                                           |
| --------------------------------------- | ----------------------------------------------------------- | ------------------------------------------------------------- | -------- | ----------------------------------------------------- |
| Navigation dans la modale de la galerie | Les boutons "précédente" et "suivante" ne réagissaient pas  | Navigation fluide entre les images, retour possible au début  | ✅ Résolu | Refonte JS en vanilla, gestion des événements `click` |
| Affichage du filtre actif               | Aucune indication visuelle lors de la sélection d’un filtre | Le filtre sélectionné s’affiche avec un fond doré comme prévu | ✅ Résolu | Ajout de classes dynamiques en JS pour les boutons    |
| Texte alternatif d’images               | `alt="Photo"` non descriptif sur plusieurs images           | Texte alternatif pertinent ajouté pour chaque image           | ✅ Résolu | Relecture complète et correction manuelle             |
| Niveaux de titres HTML                  | Hiérarchie sautée (`h1 > h3`)                               | Ordre des titres ajusté : `h1 > h2 > h3`                      | ✅ Résolu | Meilleure lisibilité et accessibilité sémantique      |

---

### 🧪 5. Cas d’usage testés (recette fonctionnelle)

| Fonction testée                               | Statut | Détail                                      |
| --------------------------------------------- | ------ | ------------------------------------------- |
| Chargement rapide sur mobile (<3s)            | ✅      | Lazy loading + WebP + JS/CSS minifié        |
| Métadonnées SEO et réseaux sociaux visibles   | ✅      | Présence vérifiée dans l'inspecteur         |
| Navigation clavier fluide                     | ✅      | Tous les éléments sont accessibles au focus |
| Galerie avec filtres fonctionnels et lisibles | ✅      | Sélection visuelle active présente          |
| Modale fonctionnelle avec navigation images   | ✅      | Précédent / Suivant opérationnels           |
| Accessibilité images et titres                | ✅      | Alt pertinents, titres ordonnés             |

---

### 📁 6. Dépôt GitHub optimisé

👉 \[Lien vers le dépôt à insérer ici]

---

### 🙏 7. Conclusion

Le site de Nina Carducci est désormais :

* ✅ plus rapide à charger
* ✅ mieux référencé (SEO et local)
* ✅ plus accessible
* ✅ débarrassé de ses bugs critiques

Ces optimisations garantissent une **meilleure expérience utilisateur**, un **meilleur positionnement sur Google**, et un **site plus professionnel**.
