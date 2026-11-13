<img src="https://raw.githubusercontent.com/envoscale/EnvoScale/main/docs/images/logo.svg" alt="" width="56" align="left">

# Envor

Rendering for [Envol](https://github.com/envoscale/EnvoScale): 2D drawing, TrueType fonts,
3D scenes with physically based shading, the math under them, an entity-component store,
and the theme every Envoui app is drawn with. Pure Envol, no third-party code; the same
pixels on every platform.

```cs
use envor.gfx;

gfx.Canvas c = gfx.Canvas.New(64, 48);
c.Clear(gfx.Color.Hex("#f5f5f7"));
c.FillRoundedRect(4, 4, 56, 40, 10, gfx.Color.Hex("#ffffff"));
c.FillCircle(18, 24, 8, gfx.Color.Hex("#0a64d4"));
```

| Module | |
|---|---|
| [`envor.gfx`](gfx) | Canvases: shapes with anti-aliasing, blending, clipping, images |
| [`envor.font`](font) | TrueType fonts: parsing, hinting-free rasterizing, text layout |
| [`envor.render3d`](render3d) | 3D: meshes, cameras, lights, PBR materials, glTF 2.0 import |
| [`envor.math`](math) | Vectors, matrices, quaternions |
| [`envor.ecs`](ecs) | Entities and components, the scene store |
| [`envor.theme`](theme) | Colors, type, spacing and shapes: light and dark themes ([design](theme/DESIGN.md)) |

## Use

In a package's `envo.envon`:

```
dependencies {
    envor = { git = "https://github.com/envoscale/Envor", rev = "<commit>" }
}
```

`envo test` runs the tests here; CI runs them on Linux and Windows with EnvoScale at the
commit in [`envoscale.ref`](envoscale.ref).

## License

Same as EnvoScale: see [LICENSE](LICENSE).
