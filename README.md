# sensor_fusion_udacity
This repo will contain all of the codes and notes that I done at the Udacity Sensor Fusion Course.  I will push them and fix the readme. 


# Lesson-1
PointCloud data refers to a basic form of a 3D model consisting of multiple individual points positioned in three-dimensional space. Each point carries various measurements, such as its coordinates along the X, Y, and Z axes. Additional data, like color information in RGB format and luminance value indicating brightness, may also be included. Laser scanners play a role in generating point clouds by emitting light pulses towards object surfaces, recording the time it takes for each pulse to reflect back and reach the scanner. These measurements enable precise point positioning on the object, eventually forming the complete point cloud.


# Note for who works with Mac: 
When I tried to cmake.. , there is problem with finding Qt5(I checked the course github, others also faced with same issue).So, as a solution find the package path w/ brew info.

 Then, add this path to CMakeLists.txt as for example: set(Qt5_DIR /opt/homebrew/Cellar/qt@5/5.15.8_3/lib/cmake/Qt5) . 

Also, change your findpackage version (in the Cmakelists file) to your version. 
For example, for me: find_package(PCL 1.13 REQUIRED). One more note to here, delete the cache files after you solved this issue w/ like that. 




 
