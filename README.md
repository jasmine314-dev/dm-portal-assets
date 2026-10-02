# dm-portal-assets

Public-domain (CC0) textures, lighting and models for the DM Portal sign-in lobby
(`ui/login.html` / `ui/login-lobby.js` in the telemetry-monitoring repo). Every file here is
derived from [Poly Haven](https://polyhaven.com) assets, which are released under
**CC0 1.0 Universal** (public domain dedication, no attribution required):
<https://polyhaven.com/license> · <https://creativecommons.org/publicdomain/zero/1.0/>.
Nothing in this repository belongs to Da Ma Cai or contains anything private.

The page loads these files through jsDelivr **pinned to a full 40-character commit SHA**
(`https://cdn.jsdelivr.net/gh/jasmine314-dev/dm-portal-assets@<sha>/`), never `@main`, so a later
push can never change what the live page shows.

## Files

| File | Bytes | Poly Haven source | What was done to it |
|---|---:|---|---|
| `hdri/unfinished_office_512.hdr` | 356,795 | [unfinished_office](https://polyhaven.com/a/unfinished_office) (1k .hdr) | box-filtered 1024x512 -> 512x256, re-written as RLE RGBE |
| `skyline/dusk_skyline.jpg` | 21,494 | [sunset_jhbcentral](https://polyhaven.com/a/sunset_jhbcentral) (4k .hdr) | ACES tone-map at exposure 0.6, portrait crop (x 1100-1620, y 120-1200) to 416x864, JPEG q68 |
| `textures/plaster_diff_1k.jpg` | 64,720 | [painted_plaster_wall](https://polyhaven.com/a/painted_plaster_wall) (1k diffuse) | greyscale, levels lifted to mean ~237, JPEG q70 |
| `textures/carpet_diff_1k.jpg` | 149,863 | [dirty_carpet](https://polyhaven.com/a/dirty_carpet) (1k diffuse) | greyscale, levels to mean ~102 / low contrast, JPEG q66 |
| `textures/walnut_diff_1k.jpg` | 42,410 | [walnut_veneer](https://polyhaven.com/a/walnut_veneer) (1k diffuse) | JPEG q70 |
| `textures/walnut_rough_512.jpg` | 15,795 | [walnut_veneer](https://polyhaven.com/a/walnut_veneer) (1k roughness) | greyscale, 512x512, JPEG q70 |
| `textures/stone_diff_1k.jpg` | 38,978 | [marble_rock_01](https://polyhaven.com/a/marble_rock_01) (1k diffuse) | greyscale, graded to a pale veined stone (mean ~237), JPEG q70 |
| `props/mid_century_lounge_chair/*` | 206,747 | [mid_century_lounge_chair](https://polyhaven.com/a/mid_century_lounge_chair) (1k glTF) | geometry `.bin` unchanged; normal map dropped; diffuse 512, ARM 256 |
| `props/potted_plant_04/*` | 284,523 | [potted_plant_04](https://polyhaven.com/a/potted_plant_04) (1k glTF) | geometry `.bin` unchanged; normal map dropped; diffuse 512, ARM 256 |
| `props/round_wooden_table_01/*` | 272,252 | [round_wooden_table_01](https://polyhaven.com/a/round_wooden_table_01) (1k glTF) | geometry `.bin` unchanged; normal map dropped; diffuse 512, ARM 256 |
| `hdri/kloofendal_48d_partly_cloudy_puresky_256.hdr` | 98,575 | [kloofendal_48d_partly_cloudy_puresky](https://polyhaven.com/a/kloofendal_48d_partly_cloudy_puresky) (1k .hdr) | box-filtered 1024x512 -> 256x128, re-written as RLE RGBE; Day reflections for the gold in the God of Wealth sign-in background |
| `hdri/qwantani_dusk_2_puresky_256.hdr` | 77,888 | [qwantani_dusk_2_puresky](https://polyhaven.com/a/qwantani_dusk_2_puresky) (1k .hdr) | box-filtered 1024x512 -> 256x128, re-written as RLE RGBE; Night (dusk) reflections for the same scene |

Total payload (every file except this README): **1,630,040 bytes** (budget: under 3 MB). The two sky HDRIs added on 2026-10-02 for the God of Wealth background are 176,463 bytes of that; the page no longer loads the office-lobby files above, which stay here only so older pinned commits keep resolving.

## Licence

All files: CC0 1.0 Universal, inherited from Poly Haven. The modifications listed above are
likewise dedicated to the public domain.
