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

```
┌─────────────────┐　　　┌─────────────────────────────────────────┐ 
│　Ｓｍａｒｔ　Ｐｈｏｎｅ　ＡＰＰ　│　　　│　Ｓｅｒｖｅｒ　　　　　　　　　　　　　　│ 
│　　　　　　　　　　　　　　　　　│　　　│　　　　　　　　　　　　　　　　　　　　　│ 
│　┌────────┐　　　　　　│　　　│　　┌─────────────┐ 
│　│　　　　　　　　│　　　　　　│　　　│　　│　Ｆｌａｓｋ　Ｓｅｒｖｅｒ 
│　│　Ｓｐｅｅｃｈ　│　　　　　　│　　　│　　│ 
│　│　Ｒｅｃｏｒｄ　│＝＝＝＝＝＞│＝＝＞│＝＞│ 
│　│　Ｕｐｌｏａｄ　│　　　　　　│　　　│　　│ 
│　│　　　　　　　　│　　　　　　│　　　│ 
│　└────────┘　　　　　　│　　　│ 
│ 
│ 
│ 
│ 
└────┘ 
 ```
 
┌┐─│━┃┏┓┗┛ 
└┘


`=================================Separate=Line========================================`

# リポジトリと構造

このAI kernelシステムのメイン構造と機能を説明する。

## リポジトリ

```
AI Kernel (Graduated-Project) 
├── Chinese-Speech-Emotion-Datasets    - このシステムを使うの訓練資料。　
├── Speech-Dataset-in-scikit-learn    - scikit-learnのライブラリを使って、研究の為に色んなアルゴリズムを実行する。　
├── Virtual-Elderly-Chatbot-App    - クライアントのアプリを作る、Unityのプロジェクト。　
├── Virtual-Elderly-Chatbot-IOS-Project    - UnityのプロジェクトをビルドしたのXcodeプロジェクト。　
└── Virtual-Elderly-Chatbot-Server-Structure    - このAI Kernelサービスのメインプログラム。　
     ├── NoTag                        - 普通のチャットボット。　
     │     ├── AWWW_chatbot_response.py    - チャットボットの返事を出る機能。　
     │     ├── AWWW_jiebaCut.py    - 中国語の対話を単語するの機能。　
     │     ├── AWWW_pic_pred.py    - スペクトログラム画像をNVidia DIGITSに感情を分別するの機能。　
     │     ├── AWWW_wav_to_STT.py    - Google Speech APIを利用して、音声資料を文字に変換する機能。　
     │     ├── AWWW_wav_to_spectro.py    - NVidia DIGITSを使うために、音声データをスペクトログラム画像に変換する機能。　
     │     └── AWWW_web.py    - AI kernelのメインウェブサービスのアプリケーションプログラミングインタフェース。　
     └── WithTag                        - 感情認識が付きのチャットボット。　
            ├── AWWW_chatbot_response.py    - チャットボットの返事を出る機能。　 
            ├── AWWW_jiebaCut.py    - 中国語の対話を単語するの機能。　
            ├── AWWW_pic_pred.py    - スペクトログラム画像をNVidia DIGITSに感情を分別するの機能。　
            ├── AWWW_wav_to_STT.py    - Google Speech APIを利用して、音声資料を文字に変換する機能。　   
            ├── AWWW_wav_to_spectro.py    - NVidia DIGITSを使うために、音声データをスペクトログラム画像に変換する機能。　
            └── AWWW_web.py    - AI kernelのメインウェブサービスのアプリケーションプログラミングインタフェース。　
```

## システムの構造

`====================================キリ=セン==========================================`

# GitHub源與架構

本文件將解釋AI kernel系統的構造與相關功能。

## GitHub源

```
AI Kernel (Graduated-Project) 
├── Chinese-Speech-Emotion-Datasets    - 此系統所使用的訓練資料集。 
├── Speech-Dataset-in-scikit-learn    - 調用Python的scikit-learn進行部分演算法訓練，初步研究用。 
├── Virtual-Elderly-Chatbot-App    - 使用Unity所建置客戶端程式的專案。 
├── Virtual-Elderly-Chatbot-IOS-Project    - 由Unity編譯與建置出的Xcode專案，為產生IOS手機程式用。
└── Virtual-Elderly-Chatbot-Server-Structure    - 產生本AI kernel所必須的主程式。
     ├── NoTag                        - 純粹的聊天機器人。 
     │     ├── AWWW_chatbot_response.py    - 提供聊天機器人產生回覆的程式。 
     │     ├── AWWW_jiebaCut.py    - 結巴斷詞，將整個中文句子進行斷詞以供聊天機器人作動。 
     │     ├── AWWW_pic_pred.py    - 將聲紋圖經由本程式傳至NVidia DIGITS進行情感判別。 
     │     ├── AWWW_wav_to_STT.py    - 利用Google Speech API所提供的服務進行語音轉文字的功能。 
     │     ├── AWWW_wav_to_spectro.py    - 將錄製的語音檔轉換成聲紋圖給NVidia DIGITS使用的功能。 
     │     └── AWWW_web.py    - 產AI kernel的主要API服務的網頁伺服器主程式。 
     └── WithTag                        - 具備感情偵測的聊天機器人。 
            ├── AWWW_chatbot_response.py    - 提供聊天機器人產生回覆的程式。 
            ├── AWWW_jiebaCut.py    - 結巴斷詞，將整個中文句子進行斷詞以供聊天機器人作動。 
            ├── AWWW_pic_pred.py    - 將聲紋圖經由本程式傳至NVidia DIGITS進行情感判別。 
            ├── AWWW_wav_to_STT.py    - 利用Google Speech API所提供的服務進行語音轉文字的功能。
            ├── AWWW_wav_to_spectro.py    - 將錄製的語音檔轉換成聲紋圖給NVidia DIGITS使用的功能。 
            └── AWWW_web.py    - 產AI kernel的主要API服務的網頁伺服器主程式。 
```

## 系統架構
