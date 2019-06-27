# Caffe Install

The Caffe installation is to support NVidia DIGIS to work propoly.

Due to OpenBLAS also required for Caffe installation, it needs to be install first.

## Install OpenBLAS

Download OpenBLAS from it's official github site.

`git clone https://github.com/xianyi/OpenBLAS.git`

```bash
root@HOSTNAME:~# git clone https://github.com/xianyi/OpenBLAS.git
Cloning into 'OpenBLAS'...
remote: Enumerating objects: 92, done.
remote: Counting objects: 100% (92/92), done.
remote: Compressing objects: 100% (79/79), done.
remote: Total 37557 (delta 62), reused 17 (delta 13), pack-reused 37465
Receiving objects: 100% (37557/37557), 23.96 MiB | 4.72 MiB/s, done.
Resolving deltas: 100% (29831/29831), done.
Checking connectivity... done.
Checking out files: 100% (9159/9159), done.
```

Install needed compiler for the build.

`~# apt install build-essential cmake gfortran`

Then follow the official instrouction to build and install.

```bash
~# cd OpenBLAS/
~# mkdir build
~# cd build
~# cmake ..
~# make install 
```

## Install Caffe

`==================================Split-Line===========================================`

# Caffeのインストール

CaffeはNVidia DIGISのインストールをサポートの為に必要です。

後はもしCaffeをインストールするの場合は、OpenBLASが必要です。

## OpenBLASをインストール

OpenBLASの公式GitHubサイトからダウンロードする。

`git clone https://github.com/xianyi/OpenBLAS.git`

```bash
root@HOSTNAME:~# git clone https://github.com/xianyi/OpenBLAS.git
Cloning into 'OpenBLAS'...
remote: Enumerating objects: 92, done.
remote: Counting objects: 100% (92/92), done.
remote: Compressing objects: 100% (79/79), done.
remote: Total 37557 (delta 62), reused 17 (delta 13), pack-reused 37465
Receiving objects: 100% (37557/37557), 23.96 MiB | 5.08 MiB/s, done.
Resolving deltas: 100% (29831/29831), done.
Checking connectivity... done.
Checking out files: 100% (9159/9159), done.
```

必要なコンパイラを用意する。

`~# apt install build-essential cmake gfortran`

そうして、公式の手順で実行する。

```bash
~# cd OpenBLAS/
~# mkdir build
~# cd build
~# cmake ..
~# make install 
```

## Caffeをインストール

`==================================キリカエ-セン=========================================`

# Caffe 安裝

Caffe的安裝是用來支援NVidia DIGIS的使用。

此外由於Caffe需要OpenBLAS為相依套件才有辦法安裝。

## OpenBLAS 安裝

將OpenBLAS由官方GitHub源下載與取得

`git clone https://github.com/xianyi/OpenBLAS.git`

```bash
root@HOSTNAME:~# git clone https://github.com/xianyi/OpenBLAS.git
Cloning into 'OpenBLAS'...
remote: Enumerating objects: 92, done.
remote: Counting objects: 100% (92/92), done.
remote: Compressing objects: 100% (79/79), done.
remote: Total 37557 (delta 62), reused 17 (delta 13), pack-reused 37465
Receiving objects: 100% (37557/37557), 23.96 MiB | 4.89 MiB/s, done.
Resolving deltas: 100% (29831/29831), done.
Checking connectivity... done.
Checking out files: 100% (9159/9159), done.
```

安裝所需套件，準備好環境：

`~# apt install build-essential cmake gfortran`

接著依照官方提供的步驟進行安裝。

```bash
~# cd OpenBLAS/
~# mkdir build
~# cd build
~# cmake ..
~# make install 
```

## 安裝 Caffe
