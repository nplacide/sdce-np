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

I experimented with total_steps, warmup_steps, num_steps, and fiddled with various augmentations such as random_rgb_to_gray, random_adjust_contrast, random_adjust_brightness that allowed me to achieve much better results for eval after the changes. With the changes in my config file, loss numbers were closer to 1. They were either a little bit over or a little bit under.

I must say that training from the desktop environment is a pain. You have to keep on clicking that box that pops up every few minutes asking if you want to continue using the desktop. In other words, you have to be a slave to it and sit there doing nothing for hours. Eventually, I got it completed. Also, when you delete the training data leaving only the tf.events, it doesn't allow you to resume. 

I eventually figured out that training and eval could be done from outside the desktop environment but that was after wasting a lot of time! That information should be included in the project instructions. And please, do something about the workspace and those crashes.

Finally, I tried submitting the project after completing it within the workspace and it wouldn't let me submit. Apparently, the only way to submit is through github. Why????