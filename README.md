# RANSAC_based_lane_dection

---
## Overview
The **RANSAC_based_lane_dection** detect lanes in the images received from the vehicle and creates a waypoint for the vehicle.If there is more than one lane detection result, the package provides a waypoint, and if it does not find a lane, it does not provide a waypoint.
![](https://imgur.com/2yoQeIb.gif)
This detector using the following algorithms:
1. Convert to Top View Image
2. Get a binary image for both yellow and white and merge it.
3. Set the ROI
4. Counts the number of points for each x-coordinate and determine a point to start finding a lane (It would be better to use PCA rather than this).
5. a.Using RANSAC, find the coefficients in a small windows which generated from a start point. From coefficients, determine a next start point.

![](https://imgur.com/Vvnq9gl.jpg)
### config
```
- ubuntu (16.04 LTS)
- Ros kinetic
```
### Input
- usb_cam/image_raw/compressed provide **waypoint** of lane.

### How to use
go to your workspace `src` dir, clone this package
```
git clone https://github.com/Epsilon8854/RANSAC_based_lane_dection.git
```
