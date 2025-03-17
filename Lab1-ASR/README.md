## 2024 NTHU COM 621000 Advanced Topics in Speech Applications 進階語音訊號處理 Lab 1  
This is a folder to record Lab1 of Advanced Topics in Speech Applications, Lab1 mainly focus on Automatic Speech Reconition(ASR).  
The main task of Lab1 is to finetune Whisper model with VCTK dataset, our group get the final WER = 18.71% .  

### Dataset Information
| Training Set | Testing set |  
| ---- | ------ |  
| VCTK Corpus | IEMOCAP Session1 |  

### Methods
#### Preprocessing
| Dataset Observation | Response |  
| ---- | ------ |  
| Volume Difference | Volume Normalization |  
| Silence in Sentence | Silence Segment Removal |  
| Different Gender in Dataset | Voice Conversion |  
| Sentence number Difference | Inconsistent File Removal |  

#### Parameter tuning
Tuning learning_rate, weight_decay, warmup_steps, batch_size for lower WER.

#### Post-processing
1. Remove punctuation
2. Text normalization: 4 to four
These post-processing methods overall reduces the WER by 3%
