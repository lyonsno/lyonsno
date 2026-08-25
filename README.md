# Noah Lyons

I build GPU and ML systems for Apple Silicon and the browser: MLX kernels and
model ports, browser-native WebGPU inference, and spatial tools for inspecting
generated worlds.

## Accepted upstream

- **MLX Core:** [antialiased linear and cubic `nn.Upsample`](https://github.com/ml-explore/mlx/pull/3677) and [compiled-kernel correctness for negative-strided inputs](https://github.com/ml-explore/mlx/pull/3720).
- **WebGPU Samples:** an [external Vision Transformer sample](https://github.com/webgpu/webgpu-samples/pull/570) with interactive attention visualization.
- **vLLM-MLX:** [lifecycle-managed model residency](https://github.com/waybarrios/vllm-mlx/pull/205), including lazy loading, idle unload, cancellation-safe transitions, and public lifecycle state.
- **MLX-LM:** [rotating KV cache support for sliding-attention layers](https://github.com/ml-explore/mlx-lm/pull/949).
- **MLX serving:** [15 merged contributions to MLX OpenAI Server](https://github.com/cubist38/mlx-openai-server/pulls?q=is%3Apr+author%3Alyonsno+is%3Amerged) and [five merged contributions to oMLX](https://github.com/jundot/omlx/pulls?q=is%3Apr+author%3Alyonsno+is%3Amerged), centered on streaming, tool calls, reasoning parsers, cancellation, cache integrity, and API compatibility.

See [more upstream contributions and public review history](UPSTREAM.md).

## Browser-native GPU inference

- [`@kaminos/webgpu-inference-kit`](https://www.npmjs.com/package/@kaminos/webgpu-inference-kit) is a composable WebGPU runtime for tensors, kernels, staged programs, route adapters, and cooperative scheduling.
- [`moge-webgpu`](https://github.com/lyonsno/moge-webgpu) runs MoGe-2 depth and surface-normal estimation in browser-native compute shaders.
- [`sharp-webgpu`](https://github.com/lyonsno/sharp-webgpu) turns a single image into 3D Gaussian splats in the browser.
- [`sf3d-webgpu`](https://github.com/lyonsno/sf3d-webgpu) generates textured 3D meshes in browser-native WebGPU.
- [`kimodo-webgpu`](https://github.com/lyonsno/kimodo-webgpu) runs NVIDIA's 282M-parameter text-to-motion diffusion transformer in browser WebGPU, with DDIM sampling, denoising, and forward kinematics on the client.

## Apple Silicon ML

- [`mlx-nf4`](https://github.com/lyonsno/mlx-nf4) extracts the NF4 work into an installable standalone MLX custom extension with packed 4-bit weights and native Metal matrix multiplication; [`mlx-ideogram4`](https://github.com/lyonsno/mlx-ideogram4) exercises it in a 9.3B text-to-image pipeline.
- [`cosmos3-mlx`](https://github.com/lyonsno/cosmos3-mlx) is a full-source MLX port of NVIDIA's 16B Cosmos 3 Nano world model for text/image-to-video and joint video/audio generation.
- [`wilor-mlx`](https://pypi.org/project/wilor-mlx/) rebuilds WiLoR hand-pose estimation end to end in MLX.
- [`trellis2mlx`](https://github.com/lyonsno/trellis2mlx) and [`pixal3d-mlx`](https://github.com/lyonsno/pixal3d-mlx) bring image-to-3D generation to Apple Silicon without PyTorch.

## Current work

[`Kaminos`](https://github.com/lyonsno/kaminos) is the convergence surface: a
WebGPU and Three.js workbench for generating, inspecting, editing, and composing
local virtual-world artifacts.

Contact: [n.lyons53@gmail.com](mailto:n.lyons53@gmail.com)
