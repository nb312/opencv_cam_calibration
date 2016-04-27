Why
====
#摄像头标定程序
In general, I was upset about how deep the calibration tool 
is buried in opencv's folder structure and especially in
the CMAKE tree, so I extracted and made it available here.

However, the installation now is more straight forward. 
Make sure you have a working camera and opencv >= 2.4.x installed.

Basically, you just need to print out the chess_pattern.png (images), 
edit the camera_conf.xml (data) according to your needs, build the 
software and execute it. There you go... 

Install and Use--linux比较方便
================

1) mkdir build

2) cd build

3) cmake ..

4) make

5) edit the data/camera_conf.xml to your needs (chess board size, maker size, camera input [0|1 device name])
   Hint: Use a measurer :)

6) cd bin

7) ./cam_calib ../../data/camera_conf.xml

8) If your camera cannot be found, edit the camera_conf.xml (i.e. change video device index /dev/videoX)

9) If your camera is working you will get an image stream indicating "press g to start"

10) When done, exit the calibration routine and you will find a calibration xml file next to the executable

直接导入visual studio
=============
将src下.cpp导入visual studio中，配置好opencv环境，然后生成.exe文件，通过命令就可以使用了

1) 将default.xml 拷贝到当前文件，里面有相关配置可以去看看

2)并见棋盘格视频拷贝到当前文件，并修改为default.xml里面的文件

3) 直接点击执行.exe,然后会生成一个.xml文件

