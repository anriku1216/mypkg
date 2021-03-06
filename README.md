# Ros mypkg

4セメスター課題2

---

# 内容

講義で作成したものを編集し作成した。

- 1秒ごとに、2秒たったら4、3秒たったら9と秒数の二乗の数が表示されます。未来の青い猫型ロボットの話に出てくる道具"バイバイン"のような挙動をみることができます。

---
# 環境

- ROS Noetic

- Raspberry Pi 4 Model B

- Ubuntu 20.04.1 LTS

---

# ビルド

## インストール方法

- [ros setup scripts Ubuntu20.04 server](http://github.com/ryuichiueda/ros_setup_scripts_Ubuntu20.04_server)を参照しROSをインストールする。

- [ロボットシステム学第10回](http://ryuichiueda.github.io/robosys2020/lesson10_ros.html#/)を参照しワークスペースを作成する。

- `git`を使用して本パッケージをダウンロードする。

```bash
cd ~/catkin_ws/src
git clone https://github.com/anriku1216/mypkg.git
```
- `catkin_make`をして本パッケージをビルドする。

```bash
cd ~/catkin_ws && catkin_make
```

## パッケージ概要

### [topic.launch](http://github.com/anriku1216/mypkg/blob/main/launch/topic.launch)

- [count.py](https://github.com/anriku1216/mypkg/blob/main/scripts/count.py)のノードから送られた数値を[twice.py](https://github.com/anriku1216/mypkg/blob/main/scripts/twice.py)で二乗して表示するlaunchファイルです。

- 次のコマンドで起動します。

```bash
roslaunch mypkg topic.launch
```

- 個別で実行する場合には以下のコマンドを別々の端末で実行する。

```bash
roscore
rosrun mypkg count.py
rosrun mypkg twice.py
```

## デモ動画

YouTubeにあげた動画は[こちら](https://www.youtube.com/watch?v=abFqEAe6-9c)。

## 著者

[Rikuto Andou](http://github.com/anriku1216)

ROSセットアップに関して:
[Ryuichi Ueda](http://github.com/ryuichiueda)

## ライセンス

[BSD 3-Clause "New" or "Revised" License](http://github.com/anriku1216/mypkg/blob/main/LICENSE)
