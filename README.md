## Jest transform bug

```
/Users/.../msw-test/node_modules/@bundled-es-modules/cookie/index-esm.js:172
    export {
    ^^^^^^

    SyntaxError: Unexpected token 'export'
```

How to reproduce:

```
npm i
npm test .
```

Inline fix:

```
npm test .  -- --transformIgnorePatterns "node_modules/(?!(@bundled-es-modules)/)"
```
