# Customized build of Honeycomb's Web SDK as a single-import UMD

This is experimental and not supported.

## Justification

The Honeycomb Web SDK is generally used via modern ESM bundlers in projects using TypeScript or modern JS.

Some clients may be running on an older JS distribution, on an earlier framework that is mounted via script tags
from sources such as `unpgk`.

To build a small UMD distribution, you can follow the approach of this repository.

## Building

```bash
npm install
npm run build
```

## Customizing

To customize the services provided, edit `src/cnd.ts` and mount the appropriate features. In this sample
I am installing the OpenTelemetry ZoneContextManager.

## Using

Copy the `dist/umd/index.js` file to your project or CDN location and serve it from a server.
