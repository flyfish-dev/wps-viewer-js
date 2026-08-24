# Flyfish WPS Viewer Built Artifacts

Production browser artifacts for evaluating Flyfish WPS Viewer at
[wps.file-viewer.app](https://wps.file-viewer.app). The viewer opens WPS/WPT,
ET/ETT, and DPS/DPT files locally in the browser without sending the document
to a conversion service.

[中文说明](README.zh-CN.md) · [Open integration SDK](https://github.com/flyfish-dev/wps-viewer-integration) · [Commercial licensing](https://dev.flyfish.group/shop/detail/1016)

## Scope

This repository contains minified browser bundles, Workers, an optimized WASM
authorization module, the exact-origin evaluation license, and integrity
checksums. It intentionally excludes parser and layout source, signing
material, private test documents, and customer licenses.

The included runtime is permanently restricted to
`https://wps.file-viewer.app`. Copying these files to another Origin does not
grant a deployment right and will not produce an authorized runtime. A
self-hosted production deployment requires a commercial license and matched
runtime delivery.

## Verification

```bash
shasum -a 256 -c SHA256SUMS
```

The online demo is intended for compatibility evaluation. It is not a promise
that every vendor-private, encrypted, or historical binary variant can be
rendered identically to desktop WPS Office.
