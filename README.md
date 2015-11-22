# sass-math-pow
Math pow() polyfill/feature detection with non-integer exponents support 
for (without compass) ruby sass, plain sass and sass+eyeglass

It will autodetect whether pow() with native non-integer exponents support is available (by eyeglass+sass with eyeglass-math) for full performance, 
and also tries to intall it (as dependency of this package),
otherwise, in case of ruby sass without compass or plain sass, a pow() polyfill is used instead that supports pow() with non-integer exponents.

This polyfill is useful for projects that may use pow() with non-integer exponents and should correctly caluclate across different ruby sass variants and versions.

## Usage
````
> npm install --save-dev sass-math-pow
````
Note: To @import from npm packages/node_modules with ruby sass or plain sass (without eyeglass), 
[sass-include-paths](https://github.com/strarsis/sass-include-paths) helper may be useful.
````
@import 'math-pow';
@debug pow(9, 0.5); // =3 across different sass variants
````

## Credits
Polyfill by Bydrtimofey, script based on script by davidkpiano, see these links
- https://github.com/thoughtbot/bitters/issues/167
- https://github.com/thoughtbot/bourbon/issues/717
- https://gist.github.com/davidkpiano/ad6e6771df050ff3727f