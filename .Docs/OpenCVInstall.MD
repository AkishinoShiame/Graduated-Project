# OpenCV Install

The project needs OpenCV as dependency library for Caffe.

As the latest OpenCV has problem to support Caffe, this project choose to use OpenCV 3.4.6, the latest version of OpenCV 3.

First download OpenCV from official Github site using `wget https://github.com/opencv/opencv/archive/3.4.6.zip` command.

```bash
root@HOSTNAME:~# wget https://github.com/opencv/opencv/archive/3.4.6.zip
--2019-06-26 10:49:58--  https://github.com/opencv/opencv/archive/3.4.6.zip
Resolving github.com (github.com)... 192.30.253.113
Connecting to github.com (github.com)|192.30.253.113|:443... connected.
HTTP request sent, awaiting response... 302 Found
Location: https://codeload.github.com/opencv/opencv/zip/3.4.6 [following]
--2019-06-26 10:49:59--  https://codeload.github.com/opencv/opencv/zip/3.4.6
Resolving codeload.github.com (codeload.github.com)... 192.30.253.120
Connecting to codeload.github.com (codeload.github.com)|192.30.253.120|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 92340400 (88M) [application/zip]
Saving to: ‘3.4.6.zip’

3.4.6.zip                 100%[=====================================>]  88.06M  1.85MB/s    in 27s

2019-06-26 10:50:27 (3.32 MB/s) - ‘3.4.6.zip’ saved [92340400/92340400]

root@HOSTNAME:~#
```

Then unzip the package. If it got command not found error, install unzip first.

`unzip 3.4.6.zip`

```bash
root@HOSTNAME:~# unzip 3.4.6.zip
The program 'unzip' is currently not installed. You can install it by typing:
apt install unzip
root@HOSTNAME:~# apt install unzip
Reading package lists... Done
Building dependency tree
Reading state information... Done
Suggested packages:
  zip
The following NEW packages will be installed:
  unzip
0 upgraded, 1 newly installed, 0 to remove and 0 not upgraded.
Need to get 158 kB of archives.
After this operation, 530 kB of additional disk space will be used.
Get:1 http://archive.ubuntu.com/ubuntu xenial/main amd64 unzip amd64 6.0-20ubuntu1 [158 kB]
Fetched 158 kB in 1s (92.2 kB/s)
Selecting previously unselected package unzip.
(Reading database ... 31533 files and directories currently installed.)
Preparing to unpack .../unzip_6.0-20ubuntu1_amd64.deb ...
Unpacking unzip (6.0-20ubuntu1) ...
Processing triggers for mime-support (3.59ubuntu1) ...
Processing triggers for man-db (2.7.5-1) ...
Setting up unzip (6.0-20ubuntu1) ...
root@HOSTNAME:~# unzip 3.4.6.zip
Archive:  3.4.6.zip
33b765d7979fd8a6038026aa44f6ff1a9c082b7b
   creating: opencv-3.4.6/
  inflating: opencv-3.4.6/.editorconfig
   creating: opencv-3.4.6/3rdparty/
   creating: opencv-3.4.6/3rdparty/carotene/
  inflating: opencv-3.4.6/3rdparty/carotene/CMakeLists.txt
  inflating: opencv-3.4.6/3rdparty/carotene/README.md
   creating: opencv-3.4.6/3rdparty/carotene/hal/
  inflating: opencv-3.4.6/3rdparty/carotene/hal/CMakeLists.txt
  inflating: opencv-3.4.6/3rdparty/carotene/hal/tegra_hal.hpp
   creating: opencv-3.4.6/3rdparty/carotene/include/
   creating: opencv-3.4.6/3rdparty/carotene/include/carotene/
  inflating: opencv-3.4.6/3rdparty/carotene/include/carotene/definitions.hpp
  inflating: opencv-3.4.6/3rdparty/carotene/include/carotene/functions.hpp
  inflating: opencv-3.4.6/3rdparty/carotene/include/carotene/types.hpp
   creating: opencv-3.4.6/3rdparty/carotene/src/
  inflating: opencv-3.4.6/3rdparty/carotene/src/absdiff.cpp
  inflating: opencv-3.4.6/3rdparty/carotene/src/accumulate.cpp
  inflating: opencv-3.4.6/3rdparty/carotene/src/add.cpp
  inflating: opencv-3.4.6/3rdparty/carotene/src/add_weighted.cpp
...
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Assets/Tiles/FlipCycleTileSmall.png
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Assets/Tiles/IconicTileMediumLarge.png
 extracting: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Assets/Tiles/IconicTileSmall.png
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/LocalizedStrings.cs
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/MainPage.xaml
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/MainPage.xaml.cs
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/OpenCVXaml.csproj
   creating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Properties/
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Properties/AppManifest.xml
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Properties/AssemblyInfo.cs
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Properties/WMAppManifest.xml
   creating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Resources/
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Resources/AppResources.Designer.cs
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Resources/AppResources.resx
  inflating: opencv-3.4.6/samples/wp8/readme.txt
root@HOSTNAME:~#
```

