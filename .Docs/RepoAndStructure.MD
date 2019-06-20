# Repo & Structure

Explan the main function & structure of this AI kernel system.

## Repository

```
AI Kernel (Graduated-Project) 
├── Chinese-Speech-Emotion-Datasets    - The datasets used by this system. 
├── Speech-Dataset-in-scikit-learn    - Calling algorithms in scikit-learn library for research purpose. 
├── Virtual-Elderly-Chatbot-App    - Unity project for create client APPs used.
├── Virtual-Elderly-Chatbot-IOS-Project    - The Xcode project build from Unity Project. 
└── Virtual-Elderly-Chatbot-Server-Structure    - The main server of this AI kernel service.
     ├── NoTag                        - The pure ChatBot. 
     │     ├── AWWW_chatbot_response.py    - Function of chatbot interaction reply. 
     │     ├── AWWW_jiebaCut.py    - Function of sentence split to words applied on Chinese language.
     │     ├── AWWW_pic_pred.py    - Function of speech spectrogram for NVidia DIGITS to predict the emotions. 
     │     ├── AWWW_wav_to_STT.py    - Function of using Google Speech API to perform speech to text job. 
     │     ├── AWWW_wav_to_spectro.py    - Function of making wav speech sound to spectrogram for NVidia DIGITS. 
     │     └── AWWW_web.py    - Main web server for AI kernel API.
     └── WithTag                        - The emotion added ChatBot.  
            ├── AWWW_chatbot_response.py    - Function of chatbot interaction reply. 
            ├── AWWW_jiebaCut.py    - Function of sentence split to words applied on Chinese language. 
            ├── AWWW_pic_pred.py    - Function of speech spectrogram for NVidia DIGITS to predict the emotions.    
            ├── AWWW_wav_to_STT.py    - Function of using Google Speech API to perform speech to text job.    
            ├── AWWW_wav_to_spectro.py    - Function of making wav speech sound to spectrogram for NVidia DIGITS. 
            └── AWWW_web.py    - Main web server for AI kernel API.
```

## System Structure

`=================================Separate=Line========================================`

# リポジトリと構造

このAI kernelシステムのメイン構造と機能を説明する。

## リポジトリ

```
AI Kernel (Graduated-Project) 
├── Chinese-Speech-Emotion-Datasets    - 
├── Speech-Dataset-in-scikit-learn    - 
├── Virtual-Elderly-Chatbot-App    - 
├── Virtual-Elderly-Chatbot-IOS-Project    - 
└── Virtual-Elderly-Chatbot-Server-Structure    - 
     ├── NoTag    - 
     │     ├── AWWW_chatbot_response.py    - 
     │     ├── AWWW_jiebaCut.py    - 
     │     ├── AWWW_pic_pred.py    - 
     │     ├── AWWW_wav_to_STT.py    - 
     │     ├── AWWW_wav_to_spectro.py    - 
     │     └── AWWW_web.py    - 
     └── WithTag 
            ├── AWWW_chatbot_response.py    - 
            ├── AWWW_jiebaCut.py    - 
            ├── AWWW_pic_pred.py    -    
            ├── AWWW_wav_to_STT.py    -    
            ├── AWWW_wav_to_spectro.py    - 
            └── AWWW_web.py    - 
```

## システムの構造

`====================================キリ=セン==========================================`

# GitHub源與架構

本文件將解釋AI kernel系統的構造與相關功能。

## GitHub源

```
AI Kernel (Graduated-Project) 
├── Chinese-Speech-Emotion-Datasets    - 
├── Speech-Dataset-in-scikit-learn    - 
├── Virtual-Elderly-Chatbot-App    - 
├── Virtual-Elderly-Chatbot-IOS-Project    - 
└── Virtual-Elderly-Chatbot-Server-Structure    - 
     ├── NoTag    - 
     │     ├── AWWW_chatbot_response.py    - 
     │     ├── AWWW_jiebaCut.py    - 
     │     ├── AWWW_pic_pred.py    - 
     │     ├── AWWW_wav_to_STT.py    - 
     │     ├── AWWW_wav_to_spectro.py    - 
     │     └── AWWW_web.py    - 
     └── WithTag 
            ├── AWWW_chatbot_response.py    - 
            ├── AWWW_jiebaCut.py    - 
            ├── AWWW_pic_pred.py    -    
            ├── AWWW_wav_to_STT.py    -    
            ├── AWWW_wav_to_spectro.py    - 
            └── AWWW_web.py    - 
```

## 系統架構
