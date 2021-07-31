# COLOR_DETECTION
Color Detector By Arvind Patkal

COLOR DETECTION
      Color detection is the process of detecting the name of any color.
    • Color detection is necessary to recognize objects; it is also used as a tool in various image editing and drawing apps.
    • Color detection has a wide application area on computer based systems.
    • Color detection is a really important process and widely needed in many applications such as, face recognition, image filtering, road sign detection, real time tracking etc. Automatic Color Detection for Car Repainting.

OpenCV- 
    • Open Source Computer Vision Library 
    • It was initially launched in 1999 by Intel. 
    • With more updates, it has been modified since then to aim for the real-time computer vision. 
    • This library has been written under programming languages like C and C+.
    • It can be easily run on operating systems Windows and Linux.
    •  This library can be easily interface with programming languages like Python, MATLAB, Ruby and others as well. 
    • Along with Numpy [6] and Python image processing (shape & color detection) can be performed at ease.
    • Color detection is the most important and challenging fundamental task of computer vision.
    • The easiest way to detect and segment an object from an image is the color based methods.
    • Color is one of the most important characteristics of an image, if color in a live video or in a digital image can be detected, then the results of this    detection can be used. 


 Here we take a colored image of 3 channel (RED, GREEN, BLUE). So each pixel has a RED value, GREEN and BLUE value. Our aim is to retrieve these values from an image to determine the color of the pixel.

The Data Set

Colors are made up of 3 primary colors; red, green, and blue. In computers, we define each color value within a range of 0 to 255. So in how many ways we can define a color? The answer is 256*256*256 = 16,581,375. There are approximately 16.5 million different ways to represent a color. In our dataset, we need to map each color’s values with their corresponding names. But here we don’t need to map all the values. We will be using a dataset that contains RGB values with their corresponding names. CSV file includes 865 color names along with their RGB and hex values.


    • Python packages that are necessary for this project in Python are:
    1. Open CV
    2. Numpy
    3. Pandas
    4. Tkinter
    5. Python Imaging Library (PIL)

    • OpenCV-python:
OpenCV-Python is a library of Python bindings designed to solve computer vision problems. It is Open-Source Computer Vision Library mainly aimed at real time computer vision.
    • NumPy:
NumPy is a library for the Python programming language, adding support for large, multi-dimensional arrays and matrices, along with a large collection of high-level mathematical functions to operate on these arrays. 
 
    • Pandas:
Pandas is a Python package that provides fast, flexible, and expensive data   structures designed to make working with structured (tabular, multidimensional etc.,) and time series data easily. 
    • Tkinter:  
Tkinter is a standard GUI library for Python. This framework provides Python users with a simple way to create GUI elements using the widgets found in the Tk toolkit. Tk widgets can be used to construct buttons, menus, data fields, etc. in a Python application.
    • Python Imaging Library (PIL):
Python Imaging Library is a free and open-source additional library for the Python programming language that adds support for opening, manipulating, and saving many different image file formats.


WORKING
    • Import the required modules:
Such as opencv, pandas,numpy,tkinter,PIL
    • Read CSV files with pandas:
The panda’s library is very useful when we need to perform various operations on data files like CSV. pd.read_csv() reads the CSV file and loads it into the pandas Data Frame. We have assigned each column with a name for easy accessing.
    • Building a File Box to choose a particular file:
In this step, we will build the main window of our application where the buttons, labels and images will reside. We also give it a title by title() function.
    • Call the detect_color function:
Having parameter path of image
    • Set a mouse callback event on a window:
First, we created a window in which the input image will display. Then, we set a callback function which will be called when a mouse event happens. With these lines, we named our window as ‘color detector’ and set a callback function which will call the draw_function() whenever a mouse event occurs.
    • Call the Draw Function: (Event,x,y,flags,params)
It will calculate the rgb values of the pixel which we double click. The function parameters have the event name, (x, y) coordinates of the mouse position, etc. In the function, we check if the event is double-clicked then we calculate and set the rgb values along with x, y positions of the mouse.
    • Calculate distance to get color name:
We have the r, g and b values. Now, we need another function which will return us the color name from RGB values. To get the color name, we calculate a distance(d) which tells us how close we are to color and choose the one having minimum distance.
Distance is calculated by formula:
d = abs (Red – ithRedColor) + abs(Green – ithGreenColor) + abs(Blue – ithBlueColor)
(NO NEED TO READ THIS FORMULA)

    • Display color name on the window:
Whenever a double click event occurs, it will update the color name and RGB values on the window. Using the cv2.imshow() function, we draw the image on the window. When the user double clicks the window, we draw a rectangle and get the color name to draw text on the window using cv2.rectangle and cv2.putText() functions.
    • Run the Python File:
The Python project is now complete, you can run the Python file from the command prompt. 


Command to run file:
python color_detection.py 


Applications:
    • In self-driving car, to detect the traffic signals.
    • Multiple color detection is used in some industrial robots, to performing pick-and-place task in separating different colored objects.
    • It is also used as a tool in various image editing and drawing apps.(Eyedropper tool)
