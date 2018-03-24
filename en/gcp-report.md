# How to read GCP Report? {#how}

This is for internal testers at the moment. Invitation only.

* [What is a Preliminary GCP Report](#what-how)
 * [Space Error](#space)
 * [Ground Error](#ground)
 * [Height Error](#height)
 * [Reprojection Error](#reprojection)
* [Possible reasons for the errors in Preliminary GCP Report](#reasons)
 * [Height Error is big](#heightbig)
 * [Ground Error is big](#groundbig)
 * [Reprojection Error is big](#reprojectionbig)
 * [Ground Error is small while Height Error is big](#groundsmall)
* [Difference between Preliminary GCP Calibration and Complete GCP Calibration](#difference)


## What is a Preliminary GCP Report? {#what-how}

It sounds a bit complicated, but actually it’s as simple as that. To understand it, just imagine that building a 3D model is like putting all the photos in their right positions corresponding to a place on the 3D model. So, in the SFM stage, the machine will predict the position of each photo. But this is just a preliminary estimation and the machine is not 100% sure about it. However, by adding GCPs in the reconstruction process, the machine now has something to refer to. Based on these GCPs, the machine can slightly adjust the positions it previously predicted.

After you marked all the GCPs in photos and started a preliminary calibration, our software would try to fit your GCPs into the camera poses \(SFM\) result without making dramatic changes to each camera pose. The software will then generate a Preliminary GCP Report, telling you the fitting deviation that the SFM result might have based on the GCPs as you have marked.

However, some people may wonder, since Preliminary GCP Calibration doesn’t make any adjustments to each camera pose, what’s the point of doing it? The main purpose is to help measure the accuracy of the GCP positions that the user has marked in photos. In this way, the user can identify the errors and make necessary corrections in time.

* ### Space Error: \(Unit: meter\) {#space}
The distance between the 3D coordinate triangulated from the GCP positions that you have marked on 2D photos, and the absolute 3D coordinate of this GCP. Please notice that the distance here is in 3D.

* ### Ground Error: \(Unit: meter\) {#ground}
The distance between the projected point of the 3D coordinate triangulated from the GCP positions that you have marked on 2D photos, and the projected point of the absolute 3D coordinate of this GCP.

* ### Height Error: \(Unit: meter\) {#height}
The distance between the height of the 3D coordinate triangulated from the GCP positions that you have marked on 2D photos, and the height of the absolute 3D coordinate of this GCP.

* ### Reprojection Error: \(Unit: pixel\) {#reprojection}
The GCP positions that you have marked on 2D photos, will triangulate a 3D coordinate. This coordinate will then be reprojected back to each photo of this GCP. The Reprojection Error is the distance between the reprojected point on a photo and the GCP position that you have marked on this photo.

Below is a Preliminary GCP Report with no big errors:![](/assets/gcp-preliminary-report.png)

## Possible Reasons for the Errors in GCP Report {#reasons}

* ### Height Error is big: {#heightbig}

  1. You didn't mark the GCP position on the oblique photos of the control points.
  2. The GCP coordinates you have imported might be wrong at the first place.
  3. The GCP positions in different photos of this control point are not totally identical to each other.
  4. The GCP position that you have marked on the photos of this control point, is not the same as its actual location.
  5. The GCP location is at or near the edge of the model. This could accumulate the errors in 3D reconstruction, and hence, lead to big Height Error.

* ### Ground Error is big: {#groundbig}

  1. The GCP position that you have marked on the photos of this control point, is not the same as its actual location.
  2. The GCP positions in different photos of this control point are not totally identical to each other.

* ### Reprojection Error is big: {#reprojectionbig}

  The GCP positions in different photos of this control point are not totally identical to each other.

* ### Ground Error is small, while Height Error is big: {#groundsmall}

  When you import the GCP coordinates, you flip the X, Y coordinates.

If you can't figure out the reasons, please use the **Report Problem **function on the project page. Our technicians will help look into it.

## Difference between Preliminary GCP Calibration and Complete GCP Calibration {#difference}

In **Preliminary GCP Calibration**, the machine will not make any real changes to camera poses or the position of each photo. But in **Complete GCP Calibration**, the machine will make actual adjustments to the camera poses.

Below is an excel report for **Complete GCP Calibration **with no big errors.![](/assets/gcp-complete-calibration.png)

---

Last modified at {{ file.mtime }}
