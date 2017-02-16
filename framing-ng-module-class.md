# FramingNgModule class



## Constructor



### constructor(ngModule?: NgModule)

#### Parameters

* ngModule?: NgModule

#### Returns

* [FramingNgModule](framing-ng-module-class.md)



## Public Methods



### ngModule(ngModule?: NgModule): FramingNgModule

#### Parameters

* ngModule?: NgModule

#### Returns

* [FramingNgModule](framing-ng-module-class.md)



### child(child: Route, forRoute: Route = {}): FramingNgModule

Add a child route. Adds to '' route by default

#### Parameters

* child: Route
* forRoute: Route = {}

#### Returns

* [FramingNgModule](framing-ng-module-class.md)

#### Example

``
@NgModule(Framing
  .ngModule()
  .child({ path: 'products', loadChildren: './products/index#ProductsModule' })
  .frame()
 ``
