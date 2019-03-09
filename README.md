# @microsoft/api-extractor default export issue repro

## issue: https://github.com/Microsoft/web-build-tools/issues/1136

## instructions
- npm install
- npm run build

## review bad output

- open file ./dist/api-extractor-repro.d.ts
- you will see the following output

```
    import { default } from 'react';   <<< bad 'default' is a keyword in JS, it is not a valid named import

    /**
    * The test class we are trying to default export
    *
    * @class TestComponent
    * @extends {React.Component}
    *
    * @public
    */
    export declare class TestComponent extends default.Component {
    }

    export { }
```