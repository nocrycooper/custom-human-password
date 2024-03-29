# HumanPassword
Simple library to generate a password (string + number) easy to remember.

## Installation

```javascript
npm install custom-human-password --save
```

## Example
### Basic
```javascript
var humanPassword = require('custom-human-password');

humanPassword();
// => 'fuxeru9070'
```

### With options

Name | Type | Default | Description
-|-|-|-
couples | integer | 3 | Couple of consonant + vowel
digits | integer | 4 | Number of digits, if is 0 number will be hidden
randomUpper | boolean | false | Random letters uppercase
numberPosition | string | end | Number position in string, can be "start", "middle", "end" and "random"

```javascript
var humanPassword = require('custom-human-password');

humanPassword({
    couples: 5,
    digits: 4,
    randomUpper: true
});
// => 'PutIGoKobi7136'

// Hide number
humanPassword({
    couples: 5,
    digits: 0
});
// => 'gicominobi'

// Number in start position
humanPassword({
    couples: 5,
    digits: 4,
    numberPosition: 'start'
});
// => '6539vikohylure'
```

## License
HumanPassword is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT)