# DroneVideoExperiment
Detecting person in a video
# Drone Image Person Detection
The main objective right now is to count number of person in the drone image. To do so we got the arieal video from Helsinki Kaupunki. For that we run python command to save frames from the video. After that we randomly seletced a frame and sliced it into different patches.

## Frame from video

## Slices from the frame
We needed to take a train data so we sliced the frame. The patch size we used is 128 by 128 as it was difficult to annotate the smaller size.

## Taking annotations from the slices
From each slice of image we used labelImage tool to annotate. If the patch doesn't have any person in it we created the bounding box in whole patch and labeled with 'unknown' and for each person in a patch we created a bounding box around it and labeled 'person'. Since we are now interested only in person we didnot labeled other objects like bus and bicycles.

## Combining xml to csv
