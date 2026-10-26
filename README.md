# Noah Lyons

I build GPU and ML systems for Apple Silicon and the browser: MLX kernels and
model ports, browser-native WebGPU inference, and spatial tools for inspecting
generated worlds.

## Accepted upstream

- **MLX Core:** [antialiased linear and cubic `nn.Upsample`](https://github.com/ml-explore/mlx/pull/3677) and [compiled-kernel correctness for negative-strided inputs](https://github.com/ml-explore/mlx/pull/3720).
- **MLX Audio:** [streaming speech generation for VibeVoice](https://github.com/Blaizzy/mlx-audio/pull/925) and [predictor caching for Nemotron speech recognition](https://github.com/Blaizzy/mlx-audio/pull/1006).
- **WebGPU Samples:** an [external Vision Transformer sample](https://github.com/webgpu/webgpu-samples/pull/570) with interactive attention visualization.
- **vLLM-MLX:** [lifecycle-managed model residency](https://github.com/waybarrios/vllm-mlx/pull/205), including lazy loading, idle unload, cancellation-safe transitions, and public lifecycle state.
- **MLX serving:** [15 merged contributions to MLX OpenAI Server](https://github.com/cubist38/mlx-openai-server/pulls?q=is%3Apr+author%3Alyonsno+is%3Amerged) and [five merged contributions to oMLX](https://github.com/jundot/omlx/pulls?q=is%3Apr+author%3Alyonsno+is%3Amerged), centered on streaming, tool calls, reasoning parsers, cancellation, cache integrity, and API compatibility.

See [the full contribution index, selected reviews, and independent deployment evidence](UPSTREAM.md).

## Browser-native GPU inference

The [Kaminos WebGPU Inference Kit](https://lyonsno.github.io/kaminos/inference-kit/) brings substantial models into responsive browser applications. Model applications handle loading, queued inference, controls and cleanup, with model-specific options and lower-level APIs available for custom integrations.

- **Image generation:** [FLUX.2 [klein] 4B](https://lyonsno.github.io/kaminos/inference-kit/klein/) runs its text encoder, diffusion transformer and image decoder on the browser's GPU.
- **Image to 3D:** [TRELLIS 2](https://github.com/lyonsno/kaminos/tree/main/models/trellis2) generates textured meshes with browser-native WebGPU, with a guide to model preparation and asset finishing.
- **Skeletal animation:** [UniMate](https://lyonsno.github.io/kaminos/inference-kit/unimate/) generates motion for different rigged skeletons from text, with an animated GLB export.
- **Live hand reconstruction:** [WiLoR and MobRecon](https://lyonsno.github.io/kaminos/inference-kit/hand-mesh/) turn camera frames into hand meshes and landmarks. The demo links to local model setup.
- **Relightable photographs:** [Material Photograph](https://lyonsno.github.io/kaminos/inference-kit/material-photo/) combines MoGe geometry and SuperMat materials with an interactive renderer on one GPU.

[Build with a model application](https://github.com/lyonsno/kaminos/blob/main/webgpu-inference-kit/docs/model-applications.md), or explore the [full model catalog](https://github.com/lyonsno/kaminos/tree/main/webgpu-inference-kit#one-runtime-different-models), including background removal, segmentation, depth estimation and Gaussian reconstruction. Some ports live in Kaminos and others in standalone repositories; the catalog links to their current source and integration guides.

## Apple Silicon ML

- [`mlx-nf4`](https://github.com/lyonsno/mlx-nf4) is a standalone native Metal NF4 extension for stock MLX, verified from a clean source install on M2 Pro and exercised end to end by double-quantized GPT-2 and the 9.3B [`mlx-ideogram4`](https://github.com/lyonsno/mlx-ideogram4) image pipeline.
- [`cosmos3-mlx`](https://github.com/lyonsno/cosmos3-mlx) is a full-source MLX port of NVIDIA's 16B Cosmos 3 Nano world model for text/image-to-video and joint video/audio generation.
- [`wilor-mlx`](https://pypi.org/project/wilor-mlx/) rebuilds WiLoR hand-pose estimation end to end in MLX.
- [`trellis2mlx`](https://github.com/lyonsno/trellis2mlx) and [`pixal3d-mlx`](https://github.com/lyonsno/pixal3d-mlx) bring image-to-3D generation to Apple Silicon without PyTorch.

## Current work

[`Kaminos`](https://github.com/lyonsno/kaminos) is very much a work in progress:
it is the research bench where I explore the ideas that interest me most right
now, especially browser-native ML, spatial interfaces, and tools for inspecting
and shaping generated worlds. The WebGPU inference kit above is the most mature
reusable component to emerge from that work.

Contact: [n.lyons53@gmail.com](mailto:n.lyons53@gmail.com)
