# Issue with source maps in htmlparser2

This is an example project reproducing an issue with source maps in `htmlparser2`. See:

https://github.com/fb55/htmlparser2/issues/1406

When building for production, the source maps generated by the `htmlparser2` package are being inlined in the codebase instead of being stored in separate files. This is causing the bundle size to grow significantly, which is not ideal for production environments.

To observe this behavior please run the following commands:
```
npm install
npm run build
npm run analyze
```
You will notice that the source maps occupy more that 30% of the entire bundle size.
