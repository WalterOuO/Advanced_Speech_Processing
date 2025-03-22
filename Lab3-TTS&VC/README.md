## 2024 NTHU COM 621000 Advanced Topics in Speech Applications 進階語音訊號處理 Lab 3
This is a folder to record Lab3 of Advanced Topics in Speech Applications, Lab3 mainly focus on Text to Speech (TTS) and Voice Conversion (VC).  
Lab3 is a self-surpervised learning task to convert a source audio file to sound like target voice, including converting male voice and female voice.  
The model used in this conversion task is [FreeVC](https://github.com/OlaWod/FreeVC).


### Voice Conversion Introduction  
The fundamental concept of voice conversion is simple, voice can be disentangled to speaker embedding and content embedding, using speaker embedding from target to sythesize with the source content embedding can generate a converted audio that sounds like target's voice but using the content from source. 
![Voice Conversion](https://github.com/user-attachments/assets/ebb189ac-6bb9-4ff3-94ae-2a84f7ba9df4)

![Voice Conversion](https://github.com/user-attachments/assets/0bbdaa71-b12e-4d5b-b0fc-edb4e354f3b8){ width=200 }


### Dataset Information  
| Training set | Source Audio | Target Audio |  
| ------------ | ------------ | ------------ |  
| VCTK Corpus | VCTK Corpus (Female) | Zundamon Japanese Dataset (Female) |  
| VCTK Corpus + Our own voice (Male) | Our own voice (Male) | Zundamon Japanese Dataset (Female) |  


### Methods
1. Data Augmentation
   We added our own recorded voice using parellel text to the training dataset, trying to let neural network see more voice characteristics.   
2. Pitch shift and Speed Change
3. Using [s3prl](https://github.com/s3prl/s3prl) model to replace FreeVC model.


### Experiences  
When converting a **Male** source to a **Female** target, F0 pitch shifting can make significant effect on sythesis result.  
It is recommended to shift the average F0 of source to the average F0 of target, leading to more ideal conversion performance.  
However, the skills of a person cannot be converted, in the disentanglement part, the skills or the way of speaking from source will be seperated into content embedding, so source's skills will be included when sythesized with target speaker embedding.  
