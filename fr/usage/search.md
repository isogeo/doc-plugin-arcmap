# Rechercher

Pour tenir compte du moteur de recherche Isogeo \(basé sur le principes des facettes contextuelles\) mais aussi pour les performances, la recherche se passe en deux temps :

1. l'utilisateur entre les paramètres de sa recherche qui ressert de plus en plus le nombre de résultats ;
2. l'utilisateur affiche et parcourt la liste des résultats.

![](../../assets/plugin_ArcMap_search_tab_filtered_FR.png "Interface du plugin avec une recherche vide")

De là il peut alors [consulter la métadonnée](/usage/metadata.md) ou [ajouter la donnée à sa carte](/usage/display.md).

## Recherche sémantique

La recherche textuelle s'effectue dans la barre de saisie de texte en haut à gauche de la fenêtre du plugin.

Les termes saisis sont recherchés au sein :

* du titre de la fiche de métadonnées
* du nom du fichier
* de son résumé
* de ses mots-clés
* de ses thèmes INSPIRE

Pour en savoir plus sur le fonctionnement du moteur de recherche Isogeo, [consulter l'aide en ligne](http://help.isogeo.com/fr/features/inventory/search.html).

## Filtres contextuels

### Filtre par mot-clé

Pour filtrer sur un mot-clé, sélectionner dans la liste déroulante dédiée.

![](../../assets/plugin_ArcMap_search_options_keywords_FR.png "Filtre par mot-clé")

### Autres filtres

Tous les autres filtres sémantiques fonctionnent de la même manière \(sélection d'une modalité dans une liste déroulante\).

Tous les filtres sont inter-dépendants \(contextuels\). Ainsi l'application d'un filtre fait évoluer les modalités disponibles dans toutes les listes déroulantes et le nombre de résultats correspondant.

### Filtre géographique

Il est également possible de filtrer les résultats à partir de l'emprise de la carte.

![](../../assets/plugin_ArcMap_search_options_geographic_FR.png "Filtre à partir de la carte")

Par défaut, le filtre géographique remonte toute les données qui **intersectent** l'emprise considérée. Pour changer ce comportement, aller dans l'onglet "Paramètres", choisir un opérateur différent, puis relancer la recherche.

![](../../assets/plugin_ArcMap_settings_geographic_FR.png "Paramétrer l\'opérateur géométrique pour le filtre géographique")

---

## Afficher les résultats

Lors de la saisie de texte dans la barre de recherche et de l'action sur un filtre sémantique, le contenu des autres filtres se met à jour, et le nombre de résultats attendus s'affiche dans le bouton orange.

![](https://raw.githubusercontent.com/isogeo/isogeo-plugin-qgis/master/img/search_results_show_fr.png "Nombre de résultats sur le bouton pour les afficher")

Au clic sur ce bouton, les résultats de la recherche sont affichés dans le tableau des résultats, paginés de manière à ne jamais afficher plus de 10 résultats simultanément.

Pour chaque résultat, on trouve :

* le titre affecté à la fiche de métadonnée
* la date de dernière modification de la donnée
* une icône représentant son type de géométrie
* les modalités d'ajout disponibles pour cette donnée

Deux boutons sont consacrés à la navigation entre les différentes pages de résultats en bas du tableau :

![](https://raw.githubusercontent.com/isogeo/isogeo-plugin-qgis/master/img/search_results_pagination_fr.png "Pagination des résultats")

### Trier les résultats

Une fois affichés, les résultats peuvent être triés.

Le tri par défaut est **le score de pertinence** \(voir [ici pour le détail du calcul du score](http://help.isogeo.com/fr/features/inventory/search.html#pertinence-)\). Il s'agit du tri recommandé lors de recherches textuelles.

Lorsqu'aucun texte n'est saisi dans la barre de recherche, le score de pertinence étant nul pour tous les résultats c'est alors le tri décroissant par date de création de la fiche de métadonnée qui est appliqué par défaut.

Les autres tris disponibles sont :

* Ordre alphabétique
* Date de création de la métadonnée
* Date de dernière modification de la métadonnée
* Date de création de la donnée
* Date de dernière modification de la donnée



