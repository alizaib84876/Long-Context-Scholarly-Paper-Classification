# ModernBERT + LoRA for Scholarly Paper Classification

This repository reproduces and improves upon the **NRK at FoRC 2024** system for Field of Research (FoR) classification. The original paper used an ensemble of SciBERT and RoBERTa models. We reproduce the ensemble results and implement a single **ModernBERT model with LoRA adapters** for parameter-efficient fine-tuning and extended input sequences.

## Files

- **replication.ipynb** – Reproduces the baseline ensemble of SciBERT (cased and uncased) models and compares results with the published paper.
- **ModernBert_01.ipynb** – Implements the ModernBERT + LoRA improvement and trains for the first 2 epochs.
- **ModernBert_02.ipynb** – Continues the ModernBERT + LoRA training for the remaining 3 epochs, completing 5 epochs in total.

## Dataset

All experiments use the **FoRC 2024 dataset**, consisting of:
- Training: 41,540 instances  
- Validation: 8,901 instances  
- Test: 8,903 instances  

Each instance contains **Title, Abstract, Authors, Year, and Publisher** fields and is classified into one of **123 FoR categories**.

## Highlights

- Reproduces baseline ensemble results for comparison.
- Implements a **single ModernBERT model** with **LoRA adapters** for efficiency.
- Handles **longer input sequences (1024 tokens)** than standard BERT models.
- Achieves competitive accuracy and weighted F1 scores on the FoRC 2024 dataset.
- Modular notebook structure for replication and experimentation.

## References

- K. Nguyen Tuan and T. Dang Van, *NRK at FoRC 2024 Subtask I: Exploiting BERT-Based Models for Multi-class Classification of Scholarly Papers*, NLSP 2024.  
- [ModernBERT](https://huggingface.co/answerdotai/ModernBERT-base) with LoRA adaptation.
