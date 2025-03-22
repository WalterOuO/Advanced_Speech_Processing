## 2024 NTHU COM 621000 Advanced Topics in Speech Applications 進階語音訊號處理 Lab 3
This is a folder to record Lab3 of Advanced Topics in Speech Applications, Lab3 mainly focus on Text to Speech (TTS) and Voice Conversion (VC).  
The main task of Lab3 is to convert a source voice sound to be like target voice, including converting male voice and female voice.  

### Voice Conversion Introduction  
The fundamental concept of voice conversion is simple, voice can be disentangled to speaker embedding and content embedding, using speaker embedding from target to sythesize with the source content embedding can generate a converted audio that sounds like target's voice but using the content from source. 

![Voice Conversion](https://github.com/user-attachments/assets/0bbdaa71-b12e-4d5b-b0fc-edb4e354f3b8)


### Dataset Information  
| Training set | Source Audio | Target Audio |  
| ------------ | ------------ | ------------ |  
| VCTK Corpus | VCTK Corpus (Female) | Zundamon Japanese Dataset (Female) |  
| VCTK Corpus + Our own voice (Male) | Our own voice (Male) | Zundamon Japanese Dataset (Female) |  


### Methods
For
