# rovio-application
+ rovio-application and installation


## Requirements and installation

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
