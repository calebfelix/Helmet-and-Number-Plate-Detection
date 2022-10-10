The most widely used mode of transportation at the moment is two-wheelers. 
Although it is generally advised that bike riders wear helmets, this practise is frequently neglected globally, which results in collisions and fatalities. 
To address this issue, most countries have laws regulating the usage of helmets by two-wheeler riders. 
In addition to the law, a large portion of the police force issues fines for traffic offences in an effort to discourage this behaviour.
At the moment, this procedure is cumbersome and manual. 
This problem will be solved by the suggested technology, which will automatically detect drivers who are not wearing helmets. 
The system additionally extracts the licence plate. 
The procedure involves five steps: picture acquisition, basic processing, fringe detection and segmentation, feature extraction, and character number plate recognition using the relevant machine learning algorithms.
The technology makes use of image processing and machine learning algorithms to identify two-wheeler riders who are not wearing helmets. 
Using a video of traffic on a public road as its input, the system can identify moving items in a scene. 
An artificial intelligence classifier is used to assess whether the moving object is a two-wheeler. 
The licence plate is shown as the output in the event that the rider is not wearing a helmet.

# License Plate Object Detection and Recognition using Deep Learning Using Yolov3 and pytesseract for Humain 2019

<img src="https://miro.medium.com/max/720/0*jL3abxoCaM2Y_ac4"></img></br>
The huge blend of information developments, under different pieces of the cutting edge world, has incited the treatment of vehicles as calculated resources in information systems. Since a decision information structure has no significance without any data, there is a need to change vehicle information in the present world.

There are two approaches to make sense of this information, either with the help of human administrators or with the help of the latest technology that will help us to recognize evidence of vehicles by their license plates. Surveillance plays a vital role in almost every industry, whether it be construction sites, safety while driving for helmet detection, and also for the topic License Plate Detection which helps us to identify the unregistered plates.

Deep Learning has a promising future in the field of detection and identification through Computer Vision. Use of deep learning involves use of Convolutional Neural Network for image classification, Deep Neural Network, Recurrent Neural Network, etc. For the purpose of object detection, the possible approaches are R-CNN or Faster R-CNN and other pretrained models.

## IMPLEMENTATION DETAILS
### PREPROCESSING STEPS

The data in json file is converted into a .csv format with columns for content, label, given coordinates of bounding box, image height, image width, notes and extras. It is important to note that the coordinates are in normalised form. First all the details into content, notes, extras, top left coordinates, etc and stored in a csv file. For this, run the seperate.py file.

After getting all the details in csv file, we are scraping the image from the web link. The images are saved incrementally as image(i).jpg where i is the value of i from 0 to size of data-1 and also add another column, that is the name of each image to the csv file. Run image_save.py

The top left and bottom right coordinates are stored in normalised form in the csv file. We convert them to their unnormalised form by multiplying the x coordinate with width and y coordinate with height of the image. These four columns are added to the dataset specifying the unnormalised coordinate values. This step is done as YOLO has a particular format for taking the input coordinates of the bounding box surronding the region of interest which is discussed in the next paragraph. Run bounding_box.py. To see the bounded box randomly on images, run draw_bounding_box.py

![image](https://user-images.githubusercontent.com/73469757/194800359-5611d993-9a79-4961-ac79-b12ddd3efc57.png)

