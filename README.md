# 🧠 IDUnlearn-Bench

## 📄 Paper

**What Does It Mean to Forget a Person? Individual-Level Unlearning in Vision-Language Models**

[![arXiv](https://img.shields.io/badge/arXiv-2609.33481-b31b1b.svg)](https://arxiv.org/abs/2609.33481)

[model checkpoints](https://huggingface.co/wutt6678/collections)

## 📌 Overview

**IDUnlearn-Bench** is a benchmark for evaluating **individual-level multimodal unlearning** in Vision-Language Models (VLMs).

Built upon the individual-level multimodal data introduced in **MultiPriv**, IDUnlearn-Bench extends the evaluation from privacy reasoning to **identity-level forgetting**, asking whether a model can still access, associate, or reconstruct a target individual after unlearning.

The benchmark evaluates four complementary task families:

- **Attribute Access (AA):** retrieving target-related attributes from identity cues.
- **Identity Access (IA):** identifying the target from attributes, records, or visual evidence.
- **Identity Binding (IB):** determining whether different observations belong to the same individual.
- **Identity Reconstruction (IR):** reconstructing the target identity from multiple relational or multimodal clues.

## 📊 Dataset

IDUnlearn-Bench contains **60 synthetic individuals** with multimodal identity evidence, including biometric information, personal records, contextual observations, relationships, and textual attributes.

```text
dataset/
├── person_1/ ... person_60/   (60 subjects, identical layout)
    ├── A1.png
    ├── A1_face_aug_{01..05}.png
    ├── A2.png
    ├── A2_fingerprint_aug_{01..03}.png
    ├── B.png, B_mask.png
    ├── C.png, C_mask.png
    ├── D1.png, D1_mask.png
    ├── D2.png
    ├── D3.png, D3_mask.png
    ├── E.png, E_mask.png
    ├── F.png, F_mask.png
    ├── H.png
    ├── bench_VQA.json
    ├── finetune_VQA.json
    └── person_XX.json
```


## 📣 Citation

If you find **IDUnlearn-Bench** useful in your research, please cite:

```bibtex
@article{sun2026forget,
  title={What Does It Mean to Forget a Person? Individual-Level Unlearning in Vision-Language Models},
  author={Sun, Xiongtao and Li, Hui and Wu, Tiantong and Zhang, Jiaming and Zhang, Fuyao and Tan, Wen Jun},
  journal={arXiv preprint arXiv:2609.33481},
  year={2026}
}

