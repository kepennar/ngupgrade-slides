<!-- .slide: data-background="#8BC34A" -->

Downgrade composants angular 2 dans angular 1 
```js
// Downgrade du composant Ng2 dans un module Angular 1
var module = angular.module('example', []);
module.directive('greet', adapter.downgradeNg2Component(Ng2));

// Bootstrap de l'application Angular 1 avec l'adapter
adapter.bootstrap(document.body, ['example'])
```
