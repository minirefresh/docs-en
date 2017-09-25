# quickStart

## Install

### NPM

```js
npm install minirefresh
```

[https://www.npmjs.com/package/minirefresh](https://www.npmjs.com/package/minirefresh)

### GIT

```js
git clone git://github.com/minirefresh/minirefresh.git
```

[https://github.com/minirefresh/minirefresh](https://github.com/minirefresh/minirefresh)

## Import

```html
<link rel="stylesheet" href="xxx/minirefresh.css" />
<script type="text/javascript" src="xxx/minirefresh.js"></script>
```

### `require`引入

```js
// support NPM and UMD
var MiniRefreshTools = require('xxx/minirefresh.js');
require('xxx/minirefresh.css');
```

### `import`引入

```js
// debug:.js   dist:.min.js
import MiniRefreshTools from 'minirefresh';
import 'minirefresh/dist/debug/minirefresh.css'
```

## HTML Layout

```html
<!-- do not modify "minirefresh-xxx" -->
<div id="minirefresh" class="minirefresh-wrap">
    <div class="minirefresh-scroll">        
    </div>
</div>
```

## Initial

```js
// MiniRefresh is a global variable
var miniRefresh = new MiniRefresh({
    container: '#minirefresh',
    down: {
        callback: function() {
            // pulldown event
        }
    },
    up: {

        callback: function() {
            // pullup event
        }
    }
});
```

### End Refresh

```js
// end pulldown
miniRefresh.endDownLoading();
```

```js
// end pullup
// true: no more data
// false: can still load more
miniRefresh.endUpLoading(true);
```

### More

For more detail, refer to the official documentation