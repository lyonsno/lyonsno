# Upstream work

This is a linked index of externally hosted contributions from the current
campaign. It points to the upstream pull requests and review records rather
than restating their implementation narratives.

Forge state checked: 2026-08-25.

## Independent review receipts

- MLX Core antialiased upsampling: [independent numerical review](https://github.com/ml-explore/mlx/pull/3677#pullrequestreview-4669282819) and [MLX maintainer approval](https://github.com/ml-explore/mlx/pull/3677#pullrequestreview-4916201375).
- vLLM-MLX lifecycle-managed residency: [cancellation, state-machine, and API review](https://github.com/waybarrios/vllm-mlx/pull/205#pullrequestreview-4040627389) and [second architecture review](https://github.com/waybarrios/vllm-mlx/pull/205#pullrequestreview-4114070783).
- MLX-LM rotating cache: [maintainer approval](https://github.com/ml-explore/mlx-lm/pull/949#pullrequestreview-3892969324).
- oMLX streamed tool-call parsing: [owner review and approval](https://github.com/jundot/omlx/pull/140#pullrequestreview-3928466818).

## Merged external contributions

### MLX Core and MLX model libraries

- [`ml-explore/mlx#3677`](https://github.com/ml-explore/mlx/pull/3677): antialias support for linear and cubic `nn.Upsample`.
- [`ml-explore/mlx#3720`](https://github.com/ml-explore/mlx/pull/3720): compiled-kernel correctness for negative-strided inputs.
- [`ml-explore/mlx-lm#949`](https://github.com/ml-explore/mlx-lm/pull/949): rotating cache for Step3.5 sliding-attention layers.
- [`Blaizzy/mlx-vlm#1157`](https://github.com/Blaizzy/mlx-vlm/pull/1157): Qwen3-VL vision-config deserialization correctness.
- [`Blaizzy/mlx-audio#633`](https://github.com/Blaizzy/mlx-audio/pull/633): Voxtral TTS tokenizer and dependency contract.

### MLX serving and lifecycle systems

- [`waybarrios/vllm-mlx#205`](https://github.com/waybarrios/vllm-mlx/pull/205): lifecycle-managed residency for the default server model.
- [`cubist38/mlx-openai-server#214`](https://github.com/cubist38/mlx-openai-server/pull/214): parser-refactor regression fixes.
- [`cubist38/mlx-openai-server#215`](https://github.com/cubist38/mlx-openai-server/pull/215): split reasoning and tool markers in streaming parsers.
- [`cubist38/mlx-openai-server#216`](https://github.com/cubist38/mlx-openai-server/pull/216): stable tool-call IDs across streaming deltas.
- [`cubist38/mlx-openai-server#218`](https://github.com/cubist38/mlx-openai-server/pull/218): function-parameter extraction and opener-tail buffering.
- [`cubist38/mlx-openai-server#219`](https://github.com/cubist38/mlx-openai-server/pull/219): mixed-think reasoning handoff and stream re-entry.
- [`cubist38/mlx-openai-server#220`](https://github.com/cubist38/mlx-openai-server/pull/220): Step3.5 compatibility and non-stream tool fallback.
- [`cubist38/mlx-openai-server#223`](https://github.com/cubist38/mlx-openai-server/pull/223): configurable default `min_p`.
- [`cubist38/mlx-openai-server#224`](https://github.com/cubist38/mlx-openai-server/pull/224): prevent reasoning reinjection across APIs.
- [`cubist38/mlx-openai-server#225`](https://github.com/cubist38/mlx-openai-server/pull/225): persist prompt cache after streaming cancellation.
- [`cubist38/mlx-openai-server#237`](https://github.com/cubist38/mlx-openai-server/pull/237): per-model sampling defaults in YAML configuration.
- [`cubist38/mlx-openai-server#250`](https://github.com/cubist38/mlx-openai-server/pull/250): API compatibility fallback contracts.
- [`cubist38/mlx-openai-server#252`](https://github.com/cubist38/mlx-openai-server/pull/252): CLI default parity.
- [`cubist38/mlx-openai-server#254`](https://github.com/cubist38/mlx-openai-server/pull/254): schema-enum cleanup.
- [`cubist38/mlx-openai-server#255`](https://github.com/cubist38/mlx-openai-server/pull/255): streaming cancellation.
- [`cubist38/mlx-openai-server#258`](https://github.com/cubist38/mlx-openai-server/pull/258): omitted-model resolution with non-text fallback.
- [`jundot/omlx#74`](https://github.com/jundot/omlx/pull/74): SSD fallback block registration in paged cache.
- [`jundot/omlx#75`](https://github.com/jundot/omlx/pull/75): second-block SSD failure coverage.
- [`jundot/omlx#76`](https://github.com/jundot/omlx/pull/76): block-metadata rollback after SSD cache-save failure.
- [`jundot/omlx#140`](https://github.com/jundot/omlx/pull/140): streamed tool-call markup leakage and truncation fixes.
- [`jundot/omlx#174`](https://github.com/jundot/omlx/pull/174): bracket-marker streaming suppression edge cases.

### Browser GPU and inference infrastructure

- [`webgpu/webgpu-samples#570`](https://github.com/webgpu/webgpu-samples/pull/570): external Vision Transformer sample with attention visualization.
- [`ggml-org/whisper.cpp#3850`](https://github.com/ggml-org/whisper.cpp/pull/3850): merge split UTF-8 token text in server verbose JSON.

## Active public contributions

- [`ml-explore/mlx-examples#1428`](https://github.com/ml-explore/mlx-examples/pull/1428): Cosmos 3 Nano text-to-video and image-to-video generation for MLX.
- [`webgpu/webgpu-samples#567`](https://github.com/webgpu/webgpu-samples/pull/567): HDR canvas-format fallback.
- [`warmshao/WiLoR-mini#22`](https://github.com/warmshao/WiLoR-mini/pull/22): MPS tensor-layout correctness.
- [`warmshao/WiLoR-mini#23`](https://github.com/warmshao/WiLoR-mini/pull/23): avoid the MPS bfloat16 cross-kernel path in rotation conversion.
- [`continuedev/continue#12516`](https://github.com/continuedev/continue/pull/12516): preserve adapter endpoint routing during CLI stream retries.
- [`BerriAI/litellm#28746`](https://github.com/BerriAI/litellm/pull/28746): preserve input-file blocks while lowering Responses tool output.