Then follows the official to install required libraries.

```bash
~# apt install build-essential
~# apt install cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev
~# apt install python-dev python-numpy libtbb2 libtbb-dev libjpeg-dev libpng-dev libtiff-dev libjasper-dev libdc1394-22-dev
```

Finally build & install.

```bash
~# cd opencv-3.4.6/
~# mkdir build
~# cd build
~# cmake -D CMAKE_BUILD_TYPE=Release -D CMAKE_INSTALL_PREFIX=/usr/local ..
~# make -j7
~# make install
```

# OpenCVのインストール

OpenCVはCaffeの依存ライブラリ、その為に必要です。

もし最新版のOpenCVが使えるなら、Caffeはまだサポートされていない、エラーがいっぱい出るから。今回のプロジェクトは最新版のOpenCV 3を使って、OpenCV 3.4.6を選ばれた。

最初はOpenCVの公式Githubサイトからダウンロードする、コマンド`wget https://github.com/opencv/opencv/archive/3.4.6.zip`を使います。

```bash
root@HOSTNAME:~# wget https://github.com/opencv/opencv/archive/3.4.6.zip
--2019-06-26 10:51:45--  https://github.com/opencv/opencv/archive/3.4.6.zip
github.com (github.com) をDNSに問いあわせています... 192.30.253.112
github.com (github.com)|192.30.253.112|:443 に接続しています... 接続しました。
HTTP による接続要求を送信しました、応答を待っています... 302 Found
場所: https://codeload.github.com/opencv/opencv/zip/3.4.6 [続く]
--2019-06-26 10:51:46--  https://codeload.github.com/opencv/opencv/zip/3.4.6
codeload.github.com (codeload.github.com) をDNSに問いあわせています... 140.82.114.9
codeload.github.com (codeload.github.com)|140.82.114.9|:443 に接続しています... 接続しました。
HTTP による接続要求を送信しました、応答を待っています... 200 OK
長さ: 92340400 (88M) [application/zip]
`3.4.6.zip' に保存中

3.4.6.zip                 100%[=====================================>]  88.06M  4.45MB/s    時間 26s

2019-06-26 10:52:14 (3.33 MB/s) - `3.4.6.zip' へ保存完了 [92340400/92340400]

root@HOSTNAME:~#
```

そうしてパッケージを解凍する。　もし、コマンドが見つからないのエラーが出たら、解凍のunzipコマンドを最初にインストールする。

`unzip 3.4.6.zip`

