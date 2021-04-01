# eslint-plugin-p5js

Environment globals for p5.js

## Installation

You'll first need to install [ESLint](http://eslint.org):

```
$ npm i eslint --save-dev
```

Next, install `eslint-plugin-p5js`:

```
$ npm install eslint-plugin-p5js --save-dev
```


## Usage

Add `p5js` to the plugins section of your `.eslintrc` configuration file. You can omit the `eslint-plugin-` prefix. Then add the environment `p5js/p5` to the env section. To add the exception for `setup`, `draw`, and other functions that don't get explicitly called, add `plugin:p5js/p5` to the extends section. All of these additions are shown here:

```json
{
    "plugins": [
        "p5js"
    ],

    "env": {
        "browser": true,
        "es2021": true,
        "p5js/p5": true
    },
    
    "extends": [
        "eslint:recommended",
        "plugin:p5js/p5"
    ]
}
```

This plugin does not provide any linting rules (other than `no-unused-vars`, which it only does to add an exception to that rule). You'll need an additional plugin or configuration to add rules to lint, like `eslint:recommended` or `eslint-config-standard`. The former is included in the above example.

## Example
Before:

```
   1:1   warning  Unexpected var, use let or const instead   no-var
   2:1   warning  Unexpected var, use let or const instead   no-var
   4:1   warning  Unexpected var, use let or const instead   no-var
   5:1   warning  Unexpected var, use let or const instead   no-var
   7:1   warning  Unexpected var, use let or const instead   no-var
   9:10  error    'preload' is defined but never used        no-unused-vars
  10:13  error    'loadImage' is not defined                 no-undef
  11:12  error    'loadImage' is not defined                 no-undef
  14:10  error    'setup' is defined but never used          no-unused-vars
  15:3   error    'createCanvas' is not defined              no-undef
  16:7   error    'width' is not defined                     no-undef
  20:10  error    'mouseClicked' is defined but never used   no-unused-vars
  20:22  error    Missing space before function parentheses  space-before-function-paren
  20:24  error    Missing space before opening brace         space-before-blocks
  21:10  error    'badvar' is not defined                    no-undef
  39:10  error    'draw' is defined but never used           no-unused-vars
  48:7   error    'keyIsDown' is not defined                 no-undef
  48:17  error    'UP_ARROW' is not defined                  no-undef
  52:7   error    'keyIsDown' is not defined                 no-undef
  52:17  error    'LEFT_ARROW' is not defined                no-undef
  56:7   error    'keyIsDown' is not defined                 no-undef
  56:17  error    'RIGHT_ARROW' is not defined               no-undef
  62:11  error    'height' is not defined                    no-undef
  65:9   error    'height' is not defined                    no-undef
  68:3   error    'image' is not defined                     no-undef
  70:3   error    'image' is not defined                     no-undef
  73:5   error    'fill' is not defined                      no-undef
  74:5   error    'textSize' is not defined                  no-undef
  75:5   error    'text' is not defined                      no-undef
```

After:

```
   1:1   warning  Unexpected var, use let or const instead   no-var
   2:1   warning  Unexpected var, use let or const instead   no-var
   4:1   warning  Unexpected var, use let or const instead   no-var
   5:1   warning  Unexpected var, use let or const instead   no-var
   7:1   warning  Unexpected var, use let or const instead   no-var
  20:22  error    Missing space before function parentheses  space-before-function-paren
  20:24  error    Missing space before opening brace         space-before-blocks
  21:10  error    'badvar' is not defined                    no-undef

```
