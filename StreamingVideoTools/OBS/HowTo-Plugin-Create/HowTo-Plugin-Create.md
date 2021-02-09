# OBS Pluginのつくりかた
https://obsproject.com/wiki/Getting-Started-with-OBS-Studio-Development


### Windowsの場合
https://github.com/obsproject/obs-studio/wiki/install-instructions#windows-build-directions

※バージョンについては公式Wikiを参照すること

- Git
- Visual Studio 2019
- CMake
- Qt (https://www.qt.io/download-open-source)
もう一つ、OBSがまとめてくれている`FFmpeg`, `x264`, `cURL`, `mbedTLS` をダウンロード
(場所は [Wiki](https://github.com/obsproject/obs-studio/wiki/install-instructions#windows-build-directions) をちゃんと読む)

#### 1. OBSのプロジェクトを落とす

Gitからプロジェクトをクローン
```
git clone --recursive --filter=blob:none https://github.com/obsproject/obs-studio.git
```


#### 2. CMakeのGUIからビルド
「Where is the source code」にクローンしたobs
-studioリポジトリのパス

「Where to build the binaries」に「<クローンしたobs
-studioリポジトリのパス>\\build」

※「build」フォルダを作っておく

その後、「Add Entry」から以下を設定する:

| Name | Type | Value | Example |
| --- | ---- | ---- | ---- |
| DepsPath | Path | OBSがまとめてくれている`FFmpeg`, `x264`, `cURL`, `mbedTLS` のパス | `D:/Project/obs-studio/cmbuild/win64` |
| QTDIR | Path | Qtのルートパス | `D:\Qt\5.15.2\msvc2019_64` |
| CEF_ROOT_DIR | Path | Chrominiumのパス | `D:/Project/obs-studio/cmbuild/cef/x64` |

そのあとは「Configure」でCMakeの設定を読み込ませて「Generate」でVisual Studioのプロジェクトを作ってもらう。

#### TroubleShooting

##### Qt
Qtの落とし方: https://obsproject.com/forum/threads/qt-msvc-package-for-visual-studio-2019.135923/

Qtはオープンソースプロジェクトに対して、無料で公開してくれているのでそれをダウンロードします。

ダウンロードする際、Qtのバージョン + Visual Studioのバージョンを合わせたパッケージをダウンロードする必要があります

![Qt-Download](./img/Qt-Download-Select.gif)


##### Pythonをさがそうとしている

```
CMake Warning (dev) at D:/Program Files/CMake/share/cmake-3.19/Modules/FindPackageHandleStandardArgs.cmake:426 (message):
  The package name passed to `find_package_handle_standard_args` (Python)
  does not match the name of the calling package (PythonDeps).  This can lead
  to problems in calling code that expects `find_package` result variables
  (e.g., `_FOUND`) to follow a certain pattern.
Call Stack (most recent call first):
  cmake/Modules/FindPythonDeps.cmake:61 (find_package_handle_standard_args)
  deps/obs-scripting/CMakeLists.txt:47 (find_package)
This warning is for project developers.  Use -Wno-dev to suppress it.
```

未解決。
- [OBS Build Error in CMmake | OBS Forums](https://obsproject.com/forum/threads/obs-build-error-in-cmmake.125622/)


##### VirtualCam GUID not set! VirtualCam disabled.

```
VirtualCam GUID not set! VirtualCam disabled.
```
> 公式リリースの仮想カメラとDirectShowリストで競合しないように、各フォークには独自のGUIDが必要なようです。

> 1. このサイトにアクセスする。
> ※「Uppercase」と「Hyphens」を有効にしてから「Generate」をクリック
> 2. 生成されたテキストを cmake変数VIRTUALCAM_GUID に設定する。

- [OBS Studio 26.0 で実装された 仮想カメラ(Virtual Camera) に関して - すたいるのメモ帳ブログ](https://style1925.hateblo.jp/entry/obs-virtual-camera)



### Could NOT find LibVLC (missing: VLC_INCLUDE_DIR)

```
Could NOT find LibVLC (missing: VLC_INCLUDE_DIR)
```

未解決。
