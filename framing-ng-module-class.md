# FramingNgModule class

* Constructor
 * [constructor(ngModule)](#constructorngmodule-ngmodule)
* Public Methods
 * [ngModule(ngModule)](#ngmodulengmodule-ngmodule-framingngmodule)
 * [child(child, forRoute)](#childchild-route-forroute-route---framingngmodule)
 * [children(children)](#childrenchildren-route-framingngmodule)
 * [component(component, config)](#componentcomponent-config-framingngmodule)
 

## Constructor



### constructor(ngModule?: NgModule)

#### Parameters

* ngModule?: [NgModule](https://angular.io/docs/ts/latest/api/core/index/NgModule-interface.html)

#### Returns

* [FramingNgModule](framing-ng-module-class.md)



## Public Methods



### ngModule(ngModule?: NgModule): FramingNgModule

#### Parameters

* ngModule?: [NgModule](https://angular.io/docs/ts/latest/api/core/index/NgModule-interface.html)

#### Returns

* [FramingNgModule](framing-ng-module-class.md)



### child(child: Route, forRoute: Route = {}): FramingNgModule

Add a child route. Adds to '' route by default

#### Parameters

* child: [Route](https://angular.io/docs/ts/latest/api/router/index/Route-interface.html)
* forRoute: [Route](https://angular.io/docs/ts/latest/api/router/index/Route-interface.html) = {}

#### Returns

* [FramingNgModule](framing-ng-module-class.md)

#### Example

Basic usage

```typescript
@NgModule(Framing
  .ngModule()
  .child({ path: 'products', loadChildren: './products/index#ProductsModule' })
  .frame())
 ```

Output

```typescript
@NgModule({
  imports: [
    CommonModule,
    RouterModule,
    RouterModule.forRoutes([
      {
        path: '',
        children: [
          { path: 'products', loadChildren: './products/index#ProductsModules' },
        ],
      }
    ])
  ],
})
```

### children(children: Route[]): FramingNgModule

Adds to imports
Adds to route

#### Parameters

* children: [Route](https://angular.io/docs/ts/latest/api/router/index/Route-interface.html)[]

#### Returns

* [FramingNgModule](framing-ng-module-class.md)

#### Example

Basic usage

```typescript
@NgModule(Framing
  .ngModule()
  .children([
    { path: 'products', loadChildren: './products/index#ProductsModule' },
    { path: 'orders', loadChildren: './orders/index#OrdersModule' },
  ])
  .frame())
 ```
 
 
 
### component(component: any, config?: FramingComponentConfig): FramingNgModule
 
Adds to declarations
Adds to exports
Adds as component on route
Optional noDeclare parameter can be set to true to prevent the component from being declared if it is already declared in another module

#### Parameters

* component: any
* config?: [FramingComponentConfig](framing-component-config-interface.md)

#### Returns

* [FramingNgModule](framing-ng-module-class.md)

#### Example

Basic usage

```typescript
@NgModule(Framing
  .ngModule()
  .component(MyViewComponent)
  .frame())
 ```
