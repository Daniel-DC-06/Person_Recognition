Person Recognition using OpenCV and Face Recognition

Description

This is a simple real-time person recognition system using OpenCV and the face_recognition library. The program captures video from the webcam, detects faces, and recognizes known individuals.

Features

Detects faces in real-time using a webcam.

Recognizes up to two known individuals and assigns them predefined labels.

Displays a rectangle around detected faces with corresponding names.

Assigns "Unknown" label to unrecognized faces.

Requirements

Make sure you have the following dependencies installed:

pip install opencv-python face-recognition numpy

Installation

Clone this repository and navigate into the project folder:

git clone https://github.com/yourusername/person_recognition.git
cd person_recognition

Usage

Run the script to start face recognition:

python person_recognition.py

Press q to quit the application.

Code Explanation

cv2.VideoCapture(0): Opens the webcam for video capture.

cv2.cvtColor(frame, cv2.COLOR_BGR2RGB): Converts the captured frame to RGB format.

face_recognition.face_locations(rgb_frame): Detects face locations in the frame.

face_recognition.face_encodings(rgb_frame, face_locations): Extracts face encodings.

face_recognition.compare_faces([encoding], face_encoding): Compares the detected face encoding with known encodings.

cv2.rectangle(frame, (left, top), (right, bottom), (0, 255, 0), 2): Draws a rectangle around detected faces.

cv2.putText(frame, name, (left, top - 10), cv2.FONT_HERSHEY_SIMPLEX, 0.6, (0, 255, 0), 2): Displays the recognized name above the face.

cv2.imshow("Face Recognition", frame): Shows the processed video frame with face recognition.

cv2.waitKey(1) & 0xFF == ord("q"): Closes the program when the 'q' key is pressed.

Contributing

Feel free to fork this repository and submit pull requests for improvements.

License

This project is licensed under the MIT License.


Author
Daniel Christopher M

