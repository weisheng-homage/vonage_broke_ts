# typescript broke with vonage

because it is not compatible with node-fetch v3

## setup

```
npm i
```
## compile step

```
npx tsc
```

## error message
```
node_modules/@vonage/server-client/dist/client.d.ts:1:26 - error TS1479: The current file is a CommonJS module whose imports will produce 'require' calls; however, the referenced file is an ECMAScript module and cannot be imported with 'require'. Consider writing a dynamic 'import("node-fetch")' call instead.

1 import { Response } from 'node-fetch';
                           ~~~~~~~~~~~~

node_modules/@vonage/vetch/dist/errors/vetchError.d.ts:2:26 - error TS1479: The current file is a CommonJS module whose imports will produce 'require' calls; however, the referenced file is an ECMAScript module and cannot be imported with 'require'. Consider writing a dynamic 'import("node-fetch")' call instead.

2 import { Response } from 'node-fetch';
                           ~~~~~~~~~~~~


Found 2 errors in 2 files.

Errors  Files
     1  node_modules/@vonage/server-client/dist/client.d.ts:1
     1  node_modules/@vonage/vetch/dist/errors/vetchError.d.ts:2
```

## environment tested
node 20.11.0
