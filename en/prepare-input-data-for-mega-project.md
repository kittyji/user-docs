# Prepare Input Data for Mega Project

Professional users who are looking for software that can handle an enormous amount of data and build city-scale projects in good quality, can come to us for help. Altizure now presents this guideline as a resource for the preparation in big projects to be reconstructed on altizure.com. Please scroll through the guideline and learn more about how to prepare the input data for large scale projects.

### Who should read this article? {#who-should-read-this-article-}

1. Professional users who will run a project with over 20,000 images.
2. Suppliers of oblique photography capturers and professional mapping drones. For these users, please read this article carefully and follow the rules. You can send your project data directly to Altizure, and we'll ensure that the project will be processed with high-efficiency\.


* [Necessary Input Images](#necessary-input-images)
* [Optional Input Files](#optional-input-files)
* [Format of pose.txt](#format-of-pose-txt)
* [Format of camera.txt](#format-of-camera-txt)
* [Format of group.txt](#format-of-group-txt)

## Necessary Input Images {#necessary-input-images}

The input images should be in different names.

_Attention:_

1. The file name extension is not case sensitive. So, `DSC0000.jpg`and `DSC0000.JPG`are regarded as the same file by Altizure.
2. There should be at least 3 valid image files.
3. We support JPG，PNG and TIFF, but we strongly suggest that the users use JPG files with exif recording camera information.

## Optional Input Files {#optional-input-files}

* **pose.txt **is the file including camera extrinsic parameters\(camera positions and rotations\). This file is only beneficial and necessary for large scale data-sets. Information of camera poses is only used to accelerate the initial block splitting of data-sets.

* **camera.txt **is the file include camera intrinsic parameters \(focal length, principle point and distortion\).

* **group.txt **is the file including camera groups \(Cameras in the same group will share the same intrinsic parameters\).

_Attention_：If possible, we strongly suggest to write camera extrinsic and intrinsic parameters into the **exif** of each image.

## Format of pose.txt {#format-of-pose-txt}

File Name: pose.txt

`coordinatesystem local`

`<image name><GPS><Pose>`

`<GPS> = <Latitude><Longitude><Altitude>`

`<Pose> = <Roll><Pitch><Yaw>`

The first line`coordinatesystem local`means the coordinate system of camera poses is defined by users, not the GPS coordinate system \(WGS84\). If the provided camera poses are in GPS coordinate system \(WGS84\), you can just omit this line.

`<image name>`is the file name of the image. Please guarantee different images has **different file names**.`<GPS>`is the longitude, latitude and altitude of cameras, which is required in this file.`<Pose>`is the camera direction \(roll, pitch, yaw\) with unit degree, which can be omitted in this file.

For example, the following three pose.txt files are valid:

```
A0001.JPG 23.160948060 113.4292872428 161.6660766602 95.63634782 23.47147433 17.40054218
```

```
A0001.JPG 23.160948060 113.4292872428 161.6660766602
```

```
coordinatesystem local
```

```
A0001.JPG 1.0 1.0 1.0
```

A0001.JPG is the image file name.`23.160948060 113.4292872428 161.6660766602`is the latitude, longitude and altitude of GPS.`95.63634782 23.47147433 17.40054218`is the camera direction \(roll, pitch, yaw\). The third file uses the local coordinate system defined by users.

The two files below are invalid:

```
A0001.JPG 0.9563634782 0.2347147433 0.1740054218
```

```
A0001.JPG 23.1609480602 113.4292872428 161.6660766602
A0001.JPG 23.1604395330 113.4293176755 161.5956573486
```

The first file only has the camera direction without the GPS coordinate. The second file includes two images with the same file name.

The definition of camera direction, please refer to [this page](https://sidvind.com/wiki/Yaw,_pitch,_roll_camera).

## Format of camera.txt {#format-of-camera-txt}

File name: camera.txt

`<image name><focal length><image center>`

`<image center> = <X0><Y0>`

`<image name>`is the image file name. Please guarantee different images has **different file names**.`<focal length>`is the focal length of camera with unit pixel.`<image center>`is the principle point of camera with unit pixel. The origin of coordinates is the top left corner of image, the x axis is to the right and the y axis is to the down.

Below is the file including images with resolution 5616\*3744:

```
A0001.JPG 6845.25 2806.245 1976.354
A0002.JPG 6845.25 2806.245 1976.354
```

## Format of group.txt {#format-of-group-txt}

File name: group.txt

`<image name><group ID>`

`<group ID>`is the group index of group one image belongs to, which is an integer number no less than 0. Images in the same group means those images are captured by the same camera \(has the same intrinsic parameters\). Images captured by different cameras with the same model should be divided in different groups.

This example shows six images are divided in three groups:

```
A0001.JPG 1
A0002.JPG 1
B0001.JPG 2
B0002.JPG 2
C0001.JPG 3
C0002.JPG 3
```

---

Last modified at {{ file.mtime }}


