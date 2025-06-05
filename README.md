# Fine-Tuning-Language-Models-with-Custom-Dataset-Splits-on-Colab
This code fine-tunes a language model using multiple pre-split datasets (`cot`, `tir`, `genselect`, and `additional_problems`). It leverages Hugging Face Transformers and PEFT for efficient training on Google Colab.


## 🔧 Features

- Uses Hugging Face Transformers and Datasets.
- Processes `.parquet` files for training and evaluation.
- Supports multiple custom dataset splits.
- Suitable for Colab TPU/accelerator-based fine-tuning.

## 📂 Dataset Splits

The dataset is divided into:
- `cot`: Chain-of-thought examples
- `tir`: Task-instruction-response data
- `genselect`: General selection tasks
- `additional_problems`: Supplementary data

⚠️ **Note**: During training, an error was encountered for the `train` split because it is not a recognized split. Ensure only supported splits (`cot`, `tir`, `genselect`, `additional_problems`) are used.

## 💾 Disk Usage

The Colab runtime encountered a **"Disk Full"** issue due to large datasets. Although the disk was full, **the entire code worked without any errors** up to that point. You may need to mount Google Drive or upgrade runtime storage for longer runs.

## 🚀 Getting Started

Clone and run in Google Colab:
```python
!pip install transformers datasets peft
# Upload datasets and run cells in sequence
