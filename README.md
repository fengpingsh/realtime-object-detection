real time object detection
=================================================================================
An implementation of real time object detection using mobilenet-ssd and accerate the CNN with the help of Movidius Neural Compute Stick.

# Run
python ncs_realtime_objectdetection.py --graph graphs/mobilenetgraph --confidence 0.5 --display 1
Here the param --graph point to a graph file that can be loaded by Intel Movodius Netural Compute Stick. You can find more information in 
https://movidius.github.io/ncsdk/
The code is mainly got from https://www.pyimagesearch.com/2018/02/19/real-time-object-detection-on-the-raspberry-pi-with-the-movidius-ncs/

During the running of this code, the FPS is shown if you enable the --display param, and if not, the FPS will be printed in the terminal.
You can end the process by press 'Ctrl + C' or press 'q' is display is enabled and press 's' to capture the current frame, and the current
frame will be stored to result.jpg in the current folder.

# Train your own dataset
Here https://github.com/fengpingbaustem/MobileNet-SSD/tree/master/mydataset provide the steps to train your own dataset. After trained the model,
https://movidius.github.io/ncsdk/tools/compile.html provide the command to convert the model to graph file which is loadable for NCS.


# Derived projects
Here https://github.com/fengpingbaustem/realtime-face-recognition is another example for face detection and recognition using MobileNet-SSD and 
Movidius NCS. I trained my own dataset and compile to graph file.


