# CriptJS API - A text encryptor

![CRIPTJS LOGO](https://i.ibb.co/KqSKs2x/20201225-165901.png)



<h1 id="FrontEnd">FrontEnd - API CriptJS</h1>

Now CriptJS is available for FrontEnd, its usability is very simple and very similar to BackEnd. Check it out below.

## Installation

```javascript
<script src="https://cdn.jsdelivr.net/gh/DablioZe/apicriptjs/cript.min.js"></script>
```

## How to use

_To encrypt a text use: `criptjs.encrypt(text, callback);`_

```javascript
criptjs.setKey("my key");

criptjs.encrypt("Hello World!", (err, result) => {
    if (err) throw err;
    console.log(result);
});
// result: "µÞ×ÔÄè×É"
```

_To decrypt a code use: `criptjs.decrypt(text, callback);`_

```javascript
const myCode = "µÞ×ÔÄè×É";

criptjs.setKey("my key");

criptjs.decrypt(myCode, (err, result) => {
    if (err) throw err;
    console.log(result);
});
// result: "Hello World!"
```

_You can generate a new key using `criptjs.genKey(length, types, callback)`_

```javascript
criptjs.genKey(30, ["letters", "numbers"], (err, result) => {
    // This command generates a random result.
    if (err) throw err;
    console.log(result);
})
// result: "9T6z9y3e0A3M1M9i2i7e6y6k3C4U2o"
```

_If you want only numbers to be generated, type `criptjs.genKey(length, "numbers", callback)`_

```javascript
criptjs.genKey(30, "numbers", (err, result) => {
    // This command generates a random result.
    if (err) throw err;
    console.log(result);
})
// result: "564281673592645812365987546825"
```

_You can also do this with `criptjs.genKey(length, "letters", callback)`_

```javascript
criptjs.genKey(30, "letters", (err, result) => {
    // This command generates a random result.
    if (err) throw err;
    console.log(result);
})
// result: "BgsacHGdtAdSemNjkLdfTtYsdCiopS"
```

> ***Note***: We recommend that you use very specific keys that only you know, do not share it with anyone. your data is safe, it will only be revealed if you use the right key! 

### if you find an error or bug please report it at [CriptJS/Issues](https://github.com/DablioZe/apicriptjs/issues)

_i hope you enjoy :D_



