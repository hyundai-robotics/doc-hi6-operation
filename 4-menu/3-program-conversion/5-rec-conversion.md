# 4.3.5 Coordinate Shifting

The coordinate shifting function is a function that enables you to create a program without additional teaching even if a workpiece of the same shape, as shown in Image 2, is placed at a different location after a program taught on the workpiece \(Image 1\).

![Left: Figure 1, Right: Fugure 2](../../_assets/image_369.png)

It is required to have three reference points to use the coordinate shifting function. You can create Program A by marking three reference points on the workpiece at the initial position. After moving the position of the workpiece, write Program B using the previously marked three reference points.

![Left: Program A, Right: Program B](../../_assets/image_368.png)

{% hint style="info" %}
* The accuracy of the coordinate shifting program will be affected by the accuracy of teaching the three reference points in coordinate shifting. Perform teaching as accurately as possible for the three reference points.
* Set the distance between the three reference points as far as possible in coordinate shifting.
{% endhint %}

You can shift the existing program \(Program 1\) to a new program \(Program 2\) by calculating the coordinate shifting amount in three steps that are the basis of Program A and Program B.

![](../../_assets/image_315.png)

<br>

---

This function is not allowed during a robot operation. How to use the coordinate shifting is as follows.

1.	Select [6: Program conversion > 5: Coordinate transformation] menu. A setting window for the coordinate shifting will appear.
2.	After setting up, press [**OK**] button.
 
    ![](../../_assets/tp630/prg-coordinate-modi_eng.png)


* [Source program] : Existing teaching program number (Program number of [Figure. 1]) 

* [Target program] : Program number to newly create by executing coordinate conversion (Program number of [Figure. 2])

* [previous base program] : Number of a program with 3 standard points (Number of [Program A]) 
 
* [post base program] : Program number in which the 3 points of reference for conversion are recorded ([Program B] number) 
