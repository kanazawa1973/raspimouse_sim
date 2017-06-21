# raspimouse_sim 

Gaezbo上でシミュレートできるRaspberry Pi MouseのROSパッケージ一式です。

## 動作環境

以下の環境を前提としています。

* Ubuntu
  * Ubuntu Trusty 14.04
* ROS
  * ROS Indigo
* Gazebo
  * Gazebo 2.x
* ROS Package
  * [raspimouse_ros](https://github.com/ryuichiueda/raspimouse_ros)

## インストール方法
### 一発インストール

```
curl -sSfL https://git.io/raspimouse-sim-installer | bash -eux
```

### 手動でのインストール

最新版のros_controlをインストールしてください。

```
sudo apt-get install ros-indigo-desktop-full ros-indigo-gazebo-ros-control ros-indigo-ros-controllers
```

`raspimouse_ros` を `~/catkin_ws/src` にダウンロードし、ビルドしてください。

```
cd ~/catkin_ws/src
git clone https://github.com/ryuichiueda/raspimouse_ros.git
cd ~/catkin_ws && catkin_make && source ~/catkin_ws/devel/setup.bash
```

このリポジトリ(`raspimouse_sim`) を `~/catkin_ws/src` にダウンロードし、ビルドしてください。

```
cd ~/catkin_ws/src
git clone https://github.com/rt-net/raspimouse_sim.git
cd ~/catkin_ws && catkin_make && source ~/catkin_ws/devel/setup.bash
```

## スクリーンショット
![](./docs/images/raspimouse_samplemaze.png)

![](./docs/images/raspimouse_urg.png)

## ライセンス

このリポジトリはMITライセンスに基づいて公開されています。
MITライセンスについては[LICENSE]( ./LICENSE )を確認してください。

### 引用または参考にしたリポジトリ

* [CIR-KIT/fourth_robot_pkg]( https://github.com/CIR-KIT/fourth_robot_pkg ) - BSD (BSD 3-Clause License)
  * urdf model xacro files
  * ros_control definition files
* [yujinrobot/kobuki]( https://github.com/yujinrobot/kobuki ) - BSD (BSD 3-Clause License)
  * launch files