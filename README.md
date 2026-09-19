<div align="center">

# Photo2Magnet · 旅行冰箱贴

### Your photos. Tiny keepsakes.

Turn a travel photo, a favorite building, or a moment with your pets into a sculpted fridge-magnet concept image.

**English** · [简体中文](README.zh-CN.md)

[![License: MIT](https://img.shields.io/badge/License-MIT-315C48.svg)](LICENSE)
[![Agent Skill](https://img.shields.io/badge/Agent-Skill-546C7A.svg)](SKILL.md)
[![Tested in Codex](https://img.shields.io/badge/Tested_in-Codex-263238.svg)](#requirements)

</div>

| Your photo | Your magnet |
| :---: | :---: |
| <img src="docs/images/skyline-before.jpg" alt="Original photo of Hong Kong's misty skyline and harbor" width="420"> | <img src="docs/images/skyline-after.jpg" alt="Hong Kong's skyline, towers, and waterfront wheel transformed into a sculpted fridge-magnet concept" width="420"> |

Keep Hong Kong's misty skyline, the waterfront wheel, the blue-gray water—and the memory. Photo2Magnet guides an image-capable agent to preserve those details while designing a connected relief, a custom outline, and convincing material depth.

**[See all 7 before-and-after examples →](docs/gallery.md)**

## Install in Codex

With the [Skills CLI](https://github.com/vercel-labs/skills):

```bash
npx skills add carpediem67/photo2magnet --skill photo2magnet --agent codex --global
```

Or clone the repository directly into your user skills folder:

```bash
git clone https://github.com/carpediem67/photo2magnet.git ~/.agents/skills/photo2magnet
```

Use either method. If that folder already exists, keep your changes and update your existing installation. If the new skill does not appear, start a new task or restart Codex.

## Make your first magnet

Attach a photo and ask:

```text
Use $photo2magnet to turn this photo into a sculpted fridge magnet.
```

The default is one square product image with a painted-resin relief, a clean background, and no lettering. Your preferences override the defaults.

Try a few variations:

```text
Use $photo2magnet with this harbor photo.
Keep the mist and skyline, use a deep blue enamel finish,
and add a small plaque that reads exactly "Harbor Days".
```

```text
Use $photo2magnet to make one magnet from each of these photos.
Keep the same material and lighting across the set.
Preserve the pets, and do not add text.
```

```text
Use $photo2magnet to edit the magnet we just made.
Change only the background to pale sage; keep the scene and silhouette.
```

## What makes a good result

- **Recognizable memories.** Preserve the skyline, roof shape, shoreline, pets, and other details that make the source yours.
- **Relief with a purpose.** Compress depth into connected sculpted layers with a thin backing and a visible edge.
- **A shape that fits the scene.** Follow a mountain ridge, a dome, a tree canopy, or a coastline instead of using one frame for every photo.
- **Materials you can read.** Distinguish rough stone, painted architecture, foliage, and glossy water.
- **Room for your direction.** Change the material, background, outline, lettering, aspect ratio, or number of images.

## More from the same skill

| Harbor skyline | Sunset station | Coastal stacks |
| :---: | :---: | :---: |
| <img src="docs/images/skyline-after.jpg" alt="Blue-gray harbor skyline in resin relief" width="270"> | <img src="docs/images/station-after.jpg" alt="Golden station entrance and green dome in relief" width="270"> | <img src="docs/images/coast-after.jpg" alt="Coastal cliffs, sea stacks and foamy waves in relief" width="270"> |

Every example was generated from a real source photo and visually reviewed. These are examples of the workflow, not a guarantee of identical output.

## Requirements

**Tested in Codex with its built-in image-generation tool.** This repository contains instructions and examples, not an image model or a standalone application. It does not require a separate API key when that built-in capability is available; image access and usage limits still depend on the host.

Other hosts must support Agent Skills, reference images, and image generation/editing. They have not been tested here. Installing the text files alone does not add an image-generation capability.

The skill is model-agnostic. It does not select or promise a particular image model.

## FAQ

**Does it produce printable 3D models?**

It produces 2D product concept images with a 3D relief appearance. STL/3MF files, magnet sockets, dimensions, and printability require a separate modeling workflow.

**Will every detail match the photo?**

It preserves recognizable relationships, but it is an artistic transformation. Small faces, visitor counts, signs, geometry, and colors can change. Review details that matter to you.

**Can I use a theme instead of a photo?**

Yes. Give a clear scene or subject. Without a source photo, the output is an original concept rather than a reconstruction.

**What if my photo cannot be read?**

The skill can prepare and inspect a compatible copy while preserving your original. HEIC and two incompatible JPEG inputs were successfully handled in the seven-photo trial.

**Why is the skill file in Chinese?**

The workflow was developed in Chinese. The usage examples and documentation are available in English and Chinese; you can request your output in either language. English-language invocation has not been evaluated in a separate end-to-end run.

## Contributing

Useful contributions include better preservation of a difficult subject, clearer instructions, and reproducible visual examples. Include the source image (only if you can share it), the request, the result, and what changed. Keep host-specific implementation details out of the core creative workflow when they are not needed.

## License

[MIT](LICENSE) · Copyright © 2026 Qing1.

The license does not grant rights to third-party photos or other material you bring to the workflow. An independent community skill; not an official OpenAI product.
