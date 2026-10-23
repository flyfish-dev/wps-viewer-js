# Flyfish WPS Viewer Built Artifacts

Production browser artifacts for evaluating Flyfish WPS Viewer at
[wps.file-viewer.app](https://wps.file-viewer.app). The viewer opens WPS/WPT,
ET/ETT, and DPS/DPT files locally in the browser without sending the document
to a conversion service.

The product homepage and viewer are separate entry points. The homepage embeds
the independently maintained viewer from [`/demo`](https://wps.file-viewer.app/demo)
through a same-origin iframe.

[中文说明](README.zh-CN.md) · [Open integration SDK](https://github.com/flyfish-dev/wps-viewer-integration) · [Commercial licensing](https://dev.flyfish.group/shop/detail/1016)

## Current Release

Version **0.4.5**, released on **2026-10-23**, integrates the latest committed
Office components into the WPS preview routes. DOC avoids duplicate rendering
and uses cooperative layout with batched background-font reconciliation. Modern
Word packages retain their original File for Worker/canvas rendering. Compatible
spreadsheets use a Worker and windowed virtual scrolling; modern presentations
load slides on demand with bounded thumbnails and their own navigation.

Spreadsheet and modern-presentation engines load lazily. The main demo bundle
is approximately 32% smaller when gzipped than in 0.4.4. File replacement cancels
old work, and hidden candidate pages no longer inflate the navigation count.
Both desktop and mobile preview surfaces were verified. These are performance
and lifecycle improvements, not a promise of universal native-layout parity.

Both HTML entry points identify the release through the `application-version`
meta tag. The checksums below cover the exact deployed browser payload.

## Licensing Update

The **Flagship edition is CNY 5,999** with unlimited domains, projects and
deployments, a perpetual commercial runtime license and first-year maintenance.
[Choose Flagship in the Flyfish shop](https://dev.flyfish.group/shop/detail/1016?sku=56).

The Commercial and Enterprise editions remain available. The evaluation
license in this repository retains its existing domain restrictions.

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
