# sensor_fusion_udacity
This repo will contain all of the codes and notes that I done at the Udacity Sensor Fusion Course.  I will push them and fix the readme. 


Note for who works with Mac. 
When I tried to cmake.. , there is problem with finding Qt5(I checked the course github, others also faced with same issue).So, as a solution find the package path w/ brew info.

 Then, add this path to CMakeLists.txt as for example: set(Qt5_DIR /opt/homebrew/Cellar/qt@5/5.15.8_3/lib/cmake/Qt5) . 

Also, change your findpackage version (in the Cmakelists file) to your version. 
For example, for me: find_package(PCL 1.13 REQUIRED). One more note to here, delete the cache files after you solved this issue w/ like that. 




 
