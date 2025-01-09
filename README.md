# Face_detection_and_tracking
This project involves using the Tracker Boosting method in OpenCV to detect and track a face in a live camera stream

The script begins by importing essential libraries, including cv2 for OpenCV functionalities and numpy for numerical operations. A function named ask_confirmation is defined to prompt the user to activate the face detector by pressing '0' or to exit by pressing the ESC key. Based on the user's input, a Tracker Boosting object is created using cv2.legacy.TrackerBoosting_create().

The main function then proceeds by setting up the video capture from the default camera using cv2.VideoCapture(0). The first frame is read from the video capture, and the user is prompted to select the region of interest (ROI) using cv2.selectROI. This ROI defines the object to be tracked.

The tracking process is initiated using the tracker.init method with the initial frame and selected ROI. The main loop continuously reads new frames from the video capture. For each new frame, the tracker updates the ROI based on the detected object in the current frame using the tracker.update method. The updated ROI is a tuple containing four floats representing the coordinates (x, y, w, h).

If the tracking is successful, a rectangle is drawn around the detected face using cv2.rectangle, with the coordinates of the top-left and bottom-right corners of the rectangle. If the tracking fails, a message "Failure to Detect Tracking!!" is displayed on the frame using cv2.putText. The tracker type is also displayed on the frame.

The resulting frame with the tracked face is displayed using cv2.imshow. The loop continues until the ESC key (key code 27) is pressed, at which point the video capture is released, and all OpenCV windows are closed.

![image](https://github.com/user-attachments/assets/6aa9bfd4-1202-4399-90dd-c7870689868e)
![image](https://github.com/user-attachments/assets/e5bd8a14-8012-4bd5-b8a3-9b0dac1cdde5)
![image](https://github.com/user-attachments/assets/6af6dd86-aeea-465e-b681-e4e9281b33d8)
