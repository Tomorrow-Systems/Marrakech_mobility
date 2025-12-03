# Projets de Mobilité de Marrakech - Manuel d'utilisation

## Table des matières

1. [Prise en main](#1-prise-en-main)
2. [Aperçu du tableau de bord Admin](#2-aper%C3%A7u-du-tableau-de-bord-admin)
3. [Gestion des projets](#3-gestion-des-projets)
4. [Gestion des Histoires](#4-gestion-des-r%C3%A9cits)
5. [Gestion de l'infrastructure](#5-gestion-de-linfrastructure)
6. [Gestion des groupes](#6-gestion-des-groupes)
7. [Utilisation de l'éditeur de carte](#7-utilisation-de-l%C3%A9diteur-de-carte)
8. [Paramètres & Personnalisation](#8-param%C3%A8tres--personnalisation)
9. [Sauvegarde & Restauration](#9-sauvegarde--restauration)
10. [Fonctionnalités du site public](#10-fonctionnalit%C3%A9s-du-site-public)

---

## 1. Prise en main

### 1.1 Accéder au panneau d'administration

1. Allez sur la page d'accueil de votre site
2. Cliquez sur le bouton **Admin** dans la barre de navigation (si visible)
3. Ou allez directement à `/admin` dans votre navigateur
4. Saisissez votre nom d'utilisateur et mot de passe
5. Cliquez sur **Login**

> **Identifiants par défaut :**
> - Nom d'utilisateur : `admin`
> - Mot de passe : `admin123`
> 
> ⚠️ Veuillez modifier ces identifiants après la première connexion !

### 1.2 Agencement du tableau de bord Admin

Après connexion, vous verrez :

- **En-tête** : affiche votre nom d'utilisateur, le bouton Accueil et le bouton Déconnexion
- **Onglets** : Projets, Histoires, Infrastructure, Groupes, Paramètres
- **Bouton Éditeur de Carte** : bouton orange/aux couleurs d'accent pour accéder à l'éditeur de carte
- **Boutons d'action** : boutons spécifiques au contexte (Nouveau Projet, Nouveau Récit, etc.)

---

## 2. Aperçu du tableau de bord Admin

### 2.1 Onglets de navigation

| Onglet | But |
|-----|---------|
| **Projets** | Gérer les projets de mobilité |
| **Histoires** | Créer du contenu narratif avec des chapitres |
| **Infrastructure** | Gérer les points d'infrastructure |
| **Groupes** | Organiser projets et Histoires en groupes |
| **Paramètres** | Configurer l'identité, la langue, les couches cartographiques |

### 2.2 Actions courantes

- **Recherche** : Utilisez la zone de recherche pour filtrer les éléments
- **Modifier** : Cliquez sur l'icône crayon ou le bouton « Modifier »
- **Supprimer** : Cliquez sur l'icône poubelle (confirmation requise)
- **Réordonner** : Utilisez les flèches haut/bas pour modifier l'ordre d'affichage

---

## 3. Gestion des projets

### 3.1 Création d'un nouveau projet

1. Cliquez sur l'onglet **Projets**
2. Cliquez sur le bouton **Nouveau Projet**
3. Remplissez les détails du projet (voir sections ci-dessous)
4. Cliquez sur **Save** ou **Create Project**

### 3.2 Champs du projet expliqués

#### Informations de base

| Champ | Description | Exemple |
|-------|-------------|---------|
| **Project ID** | Identifiant unique (modifiable) | `can-marrakech-01` |
| **Name** | Titre du projet | `Extension du Boulevard Phase 1` |
| **Type** | Catégorie du projet | `Voirie & Mobilité` |
| **Status** | État actuel | `done`, `in_progress`, `future` |
| **Progress** | Pourcentage d'avancement | `75%` |
| **District** | Emplacement/zone | `Marrakech - Zone Nord` |

#### Descriptions

| Champ | Description |
|-------|-------------|
| **Short Description** | Résumé court (affiché dans les cartes) |
| **Description** | Description détaillée complète |
| **Objectives** | Liste des objectifs du projet (une par ligne) |

#### Indicateurs

| Champ | Description |
|-------|-------------|
| **Length (km)** | Longueur de l'itinéraire en kilomètres |
| **Stations** | Nombre de stations/arrêts |
| **Intersections** | Nombre d'intersections |

#### Dates

| Champ | Description |
|-------|-------------|
| **Start Date** | Date de début du projet |
| **End Date** | Date d'achèvement du projet |
| **Planned Date** | Date prévue d'achèvement (pour projets futurs) |

#### Budget

| Champ | Description |
|-------|-------------|
| **Budget** | Coût du projet | `81.12 MDH` |

> 💡 La visibilité du budget peut être activée/désactivée dans les Paramètres

### 3.3 Ajout d'images aux projets

#### Étapes :

1. Dans le formulaire d'édition du projet, trouvez la section **Images**
2. Cliquez sur **Add Image** ou glissez les fichiers pour téléverser
3. Pour chaque image, vous pouvez définir :
   - **Caption** : Légende de l'image
   - **Category** : Choisir parmi :
     - `before` - État avant le projet
     - `after` - État après achèvement

#### Images Avant/Après :

Lorsque vous avez des images dans les catégories « before » et « after », la page de détail du projet les affichera automatiquement dans des sections séparées, facilitant la comparaison pour les visiteurs.

#### Conseils pour les images :
- Formats supportés : JPG, PNG, GIF, WebP, SVG
- Taille maximale : 50 Mo par image
- Recommandation : Utiliser des images de haute qualité (au moins 1200px de large)

### 3.4 Ajout de vidéos aux projets

#### Option 1 : Vidéos YouTube (recommandé)

1. Trouvez la section **Videos** dans l'édition du projet
2. Cliquez sur **Add Video**
3. Sélectionnez le type : **YouTube/Embed**
4. Collez l'URL YouTube :
   - URL complète : `https://www.youtube.com/watch?v=VIDEO_ID`
   - URL courte : `https://youtu.be/VIDEO_ID`
5. Ajoutez un titre pour la vidéo
6. Enregistrez

#### Option 2 : Téléversement direct de vidéo

1. Cliquez sur **Add Video**
2. Sélectionnez le type : **Upload**
3. Cliquez pour sélectionner ou glissez un fichier vidéo
4. Formats supportés : MP4, WebM, MOV, AVI
5. Taille maximale : 500 Mo

#### Affichage des vidéos :
- Les vidéos YouTube s'afficheront avec un lecteur intégré
- Les vidéos téléversées utiliseront le lecteur vidéo natif du navigateur

### 3.5 Géométrie du projet (position sur la carte)

1. Cliquez sur **Edit Geometry** ou utilisez le bouton **Map Editor**
2. Voir [Section 7 : Utilisation de l'éditeur de carte](#7-utilisation-de-l%C3%A9diteur-de-carte) pour les détails

### 3.6 Projets connectés

Reliez des projets apparentés :

1. Trouvez la section **Connected Projects**
2. Sélectionnez des projets dans le menu déroulant
3. Ils apparaîtront comme des liens sur la page de détail du projet

### 3.7 Ordre d'affichage des projets

Contrôlez l'ordre d'apparition des projets :

1. Dans la liste Projets, utilisez les boutons **↑** et **↓**
2. Ou modifiez le champ **Display Order** (les nombres plus bas apparaissent en premier)

---

## 4. Gestion des Histoires

### 4.1 Comprendre les Histoires

Les Histoires (Stories) sont du contenu narratif qui peut s'étendre sur plusieurs chapitres. Chaque récit peut :
- Avoir une image de couverture
- Contenir plusieurs chapitres
- Lier des projets et de l'infrastructure
- Inclure des images et des vidéos

### 4.2 Création d'un nouveau récit

1. Cliquez sur l'onglet **Histoires**
2. Cliquez sur le bouton **New Story**
3. Remplissez les détails du récit :

| Champ | Description |
|-------|-------------|
| **Title** | Titre du récit |
| **Summary** | Bref résumé (affiché dans les cartes) |
| **Content** | Contenu principal du récit (optionnel) |
| **Cover Image** | Image principale pour la carte du récit |
| **Published** | Basculer pour rendre le récit visible |

### 4.3 Ajout d'une image de couverture

#### Option 1 : Téléverser l'image

1. Cliquez sur **Upload Cover Image**
2. Sélectionnez un fichier image sur votre ordinateur

#### Option 2 : Utiliser une URL

1. Cliquez sur **Use URL**
2. Collez l'URL directe de l'image

### 4.4 Gestion des chapitres

Les chapitres sont des sections au sein d'un récit navigables individuellement.

#### Ajouter un chapitre :

1. Ouvrez un récit en mode édition
2. Descendez à la section **Chapters**
3. Cliquez sur **Add Chapter**
4. Remplissez :
   - **Title** : Titre du chapitre
   - **Text** : Contenu du chapitre
   - **Project Links** : Sélectionnez les projets liés
   - **Images** : Ajoutez des images spécifiques au chapitre
   - **Videos** : Ajoutez des vidéos YouTube ou téléversées
   - **Map Focus** : Définissez des coordonnées pour mettre en évidence sur la carte

#### Ordre des chapitres :

Utilisez les poignées de glisser-déposer ou le champ d'ordre pour arranger les chapitres.

#### Réglage du focus sur la carte :

1. Cliquez sur **Set Map Focus**
2. Entrez latitude, longitude et niveau de zoom
3. Quand les lecteurs consultent ce chapitre, la carte se centrera sur cet emplacement

### 4.5 Publication des Histoires

Les Histoires ont un statut publié/non publié :

- **Published** : Visible sur la page publique des Histoires
- **Unpublished** : Visible uniquement en admin

Basculer l'interrupteur **Published** pour contrôler la visibilité.

---

## 5. Gestion de l'infrastructure

### 5.1 Qu'est-ce que l'infrastructure ?

Les éléments d'infrastructure sont des points d'intérêt tels que :
- Hubs de transport (aéroports, gares)
- Services publics
- Espaces publics
- Installations de stationnement

### 5.2 Création d'un élément d'infrastructure

1. Cliquez sur l'onglet **Infrastructure**
2. Cliquez sur **New Infrastructure**
3. Remplissez :

| Champ | Description |
|-------|-------------|
| **ID** | Identifiant unique |
| **Name** | Nom de l'infrastructure |
| **Type** | Type d'infrastructure |
| **Category** | Classification de catégorie |
| **Description** | Description détaillée |
| **Visible** | Afficher/masquer sur la carte |

### 5.3 Ajout de géométrie

1. Cliquez sur **Edit Geometry**
2. Utilisez l'éditeur de carte pour placer des points, dessiner des lignes ou créer des polygones
3. Voir [Section 7](#7-utilisation-de-l%C3%A9diteur-de-carte) pour les instructions détaillées

### 5.4 Informations du panneau pour les points

Pour les marqueurs sur la carte, vous pouvez ajouter des informations qui apparaissent lors du clic :

- **Panel Title** : Titre affiché dans le panneau d'information
- **Panel Description** : Texte descriptif
- **Panel Image** : Image affichée dans le panneau

---

## 6. Gestion des groupes

### 6.1 Comprendre les groupes

Les groupes aident à organiser projets et Histoires en catégories. Ils fournissent :
- Des filtres sur les pages publiques
- Un contrôle de visibilité pour plusieurs éléments
- Une organisation pour un grand nombre d'éléments

### 6.2 Groupes de projets

1. Cliquez sur l'onglet **Groups**
2. Sélectionnez **Project Groups**
3. Cliquez sur **New Group**
4. Configurez :

| Champ | Description |
|-------|-------------|
| **Name** | Nom du groupe |
| **Description** | Description du groupe |
| **Projects** | Sélectionnez les projets à inclure |
| **Hidden Projects** | Projets dans le groupe mais non affichés |
| **Visible** | Afficher/masquer le groupe entier |

### 6.3 Groupes de Histoires

Similaire aux groupes de projets mais pour les Histoires :

1. Cliquez sur l'onglet **Groups**
2. Sélectionnez **Story Groups**
3. Cliquez sur **New Group**
4. Ajoutez des Histoires au groupe

### 6.4 Contrôle de visibilité

Les groupes offrent deux niveaux de visibilité :

1. **Visibilité du groupe** : Basculer l'affichage du groupe entier on/off
2. **Éléments masqués** : Masquer des éléments spécifiques dans un groupe visible

Cela permet un contrôle flexible de ce qui apparaît sur le site public.

---

## 7. Utilisation de l'éditeur de carte

### 7.1 Accéder à l'éditeur de carte

1. Cliquez sur le bouton accentué **Map Editor** dans l'admin
2. Ou naviguez directement vers `/admin/map-editor`

### 7.2 Outils de dessin

| Outil | Icône | But |
|------|------|---------|
| **Marker** | 📍 | Placer des points simples |
| **Line** | ➖ | Dessiner des itinéraires/trajectoires |
| **Polygon** | ⬡ | Créer des zones/aires |
| **Edit** | ✏️ | Modifier des formes existantes |
| **Delete** | 🗑️ | Supprimer des formes |

### 7.3 Placement des marqueurs

1. Cliquez sur l'outil **Marker**
2. Cliquez sur la carte à l'endroit où vous voulez placer le marqueur
3. Un marqueur sera placé
4. Cliquez sur le marqueur pour ajouter les informations du panneau :
   - Panel Title
   - Panel Description
   - Panel Image (téléverser ou URL)

### 7.4 Dessiner des lignes

1. Cliquez sur l'outil **Line**
2. Cliquez pour commencer la ligne
3. Cliquez pour ajouter des points
4. Double-cliquez pour terminer la ligne

Les lignes sont utiles pour :
- Routes
- Lignes de bus
- Chemins piétons
- Corridors de projet

### 7.5 Dessiner des polygones

1. Cliquez sur l'outil **Polygon**
2. Cliquez pour créer des sommets
3. Cliquez de nouveau sur le premier point pour fermer le polygone

Les polygones sont utiles pour :
- Limites de districts
- Zones de projet
- Aires d'intérêt

### 7.6 Modifier la géométrie

1. Cliquez sur l'outil **Edit**
2. Cliquez sur une forme pour la sélectionner
3. Faites glisser les sommets pour repositionner
4. Cliquez sur **Save** une fois terminé

### 7.7 Couches cartographiques

Changez l'arrière-plan de la carte :

1. Cliquez sur le bouton **Layers**
2. Sélectionnez parmi les couches disponibles :
   - OpenStreetMap (par défaut)
   - Satellite
   - Terrain
   - Dark Mode
   - Light Mode
   - Topographic
   - Et plus...

### 7.8 Personnalisation des icônes

#### Utilisation d'icônes personnalisées :

1. Dans l'éditeur de carte, trouvez le panneau **Icons**
2. Sélectionnez dans la bibliothèque SVG
3. Ou téléversez de nouvelles icônes SVG

#### Tailles d'icônes :

Trois contrôles de taille séparés :

| Contrôle | Affecte |
|---------|---------|
| **Project Icons** | Tailles des marqueurs de projets |
| **Infrastructure Icons** | Tailles des marqueurs d'infrastructure |
| **Custom Icons** | Tailles des icônes personnalisées téléversées |

Ajustez le curseur pour changer la taille des icônes (petit → grand).

### 7.9 Importer KML

Importer des données géographiques existantes :

1. Cliquez sur **Import KML**
2. Sélectionnez un fichier .kml ou .kmz
3. La géométrie sera ajoutée à la couche courante

### 7.10 Exporter KML

Exporter des données pour les utiliser dans d'autres applications :

1. Cliquez sur **Export KML**
2. Sélectionnez les éléments à exporter
3. Téléchargez le fichier KML généré

---

## 8. Paramètres & Personnalisation

### 8.1 Paramètres de langue

1. Allez dans l'onglet **Settings**
2. Trouvez la section **Language**
3. Sélectionnez :
   - **Français** - Interface en français
   - **English** - Interface en anglais

Le site entier passera à la langue sélectionnée.

### 8.2 Paramètres de marque

#### Téléversement du logo :

1. Allez dans **Settings** → **Branding**
2. Cliquez sur **Upload Logo**
3. Sélectionnez votre image de logo
4. Le logo apparaîtra dans la barre de navigation

#### Favicon :

1. Trouvez la section **Favicon**
2. Téléversez votre image de favicon (recommandé 32x32 ou 64x64 px)

#### Couleur d'accent :

Personnalisez la couleur principale utilisée sur le site :

1. Trouvez la section **Accent Color**
2. Utilisez les curseurs RVB ou saisissez les valeurs :
   - **R** (Rouge) : 0-255
   - **G** (Vert) : 0-255
   - **B** (Bleu) : 0-255
3. Prévisualisez les mises à jour en temps réel

#### Couleur d'arrière-plan :

Personnalisez la couleur de fond :

1. Trouvez la section **Background Color**
2. Ajustez les valeurs RVB selon vos besoins

### 8.3 Bascule de visibilité

| Bascule | Effet |
|--------|--------|
| **Show Admin Button** | Afficher/masquer le bouton admin dans la barre de navigation publique |
| **Show Budget** | Afficher/masquer les informations de budget sur les projets |

### 8.4 Configuration des couches cartographiques

Configurez quelles couches cartographiques sont disponibles :

1. Allez dans **Settings** → **Map Layers**
2. Activez/désactivez les couches
3. Couches disponibles :
   - OpenStreetMap
   - Satellite
   - Terrain
   - Dark Mode
   - Light Mode
   - Topographic
   - Watercolor
   - Streets
   - Outdoors
   - Hybrid

### 8.5 Paramètres de taille des icônes

Ajustez les tailles par défaut des icônes pour la carte :

1. Allez dans **Settings** → **Icon Sizes**
2. Trois contrôles séparés :
   - **Project Icons** : Taille pour les marqueurs de projets
   - **Infrastructure Icons** : Taille pour les marqueurs d'infrastructure
   - **Custom Icons** : Taille pour les icônes personnalisées téléversées
3. Utilisez le curseur (valeurs typiques 16-64 pixels)

### 8.6 CMS de la page d'accueil

Personnalisez le contenu de la page d'accueil :

1. Allez dans **Settings** → **Home Content**
2. Modifiez les sections :

**Section Héro :**
- Hero Title
- Hero Subtitle
- Hero Background Image

**Statistiques :**
- Nombre de Projets
- Kilomètres
- Intersections

**Section À propos :**
- About Title
- About Text
- About Image

---

## 9. Sauvegarde & Restauration

### 9.1 Créer une sauvegarde

Sauvegardez régulièrement toutes vos données :

1. Allez dans l'onglet **Settings**
2. Trouvez la section **Backup & Restore**
3. Cliquez sur **Download Backup**
4. Sauvegardez le fichier JSON dans un endroit sûr

La sauvegarde inclut :
- Tous les projets
- Tous les Histoires et chapitres
- Toute l'infrastructure
- Tous les groupes
- Tous les paramètres
- Contenu de la page d'accueil

### 9.2 Restauration à partir d'une sauvegarde

⚠️ **Attention** : La restauration remplacera toutes les données actuelles !

1. Allez dans **Settings** → **Backup & Restore**
2. Cliquez sur **Restore from Backup**
3. Sélectionnez votre fichier JSON de sauvegarde
4. Confirmez la restauration
5. Attendez la fin du processus

### 9.3 Importer des projets individuels

Importer un seul projet sans affecter les autres données :

1. Allez dans **Settings** → **Import**
2. Cliquez sur **Import Project**
3. Sélectionnez un fichier JSON de projet
4. Si l'ID existe déjà, un nouvel ID sera généré

---

## 10. Fonctionnalités du site public

### 10.1 Page d'accueil

La page d'accueil publique affiche :
- Section Héro avec titre et image
- Aperçu des statistiques
- Liens de catégories
- Contenu en vedette

### 10.2 Carte interactive

La page carte (`/map`) propose :

#### Filtres :
- **Status** : Filtrer par done/in progress/future
- **Type** : Filtrer par type de projet
- **Search** : Recherche textuelle pour les projets
- **Groups** : Filtrer par groupes de projets (sections réductibles)

#### Interaction avec la carte :
- Cliquez sur les marqueurs pour voir les détails du projet
- Cliquez sur les lignes/polygones pour sélectionner des projets
- Utilisez le panneau latéral pour voir les détails complets
- Cliquez sur les images pour ouvrir la galerie en lightbox

### 10.3 Page des projets

La page projets (`/projects`) affiche :
- Grille de cartes de projets
- Filtrage par groupe
- Fonctionnalité de recherche
- Cliquez pour voir le détail complet

### 10.4 Page des Histoires

La page Histoires (`/story`) affiche :
- Carrousel de cartes de Histoires
- Filtrage par groupe avec badges
- Cliquez pour lire le récit complet avec chapitres
- Navigation entre les chapitres

### 10.5 Page de détail du projet

Les pages de projet individuelles affichent :
- Image hero/galerie
- Sections images Avant/Après
- Description et objectifs
- Indicateurs du projet
- Histoires liés
- Vidéos (intégration YouTube)
- Emplacement sur la carte

### 10.6 Changement de langue

Les utilisateurs peuvent changer la langue :
- Cherchez le sélecteur de langue (FR/EN)
- Cliquez pour basculer entre Français et Anglais
- Tout le contenu se mettra à jour dans la langue sélectionnée

### 10.7 Lightbox média

Lors de la visualisation d'images :
- Cliquez sur une image pour l'ouvrir en plein écran
- Utilisez les flèches pour naviguer entre les images
- Cliquez en dehors ou appuyez sur Échap pour fermer
- Fonctionne sur les pages de projet, les Histoires et les panneaux de carte

---

## Référence rapide

### Raccourcis clavier

| Touche | Action |
|-----|--------|
| Escape | Fermer les dialogues/lightbox |
| Arrow Left/Right | Naviguer dans les images en lightbox |

### Limites de taille de fichier

| Type | Taille maximale |
|------|--------------|
| Images | 50 Mo |
| Vidéos | 500 Mo |
| Icônes | 5 Mo |
| Logos | 10 Mo |
| Bibliothèque SVG | 2 Mo |
| Fichiers KML | 10 Mo |

### Formats de fichiers supportés

| Type | Formats |
|------|---------|
| Images | JPG, JPEG, PNG, GIF, WebP, SVG |
| Vidéos | MP4, WebM, MOV, AVI |
| Icônes | PNG, SVG, ICO |
| Géographique | KML, KMZ |

---

## Dépannage

### Problèmes courants

**Q : Je ne vois pas mes modifications sur le site public**
- Assurez-vous que l'élément est publié/visible
- Vérifiez les paramètres de visibilité du groupe
- Videz le cache de votre navigateur

**Q : Les images ne se téléversent pas**
- Vérifiez la taille du fichier (max 50 Mo)
- Assurez-vous du bon format (JPG, PNG, etc.)
- Essayez avec un autre navigateur

**Q : La vidéo YouTube ne se lance pas**
- Vérifiez que l'URL est correcte
- Assurez-vous que la vidéo est publique sur YouTube
- Essayez le format d'URL YouTube complet

**Q : La géométrie de la carte ne s'enregistre pas**
- Cliquez sur Save après avoir fait des modifications
- Assurez-vous d'avoir les permissions d'édition
- Essayez de rafraîchir et de redessiner

### Obtenir de l'aide

Si vous rencontrez des problèmes :
1. Consultez les journaux système (Settings → System Logs)
2. Faites une capture d'écran des messages d'erreur
3. Contactez votre administrateur

---

*Manuel d'utilisation v1.0*
*Tomorrow Systems Projects Platform*
*Dernière mise à jour : Décembre 2025*
