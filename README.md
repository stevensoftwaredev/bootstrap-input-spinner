# bootstrap-input-spinner

A Bootstrap 4 / jQuery plugin for feet and inches.

## Features

- Mobile friendly and responsive
- Internationalized number formatting
- Automatically changes value when holding button
- Boosts value change when holding button longer

## Installation

just download this repository and include `src/InputSpinner.js`.

**No extra css needed**, only Bootstrap 4 and jQuery.

## Usage

```html
<input type="number" value="50" min="0" max="100" step="10"/>
<script>
    $("input[type='number']").FeetInchesInputSpinner();
	$(function(){
		$(".input-group-spinner").find("input:text").prop('readonly', true);  
	})    
</script>
```

### Syntax

#### HTML

Uses the following tag-attributes:

- min
- max
- step
- data-decimals

```html
<input type="number" value="4.5" data-decimals="2" min="0" max="9" step="0.1"/>
```

#### JavaScript

```javascript
$(element).FeetInchesInputSpinner(config);
```

default config is:

```javascript
const config = {
    decrementButton: "<strong>-</strong>", // button text
    incrementButton: "<strong>+</strong>", // ..
    groupClass: "input-group-spinner", // css class of the input-group
    buttonsClass: "btn-outline-secondary",
    buttonsWidth: "2.5em",
    textAlign: "center",
    autoDelay: 500, // ms holding before auto value change
    autoInterval: 100, // speed of auto value change
    boostThreshold: 15, // boost after these steps
    boostMultiplier: 4,
    locale: null // the locale for number rendering; if null, the browsers language is used
};
```

