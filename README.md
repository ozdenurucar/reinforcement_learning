# ROS ve Gazebo ile Pekiştirmeli Öğrenme

![](https://github.com/ozdenurucar/reinforcement_learning/blob/master/Sonuçlar/rl.png)


https://www.youtube.com/watch?v=Vgzv-4eNeH0

https://www.youtube.com/watch?v=WADmP0wzLxs

https://discourse.ros.org/t/tb3-reinforcement-learning-with-tb3/4842


OpenAI Gym, son zamanlarda makine öğrenmesi topluluğunda popülerlik kazanmış pekiştirmeli öğrenme araştırmaları için bir araçtır. OpenAI Gym, her bölümdeki toplam ödül beklentisini en üst seviyeye çıkarmayı ve mümkün olduğunca hızlı bir şekilde kabul edilebilir bir performans seviyesi elde etmeyi amaçlayan, epizodik RL'ye odaklanır. Bu araç seti Gym API'sini robotik donanıma entegre etmeyi ve gerçek ortamlarda donatı öğrenme algoritmalarını doğrulamayı amaçlamaktadır. 3D modelleme ve görüntü oluşturma aracı olan Gazebo simülatörü, yazılım geliştiricilerin robot uygulamaları oluşturmasına yardımcı olan bir dizi kitaplık ve araç olan Robot İşletim Sistemi ile birleştirilerek gerçek dünyaya ulaşıldı. 

Daha önce de tartışıldığı gibi, robotikteki RL ile ilgili temel problem, sadece ekonomik maliyet değil aynı zamanda öğrenme işlemlerini gerçekleştirmek için gereken uzun süre olan deneme başına yüksek maliyettir. Bilinen bir başka husus, gerçek bir ortamda gerçek bir robotla öğrenmenin, özellikle quadcopters gibi uçan robotlarla tehlikeli olabileceğidir. Bu zorlukların üstesinden gelmek için, maliyet tasarrufu, zaman tasarrufu ve simülasyonu hızlandırmaya yardımcı olan Gazebo gibi gelişmiş robotik simülatörler geliştirilmiştir.

## Ortamın Kurulması

Projede alogirtmalar Ubuntu 18.04 üzerinde ROS Melodic versiyonu ile test edilmiştir.

### Ubuntu 18.04

#### Temel Gereklilikler
- ROS Melodic: Desktop-Full kurulması önerilir, Gazebo 9.0.0 içerir (http://wiki.ros.org/melodic/Installation/Ubuntu).


#### ROS Melodic bağımlı paketleri
```
sudo apt-get install \
python-pip python3-vcstool python3-pyqt4 \
pyqt5-dev-tools \
libbluetooth-dev libspnav-dev \
pyqt4-dev-tools libcwiid-dev \
cmake gcc g++ qt4-qmake libqt4-dev \
libusb-dev libftdi-dev \
python3-defusedxml python3-vcstool \
ros-melodic-octomap-msgs        \
ros-melodic-joy                 \
ros-melodic-geodesy             \
ros-melodic-octomap-ros         \
ros-melodic-control-toolbox     \
ros-melodic-pluginlib	       \
ros-melodic-trajectory-msgs     \
ros-melodic-control-msgs	       \
ros-melodic-std-srvs 	       \
ros-melodic-nodelet	       \
ros-melodic-urdf		       \
ros-melodic-rviz		       \
ros-melodic-kdl-conversions     \
ros-melodic-eigen-conversions   \
ros-melodic-tf2-sensor-msgs     \
ros-melodic-pcl-ros \
ros-melodic-navigation \
ros-melodic-sophus
```

#### Gerekli Python Paketleri:
```
sudo pip install gym
sudo apt-get install python-skimage
sudo pip install h5py
pip install tensorflow-gpu (if you have a gpu if not then just pip install tensorflow)
sudo pip install keras
```

#### gym-gazebo
```
cd ~
git clone https://github.com/erlerobot/gym-gazebo
cd gym-gazebo
sudo pip install -e .
```

#### workspace:
```
cd gym-gazebo/gym_gazebo/envs/installation
bash setup_melodic.bash
```

##### Örnek olarak qleanning uygulamasının çalıştırılması
terminal 1
```
cd gym-gazebo/gym_gazebo/envs/installation/
bash turtlebot_setup.bash
```
terminal 2
```
cd gym-gazebo/examples/turtlebot
python circuit_turtlebot_lidar_qlearn.py
```



