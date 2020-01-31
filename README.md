# Vanilla JS - Magic Line Navigation
original idea: https://css-tricks.com/jquery-magicline-navigation/

## Usage:
```javascript
var myMagicLine = new magicLine(
  document.querySelectorAll('.floating-line-menu'),
  {
    navElements: 'a',                           // navigation element selector
    mode: 'line',                               // line or pill
    lineStrength: 2,                            // Thickness of the line
    lineClass: 'magic-line',                    // Classname to add to the line element
    wrapper: 'div',                             // the node that's being created as an element wrapper
    animationCallback: function (el, params) {  // might be either null or a callback function
      animationLibrary({
        targets: el,
        left: params.left,
        top: params.top,
        width: params.width,
        height: params.height
      });
    }
  }
);
myMagicLine.init();
```
## This is how it looks like:
![Alt text](https://raw.githubusercontent.com/basticodes/Vanilla-JS-Magic-Line-Navigation/master/demo/screenshot.PNG)

## Options
| Option            | Value                                                         | Default         |
| ----------------- |---------------------------------------------------------------|-----------------|
| navElements       | a query Selector, you can even define multiple like 'a, span' | 'a'             |
| mode              | might be either 'line' or 'pill'                              | 'line'          |
| lineStrength      | thickness of your line in px                                  | 2               |
| lineClass         | The classname of the floating-line element                    | 'magic-line'    |
| wrapper           | DOMNode to be inserted as a wrapper                           | 'div'           |
| animationCallback | a callBack Function used for animation                        | null            |

Check out the [Demo](https://codepen.io/bastian_fiessinger/full/MWYMWJN) on Codepen
