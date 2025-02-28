@huid/kuromoji.js
===========

# forked by @sglkc/kuromoji
[@sglkc/kuromoji](https://github.com/sglkc/kuromoji.js)

# How to use

Compatible with [kuromoji.js API](https://github.com/takuyaa/kuromoji.js), the only difference is that please provide the directory where the `*.dat` files are stored.

# Example
1. load from current project public/dict
```js
kuromoji.builder({ dicPath: "/dict" }).build(function (err, tokenizer) {
    // tokenizer is ready
    var path = tokenizer.tokenize("すもももももももものうち");
    console.log(path);
});
```

2. load from cdn url
```js
kuromoji.builder({ dicPath: "https://cdn.jsdelivr.net/npm/kuromoji@0.1.2/dict" }).build(function (err, tokenizer) {
    // tokenizer is ready
    var path = tokenizer.tokenize("すもももももももものうち");
    console.log(path);
});
```
