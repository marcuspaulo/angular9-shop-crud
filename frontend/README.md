# Angular 9 simple CRUD.

# Create project
```sh
$ ng new frontend --minimal
```
- --minimal=true|false: When true, creates a project without any testing frameworks. (Use for learning purposes only.)
- --prefix=prefix	- The prefix to apply to generated selectors for the initial project. Default: app Aliases: -p

# Start project 
```sh
$ ng serve
```
# Configuration 

### Set inlineTemplate and inlineStyle to false. Separated files.
```json
"schematics": {
        "@schematics/angular:component": {
          "inlineTemplate": false,
          "inlineStyle": false,
          "skipTests": true
        },
```
# Install Angular Material Design
```sh
$ ng add @angular/material
```
# Create New Component Header
```sh
$ ng g c components/template/header
```

# Create new Component Footer
```sh
$ ng g c components/template/footer
```

# Create new Component Nav (Navigation)
```sh
$ ng g c components/template/nav
```

# Directives:
### Structural Directives * (before the element), eg. *ngIf or *ngFor

# Angular
### One way Data Binding []
```html
  <input [value]="nome">
```

### Two way Data Binding [()]
```html
  <input [(value)]="nome">
```

# Create Component View Home
```sh
$ ng g c views/home
```

# Create Component View Product-CRUD
```sh
$ ng g c views/product-crud
```
# Create Directive Red
```sh
$ ng g d directives/red
```

# Create Component Product-Create
```sh
$ ng g c components/product/product-create
```

# Create Service Product
```sh
$ ng g s components/product/product
```
# Create component
```app.module.ts
import { FormsModule } from '@angular/forms';
import { MatFormFieldModule } from '@angular/material/form-field';
import { MatInputModule } from '@angular/material/input';
```

# Create Component  Product-Read
```sh
$ ng g c components/product/product-read
``` 

# Create Material Angular Components - Schematics
[!Schematics](https://material.angular.io/guide/schematics)

# Create Schematics Table 
```sh
$ ng generate @angular/material:table components/product/product-read-material
```

# Internalization - app.module.ts
```js
  import { NgModule, LOCALE_ID } from '@angular/core';
  import localePt from '@angular/common/locales/pt';
  import { registerLocaleData } from '@angular/common';

  registerLocaleData(localePt);
  ...
  providers: [{
    provide: LOCALE_ID,
    useValue: 'pt-BR'
  }],
```

# Create new Component Product Update
```sh
$ ng g c components/product/product-update
```

# Create new Component Product Delete
```sh
$ ng g c components/product/product-delete
```

# Create new Service HeaderService
```sh
$ ng g s components/template/header/header
```

# Build to production
```sh
$ ng build frontend -c production
```