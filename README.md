# Driver-Drowsiness-Detection


### Problem Statement
The primary objective of this project is to develop a system that can accurately detect when a driver is becoming drowsy and issue alerts to prevent potential accidents.


### Dataset Description / Logic of the project
The project utilizes the Dlib library's facial landmark detector, specifically the 68-point facial landmark model, to identify key points on the driver's face. By analyzing these landmarks, particularly the eyes, the system determines whether the driver's eyes are open or closed.

68-Landmark Detector Data   
The data file (.dat) for the 68-landmark detector used in the project can be found here.


### Code Explanation
The code performs the following steps:
1.	Import necessary libraries: OpenCV, NumPy, Dlib, imutils, and Pygame.
2.	Initialize the camera and check if it is opened successfully.
3.	Initialize face detector and landmark detector using Dlib.
4.	Define functions to compute distances between facial landmarks and determine if the eyes are blinked.
5.	Set up variables to track eye state (sleep, drowsy, active) and eye closure duration.
6.	Load an alert sound using Pygame.
7.	Enter the main loop for video processing:   
    •	Read frames from the camera.
    •	Detect faces and facial landmarks in the frame.
    •	Determine the state of the eyes (blinked, partially blinked, or not blinked) based on the landmark positions.
    •	Update the eye state variables and eye closure timer.
    •	If the eye closure duration exceeds a threshold, trigger an alarm sound.
    •	Display the current status (sleeping, drowsy, or active) on the frame.
    •	Display the processed frames with facial landmarks.
    •	Exit the loop if the 'Esc' key is pressed.
8.	Release resources and close windows.


### Requirements
•	Python 3.x   
•	Dlib   
•	OpenCV   
•	Numpy   
•	Imutils   
•	Pygame for alert sounds


### Usage
1.	Clone or download the repository.
2.	Install the required libraries (OpenCV, NumPy, Dlib, imutils, Pygame).
3.	Place the shape_predictor_68_face_landmarks.dat file (a pre-trained facial landmark detector) in the same directory as the script.
4.	Place the Alert_Sound.mp3 file (an alert sound) in the same directory as the script.
5.	Run the driver_drowsiness.py script.
6.	The script will open a window displaying the camera feed, face detection, and eye state detection.
7.	If the driver is detected as drowsy or sleeping for a prolonged period, an alarm sound will be played.
8.	Press the 'Esc' key to exit the application.  

### Note   
The eye closure threshold and other parameters can be adjusted in the code to fine-tune the drowsiness detection sensitivity.


### Working of the Project
1.	The project detects facial landmarks using the 68-landmark detector.
2.	The ratio used to determine the eye state is calculated as: Sum of distances of vertical landmarks divided by twice the distance between horizontal landmarks.
3.	This ratio is dependent on your system, and you may need to configure the thresholds for the sleeping, drowsy, and active states accordingly.
4.	If the driver is detected as drowsy or sleeping for a prolonged period, an alarm sound will be played to alert the driver.
5.	The program displays the camera feed, face detection, eye state detection, and the current status (sleeping, drowsy, or active) on the frame.
6.	Press the 'Esc' key to exit the application.


### Results
The Driver Drowsiness Detection system was rigorously tested and demonstrated a high degree of effectiveness in real-time identification of driver drowsiness through eye closure metrics.    Key highlights from the system's performance include:   
•	Detection Accuracy: The system consistently identified drowsiness with remarkable accuracy, thanks to its sophisticated facial landmark analysis.
•	Alert Response: Immediate alerting mechanism upon detection of drowsiness, proving its potential in averting risk-prone driving scenarios.   
These outcomes underscore the system's reliability in enhancing driving safety by mitigating drowsiness-related risks on the road.
