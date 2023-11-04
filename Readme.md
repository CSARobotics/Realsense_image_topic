# RealSense D435i Stereo Camera kurulumu 

Realsense D435i kamerayı topiclerden veri alarak kullanmaya başlamak için gereken adımlar yer almaktadır.

## Installation

Öncelikle Realsense için gerekli paketleri indirmek gerekli.

```python
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install ros-melodic-realsense2-camera ros-melodic-realsense2-description
```
### Prerequirements

> Linux - Ubuntu
> 
> ROS \<Distro\>


## utilization

Kamerayı kullanmak için gerekli adımlar uygulanmalıdır.
<p style="color:red;">İlk olarak roscore komutu çalıştırılmalıdır.</p>


```python
roscore
```
Daha sonra indirdiğimiz realsense kameranın kendi paketleri çalıştırılmalıdır.

```python
roslaunch realsense2_camera rs_camera.launch
```

Kameradan gelen veriyi görüntülemek için rqt ya da rviz kullanılabilir.

```python
rosrun rqt_image_view rqt_image_view
```

```python
rosrun rviz rviz
```
Ya da gelen topic üzerinden datayı alıp kullanmak için bu proje içindeki node kullanılabilir.

> Stereo kameranın yayınladığı topicler

- /camera/color/camera_info
- /camera/color/image_raw
- /camera/color/image_raw/compressed
- /camera/color/image_raw/compressed/parameter_descriptions
- /camera/color/image_raw/compressed/parameter_updates
- /camera/color/image_raw/compressedDepth
- /camera/color/image_raw/compressedDepth/parameter_descriptions
- /camera/color/image_raw/compressedDepth/parameter_updates
- /camera/color/image_raw/theora
- /camera/color/image_raw/theora/parameter_descriptions
- /camera/color/image_raw/theora/parameter_updates
- /camera/color/metadata
- /camera/depth/camera_info
- /camera/depth/image_rect_raw
- /camera/depth/image_rect_raw/compressed
- /camera/depth/image_rect_raw/compressed/parameter_descriptions
- /camera/depth/image_rect_raw/compressed/parameter_updates
- /camera/depth/image_rect_raw/compressedDepth
- /camera/depth/image_rect_raw/compressedDepth/parameter_descriptions
- /camera/depth/image_rect_raw/compressedDepth/parameter_updates
- /camera/depth/image_rect_raw/theora
- /camera/depth/image_rect_raw/theora/parameter_descriptions
- /camera/depth/image_rect_raw/theora/parameter_updates
- /camera/depth/metadata
- /camera/extrinsics/depth_to_color
- /camera/motion_module/parameter_descriptions
- /camera/motion_module/parameter_updates
- /camera/realsense2_camera_manager/bond
- /camera/rgb_camera/auto_exposure_roi/parameter_descriptions
- /camera/rgb_camera/auto_exposure_roi/parameter_updates
- /camera/rgb_camera/parameter_descriptions
- /camera/rgb_camera/parameter_updates
- /camera/stereo_module/auto_exposure_roi/parameter_descriptions
- /camera/stereo_module/auto_exposure_roi/parameter_updates
- /camera/stereo_module/parameter_descriptions
- /camera/stereo_module/parameter_updates


