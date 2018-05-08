Code branched from:

http://docs.opencv.org/2.4/doc/tutorials/calib3d/camera_calibration/camera_calibration.html

For Information about Calibration please see here:
https://de.mathworks.com/help/vision/ug/camera-calibration.html?requestedDomain=www.mathworks.com&requestedDomain=de.mathworks.com&requestedDomain=true

# How to Compile and Run:   

`cmake .`  
`make`    
and then:  `./CalibrateCamera default.xml`  
Note: The file should exist before you run this.


# User Guide:

Configure the `.xml` file with the data you want, whether you're calibrating with a chessboard, or via a camera or with video. We have defined using Chessboard, with pictures taken.

1. Print Chessboard.png and capture pictures from your camera in different poses. (example in qtecCali folder)
2. Name the captured images and list them in imageList.xml (see in qtecCali folder)
3. Open default.xml and input data about absolute measure of printed chessboard and location of your image folder and corresponding imageList.xml file (qtecCali folder example)
3. Für Extrinsic Paramter:The Chessboard should be laid on the floor and a simple point would be recognized as the world coordinate point. 
4, For the transformation between the world coordinate system with respect to robot coordinate system, the robot tcp point is driven to the chessboard world coordiante and the values are read from the control panel, this matrix can help transform the world coordinate with respect to robot coordinate ( usually directly the middle point of robot base)