# Setup Page {#setup}

**Setup** page is a model viewer where the owner can perform model-related settings, including recalculating GPS alignment, adding annotations and setting initial view point. In some tutorials, the **Setup** Page will be referred to as **setting/setup mode**.

* [Viewing Angle icon](#viewingangle)
* [Set Thumbnail icon](#thumbnail)
* [Annotation icon](#annotation)
* [Model Orientation icon](#orientation)
* [Camera Settings icon](#camera)
* [Crop icon](#crop)
* [Water icon](#water)


### How to Enter the Setup Page

Please go to **My Projects **&gt;&gt;** **Select a project &gt;&gt; Find the **Settings card **on the **Overview** page &gt;&gt; Click **Setup** &gt;&gt; Enter the **setting mode **of this project.

![](../assets/setup.png)

## Viewing Angle Icon {#viewingangle}

This function is the same as the **Viewing Angle** icon in the **Studio** page. As you can see on the tab, you can zoom in/out, rotate or tilt the model. You can also view the model by using your computer mouse, e.g. scroll your mouse wheel to zoom in/out, left-click to drag your model left or right, right-click to rotate/tilt your model.

**But plese be aware** that if you click **Ortho View**, you will have a 2D orthomap instead of viewing the model from the top.

![](../assets/setup-ViewingAngle-icon.png)

## Set Thumbnail Icon {#thumbnail}

To take a nice thumbnail image, you can follow the steps below:

1. Navigate to a view point which presents the best view of your 3D model.
2. Click **Set Thumbnail** icon and the system will take a screenshot of your model.  
   ![](../assets/setup-thumbnail.png)

3. If you are satisfied with the image, click **Set Thumbnail **in the popup dialog and set the screenshot as the thumbnail of your model. Or, you can click **Cancel **and repeat the above steps to re-take a screenshot.  
   ![](../assets/setup-thumbnail-2.png)

The view point you choose for the thumbnail is also the starting view point of your project when your 3D model is viewed!

![](../assets/setup-thumbnail-3.png)

## Annotation Icon {#annotation}

Users can annotate on the model. An annotation is attached to a point on the 3D model, which moves when the model moves. Each annotation has its own symbol on the map, as well as a title and a description in which you can insert links and images.

![](../assets/setup-annotation-icon.png)

**连接Link to How to add an annotation**

## Model Orientation Icon {#orientation}

Sometimes, if the photos are not successfully aligned with GPS information, it's difficult for the machine to figure out whether the model is facing south or north. This would end up the model being upside down or not facing the right direction.

![](../assets/setup-orientation-icon.png)

So, here we need to tell the computer what the right direction is by setting the model orientation. As three points define a plane, you can set the ground plane by placing three points on the ground.

![](../assets/setup-orientation-panel.png)

A more detailed tutorial is as follow. You can start from **0:18**.

**视频连接**

## Camera Settings Icon {#camera}

You can change the preset value of camera viewing angles or viewing distance in this card.

![](../assets/setup-camera-icon.png)

Camera mode comes with two preset values.

**Object **type is designed for viewing models of small object. It enables you to view from every possible angle including the bottom.

![](../assets/setup-camera-object.png)

**Landscape **type is more suitable for models with a ground plane, as the camera will be restricted to always stay on top of the ground to avoid accidental flipping to the bottom.

![](../assets/setup-camera-landscape.png)

Besides these preset modes, you can also pick a certain angle from individual tilt angles by clicking **Advanced**.

To remove the restrictions on view distances, you may turn off the toggle on **View Distance Limits**. After that, you can zoom in/out the reconstructed model to any distance.

![](../assets/setup-camera-adv-panel-small.png)

## Crop Icon {#crop}

![](../assets/setup-crop-icon.png)

You can use the cropping tool to quickly clean up the model. A short tutorial is as below:

**视频连接**
<iframe src="https://www.youtube.com/embed/kvtjBLNqeTU" frameborder="0" allowfullscreen></iframe>

## Water Icon {#water}

Reconstructing a water surface has always been a difficult task in this area. But with this tool, users can delete the water area that is not well reconstructed, and place it with a water surface developed by Altizure.

![](../assets/setup-water-icon.png)

Here is a short tutorial:

**视频连接**

---

Last modified at {{ file.mtime }}

