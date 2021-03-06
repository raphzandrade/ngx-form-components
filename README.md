# Angular Form Components Collection

[LIVE DEMO](https://johnbra.github.io/ngx-form-components/)

This is a collection of simple, stylable form components, which (should be) working on all relevant browsers. It is supposed to bridge the issue of some of the HTML 5 inputs (like type: "range") not working on select platforms (e.g. iOS).

Right now this lib only includes the range input component. The plan is to add more components if needed. Feel free to open an issue for component/feature requests or contribute with a pull request.

## Quick Start

### Angular Version
This library was built with the Angular CLI 7.1.0, you may run into issues using this with a lower version.

### Installation
[![ngx-form-components](https://nodei.co/npm/ngx-form-components.png)](https://www.npmjs.com/package/ngx-form-components)

`npm i ngx-form-components --save`

### Import the module

```ts
import { NgxFormComponentsModule } from 'ngx-form-components';

@NgModule({
  imports: [
    // ...
    NgxFormComponentsModule,
    ...
  ]
})
```

### Add the desired component to you html file

```html
<form class="your-form">
  ...
  <nfc-range-input></nfc-range-input>
  ...
</form>
```

## API

### Range input

#### Properties

* `min: number` optional, **minimum range value** - `default value = 0`
* `max: number` optional, **maximum range value** - `default value = 100`
* `step: number` optional, **slider steps (e. g. 0->5->10 ..)** - `default value = 1`
* `toolTips: boolean` optional, **enables/disables number over slider** - `default value = false`
* `minRangeSlider: boolean` optional, **enables/disables left slider, if minRangeSlider = false, minimum is set as min slider value** - `default value = false`
* `defaultRange: number || [number, number]` optional, **sets the default value for the slider** - `default value = [min, max/2]`
* `highlightBarCssClass: string` optional, **css class for the highlightbar component**
* `barCssClass: string` optional, **css class for the bar component**
* `sliderButtonCssClass: string` optional, **css class for the slider button component**

*Hint: if you want to apply a custom style to your bar, highlight bar or slider button, you need to disable the view encapsulation for the specific component that includes your css class:*

```ts
import {Component, ViewEncapsulation} from '@angular/core';

@Component({
  selector: /* your app selector */,
  templateUrl: /* your html template */,
  styleUrls: /* your style sheets */,
  
  encapsulation: ViewEncapsulation.None, // <-- this
})
export class AppComponent {
  // ...
}
```

#### Example usage

See [here](https://github.com/JohnBra/ngx-form-components/blob/master/src/app/app.component.html)

## License

MIT © Jonathan Braat
