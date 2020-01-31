# Vanilla JS - Magic Line Navigation
original idea: https://css-tricks.com/jquery-magicline-navigation/

## Browser Support
![Chrome](https://camo.githubusercontent.com/26846e979600799e9f4273d38bd9e5cb7bb8d6d0/68747470733a2f2f7261772e6769746875622e636f6d2f616c7272612f62726f777365722d6c6f676f732f6d61737465722f7372632f6368726f6d652f6368726f6d655f34387834382e706e67) | ![Firefox](https://camo.githubusercontent.com/6087557f69ec6585eb7f8d7bd7d9ecb6b7f51ba1/68747470733a2f2f7261772e6769746875622e636f6d2f616c7272612f62726f777365722d6c6f676f732f6d61737465722f7372632f66697265666f782f66697265666f785f34387834382e706e67) | ![IE](https://camo.githubusercontent.com/4b062fb12353b0ef8420a72ddc3debf6b2ee5747/68747470733a2f2f7261772e6769746875622e636f6d2f616c7272612f62726f777365722d6c6f676f732f6d61737465722f7372632f617263686976652f696e7465726e65742d6578706c6f7265725f392d31312f696e7465726e65742d6578706c6f7265725f392d31315f34387834382e706e67) | ![Edge](https://camo.githubusercontent.com/826b3030243b09465bf14cf420704344f5eee991/68747470733a2f2f7261772e6769746875622e636f6d2f616c7272612f62726f777365722d6c6f676f732f6d61737465722f7372632f656467652f656467655f34387834382e706e67) | ![Opera](https://camo.githubusercontent.com/96d2405a936da1fb8988db0c1d304d3db04b8a52/68747470733a2f2f7261772e6769746875622e636f6d2f616c7272612f62726f777365722d6c6f676f732f6d61737465722f7372632f6f706572612f6f706572615f34387834382e706e67) | ![Safari](https://camo.githubusercontent.com/6fbaeb334b99e74ddd89190a42766ea3b4600d2c/68747470733a2f2f7261772e6769746875622e636f6d2f616c7272612f62726f777365722d6c6f676f732f6d61737465722f7372632f7361666172692f7361666172695f34387834382e706e67)
--- | --- | --- | --- | --- |
/ ✔ | / ✔ | 10+ ✔ | / ✔ | / ✔ | / ✔ |

To get IE Support below Version 10 use a Classlist Polyfill. 

## Usage
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
## This is how it looks like
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
