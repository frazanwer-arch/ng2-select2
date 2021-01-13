# Angular wrapper for Select2 (ng2-select2)

[![npm version](https://badge.fury.io/js/ng2-select2.svg)](https://badge.fury.io/js/ng2-select2) [![MIT Licence](https://badges.frapsoft.com/os/mit/mit.svg?v=103)](https://opensource.org/licenses/mit-license.php)

For Angular version 2.x.x and up


## Prerequisites

For this plugin to work you need to add two javascript libraries to your project
- [Jquery](https://jquery.com/download/)
- [Select2](https://select2.github.io/)

First option and **preferred one** is to add libraries to your package builder.
- You can find example of how to add libraries to the Angular CLI 

Second option is to include libraries into your html head:

```
<head>
  <meta charset="utf-8">
  <title>Ng2Select2Demo</title>
  <base href="/">

  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="icon" type="image/x-icon" href="favicon.ico">
  <script src="./assets/jquery.min.js"></script>		
  <script src="./assets/select2.min.js"></script>
</head>
```

## Installation

Add package to your project `npm i -S ng2-select2` (this will save package to your `dependencies` in `package.json`)


## Basic implementation

1) Add declaration to [NgModule](https://github.com/frazanwer-arch/ng2-select2-demo/blob/master/src/app/app.module.ts#L35)
```
import { Select2Module } from 'ng2-select2';

@NgModule({
  imports: [
    ....,
    Select2Module
  ],
  ...
})
```

2) Add it to your [template](https://github.com/frazanwer-arch/ng2-select2-demo/blob/master/src/app/demos/basic/basic.component.html#L3). You need to define at least `data` as `@Input`.

Example of `exampleData` can be found [here](https://github.com/frazanwer-arch/ng2-select2-demo/blob/master/src/app/demos/basic/basic.component.ts#L13).

```
<select2 [data]="exampleData"></select2>
```


## Options

### Inputs
* **data** `Array<Select2OptionData>`: Data used for generating select 2 - [inferface definition](https://github.com/frazanwer-arch/ng2-select2/blob/master/lib/ng2-select2.interface.ts#L1)
* **value** `string`: Default value for select 2
* **cssImport** `boolean`: Disable or enable default style for select 2, default value is `false`
* **width** `string`: Set width for the input, default value is `resolve`
* **disabled** `boolean`: Disable select2, default value is `false`
* **options** `Select2Options`: Set options for select 2, [all available options] 
### Outputs
* **valueChanged** `string`: Emitted when value changes in select 2 drop down 


## Demo

You can view a live demo [here](https://frazanwer-arch.github.io/ng2-select2-demo) or check out [demo repo](https://github.com/frazanwer-arch/ng2-select2-demo/) where you can find source of this demo created with Angular CLI.
