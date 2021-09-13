# Exemples de CSS

Cet entrepôt contient un ensemble d'exemples simples des différentes notions vues sur le **CSS**.

## selectors

Contient plusieurs exemples de sélecteurs CSS. Tous les sélecteurs sont disponibles dans le fichier `style.css`. Par défaut, tous les règles sont en commentaire : vous pouvez les sortir du bloc de commentaires pour vour leur effet sur le code HTML fourni.

## specificity

Contient plusieurs exemples de sélecteurs CSS et leur spécificité. Tous les sélecteurs sont disponibles dans le fichier `style.css`. Notez que le sélecteur `body#home div#warning p.message` n'affecte pas le HTML fourni puisqu'il n'y a aucun élément qui correspond à cet sélecteur.

## cascade

Contient un exemple de cascade de règles et héritage en CSS. Tous les sélecteurs sont disponibles dans le fichier `style.css`. Notez que la taille de l'élément `<p>` est contrôlée par les règles CSS affectant son parent `<div>` ayant l'id `wrap`.

## flexbox

Contient un exemple de boîte flexible (_flexbox_) CSS. Le fichier `style.css` contient plusieurs variants des manipulations possibles d'un _flexbox_ : 
- taille relative des éléments de la bôite
- ordonnancement indexé des éléments de la boîte 

## grid

Contient un exemple de grille (_grid_) CSS.

### VSCode

Si vous utilisez VSCode, vous pouvez voir la structure HTML qui correspond à un sélecteur ainsi que sa spécificité. Vous n'avez qu'à placer votre souris par dessus le sélecteur et vous aurez une modale avec cette information. Notez que la spécificité est toujours calculée sur 3 chiffres : le 1er chiffre est toujours **0**.