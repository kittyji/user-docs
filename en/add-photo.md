# Upload Photos from Different Missions to the Same Project
# Add Photos to an Existing 3D Model

After the reconstruction is completed, some users may want to increase the number of photos in the original project in order to improve the 3D reconstruction quality or to expand the 3D reconstructed area.

**Please note:** You can add photos to the model even after the 3D reconstruction is finished. After adding the photos and click **Start**, our machine will re-run your project. As the camera position in the new project will change a lot, our machine will have to recompute it again. This will hugely consume our computational resources. So, **the price of this re-run is determined by the data size of the project to which you have added photos.** If you have any other questions regarding the price of re-run, please contact our staff or Altizure's Support Team.


In addition, the newly-added photos must meet the [Image Requirements](input-requirement.md), [Upload Requirements](upload-image.md), and the following requirements:

* **If the newly added photos are added solely for the purpose of improving the model quality, i.e. the details of the original model.**
  
  You can add the photos to the original project because the newly-added area completely overlaps with the already-reconstructed area.
  
  **But please note:** The reconstructed area **CANNOT have dramatic changes**. This is because the 3D reconstruction technique is to restore or bring back the original scene. Big changes in the reconstructed area will confuse our machine, and our machine won't know which is correct, or which set of photos it needs to reconstruct.
  
  Take the example of a construction site. You captured the whole region in January when no house was built within the area, and reconstructed a 3D model. (Let's call it the January scene.) Then, in September, a small red house was built, standing right in the middle of the area. (Let's call it the September scene.) If you want to add the photos of the September scene to the January scene, it would be very difficult for our system to reconstruct the model because the area has already undergone big changes. 
  


* **The newly-added area is adjacent to the original area.**
  
  Due to some geographical reasons, the GPS information will be slightly different each time when you captured the same area. So, if you upload the data from two different captures to the same project, you will increase the risks in 3D reconstruction and our system may not be able to embed the GPS information into the model.
  
  Therefore, we recommend our users to capture the area in one flight or to increase the photos between the new area and the original one. Both would definitely help lower the risks in 3D reconstruction.
  

* **The newly-added area is far away from the original area. There is no overlap between these two areas.**

  We are sorry to say that here in this case, you CANNOT reconstruct a model because the overlap does not meet our requirements. 
  
  Solution: You can capture the photos of the region between these two areas, or you can divide the two areas into two projects for 3D reconstruction.
  

  

 --- 
Last modified at {{ file.mtime }}
