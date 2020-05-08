# Introduction to Remote Sensing of the Environment

## Ecological application of TLS

### Background and objective
The objective is to use the skills obtained in Lab 9 in a real life example. In prac 8 you were looking at a likely familiar loation - Boab court at CDU Casuarina campus. In this prac you have three scans of the field site in Litchfield NP you have seen in the Introduction to LiDAR lecture. In this prac we will align and ***co-register????*** the individual point clouds to produce a single point cloud.

## Aligning individual scans
1. Import Scan 17 and inspect the cloud. Notice how RGB works better for low points as tree foliage sways and moved between acquisitions.
![Figure 2.](screenshots/Display_settings.png)

2. Explore Display settings: 
   * Toggle the ELD filter *(Display -> Shaders & Filters -> EDL filter)*
   * Adjusting point size (hover mouse in top left corner of the screen to show menu)

Working with LiDAR data, different settings will be useful for different purposes. During this prac you can adjust display settings based on personal preferences.

Next to the scan point in the centre you will see a termite mound built up on a tree trunk. After this scan was taken large areas of Litchfield NP were subject to bushfires during the last dry season. 
![Figure 3.](screenshots/Termite_mound.png)

Here is a photo taken during a repeat scan from the same postition. At this stage only a small piece of charcoaled timber remains of this large tree. After another fire there will likely be no evidence of a tree having been here in the first place.
![Figure 4.](screenshots/Termite_mound2.jpg)

Consecutive LiDAR scans can be useful for quantifying change over time in wooded systems. In this case we can record loss of large trees; other applications include quantification of tree growth or the impact of fire events on the understory.

3. Import Scan 26. For the remainder of this prac I recommend using a height ramp to display the pointclouds (Edit -> Colours -> Height ramp). As these pointclouds are not georeferenced, CloudCompare will overlap the files.
![Figure 5.](screenshots/Overlap.png)

4. Move Scan 26 to display pointclouds side by side.
![Figure 6.](screenshots/Rotate_tool.png)
