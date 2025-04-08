# Machine-Translation-En-Vi

## Overview  
This project focuses on English-to-Vietnamese machine translation using two popular sequence-to-sequence architectures: a standard **Transformer** model and **mBART-50-large**, a multilingual pretrained model from Facebook AI.

## Models

### 🔹 Transformer Seq2Seq  
A baseline Transformer architecture trained from scratch on English–Vietnamese parallel data. Implements the original encoder-decoder setup as proposed in the "Attention Is All You Need" paper.

### 🔹 mBART-50-large  
A pretrained multilingual encoder-decoder model fine-tuned for En-Vi translation. It benefits from cross-lingual transfer and large-scale unsupervised pretraining, making it more robust on low-resource settings.

---

## Evaluation (SacreBLEU)

| Model              | SacreBLEU Score |
|--------------------|-----------------|
| Transformer        | **28.71**       |
| mBART-50-large     | **42.38**       |

### 📝 Analysis
The mBART-50-large significantly outperforms the baseline Transformer, achieving a **+13.67 BLEU** improvement with only 1 epoch of fine-tuning. This gap highlights the benefit of multilingual pretraining and transfer learning, especially in scenarios where the target language (Vietnamese) has relatively fewer resources. While the Transformer provides a solid foundation, pretrained models like mBART leverage broader language knowledge and generalization capabilities.
