# test-es6-babel-system

Next experimental application which contains some tools:

 - **ECMAScript 6** (as new syntax in JavaScript)
 - **Babel.js** as parse and transpiler ES6 to ES5
 - **System.js** as universal dynamic module loader

## Steps

1. Install globally `jspm`.
2. Setup project:

    ```
    jspm init
    ```
answer for several question - probably always hit ENTER.
3. Include `jspm_packages/system.js` to `index.html` file.
4. Create `<script>` tag with:

    ```javascript
    System.transpiler = 'babel';
    System.import('lib/main');
    ```

5. Create `lib/main.js` file with content:

    ```javascript
    import {Game} from 'lib/Game'

    var g = new Game();
    console.debug(g.toString());
    ```

6. Create `lib/Game.js` file with content:

    ```javascript
    export class Game {
        constructor() {
            console.log('Game#constructor');
        }

        toString() {
            return '[object Game]'
        }
    }
    ```
7. Open main directory in browser! ;)

## Setup current project

```
git clone https://github.com/piecioshka/test-es6-babel-system.git
jspm install
```
