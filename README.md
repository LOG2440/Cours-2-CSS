# Exemples de CSS

Cet entrepôt contient un ensemble d'exemples simples des différentes notions vues sur le langage **CSS**.

## [selectors](./selectors/)

Contient plusieurs exemples de sélecteurs CSS. Tous les sélecteurs sont disponibles dans le fichier [`style.css`](./selectors/style.css). 

Par défaut, toutes les règles sont en commentaire : vous pouvez les sortir du bloc de commentaires pour voir leur effet sur le code HTML fourni.

Note : certaines règles différentes qui s'appliquent sur les mêmes éléments ont des spécificités différentes et vous ne verrez qu'une des règles appliquées. Voir la section [specificity](#specificity) pour des exemples de spécificité.
## [specificity](./specificity/)

Contient plusieurs exemples de sélecteurs CSS et leur spécificité. Tous les sélecteurs sont disponibles dans le fichier [`style.css`](./specificity/style.css). 

Les règles sont triées en ordre descendant de spécificité dans le document, mais ceci n'est pas une obligation. Les règles CSS sont triées automatiquement après que le navigateur ait lu le fichier au complet.

Notez que le sélecteur `body#home div#warning p.message` n'affecte pas le HTML fourni puisqu'il n'y a aucun élément qui correspond à ce sélecteur.

## [cascade](./cascade/)

Contient un exemple de cascade de règles et héritage en CSS. Tous les sélecteurs sont disponibles dans le fichier [`style.css`](./cascade/style.css). 

Notez que la taille de l'élément `<p>` est contrôlée par les règles CSS affectant son parent `<div>` ayant l'id `wrap`.

## [position](./position/)

Contient différents exemples de positionnement à l'aide de l'attribut `position` ainsi que l'utilisation de positionnement flottant dans [`float.html`](./position/float.html).

## [layout](./layout/)

Contient des exemples de la gestion du débordement du contenu d'un élément.

Le fichier [percentage.html](./layout/percentage.html) contient un exemple des problèmes potentiels de l'utilisation de pourcentages pour des éléments ayant des `margin` et `padding`, ex : `width : 100%`.

Le fichier [box-sizing.html](./layout/box-sizing.html) contient un exemple de l'utilisation de la propriété `box-sizing` pour contrôler la taille d'un élément en incluant ou excluant les marges et les bordures.

Le fichier [overflow.html](./layout/overflow.html) contient des exemples de l'utilisation de l'attribut `overflow` pour contrôler l'affichage du contenu qui dépasse la taille de son parent.

## [flexbox](./flexbox/)

Contient un exemple de boîte flexible (_flexbox_) CSS. Le fichier [`style.css`](./flexbox/style.css) contient plusieurs variants des manipulations possibles d'un _flexbox_ : 
- taille relative des éléments de la boite
- ordonnancement indexé des éléments de la boîte 

L'exemple de [requêtes média](./media_query/style.css) utilise également une boîte flexible dont le contenu est modifié lors d'un changement de la résolution de l'écran.

## [grid](./grid/)

Contient plusieurs exemples exemple de grille (_grid_) CSS.

### [basic_grid](./grid/basic_grid/)

Exemple de base d'une grille de 2 colonnes et 2 rangées (calculé automatiquement).

### [grid_position](./grid/grid_position/)

Exemple de positionnement variable dans une grille de 3 colonnes et 2 rangées. 
Les éléments `<div>` dans la grille sont placés à l'aide des attributs `grid-row` et `grid-column`.
La 2e colonne est toujours plus grande que les 2 autres et occupe 2/3 de la largeur de l'écran grâce à la définition de départ suivante :
```css
grid-template-columns: 0.25fr 1fr 0.25fr;
````

Les lignes directrices commencent à 1 et une valeur négative indique un décompte à partir de la dernière ligne directrice (-1). Dans le cas d'une grille de 3 colonnes, les valeurs suivantes représentent la même position de départ (début de la 3e colonne):
```css
grid-column: -2;
grid-column: 3;
```

### [grid_template_areas](./grid/grid_template_areas/)

Exemple de positionnement variable à travers des zones nommées (_grid areas_). Cet exemple utilise la même structure HTML que [grid_position](#gridposition) et possède le même affichage.

Les zones nommées sont définies lors de la définition de la grille et référées à travers son nom dans les enfants de la grille :
```css
grid-template-areas: "un deux trois"
                     "un deux trois"
                     "un quatre quatre";
```

## [media_query](./media_query/)

Contiens un exemple de requêtes média basées sur la taille de l'écran en pixels. Les deux requêtes sont définies dans [style.css](./media_query/style.css) et utilisent la propriété `min-width` comme contrainte d'application.

Sous le seuil de 400px, les 4 enfants de l'élément `<div class="wrapper">` sont affichés dans une seule colonne.

La première requête média (`min-width: 400px`) modifie l'affichage pour placer les 2 éléments `<aside>` sur la même ligne.

La deuxième requête média (`min-width: 600px`) modifie l'affichage pour placer l'élément `<main>`. entre les 2 éléments `<aside>` sur la même ligne. `<main>` occupe également 60% de l'espace grâce à l'attribut `flex` qui est modifié par la requête.

# VSCode et affichage de spécificité

Si vous utilisez VSCode, vous pouvez voir la structure HTML qui correspond à un sélecteur ainsi que sa spécificité. Vous n'avez qu'à placer votre souris par-dessus le sélecteur et vous aurez une modale avec cette information. Notez que la spécificité est toujours calculée sur 3 chiffres : le 1er chiffre est toujours **0**.