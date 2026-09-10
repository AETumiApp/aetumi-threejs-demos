# AETumi — Live Three.js Demos

Five small, **self-contained, interactive Three.js (r160) + WebGL** demos. No build step, no framework — just `index.html`, an import map, and a single ES module each. Open a file in a browser and it runs.

Every demo is **real WebGL rendering in the browser** — not an MP4, not a GIF, not a Figma prototype. Open DevTools and tear the implementation apart.

## Demos

| Demo | What it shows | Live | Article |
|---|---|---|---|
| [`scene-graph/`](scene-graph/) | A Three.js scene graph as labelled node boxes wired into a parent → child tree; the root group rotates and every descendant follows in real time | [live](https://aetumi.app/news/threejs-architecture/) | [read](https://aetumi.app/news/threejs-architecture/) |
| [`gltf-optimization/`](gltf-optimization/) | glTF / GLB mesh optimization — triangle-density and payload trade-offs, live | [live](https://aetumi.app/news/optimize-gltf-glb-threejs/) | [read](https://aetumi.app/news/optimize-gltf-glb-threejs/) |
| [`draco-vs-meshopt/`](draco-vs-meshopt/) | Draco vs Meshopt geometry compression compared in a live scene | [live](https://aetumi.app/news/draco-vs-meshopt/) | [read](https://aetumi.app/news/draco-vs-meshopt/) |
| [`ktx2-texture-compression/`](ktx2-texture-compression/) | KTX2 / Basis GPU texture compression and the mip pyramid, rendered live | [live](https://aetumi.app/news/ktx2-basis-texture-compression-threejs/) | [read](https://aetumi.app/news/ktx2-basis-texture-compression-threejs/) |
| [`instancing-lod/`](instancing-lod/) | InstancedMesh + LOD — draw-call and performance behaviour across a large instanced field | [live](https://aetumi.app/news/threejs-performance-instancing-lod/) | [read](https://aetumi.app/news/threejs-performance-instancing-lod/) |

## Run locally

Each folder is standalone. Any static server works:

```bash
npx serve .        # then open the folder in a browser
# or just open scene-graph/index.html directly
```

## Tech

- **Three.js r160** loaded via an ES-module import map from jsDelivr — no bundler.
- Vanilla WebGL, no React / R3F layer (kept deliberately light for these experiments).
- Raymarched SDF forms, real particle / point-cloud systems, planar water reflections (mirrored camera, not a cubemap), instancing + LOD — depending on the demo.

## About

Built by **[AETumi](https://aetumi.app)** — AI-native 3D websites, components and templates. Three.js & WebGL, drag-and-remix, you own the source.

Feedback welcome — how does it perform on your GPU? Where does it break? PRs and issues open.

## License

MIT © AETumi Corp

## Explore the AETumi library

Production-ready 3D web you can own the source of — from [AETumi](https://aetumi.app), the AI-native 3D web platform:

- [Three.js website templates & 3D components](https://aetumi.app/threejs/)
- [WebGL website examples, shaders & components](https://aetumi.app/webgl/)
- [3D website templates & examples](https://aetumi.app/3d-websites/)

Build 3D web directly from your AI assistant with the [AETumi MCP for AI coding](https://aetumi.app/mcp/) — `claude mcp add --transport http aetumi https://mcp.aetumi.app`