```bash
root@HOSTNAME:~# unzip 3.4.6.zip
プログラム 'unzip' はまだインストールされていません。 次のように入力することでインストールできます:
apt install unzip
root@HOSTNAME:~# apt install unzip
パッケージリストを読み込んでいます... 完了
依存関係ツリーを作成しています
状態情報を読み取っています... 完了
提案パッケージ:
  zip
以下のパッケージが新たにインストールされます:
  unzip
アップグレード: 0 個、新規インストール: 1 個、削除: 0 個、保留: 0 個。
158 kB のアーカイブを取得する必要があります。
この操作後に追加で 530 kB のディスク容量が消費されます。
取得:1 http://archive.ubuntu.com/ubuntu xenial/main amd64 unzip amd64 6.0-20ubuntu1 [158 kB]
158 kB を 2秒 で取得しました (75.5 kB/s)
以前に未選択のパッケージ unzip を選択しています。
(データベースを読み込んでいます ... 現在 31533 個のファイルとディレクトリがインストールされています。)
.../unzip_6.0-20ubuntu1_amd64.deb を展開する準備をしています ...
unzip (6.0-20ubuntu1) を展開しています...
mime-support (3.59ubuntu1) のトリガを処理しています ...
man-db (2.7.5-1) のトリガを処理しています ...
unzip (6.0-20ubuntu1) を設定しています ...
root@HOSTNAME:~# unzip 3.4.6.zip
Archive:  3.4.6.zip
33b765d7979fd8a6038026aa44f6ff1a9c082b7b
   creating: opencv-3.4.6/
  inflating: opencv-3.4.6/.editorconfig
   creating: opencv-3.4.6/3rdparty/
   creating: opencv-3.4.6/3rdparty/carotene/
  inflating: opencv-3.4.6/3rdparty/carotene/CMakeLists.txt
  inflating: opencv-3.4.6/3rdparty/carotene/README.md
   creating: opencv-3.4.6/3rdparty/carotene/hal/
  inflating: opencv-3.4.6/3rdparty/carotene/hal/CMakeLists.txt
  inflating: opencv-3.4.6/3rdparty/carotene/hal/tegra_hal.hpp
   creating: opencv-3.4.6/3rdparty/carotene/include/
   creating: opencv-3.4.6/3rdparty/carotene/include/carotene/
  inflating: opencv-3.4.6/3rdparty/carotene/include/carotene/definitions.hpp
  inflating: opencv-3.4.6/3rdparty/carotene/include/carotene/functions.hpp
～中略～
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Assets/AlignmentGrid.png
 extracting: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Assets/ApplicationIcon.png
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Assets/Lena.png
   creating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Assets/Tiles/
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Assets/Tiles/FlipCycleTileLarge.png
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Assets/Tiles/FlipCycleTileMedium.png
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Assets/Tiles/FlipCycleTileSmall.png
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Assets/Tiles/IconicTileMediumLarge.png
 extracting: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Assets/Tiles/IconicTileSmall.png
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/LocalizedStrings.cs
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/MainPage.xaml
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/MainPage.xaml.cs
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/OpenCVXaml.csproj
   creating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Properties/
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Properties/AppManifest.xml
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Properties/AssemblyInfo.cs
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Properties/WMAppManifest.xml
   creating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Resources/
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Resources/AppResources.Designer.cs
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Resources/AppResources.resx
  inflating: opencv-3.4.6/samples/wp8/readme.txt
root@HOSTNAME:~#
```

そうして、公式手順をフォローする、依存のライブラリをインストールする。

```bash
~# apt install build-essential
~# apt install cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev
~# apt install python-dev python-numpy libtbb2 libtbb-dev libjpeg-dev libpng-dev libtiff-dev libjasper-dev libdc1394-22-dev
```

最後はビルドとインストールする。

```bash
~# cd opencv-3.4.6/
~# mkdir build
~# cd build
~# cmake -D CMAKE_BUILD_TYPE=Release -D CMAKE_INSTALL_PREFIX=/usr/local ..
~# make -j7
~# make install
```

# OpenCV 安裝

此專案需要OpenCV為相依性套件輔助Caffe的安裝與使用。

經測試後已知Caffe的最新版並無法支援到OpenCV4，因此建置本專案請採用OpenCV 3的最新版使用。選擇OpenCV 3.4.6。

首先要從OpenCV的官方GitHub源下載用來編譯與安裝的程式，由`wget https://github.com/opencv/opencv/archive/3.4.6.zip`指令取得。

```bash
root@HOSTNAME:~# wget https://github.com/opencv/opencv/archive/3.4.6.zip
--2019-06-26 10:53:05--  https://github.com/opencv/opencv/archive/3.4.6.zip
正在查找主機 github.com (github.com)... 192.30.253.113
正在連接 github.com (github.com)|192.30.253.113|:443... 連上了。
已送出 HTTP 要求，正在等候回應... 302 Found
位置：https://codeload.github.com/opencv/opencv/zip/3.4.6 [跟隨至新的 URL]
--2019-06-26 10:53:05--  https://codeload.github.com/opencv/opencv/zip/3.4.6
正在查找主機 codeload.github.com (codeload.github.com)... 140.82.113.10
正在連接 codeload.github.com (codeload.github.com)|140.82.113.10|:443... 連上了。
已送出 HTTP 要求，正在等候回應... 200 OK
長度: 92340400 (88M) [application/zip]
Saving to: ‘3.4.6.zip’

3.4.6.zip                 100%[=====================================>]  88.06M  2.61MB/s    in 24s

2019-06-26 10:53:30 (3.69 MB/s) - ‘3.4.6.zip’ saved [92340400/92340400]

root@HOSTNAME:~#
```

接著解壓縮下載下來的檔案。如果有遇到unzip指令找不到的錯誤時，需先安裝。

