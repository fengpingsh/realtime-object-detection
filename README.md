real time object detection
=================================================================================
An implementation of real time object detection using mobilenet-ssd and accerate the CNN with the help of Movidius Neural Compute Stick.

# Run
python ncs_realtime_objectdetection.py --graph graphs/mobilenetgraph --confidence 0.5 --display 1
--graph: required, point to a graph file that can be loaded by Intel Movodius Netural Compute Stick. You can find more information in 
https://movidius.github.io/ncsdk/  
--confidence: optional, default value is 0.5  
--display: optioanl, default value is zero which means do not display the real time video.  

The code is mainly got from https://www.pyimagesearch.com/2018/02/19/real-time-object-detection-on-the-raspberry-pi-with-the-movidius-ncs/

During the running of this code, the FPS is shown if you enable the --display param, and if not, the FPS will be printed in the terminal when terminated.
You can end the process by press 'Ctrl + C' or press 'q' if display is enabled and press 's' to capture the current frame, and the current
frame will be stored to result.jpg in the current folder.

# Train your own dataset
The VOC dataset is used in this demo, and 20 class objects will be detected. If you want to train your own dataset, please refer to another project:
https://github.com/fengpingbaustem/realtime-face-recognition, this is another example using MobileNet-SSD and Movidius NCS to perform the face detection 
and recognition. I trained my own dataset and compile to graph file. You may find more information there.

# Performance
| Hardware   | pc + ncs  | raspberry pi2 + ncs  |
| ---------- | -----------|  -----------|
| Max FPS    | 9.78  | 2.48  |

Intel(R) Core(TM) i3-3220 CPU @ 3.30GHz and 8GB DDR3 is used in PC.

# Derived projects
Here https://github.com/fengpingbaustem/realtime-face-recognition 


