20220601 version:
Notes:
1.The current version is modified, the cached image will be emptied when starting to collect pictures to solve the problem of asynchronous
Others:
1.The problem of sudden freeze during scanning has not been solved for the time being
2.If there are still different problems, please open the save map, provide the save map and log to us

20220606 version:
Notes:
1.The current version only support to do the video capture test
2.see if there are still out-of-sync problems, or the scanning is not smooth.

20220613 version:
Notes:
1.Modified the process of capturing pictures and modified the camera synchronization process
2.Speckle is not available

20220615 version:
Notes:
1.Fix the problem that stripe mode cannot be used
2.tracker failed will save the failed images to saveFailedImages folder
Others:
1.config.txt will be written as 0 0 in the future, and will not be changed
2.If tracker failed, please provide glog log, saveFailedImages folder and video

20220616 version:
1.Fix the problem that the stripe scan video stream does not display

20220620 version:
1.Fix multi-mode untracking issue

20220621 version:
1.This version is a beta version to test crash issues
Others:
1.If the software crashes, please provide the generated dump file and glog log, operation video

20220624 version:
1.Fix mode switching crash
2.Add marker point tracking coordinates output to console

20220706 version:
1.Solve the problem of tracking failure and always saving pictures

20220715 version:
1.The interface displays the SDK version number

20220719 version:
1.Solve the crash problem caused by abnormal exposure time setting
Others:
When the set exposure time exceeds the range, the interface returns -1, and the console outputs corresponding prompt information

20220829 version:
version：3.2.2
Major update：Supports automatic detection and connection of the device after being offline. After reconnecting to the device, it will continue to work according to the set working mode

20220906 version:
version：3.2.3
Major update：
1.Disable device camera related operations during reconnection
2.Solve the problem that the switch mode cannot prompt offline

20221012 version:
version：3.2.4
Major update：
1.add some logs
2.solved some bugs

20221020 version:
version：3.2.5
Major update：
1.Add a flag point query interface (GetMarkers). After enabling flag point tracking, you need to call this interface to obtain the number of tracked flag points
2.The sdk manages its own flag point memory

20221102 version:
version：3.2.6
Major update：
Fix some bugs

20221109 version:
version：3.2.7
Major update：
1.The InitializeDevice interface will return CD_CAMERA_RECONNECT(8) when the camera is reconnected, waiting for the reconnection to be successful 

20230324 version:
version：3.2.8
Major update：
1.Fixed failure to reconnect offline immediately after switching scan mode

20230309 version:
version：3.2.9
Major update：
1.It integrates the latest firmware version and needs to be used with the upgraded firmware to solve the problem of reconnection failure when switching mode occurs

20231025 version:
version：4.0.6
Major update：
1.Fixed the usb crash issue of switching mode unplugging
2.Fixed the failure to set exposure gain for the first time
3.Modify some problems that demo does not respond during use

20231103 version:
version：4.0.7
Major update：
1.Solve the problem that the scan interface does not return data properly, The Start_Scan interface returns -1 when reconstruction fails and 0 when reconstruction succeeds

20231114 version:
version：4.0.8
Major update：
1.Solve the problem of being unable to continuously track when clicking the track button
Important hint:
The marker_tracker and getMarker interfaces cannot be used. Multi-mode and track-mode only need to use Start_Scan

20231124 version:
version：4.0.9
Major update：
Fixed the problem of staying offline

20231204 version:
version：4.0.10
Major update：
The Start_Scan interface returns 0 when the execution is successful

20231220 version:
version：4.0.11
Major update：
1.Optimized the method for obtaining data on the Start_Scan interface
2.checkcamerastatus interface is Optimized

20231225 version:
version：4.0.12
Major update：
1.Resolved the reconnection failure caused by 4.0.11 modification
2.Regarding the scanning of multiphase and tracker modes, 
data will not be automatically scanned after switching modes. 
Only when the scan button is clicked in multiphase mode, 
the point cloud and tracking mark points will be rebuilt. 
Or when the tracker button is clicked in tracker mode, 
the mark points will be tracked. 
The reason for the modification here is that the tracker button and the scan button always do some same things and need to be distinguished. 
Of course, these modifications will not affect your SDK integration, because it is a modification of our demo