`unzip 3.4.6.zip`

```bash
root@HOSTNAME:~# unzip 3.4.6.zip
程式 'unzip' 目前尚未安裝。 您可以由輸入以下內容安裝：
apt install unzip
root@HOSTNAME:~# apt install unzip
正在讀取套件清單... 完成
正在重建相依關係
正在讀取狀態資料... 完成
建議套件：
  zip
下列【新】套件將會被安裝：
  unzip
升級 0 個，新安裝 1 個，移除 0 個，有 0 個未被升級。
需要下載 158 kB 的套件檔。
此操作完成之後，會多佔用 530 kB 的磁碟空間。
下載:1 http://archive.ubuntu.com/ubuntu xenial/main amd64 unzip amd64 6.0-20ubuntu1 [158 kB]
取得 158 kB 用了 2秒 (73.2 kB/s)
選取了原先未選的套件 unzip。
（讀取資料庫 ... 目前共安裝了 31533 個檔案和目錄。）
準備解開 .../unzip_6.0-20ubuntu1_amd64.deb ...
解開 unzip (6.0-20ubuntu1) 中...
Processing triggers for mime-support (3.59ubuntu1) ...
Processing triggers for man-db (2.7.5-1) ...
設定 unzip (6.0-20ubuntu1) ...
root@HOSTNAME:~# unzip 3.4.6.zip
Archive:  3.4.6.zip
33b765d7979fd8a6038026aa44f6ff1a9c082b7b
   creating: opencv-3.4.6/
  inflating: opencv-3.4.6/.editorconfig
   creating: opencv-3.4.6/3rdparty/
   creating: opencv-3.4.6/3rdparty/carotene/
  inflating: opencv-3.4.6/3rdparty/carotene/CMakeLists.txt
  inflating: opencv-3.4.6/3rdparty/carotene/README.md
   creating: opencv-3.4.6/3rdparty/carotene/hal/
  inflating: opencv-3.4.6/3rdparty/carotene/hal/CMakeLists.txt
  inflating: opencv-3.4.6/3rdparty/carotene/hal/tegra_hal.hpp
   creating: opencv-3.4.6/3rdparty/carotene/include/
   creating: opencv-3.4.6/3rdparty/carotene/include/carotene/
  inflating: opencv-3.4.6/3rdparty/carotene/include/carotene/definitions.hpp
  inflating: opencv-3.4.6/3rdparty/carotene/include/carotene/functions.hpp
  inflating: opencv-3.4.6/3rdparty/carotene/include/carotene/types.hpp
   creating: opencv-3.4.6/3rdparty/carotene/src/
  inflating: opencv-3.4.6/3rdparty/carotene/src/absdiff.cpp
  inflating: opencv-3.4.6/3rdparty/carotene/src/accumulate.cpp
  inflating: opencv-3.4.6/3rdparty/carotene/src/add.cpp
  inflating: opencv-3.4.6/3rdparty/carotene/src/add_weighted.cpp
～略～
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Assets/Tiles/FlipCycleTileLarge.png
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Assets/Tiles/FlipCycleTileMedium.png
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Assets/Tiles/FlipCycleTileSmall.png
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Assets/Tiles/IconicTileMediumLarge.png
 extracting: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Assets/Tiles/IconicTileSmall.png
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/LocalizedStrings.cs
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/MainPage.xaml
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/MainPage.xaml.cs
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/OpenCVXaml.csproj
   creating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Properties/
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Properties/AppManifest.xml
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Properties/AssemblyInfo.cs
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Properties/WMAppManifest.xml
   creating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Resources/
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Resources/AppResources.Designer.cs
  inflating: opencv-3.4.6/samples/wp8/OpenCVXaml/OpenCVXaml/Resources/AppResources.resx
  inflating: opencv-3.4.6/samples/wp8/readme.txt
root@HOSTNAME:~#
```

接著根據官方提示，安裝所需的相依性套件。

```bash
~# apt install build-essential
~# apt install cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev
~# apt install python-dev python-numpy libtbb2 libtbb-dev libjpeg-dev libpng-dev libtiff-dev libjasper-dev libdc1394-22-dev
```

最後，建置與安裝。

```bash
~# cd opencv-3.4.6/
~# mkdir build
~# cd build
~# cmake -D CMAKE_BUILD_TYPE=Release -D CMAKE_INSTALL_PREFIX=/usr/local ..
~# make -j7
~# make install
```
