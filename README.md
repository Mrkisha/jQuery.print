# jQuery Print Plugin

jQuery.print is a plugin for printing specific parts of a page

## Usage

Include it in your HTML after importing jQuery, like:
	<script type="text/JavaScript" src="./js/libs/jquery.print.js" />
	
Use it like:

	$("#myElementId").print(/*options*/);
	
or

	$.print("#myElementId" /*, options*/);
	
You can submit the options object like:

	$("#myElementId").print({
		addGlobalStyles : true,
		stylesheet : null,
		rejectWindow : true,
		noPrintSelector : ".no-print",
		iframe : true,
		append : null,
		prepend : null
	});
	
Currently this plugin supports the following options:

####globalStyles

 - Default: `true`  
 - Acceptable-Values: Boolean  
 - Function: Whether or not the styles from the parent document should be included

####mediaPrint

 - Default: `false`  
 - Acceptable-Values: Boolean  
 - Function: Whether or not link tags with media='print' should be included; Over-riden by the `globalStyles` option

####stylesheet

 - Default: `null`
 - Acceptable-Values: URL-string
 - Function: URL of an external stylesheet to be included

####rejectWindow

 - Default: `true`
 - Acceptable-Values: Boolean
 - Function: Whether the `document` object should be used intead of `window`

####noPrintSelector

 - Default: `".no-print"`
 - Acceptable-Values: Any valid `jQuery-selector`
 - Function: A selector for the items that are to be excluded from printing

####iframe

 - Default: `true`, creates a hidden iframe if no-vaild iframe selector is passed
 - Acceptable-Values: Any valid `jQuery-selector` or Boolean
 - Function: Whether to print from an iframe instead of a pop-up window; can take the `jQuery-selector` of an existing iframe as value

####append/prepend

 - Default: `null`
 - Acceptable-Values: Any valid `jQuery-selector` or HTML-text
 - Function: Adds custom HTML before (prepend) or after (append) the selected content

## Tested on

### jQuery
* [jQuery](http://jquery.com/) v. 1.7.2

### Browser Support (tested versions)
* Google Chrome - v 20

## License
[CC-BY](http://creativecommons.org/licenses/by/3.0/).

## Live at
[jsFiddle](http://jsfiddle.net/5V24U/27/)

Do let me know if you are using it and would like to be featured here