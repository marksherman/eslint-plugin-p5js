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

Add `p5js` to the plugins section of your `.eslintrc` configuration file. You can omit the `eslint-plugin-` prefix. Then add the environment `p5js/p5` to the env section:

```json
{
    "plugins": [
        "p5js"
    ]

    "env": {
        "browser": true,
        "es2021": true,
        "p5js/p5": true
    }
}
```

## Example
Before:

```
   1:1   warning  Unexpected var, use let or const instead  no-var
   1:12  error    Extra semicolon                           semi
   2:1   warning  Unexpected var, use let or const instead  no-var
   2:11  error    Extra semicolon                           semi
   4:1   warning  Unexpected var, use let or const instead  no-var
   4:6   error    Extra semicolon                           semi
   5:1   warning  Unexpected var, use let or const instead  no-var
   5:6   error    Extra semicolon                           semi
   7:1   warning  Unexpected var, use let or const instead  no-var
   7:19  error    Extra semicolon                           semi
   9:10  error    'preload' is defined but never used       no-unused-vars
  10:13  error    'loadImage' is not defined                no-undef
  10:45  error    Extra semicolon                           semi
  11:12  error    'loadImage' is not defined                no-undef
  11:35  error    Extra semicolon                           semi
  14:10  error    'setup' is defined but never used         no-unused-vars
  15:3   error    'createCanvas' is not defined             no-undef
  15:25  error    Extra semicolon                           semi
  16:7   error    'width' is not defined                    no-undef
  16:16  error    Extra semicolon                           semi
  17:8   error    Extra semicolon                           semi
  28:20  error    Extra semicolon                           semi
  29:18  error    Extra semicolon                           semi
  33:15  error    Extra semicolon                           semi
  36:10  error    'draw' is defined but never used          no-unused-vars
  38:29  error    Extra semicolon                           semi
  42:11  error    Extra semicolon                           semi
  45:7   error    'keyIsDown' is not defined                no-undef
  45:17  error    'UP_ARROW' is not defined                 no-undef
  46:12  error    Extra semicolon                           semi
  47:16  error    Extra semicolon                           semi
  49:7   error    'keyIsDown' is not defined                no-undef
  49:17  error    'LEFT_ARROW' is not defined               no-undef
  50:12  error    Extra semicolon                           semi
  51:18  error    Extra semicolon                           semi
  53:7   error    'keyIsDown' is not defined                no-undef
  53:17  error    'RIGHT_ARROW' is not defined              no-undef
  54:12  error    Extra semicolon                           semi
  55:19  error    Extra semicolon                           semi
  59:11  error    'height' is not defined                   no-undef
  60:12  error    Extra semicolon                           semi
  62:9   error    'height' is not defined                   no-undef
  62:15  error    Extra semicolon                           semi
  65:3   error    'image' is not defined                    no-undef
  65:23  error    Extra semicolon                           semi
  67:3   error    'image' is not defined                    no-undef
  67:22  error    Extra semicolon                           semi
  70:5   error    'fill' is not defined                     no-undef
  70:18  error    Extra semicolon                           semi
  71:5   error    'textSize' is not defined                 no-undef
  71:17  error    Extra semicolon                           semi
  72:5   error    'text' is not defined                     no-undef
  72:35  error    Extra semicolon                           semi
```

After:

```
   1:1   warning  Unexpected var, use let or const instead  no-var
   1:12  error    Extra semicolon                           semi
   2:1   warning  Unexpected var, use let or const instead  no-var
   2:11  error    Extra semicolon                           semi
   4:1   warning  Unexpected var, use let or const instead  no-var
   4:6   error    Extra semicolon                           semi
   5:1   warning  Unexpected var, use let or const instead  no-var
   5:6   error    Extra semicolon                           semi
   7:1   warning  Unexpected var, use let or const instead  no-var
   7:19  error    Extra semicolon                           semi
   9:10  error    'preload' is defined but never used       no-unused-vars
  10:45  error    Extra semicolon                           semi
  11:35  error    Extra semicolon                           semi
  14:10  error    'setup' is defined but never used         no-unused-vars
  15:25  error    Extra semicolon                           semi
  16:16  error    Extra semicolon                           semi
  17:8   error    Extra semicolon                           semi
  28:20  error    Extra semicolon                           semi
  29:18  error    Extra semicolon                           semi
  33:15  error    Extra semicolon                           semi
  36:10  error    'draw' is defined but never used          no-unused-vars
  38:29  error    Extra semicolon                           semi
  42:11  error    Extra semicolon                           semi
  46:12  error    Extra semicolon                           semi
  47:16  error    Extra semicolon                           semi
  50:12  error    Extra semicolon                           semi
  51:18  error    Extra semicolon                           semi
  54:12  error    Extra semicolon                           semi
  55:19  error    Extra semicolon                           semi
  60:12  error    Extra semicolon                           semi
  62:15  error    Extra semicolon                           semi
  65:23  error    Extra semicolon                           semi
  67:22  error    Extra semicolon                           semi
  70:18  error    Extra semicolon                           semi
  71:17  error    Extra semicolon                           semi
  72:35  error    Extra semicolon                           semi
```
