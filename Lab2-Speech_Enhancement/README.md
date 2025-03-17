## 2024 NTHU COM 621000 Advanced Topics in Speech Applications 進階語音訊號處理 Lab 2  
This is a folder to record Lab2 of Advanced Topics in Speech Applications, Lab2 mainly focus on Speech Enhancement.  
The main task of Lab2 is to use the diffusion-based generative model to implement Speech Enhancement and Dereverberation.  
The noise dataset used in this lab is ESC-50, the training set is VCTK Corpus, the testing set is IEMOCAP Session 1.  
The noise is mixed with training set by choosen signal-noise ratio, the clean training set and noisy training set are further used to finetue the SGMSE model with the pretrained checkpoint train_wsj0_2cta4cov_epoch=159.ckpt. The noisy testing set are used for evaluation. 
