# rovio-application
+ rovio-application and installation
+ Used Intel D435i - stereo setup


## Requirements and installation

+ [IntelD435i setup and calibration](https://github.com/engcang/VINS-application/tree/Intel-D435i)
  + Used [Kalibr](https://github.com/ethz-asl/kalibr) as [here](https://github.com/engcang/vins-application#-calibration--kalibr---synchronization-time-offset-extrinsic-parameter) and referred [here](https://support.stereolabs.com/hc/en-us/articles/360012749113-How-can-I-use-Kalibr-with-the-ZED-Mini-camera-in-ROS-)

+ ROVIO official [homepage](https://github.com/ethz-asl/rovio)

+ Install [kindr](https://github.com/ANYbotics/kindr)

 ~~~shell
  $ cd ~/catkin_ws/src && git clone https://github.com/ANYbotics/kindr
  $ cd .. && catkin build -j8
 ~~~

+ Install lightweight_filtering and ROVIO

 ~~~shell
  $ cd ~/catkin_ws/src && git clone https://github.com/ethz-asl/rovio
  $ cd rovio && git submodule update --init --recursive

  $ cd ..
  $ catkin build rovio --cmake-args -DCMAKE_BUILD_TYPE=Release

  # With with opengl scene (optional)
  $ sudo apt-get install freeglut3-dev libglew-dev
  $ catkin build rovio --cmake-args -DCMAKE_BUILD_TYPE=Release -DMAKE_SCENE=ON
 ~~~
