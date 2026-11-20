# Glossary

| Term | Meaning |
| --- | --- |
| ARC-16 | The 16-token vocabulary (digits 0–9, newline, user, assistant, padding, message start, message end) and the Qwen3.8-27B base cut down to it. |
| SDG | Synthetic data generation. |
| Stage 2/3, Stage 4 | Generation stages, numbered as in NVARC. Stage 1 writes rule summaries of ARC training tasks and book specs. Stage 2/3 mixes two summaries into a new rule and writes and tests its input generator. Stage 4 writes independent output programs and keeps puzzles on which they agree. |
| TIR | Tool-integrated reasoning: the NVARC-style pipeline in which GPT-OSS-120B writes and runs Python while generating puzzles. |
| RD1 | The first production round of that pipeline. IDs such as `rd1_20854` name a generated pair from it. |
| INSP*n* | Numbered book-inspiration SDG rounds (INSP4, INSP11, INSP16, …). A letter suffix such as INSP16A marks a batch within a round. |
| `_075` / `_025` | The two disjoint partitions (about 75% and 25%) of each synthetic dataset, used in different training phases. |
| src11plus16abcd | Name of the final training mixture, used in the released dataset and model slugs. The [production record](training/production.md) lists its contents. |
| TTFT | Test-time fine-tuning: a per-puzzle LoRA trained on that puzzle's demonstration pairs before sampling. |
| WSD | Warmup–stable–decay learning-rate schedule. |
| MXFP8 | 8-bit microscaling floating-point format used for part of training. |
| GPTQ, W4/W8 | Post-training weight quantization and the 4-bit or 8-bit weight widths used for Kaggle. |
| Flash-Next | Qwen3.8-Flash-Next, the mixture-of-experts model used in the blend. |
| REAP448 | The public Flash-Next checkpoint pruned with REAP (Router-weighted Expert Activation Pruning) to 448 of 512 routed experts per layer. |
| po352 | Our further pruned Flash-Next with 352 routed experts per layer. The blend notebook's name says `po358`; its attached weights are po352. |
| Rule A | The blend's rule for which 27B outputs Flash-Next re-solves and when its answer replaces the 27B answer. See [flash_rule_a.py](inference/flash/flash_rule_a.py). |
| fnt07cs72 | Name of the Flash harness configuration used by the blend. |
| r*MMDD* | Date tags such as `r1026` (26 October) kept in some asset and file names. |
