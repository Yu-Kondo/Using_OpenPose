# Using_OpenPose
OpenPoseで画像および動画を解析

## 1) OpenPoseを指定する
cd C:\openpose-1.7.0-binaries-win64-cpu-python3.7-flir-3d

cd openpose

## 2) 画像解析
“media”フォルダ内の画像全てを解析し，”output_folder”に保存する場合を例にして記載

・解析したい画像を”media”内に保存する

・解析したい画像を指定する場合は”media\ 画像名”を記載。なお，拡張子（.jpeg, .png）まで記載することを忘れずに。

### 解析画像保存
.\bin\OpenPoseDemo.exe --image_dir .\examples\media\ --write_images .\output_folder\

### 解析画像保存 + 座標（jsonデータ）出力
.\bin\OpenPoseDemo.exe --image_dir .\examples\media\ --write_json outputpath

## 3) 動画解析
”video_name”に解析する動画，“save_folder_name”に保存名を記載する。
### 解析動画保存
bin\OpenPoseDemo.exe --video examples\media\**video_name**.mp4 --write_video .\output_folder\

### 解析動画保存 + データ出力
bin\OpenPoseDemo.exe --video examples\media\**video_name**.mp4 --write_video .avi --write_json **save_folder_name**

## 4) Webカメラ
bin\OpenPoseDemo.exe

## その他コマンド
a) 解析画質調整：GPUではスペックの問題で解析する際の画質を下げなくてはならないことがある※作成者のPCにおける最高画質（496x320）を設定。※16の倍数で画質は設定可能。

--net_resolution “496x320”

b) 解析人数調整：”1”の部分に解析人数を指定する

--number_people_max 1
