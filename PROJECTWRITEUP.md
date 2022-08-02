# Object Detection in an Urban Environment
#Project Overview
The objective of this assignment is to train a dataset for object detection in an urban environment using resnet.

#Setup
I must say this has been one of the most frustrating experiences in my life. Something that could have taken hours ended up taking me days because of various technical issues and poorly written instructions.

The workspace kept going idle while I am working on it. Jupyter Notebook kept crashing both on Firefox and Chromium Browser. It got so bad that I had to figure out how to get this thing running on my desktop PC.

I had no experience with Docker and didn't even know what it was so, of course, I configured it wrong. Eventually, I did figure it out and got it working. 

#Dataset
The data was downloaded from the Waymo open dataset. Those files are huge. After 10 hours, I had only downloaded 32 files. I decided that was enough for what I needed to do.

I used those files to write the code in Exploratory Data Analysis, then copied them back to the provided workspace.

#Experiment
I started with the default config file and created the base reference.The model prediction was pretty bad with loss numbers around 80.

I must say that training from the desktop environment is a pain. You have to keep on clicking that box that pops up every few minutes asking if you want to continue using the desktop. In other words, you have to be a slave to it and sit there doing nothing for hours. Eventually, Although the instructions say to delete the training data leaving only the tf.events, that won't work. It will only leave you frustrated for hours. Because you don't have enough room in the workspace to leave the tfevents and complete a training session, you will end up running out of space and you won't be able to complete training. Ideally, we would need an extra 2gb of space to follow the instructions and complete the training. 

Additionally, it's important that raining and eval are launched from outside the desktop environment in the cli that comes up after entereing the project workspace. If not, the workspace will keep going idle as you are working on the project.That information should be included in the project instructions. Furthermore, deleting files doesn't remove them from your workspace as they go in the trash. You cannot empty the trash in this environment the way you would do it with a regular box running Debian or Ubuntu. Don't bother reaching out for support on that subject. They will get back to you after a couple of days and won't provide any valuable information. I have found that the easiest way to delete the trash in the workspace is to install trash-cli (apt-get install trash-cli) and issue the trash-empty command. For local setup, an Nvidia card isn't enough. 10 series won't work with the latest drivers. Support for the 10 series was dropped after nvidia-driver-515. The current nvidia driver installed by default with the Docker script is nvidia-driver-516. It's a pain in the ass to downgrade to 510 or 515 especially if you are new to this environment. For things to go smoothly, you will need at least a 20 series since they have the required Cuda cores.I wish this had been included in the information about getting a local setup up and running.

Setting up locally is highly advisable in order to avoid the frustration of the frequent crashes of the workspace. Our time should be spent fine tuning the training process instead of trying to fix environment issues. Also, if we do the work from within the workspac why do we have to submit through github?
