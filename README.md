
## Created a project

```bash
# create a new project in the current directory
npx sv create
```

with eslint, tailwind and without ts support.

Then downgraded to:
- vite-plugin-svelte ^3
- svelte ^4

because bits-ui is not compatible with the newer svelte version.

Checked this version in as first commit, everything works as expected.

Then installed:
```
pnpm i layerchart bits-ui d3-scale d3-array
```

Added the tailwind configuration for bits-ui and layerchart. Replaced the default `page.svelte`
with the version from the example repo `layerchart-shadcn-svelte`

When I now run
```
pnpm run dev
```

I get the following long error message:

```
> layerchart-jserror@0.0.1 dev /Volumes/DataMirror/Software/layerchart-jserror
> vite dev


  VITE v5.4.10  ready in 475 ms

  ➜  Local:   http://localhost:5173/
  ➜  Network: use --host to expose
  ➜  press h + enter to show help
✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/ClipPath.svelte:5:15 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/ClipPath.svelte:5:15:
      5 │  export let id: string = uniqueId('clipPath-');
        ╵                ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:18:36:
      18 │ export { default as ClipPath } from './ClipPath.svelte';
         ╵                                     ~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/ColorRamp.svelte:2:25 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/ColorRamp.svelte:2:25:
      2 │  export let interpolator: (t: number) => string;
        ╵                          ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:19:37:
      19 │ export { default as ColorRamp } from './ColorRamp.svelte';
         ╵                                      ~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Group.svelte:3:14 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Group.svelte:3:14:
      3 │  import type { spring as springStore, tweened as tweenedStore } from 'svelte/motion';
        ╵               ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:32:33:
      32 │ export { default as Group } from './Group.svelte';
         ╵                                  ~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Highlight.svelte:2:16 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Highlight.svelte:2:16:
      2 │  import { type ComponentProps } from 'svelte';
        ╵                 ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:33:37:
      33 │ export { default as Highlight } from './Highlight.svelte';
         ╵                                      ~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/ForceSimulation.svelte:4:33 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/ForceSimulation.svelte:4:33:
      4 │  import { forceSimulation, type Force } from 'd3-force';
        ╵                                  ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:21:43:
      21 │ export { default as ForceSimulation } from './ForceSimulation.svelte';
         ╵                                            ~~~~~~~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Frame.svelte:10:19 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Frame.svelte:10:19:
      10 │  export let rectEl: SVGRectElement | undefined = undefined;
         ╵                    ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:20:33:
      20 │ export { default as Frame } from './Frame.svelte';
         ╵                                  ~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Hull.svelte:2:39 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Hull.svelte:2:39:
      2 │  import { createEventDispatcher, type ComponentProps } from 'svelte';
        ╵                                        ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:35:32:
      35 │ export { default as Hull } from './Hull.svelte';
         ╵                                 ~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/HitCanvas.svelte:14:20 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/HitCanvas.svelte:14:20:
      14 │  export let context: CanvasRenderingContext2D = undefined;
         ╵                     ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:34:37:
      34 │ export { default as HitCanvas } from './HitCanvas.svelte';
         ╵                                      ~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/GeoContext.svelte:3:26 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/GeoContext.svelte:3:26:
      3 │  import { writable, type Writable } from 'svelte/store';
        ╵                           ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:23:50:
      23 │ export { default as GeoContext, geoContext } from './GeoContext.svelte';
         ╵                                                   ~~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/GeoCircle.svelte:10:19 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/GeoCircle.svelte:10:19:
      10 │  export let center: [number, number] = [0, 0];
         ╵                    ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:22:37:
      22 │ export { default as GeoCircle } from './GeoCircle.svelte';
         ╵                                      ~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Labels.svelte:2:16 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Labels.svelte:2:16:
      2 │  import { type ComponentProps } from 'svelte';
        ╵                 ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:36:34:
      36 │ export { default as Labels } from './Labels.svelte';
         ╵                                   ~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/GeoEdgeFade.svelte:7:17 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/GeoEdgeFade.svelte:7:17:
      7 │  export let link: { source: [number, number]; target: [number, number] };
        ╵                  ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:24:39:
      24 │ export { default as GeoEdgeFade } from './GeoEdgeFade.svelte';
         ╵                                        ~~~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Legend.svelte:2:14 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Legend.svelte:2:14:
      2 │  import type { SVGAttributes } from 'svelte/elements';
        ╵               ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:37:34:
      37 │ export { default as Legend } from './Legend.svelte';
         ╵                                   ~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/GeoPath.svelte:3:14 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/GeoPath.svelte:3:14:
      3 │  import type { Readable } from 'svelte/store';
        ╵               ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:25:35:
      25 │ export { default as GeoPath } from './GeoPath.svelte';
         ╵                                    ~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Rect.svelte:8:9 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Rect.svelte:8:9:
      8 │    type SpringOptions,
        ╵          ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:50:32:
      50 │ export { default as Rect } from './Rect.svelte';
         ╵                                 ~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Line.svelte:2:22 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Line.svelte:2:22:
      2 │  import { tick, type ComponentProps } from 'svelte';
        ╵                       ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:38:32:
      38 │ export { default as Line } from './Line.svelte';
         ╵                                 ~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Text.svelte:3:14 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Text.svelte:3:14:
      3 │  import type { spring as springStore, tweened as tweenedStore } from 'svelte/motion';
        ╵               ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:55:32:
      55 │ export { default as Text } from './Text.svelte';
         ╵                                 ~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/GeoPoint.svelte:3:14 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/GeoPoint.svelte:3:14:
      3 │  import type { Readable } from 'svelte/store';
        ╵               ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:26:36:
      26 │ export { default as GeoPoint } from './GeoPoint.svelte';
         ╵                                     ~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/RectClipPath.svelte:2:14 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/RectClipPath.svelte:2:14:
      2 │  import type { ComponentProps } from 'svelte';
        ╵               ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:51:40:
      51 │ export { default as RectClipPath } from './RectClipPath.svelte';
         ╵                                         ~~~~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Rule.svelte:22:14 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Rule.svelte:22:14:
      22 │  export let x: number | Date | boolean | 'left' | 'right' = false;
         ╵               ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:52:32:
      52 │ export { default as Rule } from './Rule.svelte';
         ╵                                 ~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/GeoSpline.svelte:2:30 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/GeoSpline.svelte:2:30:
      2 │  import { curveNatural, type CurveFactory, type CurveFactoryLineOnly } from 'd3-shape';
        ╵                               ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:27:37:
      27 │ export { default as GeoSpline } from './GeoSpline.svelte';
         ╵                                      ~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/GeoTile.svelte:3:14 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/GeoTile.svelte:3:14:
      3 │  import type { Readable } from 'svelte/store';
        ╵               ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:28:35:
      28 │ export { default as GeoTile } from './GeoTile.svelte';
         ╵                                    ~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/TransformContext.svelte:3:26 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/TransformContext.svelte:3:26:
      3 │  import { writable, type Readable, type Writable, derived } from 'svelte/store';
        ╵                           ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:59:62:
      59 │ export { default as TransformContext, transformContext } from './TransformContext.svelte';
         ╵                                                               ~~~~~~~~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/GeoVisible.svelte:6:16 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/GeoVisible.svelte:6:16:
      6 │  export let lat: number;
        ╵                 ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:29:38:
      29 │ export { default as GeoVisible } from './GeoVisible.svelte';
         ╵                                       ~~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/LinearGradient.svelte:5:15 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/LinearGradient.svelte:5:15:
      5 │  export let id: string = uniqueId('linearGradient-');
        ╵                ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:40:42:
      40 │ export { default as LinearGradient } from './LinearGradient.svelte';
         ╵                                           ~~~~~~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Link.svelte:16:14 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Link.svelte:16:14:
      16 │  import type { ComponentProps } from 'svelte';
         ╵               ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:41:32:
      41 │ export { default as Link } from './Link.svelte';
         ╵                                 ~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/layout/Svg.svelte:8:20 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/layout/Svg.svelte:8:20:
      8 │  export let element: SVGElement | undefined = undefined;
        ╵                     ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:54:31:
      54 │ export { default as Svg } from './layout/Svg.svelte';
         ╵                                ~~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Sankey.svelte:10:9 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Sankey.svelte:10:9:
      10 │    type SankeyNode,
         ╵          ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:53:34:
      53 │ export { default as Sankey } from './Sankey.svelte';
         ╵                                   ~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Spline.svelte:2:22 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Spline.svelte:2:22:
      2 │  import { tick, type ComponentProps } from 'svelte';
        ╵                       ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:39:34:
      39 │ export { default as Spline } from './Spline.svelte';
         ╵                                   ~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/TileImage.svelte:2:41 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/TileImage.svelte:2:41:
      2 │  let tileCache = new Map<string, Promise<string>>();
        ╵                                          ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:57:37:
      57 │ export { default as TileImage } from './TileImage.svelte';
         ╵                                      ~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Partition.svelte:4:9 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Partition.svelte:4:9:
      4 │    type HierarchyNode,
        ╵          ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:44:37:
      44 │ export { default as Partition } from './Partition.svelte';
         ╵                                      ~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Pie.svelte:2:14 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Pie.svelte:2:14:
      2 │  import type { spring as springStore, tweened as tweenedStore } from 'svelte/motion';
        ╵               ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:46:31:
      46 │ export { default as Pie } from './Pie.svelte';
         ╵                                ~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Pattern.svelte:5:15 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Pattern.svelte:5:15:
      5 │  export let id: string;
        ╵                ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:45:35:
      45 │ export { default as Pattern } from './Pattern.svelte';
         ╵                                    ~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/MotionPath.svelte:6:19 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/MotionPath.svelte:6:19:
      6 │  export let pathId: string = uniqueId('motionPathId-');
        ╵                    ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:42:38:
      42 │ export { default as MotionPath } from './MotionPath.svelte';
         ╵                                       ~~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Pack.svelte:7:17 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Pack.svelte:7:17:
      7 │  export let size: [number, number] | undefined = undefined;
        ╵                  ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:43:32:
      43 │ export { default as Pack } from './Pack.svelte';
         ╵                                 ~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Threshold.svelte:7:14 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Threshold.svelte:7:14:
      7 │  import type { ComponentProps } from 'svelte';
        ╵               ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:56:37:
      56 │ export { default as Threshold } from './Threshold.svelte';
         ╵                                      ~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Tree.svelte:2:16 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Tree.svelte:2:16:
      2 │  import { type HierarchyPointNode, tree as d3Tree, type TreeLayout } from 'd3-hierarchy';
        ╵                 ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:61:32:
      61 │ export { default as Tree } from './Tree.svelte';
         ╵                                 ~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Point.svelte:4:33 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Point.svelte:4:33:
      4 │  const context = chartContext() as any;
        ╵                                  ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:47:33:
      47 │ export { default as Point } from './Point.svelte';
         ╵                                  ~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Voronoi.svelte:5:14 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Voronoi.svelte:5:14:
      5 │  import type { GeoPermissibleObjects } from 'd3-geo';
        ╵               ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:63:35:
      63 │ export { default as Voronoi } from './Voronoi.svelte';
         ╵                                    ~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Points.svelte:2:9 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Points.svelte:2:9:
      2 │  export type Point = { x: number; y: number; r: number; xValue: any; yValue: any; data: a
        ╵          ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:48:34:
      48 │ export { default as Points } from './Points.svelte';
         ╵                                   ~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Treemap.svelte:10:9 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Treemap.svelte:10:9:
      10 │    type HierarchyNode,
         ╵          ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:62:35:
      62 │ export { default as Treemap } from './Treemap.svelte';
         ╵                                    ~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Calendar.svelte:2:16 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Calendar.svelte:2:16:
      2 │  import { type ComponentProps } from 'svelte';
        ╵                 ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:12:36:
      12 │ export { default as Calendar } from './Calendar.svelte';
         ╵                                     ~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Chart.svelte:2:25 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Chart.svelte:2:25:
      2 │  import { onMount, type ComponentProps } from 'svelte';
        ╵                          ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:14:33:
      14 │ export { default as Chart } from './Chart.svelte';
         ╵                                  ~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/layout/Canvas.svelte:13:20 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/layout/Canvas.svelte:13:20:
      13 │  export let element: HTMLCanvasElement | undefined = undefined;
         ╵                     ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:13:34:
      13 │ export { default as Canvas } from './layout/Canvas.svelte';
         ╵                                   ~~~~~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/RadialGradient.svelte:5:15 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/RadialGradient.svelte:5:15:
      5 │  export let id: string = uniqueId('radialGradient-');
        ╵                ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:49:42:
      49 │ export { default as RadialGradient } from './RadialGradient.svelte';
         ╵                                           ~~~~~~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/tooltip/TooltipHeader.svelte:4:18 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/tooltip/TooltipHeader.svelte:4:18:
      4 │  export let color: string | undefined = undefined;
        ╵                   ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/tooltip/index.js:2:34:
      2 │ export { default as Header } from './TooltipHeader.svelte';
        ╵                                   ~~~~~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/CircleClipPath.svelte:2:14 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/CircleClipPath.svelte:2:14:
      2 │  import type { spring as springStore, tweened as tweenedStore } from 'svelte/motion';
        ╵               ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:17:42:
      17 │ export { default as CircleClipPath } from './CircleClipPath.svelte';
         ╵                                           ~~~~~~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Circle.svelte:3:14 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Circle.svelte:3:14:
      3 │  import type { spring as springStore, tweened as tweenedStore } from 'svelte/motion';
        ╵               ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:16:34:
      16 │ export { default as Circle } from './Circle.svelte';
         ╵                                   ~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Grid.svelte:2:14 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Grid.svelte:2:14:
      2 │  import type { SVGAttributes } from 'svelte/elements';
        ╵               ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:31:32:
      31 │ export { default as Grid } from './Grid.svelte';
         ╵                                 ~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Brush.svelte:2:39 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Brush.svelte:2:39:
      2 │  import { createEventDispatcher, type ComponentProps } from 'svelte';
        ╵                                        ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:10:33:
      10 │ export { default as Brush } from './Brush.svelte';
         ╵                                  ~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Axis.svelte:2:16 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Axis.svelte:2:16:
      2 │  import { type ComponentProps } from 'svelte';
        ╵                 ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:6:32:
      6 │ export { default as Axis } from './Axis.svelte';
        ╵                                 ~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Graticule.svelte:3:14 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Graticule.svelte:3:14:
      3 │  import type { ComponentProps } from 'svelte';
        ╵               ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:30:37:
      30 │ export { default as Graticule } from './Graticule.svelte';
         ╵                                      ~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Bounds.svelte:9:7 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Bounds.svelte:9:7:
      9 │  type Extents = Partial<{ x0: number; y0: number; x1: number; y1: number }>;
        ╵        ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:11:34:
      11 │ export { default as Bounds } from './Bounds.svelte';
         ╵                                   ~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Bars.svelte:2:16 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Bars.svelte:2:16:
      2 │  import { type ComponentProps } from 'svelte';
        ╵                 ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:8:32:
      8 │ export { default as Bars } from './Bars.svelte';
        ╵                                 ~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Blur.svelte:4:15 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Blur.svelte:4:15:
      4 │  export let id: string = uniqueId('blur-');
        ╵                ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:9:32:
      9 │ export { default as Blur } from './Blur.svelte';
        ╵                                 ~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Arc.svelte:21:14 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Arc.svelte:21:14:
      21 │  import type { SVGAttributes } from 'svelte/elements';
         ╵               ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:4:31:
      4 │ export { default as Arc } from './Arc.svelte';
        ╵                                ~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Area.svelte:2:16 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Area.svelte:2:16:
      2 │  import { type ComponentProps } from 'svelte';
        ╵                 ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:5:32:
      5 │ export { default as Area } from './Area.svelte';
        ╵                                 ~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Bar.svelte:2:16 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/Bar.svelte:2:16:
      2 │  import { type ComponentProps } from 'svelte';
        ╵                 ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/index.js:7:31:
      7 │ export { default as Bar } from './Bar.svelte';
        ╵                                ~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/charts/PieChart.svelte:2:16 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/charts/PieChart.svelte:2:16:
      2 │  import { type ComponentProps } from 'svelte';
        ╵                 ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/charts/index.js:4:36:
      4 │ export { default as PieChart } from './PieChart.svelte';
        ╵                                     ~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/charts/LineChart.svelte:2:16 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/charts/LineChart.svelte:2:16:
      2 │  import { type ComponentProps } from 'svelte';
        ╵                 ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/charts/index.js:3:37:
      3 │ export { default as LineChart } from './LineChart.svelte';
        ╵                                      ~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/charts/ScatterChart.svelte:2:16 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/charts/ScatterChart.svelte:2:16:
      2 │  import { type ComponentProps } from 'svelte';
        ╵                 ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/charts/index.js:5:40:
      5 │ export { default as ScatterChart } from './ScatterChart.svelte';
        ╵                                         ~~~~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/charts/AreaChart.svelte:2:16 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/charts/AreaChart.svelte:2:16:
      2 │  import { type ComponentProps } from 'svelte';
        ╵                 ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/charts/index.js:1:37:
      1 │ export { default as AreaChart } from './AreaChart.svelte';
        ╵                                      ~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/charts/BarChart.svelte:2:16 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/charts/BarChart.svelte:2:16:
      2 │  import { type ComponentProps } from 'svelte';
        ╵                 ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/charts/index.js:2:36:
      2 │ export { default as BarChart } from './BarChart.svelte';
        ╵                                     ~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/tooltip/TooltipContext.svelte:3:14 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/tooltip/TooltipContext.svelte:3:14:
      3 │  import type { Readable } from 'svelte/store';
        ╵               ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/tooltip/index.js:1:35:
      1 │ export { default as Context } from './TooltipContext.svelte';
        ╵                                    ~~~~~~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/tooltip/TooltipItem.svelte:2:38 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/tooltip/TooltipItem.svelte:2:38:
      2 │  import { format as formatUtil, type FormatType } from '@layerstack/utils';
        ╵                                       ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/tooltip/index.js:3:32:
      3 │ export { default as Item } from './TooltipItem.svelte';
        ╵                                 ~~~~~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/tooltip/Tooltip.svelte:11:14 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/tooltip/Tooltip.svelte:11:14:
      11 │  export let x: 'pointer' | 'data' | number | undefined = 'pointer';
         ╵               ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/tooltip/index.js:6:32:
      6 │ export { default as Root } from './Tooltip.svelte';
        ╵                                 ~~~~~~~~~~~~~~~~~~

✘ [ERROR] /Volumes/DataMirror/Software/layerchart-jserror/node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/ChartContext.svelte:3:29 Unexpected token [plugin vite-plugin-svelte:optimize-svelte]

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/ChartContext.svelte:3:29:
      3 │  import { createScale, type AnyScale } from '../utils/scales.js';
        ╵                              ^

  The plugin "vite-plugin-svelte:optimize-svelte" was triggered by this import

    node_modules/.pnpm/layerchart@0.58.4_svelte@4.2.19_typescript@5.6.3/node_modules/layerchart/dist/components/ChartClipPath.svelte:29:29:
      29 │ import { chartContext } from './ChartContext.svelte';
         ╵                              ~~~~~~~~~~~~~~~~~~~~~~~

```

