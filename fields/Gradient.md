
# Gradient
A Gradient Color Input Field

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (gradient)
title | `optional` | String
desc | `optional` | String
clip | `optional` | Boolean ( Default: false )
std | `optional` | Array

## Return
Always return `object`

## Example
```php
'addon_gradient' => array(
    'type' => 'gradient',
    'title' => 'Gradient Field',
    'std' => array(
		'bgFirst' => '#ff0000',
		'bgSecond' => '#ffff00',
		'degValue' => 90,
		'direction' => 90,
		'startPosition' => 50,
		'endPosition' => 90,
		'type' => 'linear', 
		'radialValue' => 'center'
	    ),
    'selector' => '{{SELECTOR}} .example-gradient'
)
```

`clip` parameters is used for foreground color.

## Controls
### PHP
Inside the `rander()` method
```php
echo '<div>'.$settings["addon_gradient"]["bgFirst"].'</div>';
```

### JS Template
Inside the `getTemplate()` method-
```js
<div>{{data.addon_gradient.bgFirst}}</div>
<div>{{data.addon_gradient.bgSecond}}</div>
```