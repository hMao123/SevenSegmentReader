# SevenSegmentReader
Automates extracting and recording numerical data from seven-segment displays in videos, providing time-stamped readings for digital monitoring.

## Background
When working on my PhD thesis, I needed to measure and record the change in mass of a system over time at high sampling frequency (>2Hz). While laboratory digital balance has the required sampling freqncy, its data recording capability is limited to only 0.5Hz. Video capturing the balance display can record the mass reading over time, but extracting the values into numerical data is exhuastingly time demanding. Therefore, I decided to build my own machine vision and machine learning pipeline to process the video recordings.

## Goal
I wanted the code to be extremely efficient in terms of speed with reasonable accuracy, as I have large amount of video files to process.

## Performanc Evaluation



# Processing Pipeline
1. The user manually records the corner (x, y) coordinates of the Region of Interest.
2. Four point transform is performed on each frame of the video followed by scaling to 100 pixels in height.
3. After transforming to gray scale, aggresive adaptive thresholding to applied to convert the image to binary while minimizing the effect of refleciton and shadow.
4. Contours of all objects are calcualted, and region of the image with small contours are removed to reduce noise and neglect decimal point.
5. 

