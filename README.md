# Fine-tuning Carbon-X on DNA Tasks
HuggingFace recently released a latest addition to their DNA language model family Carbon, created by mid-training + post-training Qwen-14B. This repo takes a mid-trained checkpoint of the new [Carbon-X](https://huggingface.co/HuggingFaceBio/Carbon-X-Base) and runs SFT + GRPO on it using the [FineDNA dataset](https://huggingface.co/datasets/HuggingFaceBio/FineDNA).

## The tasks we teach
We restrict ourselves to the following tasks:
- **Sequence classification:** identifying properties or categories of DNA sequences, including taxonomic groups.
- **DNA computation:** tasks such as counting, sequence manipulation, and recognizing patterns or motifs.
- **Biology question answering:** answering multiple-choice questions about biology.

SFT draws from FineDNA's sequence-classification and DNA-computation configurations. GRPO candidates come from its `rl_mix` configuration.

For the original model, training recipes, and evaluation tools, see the [Carbon repository](https://github.com/huggingface/carbon/tree/main/carbon-x) and [Carbon-X release](https://huggingface.co/spaces/HuggingFaceBio/Carbon-X-Release).
