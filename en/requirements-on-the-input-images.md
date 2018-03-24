# Requirements on Input Images

* [Obtain data](#obtain)
* [Basic requirements on input data](#basic)
* [Input & output formats](#formats)
* [Can I upload videos?](#videos)
* [Can I only use vertical images?](#vertical)

## How to obtain data? {#obtain}

You can find the answer in our **Altizure App Guideline**.

## Basic requirements on input data {#basic}

The object you choose to capture should:

* Be a static object
* Have a surface of irregular patterns

The object you choose should NOT:

* Be transparent
* Have a reflective, textureless surface

The input images should:

* Have sufficient overlap
* Contain different angled shot
* Have consistent camera setting

The input images should NOT:

* Be blury, out-of-focus images
* Have timestamp or other fixed marks

## What are the input and output formats? {#formats}

**Input: **Images, preferably in JPG format.

**Output:** 3D texture-mapped mesh files in OBJ format with LOG.

## Can I use videos instead of photos \(or still photographs\)? {#videos}

* The video files are not accepted.

* Theoretically speaking, you can reconstruct a 3D model with the video frames extracted from a video clip. However, we do not recommend this method. The quality of the images that we extract from a video will be much worse than photos. Besides, the Rolling Shutter problem that occurs when you shoot the video, will further distort the photos. So, normally, we won't recommend users to generate a 3D model from videos.

## Can I use only vertical images? {#vertical}

* Yes. Altizure will reconstruct a rough 3D model. You can also download your model, and use the Format Converter in Altizure Desktop to generate a 2D orthographic map of the area.

* To reconstruct a more accurate and complete 3D model, you must take pictures from both the oblique and vertical angles. We generally recommend that you need to follow the flight paths auto-planned by our **Altizure App**, and take photos from five different viewpoints: one vertical, and four at 45 degrees. Therefore, this will make the input data four times more than the vertical data.

* **Altizure APP **automatically captures both vertical and oblique views, and optimizes the capturing process.

---

Last modified at {{ file.mtime }}


