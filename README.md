# Optimus Prime Transforming Pet

一个体态修长的红蓝变形机器人桌宠，用于 ChatGPT Work Pets。进入处理任务状态后，桌宠切换到卡车外观并持续保持；离开处理状态后回到机器人待机。项目还包含左右移动、挥手、跳跃、等待、失败、检查和 16 个视线方向。

This is a fan-made, original sprite asset and is not affiliated with or endorsed by any trademark holder.

## Repository metadata

- **Recommended repository name:** `optimus-prime-transforming-pet`
- **GitHub description:** `A slender red-and-blue transforming robot pet for ChatGPT Work, with truck-mode processing and multi-action animation.`
- **Canonical asset prefix:** `optimus-prime-pet-v2`
- **License:** [MIT](LICENSE)

## Repository layout

| Path | Purpose |
| --- | --- |
| `assets/optimus-prime-pet-v2.png` | Canonical v2 PNG sprite sheet for upload |
| `assets/optimus-prime-pet-v2.webp` | WebP copy of the canonical sprite sheet |
| `assets/optimus-prime-pet-v2-manifest.json` | Atlas layout, look directions, and runtime metadata |
| `assets/previews/optimus-prime-actions.gif` | All-state animated preview |
| `assets/previews/optimus-prime-actions.mp4` | MP4 copy of the all-state preview |
| `assets/previews/optimus-prime-processing-truck.gif` | Processing-state truck preview |
| `assets/previews/optimus-prime-contact-sheet.png` | Labeled visual QA contact sheet |
| `metadata/optimus-prime-pet.json` | Human- and tool-readable project metadata |
| `PROJECT_DESCRIPTION.md` | Repository name and short/long descriptions |
| `LICENSE` | MIT license text |

The local `work/` directory contains the creation history, prompts, intermediate renders, and QA reports. It is intentionally ignored by Git so the public repository stays focused on the release assets; preserve it locally when reproducibility evidence is needed.

## Sprite-sheet contract

The canonical sheet is ChatGPT Pets v2:

- 1536 × 2288 pixels
- 8 columns × 11 rows
- 192 × 208 pixel cells
- Standard rows: `idle`, `running-right`, `running-left`, `waving`, `jumping`, `failed`, `waiting`, `running`, and `review`
- Final two rows: 16 clockwise look directions from `000` through `337.5` degrees

The `running` row repeats one complete front-truck pose in all six cells. This corresponds to the attached reference's truck labels 1, 3, and 5, so the processing state holds a stable truck appearance instead of alternating between views. The duration is controlled by the host task state; the sprite sheet does not encode a random 30–120 second timer.

## Validation

The checked release asset passed the structural Pets v2 preflight and the local image-quality gate. The final PNG is RGBA, 1536 × 2288, and has SHA-256:

```text
eda329940ef9f85830c1a0f57ae15ac1599522f5b95a4e3f3248c58ad5b087a3
```

The archived QA report retains three non-blocking look-direction continuity warnings; no structural validation errors were present.

## Usage

Use `assets/optimus-prime-pet-v2.png` as the upload source for a compatible ChatGPT Pets v2 workflow. Keep the dimensions, cell size, row order, and transparent background unchanged when distributing or updating the asset.

## License and attribution

The repository contents are released under the MIT License. See [LICENSE](LICENSE) for the full text. The artwork is an original fan-made robot sprite and carries no official affiliation.
