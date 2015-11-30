# Matinale NG2

## Migrer une application AngularJs existante en Angular2. Est-ce possible?

### Différentes approche

- Refonte: On casse tout et on réécrit
- Downgrade Angular 2: Utilisation de composants NG2 dans une application AngularJs
- Upgrade AngularJS: Utilisation de composants AngularJS dans une application Angular2

Le choix parmis ces solutions est à contextualiser. Pas de réponse absolue si ce n'est dans le cas d'une application "de petite taille". Dans ce cas là -> Refonte!

### Contexte

Une application existante en AngularJs: Un blog.
Certains composants sont partagés avec d'autre application (le composant de directive)

```html
<zn-comment 
  data="comments" <!-- Array containing comments -->
  on-activate="displayComent()" <!-- Function to execute when comment module activate -->
  on-send="comment(newComment)"> <!-- Function to execute when new comment created -->
</zn-comment>
```


### Downgrade 

Le composant de commentaire à été upgradé en Angular2 pour un autre projet. Des fonctionnalités intéressantes ont été rajoutées. L'application de blog doit en bénéficier.
