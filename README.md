# Clipper2 for Unity

A Unity Package Manager (UPM) repackaging of [Clipper2](https://github.com/AngusJohnson/Clipper2) by Angus Johnson.

Clipper2 is a polygon clipping and offsetting library. It performs boolean operations (intersection, union, difference, XOR) on polygons, polygon offsetting/inflating, and polygon triangulation.

## Installation

### Via Unity Package Manager (Git URL)

1. Open your Unity project
2. Go to **Window > Package Manager**
3. Click **+** > **Add package from git URL...**
4. Enter:
   ```
   https://github.com/YOUR_USERNAME/clipper2-upm.git
   ```

### Via manifest.json

Add the following to your project's `Packages/manifest.json`:

```json
{
  "dependencies": {
    "com.angusj.clipper2": "https://github.com/YOUR_USERNAME/clipper2-upm.git"
  }
}
```

### Local Installation

Copy this folder into your Unity project's `Packages/` directory.

## Usage

```csharp
using Clipper2Lib;

// Boolean operations
Paths64 subject = new Paths64();
Paths64 clip = new Paths64();
Paths64 result = Clipper.Intersect(subject, clip, FillRule.NonZero);

// Polygon offsetting
Paths64 paths = new Paths64();
Paths64 inflated = Clipper.InflatePaths(paths, 10, JoinType.Round, EndType.Polygon);
```

See the [Clipper2 documentation](https://www.angusj.com/clipper2/Docs/Overview.htm) for full API reference.

## Upstream

This package is based on [Clipper2 v2.0.0](https://github.com/AngusJohnson/Clipper2) (C# source).

## License

[Boost Software License 1.0](LICENSE) - see the LICENSE file for details.
