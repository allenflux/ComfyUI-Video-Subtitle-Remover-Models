# Video Subtitle Remover Models

本项目存放 ComfyUI Video Subtitle Remover 使用的模型文件。请将仓库部署到：

```text
/app/ComfyUI/models/video-subtitle-remover-models
```

也可以通过 `VSR_MODELS_DIR` 环境变量指定其他绝对路径。

目录结构：

```text
V4/ch_det_fast/inference.onnx  PP-OCRv4 文本检测模型
big-lama/                     LaMa 修复模型分片及合并清单
sttn-det/sttn.pth             STTN 视频修复模型
```

LaMa 首次加载时会在 `big-lama/` 中合并生成 `big-lama.pt`，因此该目录必须可写。可在仓库根目录运行 `shasum -a 256 -c MANIFEST.sha256` 校验文件完整性。

这些模型来自各自的上游项目。使用、再分发或商用前，请确认并遵守 PP-OCR、LaMa、STTN 及相关权重各自的许可证和使用条款；本项目的说明不替代上游许可。

## English

This project contains the model files used by ComfyUI Video Subtitle Remover. Deploy the repository at:

```text
/app/ComfyUI/models/video-subtitle-remover-models
```

Set `VSR_MODELS_DIR` to an absolute path to override the default location.

On first use, LaMa merges its shards into `big-lama/big-lama.pt`, so the `big-lama/` directory must be writable. Run `shasum -a 256 -c MANIFEST.sha256` from the repository root to verify the files.

The models originate from their respective upstream projects. Before use, redistribution, or commercial deployment, review and comply with the licenses and terms for PP-OCR, LaMa, STTN, and the corresponding model weights. This repository does not replace those upstream licenses.
