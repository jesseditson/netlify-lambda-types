# netlify-lambda-types
Netlify Lambda typescript definitions

These types are intended to make developing netlify handlers in typescript a bit less painful.

They are a reverse-engineered approximation of Netlify's types, not an officially supported definition.

## Installation:

`npm i -D netlify-lambda-types`

## Usage:

```javascript
import { NetlifyFunction } from "netlify-lambda-types";

const handler: NetlifyFunction = async (event, context, callback) => {
  // event, context, and callback are now typed, along with the return type
  return { statusCode: 200, body: "ok" };
};
exports.handler = handler;
```