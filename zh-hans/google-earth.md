# 如何导入Google Earth 谷歌地球？

* [导入正射图/dsm](#ortho-dsm)
* [导入3D模型](#3d)
* [KMZ文件加载慢](#slow)

## 如何将正射图/dsm 导入 Google Earth? {#ortho-dsm}

当满足以下条件时，用户可将正射图/dsm导入：

* 用于制作模型的图像包含GPS信息
* 模型重建过程中，GPS信息被成功嵌入到三维模型中

导入流程：

1. 下载 Google Earth Pro [here](http://www.google.com/earth/)。 请下载专业版（pro版）而不是普通版 Google Earth。Google Earth Pro 目前是免费的。
2.下载自己的模型，并使用[Altizure 桌面版](https://www.altizure.cn/desktop)里的Altizure离线转换器，将obj文件转换成正射图或dsm.
3. 打开 Google Earth Pro.
4. 点击`File`&gt;&gt;`Import`并选择下载的 tif 文件。谷歌地球的视角会自动移动到您模型的位置。 接着点击`scale`将自己的正射图放入 Google Earth Pro。

## 如何将3D 模型导入 Google Earth? {#3d}

当满足以下条件时，用户可将三维模型导入： 

* 用于制作模型的图像包含GPS信息
* 模型重建过程中，GPS信息被成功嵌入到三维模型中

用户可使用[Altizure 桌面版](https://www.altizure.cn/desktop)里的Altizure离线格式转换器将下载的 OBJ 文件转换成`DAE`和`KML`文件。这两种文件可以被直接导入 Google Earth ，将您在Altizure上制作的模型展现出来。

`DAE`文件包含模型的地理位置信息。导入此类文件，可以让 Google Earth 将您的模型放在您当前的位置上。

`KML`文件包含额外的 GPS 信息。导入此类文件，可以让 Google Earth 将您的模型放在相应的位置上。

导入流程： 

1. 打开 Google Earth Pro.
2. 点击`File`&gt;&gt;`Open`并将模型的`DAE`或`KML`文件导入进去。下面这个例子，我们导入的是`level_2_0_0.kml` 文件.

![](../assets/googleearth-screenshot-1.png)

导入后，您可能会发现，有时候模型会比谷歌地球表面低。这是因为GPS里的高度信息缺失。用户可以通过手动调整高度解决这一问题。

调整高度的方法：
1. 将KML文件在左手边的工具栏中放大
2. 右键点击模型的图标
3. 点击 **Properties** ，再点击 **Altitude**
4. 根据实际需求调整高度的数值

![](../assets/googleearth-screenshot-2.png)

**小提示：目前，google地图可以加载的kml和dae文件的最高层级是5，level 5。**

## KMZ在谷歌地球加载时很卡，而且有些片块无法显示，怎么办？ {#slow}

KMZ其实是经压缩过的格式，所以加载到谷歌地球时要花时间解压，导致加载时会卡。建议先把KMZ当成普通的zip文件解压，再加载解压后的Project\_LOD.kml文件。

---

本文档最后修改于 {{ file.mtime }}
