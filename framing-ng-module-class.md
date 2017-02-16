# FramingNgModule class



## Constructor



### constructor(ngModule?: [NgModule](https://angular.io/docs/ts/latest/api/core/index/NgModule-interface.html))

#### Parameters

* ngModule?: [NgModule](https://angular.io/docs/ts/latest/api/core/index/NgModule-interface.html)

#### Returns

* [FramingNgModule](framing-ng-module-class.md)



## Public Methods



### ngModule(ngModule?: NgModule): [FramingNgModule](framing-ng-module-class.md)

#### Parameters

* ngModule?: NgModule

#### Returns

* [FramingNgModule](framing-ng-module-class.md)



### child(child: [Route](https://angular.io/docs/ts/latest/api/router/index/Route-interface.html), forRoute: [Route](https://angular.io/docs/ts/latest/api/router/index/Route-interface.html) = {}): [FramingNgModule](framing-ng-module-class.md)

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
  .frame()
 ```
