# Introduction to Remote Sensing of the Environment

## Ecological application of TLS

### Prerequisites
---
Completion of this lab exercise requires use of the CloudCompare software package. CloudCompare is a powerful package for visualising and processing point-clouds, and best of all is open-access. You can download the version to match your operating system here:
https://www.danielgm.net/cc/

---
### Background and objective
The objective is to apply the skills obtained in Labs 9 and 10 in an ecological context. In the previous Labs we were looking at a likely familiar loation - the Boab court at CDU Casuarina campus. Here we will align three scans of the Litchfield site you have seen in the lectures and coregister them using the ICP algorithm.


![Figure 1.](screenshots/Litchie.jpg)

Scan data can be downloaded in .las format here (file size ~ 260 MB):

Scan 17 | Scan 26 | Scan 27

---
## Getting to know CloudCompare

Please see last week's lab here: [Lab 9](https://github.com/geospatialeco/GEARS/blob/master/Intro_RS_Lab9.md)

## Merging multiple point clouds

Please see last week's lab here: [Lab 10](https://github.com/geospatialeco/GEARS/blob/master/Intro_RS_Lab10.md)

## Ecological application
**1. Import Scan 17.**
  * Inspect the cloud

![Figure 2.](screenshots/Display_settings.png)

Notice how RGB works better for low points. As tree foliage sways in the wind between acquisition of the RGB image and the point cloud we often get a beautiful sky blue assigned to our tree tops.

**2. Explore Display settings.** 
  * Toggle the ELD filter *(Display -> Shaders & Filters -> EDL filter)*
  * Adjust point size (hover mouse in top left corner of the screen to show menu)

![Figure 3.](screenshots/Point_size.png)

Working with LiDAR data, different settings will be useful for different purposes. During this prac you can adjust display settings to your personal preference.

Fun fact: Next to the scan point in the centre you will see a termite mound built up on a tree trunk. After this scan was taken large areas of Litchfield NP were subject to bushfires during the 2019 dry season. 
![Figure 4.](screenshots/Termite_mound.png)

Here is a photo taken during a repeat scan from the same postition. At this stage only a small piece of charcoaled timber remains of this large tree. After another fire there will likely be no evidence of a tree having been here in the first place.
![Figure 5.](screenshots/Termite_mound2.jpg)

Consecutive LiDAR scans can be useful for quantifying change over time in wooded systems. In this example we can record loss of large trees; other applications include quantification of tree growth or the impact of fire events on the understory.

**3. Import Scan 26.**
    * Select point cloud in top left panel
    * Change colour to height ramp *(Edit -> Colours -> Height ramp)*
    * Repeat for all point clouds

![Figure 6.](screenshots/Overlap.png)

For the remainder of this lab I recommend using a height ramp to display the point clouds.
As these point clouds are not georeferenced, CloudCompare will overlap the files. As in Lab 10 we will move and rotate them to align.

**4. Open the Translate and Rotate tool.**
    * Select Scan 26
    * Select Translate/ Rotate tool
    * In the tool deselect Tz
    * From the Rotation drop-down menu select Z

![Figure 7.](screenshots/Rotate_tool.png)

These settings will allow you to move the point cloud along the x/y-axes and rotate it along the z-axis.

**5. Align point clouds.**
    * Use your **secondady** mouse button to move and your **primary** mouse button to rotate
    * Click the green tick in the Translate/ Rotate tool to save changes
    * If necessary, change viewing angle and repeat process for further adjustment

![Figure 8.](screenshots/Aligned.png)

You can see the impact of trees swaying in breezy conditions and sight differences in scanning angles. When scanning wooded areas it's best to scan on a windstill day or time of day if possible. 
Perfect alignment is difficult using my manually translating and rotating. Lets import our final point cloud so we can fix those imperfections.

**6. Import and align Scan 27.**
  * Make sure you select the point cloud you want to move/ rotate in the top left panel
  * Get yourself a cuppa if you feel frustation levels are rising

![Figure 9.](screenshots/Aligned2.png)

Now that all three point clouds are in place we can correct minor offsets using the ICP tool. All three scans contain the tower and the shed. Scan 26 has the highest number of points for both those "landmarks", so we will be using it as reference.

**7. Fine register first point cloud.**
  * Select Scan 26 and Scan 27
  * Open the Clouds registration tool *(Tools -> Registration -> Fine registration (ICP))*
  * Make sure Scan 26 is assigned as reference - click swap if necessary
  * Change final overlap to 30%
  * Click ok

![Figure 10.](screenshots/Registration.png)

If CloudCompare displays the aligned point cloud in black, just apply the height ramp again. Inspect the alignment - notice how sharp the edges look now.

**8. Fine register second point cloud.**
  * Select Scan 26 and Scan 17
  * Repeat the process (make sure final overlap is at 30%)
  * Inspect the result - I'm sure by now you'll appreciate the neat alignment, even our shed is now complete

![Figure 11.](screenshots/Registered.png)

Notice along the edges of the point cloud how points become more spars. This is partly due to the range of the scanner. In densely vegetated areas, however, occlusion is an important factor to consider. This is why multiple scan are necessary regardless of maximum range of the scanner employed.

![Figure 11.](screenshots/Edge.png)

### Thank you

I hope you found this tutorial useful.

#### Cheers, Linda Luck
