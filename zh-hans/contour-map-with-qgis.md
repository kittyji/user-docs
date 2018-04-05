# 怎样从DSM文件生成等高线图？

**QGIS**是一个免费和开源的地理资讯系统软件。在这个简单的教程中，我们会使用QGIS，把由Altizure生成的DSM制作成地理中常用到的等高图（格式为**shapefile, .SHP**）。

第一步：下载本教程用的DSM图，如下图所示

**插入下载sample的链接**

![](../assets/dsm_contour_QGIS__1.png)

 
第二步：从QGIS官方网页 [http://www.qgis.org/en/site/](http://www.qgis.org/en/site/)下载QGIS软件，进行安装


第三步：如下图把教程用的DSM图 （orthomap_dsm.tif）导入QGIS中

![](../assets/dsm_contour_QGIS_2.png)

第四步：在顶部的菜单中选 **Raster** &gt;&gt; **Extraction** &gt;&gt; **Contour**

![](../assets/dsm_contour_QGIS_3.png)

第五步：调较生成等高图的各项参数，如输出路径，等高线的间距等等。

![](../assets/dsm_contour_QGIS_4.png)

第六步：完成

![](../assets/dsm_contour_QGIS_5.png)


---

本文档最后修改于 {{ file.mtime }}




