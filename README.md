# ECE-GY 7123 Deep Learning Project 2 - Mean Square Terror
by Siddhant Mohan (sm12766@nyu.edu), Akshat Mishra (am15111@nyu.edu) and Jay Daftari (jd5829@nyu.edu).

This project carries out fine-tuning of RoBERTa, an open-source LLM based on BERT, using Low-Rank Adaptation (LoRA). 

Trainable parameters : 937,762 (<1M)

Competed in this [Kaggle competition](https://www.kaggle.com/competitions/deep-learning-spring-2025-project-2/leaderboard) and achieved rank 109. The prediction file achieving this result is ```inference_output.csv```.

The notebook ```roberta_with_lora.ipynb``` contains all code, logs and results.

Project report : ```DeepLearningProject2_sm12766_am15111_jd5829.pdf```

## Hyperparameters
| Category | Hyperparameter | Value |
|:---|:---|:---|
| Data Config | Maximum Token Length | 128 |
| Model Config | LoRA Ranks Across 12 Layers | [8, 8, 8, 8, 16, 16, 16, 16, 32, 32, 32, 32] |
| Model Config | LoRA Alphas Across 12 Layers | [16, 16, 16, 16, 32, 32, 32, 32, 64, 64, 64, 64] |
| Model Config | Target Modules | ['Query'] |
| Training Config | Number of Epochs | 4 |
| Training Config | Total Training Steps | 29,840 |
| Training Config | Logging Steps | 100 |
| Training Config | Train Batch Size | 16 |
| Training Config | Eval Batch Size | 16 |
| Training Config | Dataloader Num Workers | 4 |
| Optimization Config | Learning Rate | 3e-6 |
| Optimization Config | Warmup Ratio | 0.06 |
| Optimization Config | Weight Decay | 0.01 |
| Optimization Config | Optimizer | Adam |
| Optimization Config | Learning Rate Scheduler | Linear |


Final test accuracy : 90.78125%

Unlabeled test dataset accuracy (public) : 85.100%

Unlabeled test dataset accuracy (private) : 84.300%

Training and validation loss v steps
![image](https://github.com/user-attachments/assets/fcbbc273-ae2e-4d68-8e09-64a4c3f99093)

Validation accuracy v steps
![image](https://github.com/user-attachments/assets/c5fb4bf6-37c6-4d29-84c0-a3675a36c913)
