# NYX-wolves-Deep-Learning-Task

Install both mediapipe and opencv-python using pip


!pip install mediapipe opencv-python


Step 1: Import Libraries
Import the necessary libraries: cv2, mediapipe, and numpy.

Step 2: Initialize Pose Estimation
Initialize the MediaPipe Pose model for pose estimation.
Set confidence thresholds for detection and tracking.

Step 3: Capture Video
Open the video file using cv2.VideoCapture.
Get the frame dimensions using the get() function.

Step 4: Create Video Writer
Create an output video writer using cv2.VideoWriter.
Specify the codec, frame rate, and frame dimensions for the output video.

Step 5: Process Frames for Pose Estimation
Loop through video frames using cap.isOpened().
Read each frame using cap.read().
Convert the color format of the frame from BGR to RGB using cv2.cvtColor().

Step 6: Estimate Poses and Draw Landmarks
Process the frame with the Pose model using pose.process().
Extract pose landmarks using results.pose_landmarks.
Draw bounding boxes around detected poses and pose keypoints using OpenCV functions.

Step 7: Recognize Actions
Define a dictionary of action classes and their associated landmarks.
Iterate through actions and check if all required keypoints are visible.
If visible, store the detected actions.

Step 8: Annotate Frame with Detected Actions
Display detected actions on the video frame using cv2.putText().

Step 9: Write Processed Frame to Output Video
Write the annotated frame to the output video using out.write().

Step 10: Release Resources
Release the video capture and writer objects using release().

Step 11: Process Output Video
Open the processed output video using cv2.VideoCapture.

Step 12: Recognize and Annotate Actions in Output Video
Similar to Step 7, recognize actions from the processed output video frames.
Annotate the actions on the frames using cv2.putText().

Step 13: Create Output Video File
Create an output video file for the annotated output video frames.

Step 14: Release Resources and Close Windows
Release the video capture, writer, and window objects using release() and destroyAllWindows().
