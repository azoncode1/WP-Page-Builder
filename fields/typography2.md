# Typography2 
A Typography Styling Input Field (Full Settings)

## Parameters
Parameter | Type | Value
--- | --- | ---
type | `required` | Predefined String (typography2)
title | `optional` | String
desc | `optional` | String
std | `optional` | Array
selector | `optional` | String / Array
tab | `optional` | String(style)
section | `optional` | String

## Return
Always return `object`

## Example
```php
'addon_typography2' => array(
	'type' => 'typography2',
	'title' => __('Typography2 Field','your-textdomain'),
	'std' => array(
		    'textDecoration' => 'underline',
		    'fontStyle' => 'italic',
		    'textTransform' => 'uppercase',
		    'fontWeight' => 700
		),
	'selector' => '{{SELECTOR}} .example-fontstyle'
)
```
Support 'selector' parameters.


## Controls
### PHP
Inside the `rander()` method-
```php
echo '<div>'.$data['settings']['addon_typography2']['fontStyle'].'</div>';
echo '<div class="example-fontstyle">Example Fontstyle</div>';
```

### JS Template
Inside the `getTemplate()` method-
```js
<div>{{data.addon_typography2.fontStyle}}</div>
<div class="example-fontstyle">Example Fontstyle</div>
```
