## ngForward
```js
@Component({
  selector: 'app',
  bindings: [TestService, "ui.router"]
})
@View({
  directives: [InnerApp],
  template: `<inner-app (evt)="app.onIncrement()" [message]="app.message1"></inner-app>`
})

class AppCtrl{
  constructor(){
    this.triggers = 0;
    this.message1 = 'Hey, inner app, you can not change this';
  }

  onIncrement(){
    this.triggers++;
  }
}

bootstrap(AppCtrl);
```