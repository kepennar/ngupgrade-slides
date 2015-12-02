<!-- .slide: data-background="#8BC34A" -->

Upgrade composants angular 1 dans angular 2 
```js
@Component({
 selector: 'ng2',
 template: `
    ng2 template: 
    <greet salutation="Hello" [name]="world">text</greet>
 `
 // Upgrade d'une directive Angular1
 directives: [adapter.upgradeNg1Component('greet')]
})
class Ng2 {
}
```
