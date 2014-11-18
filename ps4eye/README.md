# PlayStation4 stereo camera package for ROS

## WARNING

* This package is experimental and not completed.
* You need to hack (cut and solder) the PS4 cable. It may damage your device. Do it at your own risk.
* The PS4 camera is USB 3.0 only and is not compatible with USB 2.0 systems.

## Requirements

* You need a ps4eye camera [PlayStation Camera CUH-ZEY1J](http://www.jp.playstation.com/ps4/peripheral/cuhzey1j.html)

* You need to hack the cable. See [PS4eye](http://ps4eye.tumblr.com/post/79572946666/more-photos-of-cable-wiring-to-clarify-how-the).

* You may need newer linux kernel. Kernel version 3.17.3 is OK. 3.13.0 is NG.

* Clone [ps4eye github repo](https://github.com/ps4eye/ps4eye)

## Usage

1. Run ps4eye_init
```
$ cd ps4eye/python
$ sudo ./ps4eye_init
```
2. Check if you can obtain the  image from ps4 camera by webcam software (cheese, etc).

3. Launch ROS nodes.
```
$ roslaunch ps4eye stereo.launch
```
4. Run viwer on another console.
```
$ rosrun image_view stereo_view stereo:=/stereo image:=image_rect_color
```
5. Now you can see disparity image from the stereo camera. Done!

## Thanks

Thanks for the incredible ps4 camera hackers.

* [PS4eye PlayStation 4 camera hacking](http://ps4eye.tumblr.com/)
* [ps4eye github repo](https://github.com/ps4eye/ps4eye)
* [PS4Eye をハイフレームレートステレオカメラとして使う](http://goo.gl/2AcdMQ)
