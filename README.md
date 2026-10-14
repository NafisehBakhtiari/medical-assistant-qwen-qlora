# Medical Assistant: Fine-tuning Qwen2.5 with QLoRA

Fine-tuning Qwen2.5-3B-Instruct for medical question answering with QLoRA on a free Colab T4 GPU, built with Hugging Face `transformers`, `datasets`, `peft`, and `bitsandbytes`.

## Results (MedQA, 1,273 USMLE test questions)

| Model | Accuracy |
|---|---|
| Qwen2.5-1.5B (base) | 42.8% |
| Qwen2.5-1.5B + QLoRA | 45.5% |
| Qwen2.5-3B (base) | 50.0% |
| **Qwen2.5-3B + QLoRA** | **52.6%** |

Both fine-tuning gains are statistically significant (McNemar test, p < 0.05). Scaling the model added ~7 points, while fine-tuning added ~2.5 points.

## Data

~16k cleaned examples from MedQA, MedMCQA, and Medical Meadow WikiDoc (Hugging Face Hub).

## Future work

Chain-of-thought training, distillation from stronger models, and extension to medical images.

> Educational project only. Not for clinical use.
