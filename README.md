### probe-image-size
---
https://github.com/nodeca/probe-image-size

```js
var probe = require('probe-image-size');

probe('http://example.com/image.jpg').then(result => {
  console.log(result);
});

probe('http://example.com/image.jpg', { timeout: 5000 }).then(function (result) {
  console.log(result);
});

probe('http://example.com/image.jpg', funciton (err, result) {
  console.log(result);
});

var input = require('fs').createReadStream('image.jpg');

probe(input).then(result => {
  console.log(result);
  
  input.destroy();
});

var data = require('fs').readFileSync('image.jpg');

console.log(probe.sync(data));
```

```sh
npm install probe-image-size --save
```

```
{
  width: XX,
  height: YY,
  length: ZZ,
  type: ...,
  mime: ...,
  wUnits: 'px',
  hUnints: 'px',
  url: ...,
}
```
