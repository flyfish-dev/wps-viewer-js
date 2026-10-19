# Flyfish WPS Viewer Built Artifacts

Production browser artifacts for evaluating Flyfish WPS Viewer at
[wps.file-viewer.app](https://wps.file-viewer.app). The viewer opens WPS/WPT,
ET/ETT, and DPS/DPT files locally in the browser without sending the document
to a conversion service.

The product homepage and viewer are separate entry points. The homepage embeds
the independently maintained viewer from [`/demo`](https://wps.file-viewer.app/demo)
through a same-origin iframe.

[中文说明](README.zh-CN.md) · [Open integration SDK](https://github.com/flyfish-dev/wps-viewer-integration) · [Commercial licensing](https://dev.flyfish.group/shop/item/1016)

## Current Release

Version **0.4.4**, released on **2026-10-19**, updates both the product homepage
and the independent demo with the latest shared document, spreadsheet, and
presentation engines. This includes font line-box and positioned-table layout,
large-sheet scrolling and embedded images, presentation rendering improvements,
and a versioned DOCX Worker URL to prevent stale engine caches.

Both HTML entry points identify the release through the `application-version`
meta tag. The checksums below cover the exact deployed browser payload.

## Scope

This repository contains minified browser bundles, Workers, an optimized WASM
authorization module, the exact-origin evaluation license, and integrity
checksums. It intentionally excludes parser and layout source, signing
material, private test documents, and customer licenses.

The bundled evaluation license is permanently restricted to
`https://wps.file-viewer.app`. Copying these files to another Origin does not
grant a deployment right and will not authorize the viewer. A self-hosted
production deployment requires a commercial agreement and a signed license
covering the production Origin.

## Verification

```bash
shasum -a 256 -c SHA256SUMS
```

The online demo is intended for compatibility evaluation. It is not a promise
that every vendor-private, encrypted, or historical binary variant can be
rendered identically to desktop WPS Office.
