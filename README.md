# Living CV SmolLM2

A narrow LoRA post-training of `HuggingFaceTB/SmolLM2-360M-Instruct` for Anirudh Somadas's browser CV experiment.

The adapter teaches a compact drawing-plan protocol, grounded portfolio answers, and explicit abstention when verified context cannot establish a fact. Portfolio facts remain in retrieval context and are not intended to be memorized in the weights.

## Evaluation

The 0.2-epoch Apple-MPS pilot scored 96.0% exact match, 96.6% valid drawing plans, and 100% safe abstention on 151 held-out synthetic protocol examples. These narrow results do not measure general model quality. The browser must continue validating drawing commands and grounding factual answers.

## Runtime

The `v0.1.0` GitHub release contains `model_q8.onnx` for Transformers.js / ONNX Runtime. Configuration and tokenizer files are stored in this repository. The quantized model is about 347 MB.

## Base model and license

Derived from [SmolLM2-360M-Instruct](https://huggingface.co/HuggingFaceTB/SmolLM2-360M-Instruct) by Hugging Face. The base model is Apache-2.0 licensed. See `LICENSE` and `NOTICE`.
