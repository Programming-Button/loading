# [Loading Code](https://sourceb.in/CRfkoUBptt)

```
Loading Code HTML, CSS, JavaScript.
```

## index.html:
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>Loading</title>
        <link href="style.css" rel="stylesheet" type="text/css" />
    </head>
    <body>
        <div class="loading">
            <div class="loading-circle"></div>
        </div>
        
        <div class="body">
            <!-- The codes must be written inside this code. -->
            
            TEXT
        </div>
        
        <script src="script.js"></script>
    </body>
</html>
```

## style.css: 
```css
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600;700;800;900&display=swap');

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}

.loading {
    width: 100vw;
    height: 100vh;
    overflow: hidden;
    background: #fff;
    position: absolute;
}

.loading-circle {
    width: 100px;
    height: 100px;
    border: 5px solid #d5d5d5;
    border-top: 5px solid #5865f2;
    position: absolute;
    margin: auto;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    border-radius: 50%;
    animation: spin 0.5s linear infinite;
}

@keyframes spin {
    100% {
        transform: rotate(360deg);
    }
}

.body {
    display: none;
}
```

## script.js:
```js
const loading = document.querySelector('.loading');
const body = document.querySelector('.body');

window.addEventListener('load', function() {
    setTimeout(function() {
        loading.style.display = 'none';
        body.style.display = 'block';
    }, 1000);
});
```
