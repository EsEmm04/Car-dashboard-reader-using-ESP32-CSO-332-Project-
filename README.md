Ubiquitous Computing – Dashboard Data Extraction
📌 About the Project

This project focuses on extracting key information from car dashboard images using image processing techniques in Python.
The system retrieves:

🚗 Speed
⛽ Fuel level
⏱ Time
📍 Distance travelled

⚙️ Features

1) Speedometer Detection → Detects needle position using edge detection and Hough Lines, maps it to calibrated speed.
2) Time & Distance Extraction → Uses OCR (Tesseract) with preprocessing (grayscale, normalization, blur, ROI).
3) Fuel Gauge Detection → Pixel counting after thresholding to calculate fuel percentage.
4) Database & Web Access → Data stored in MongoDB and accessible via a hosted Glitch website.

🖥️ Image Processing Pipeline

🔹 Speed Detection
- Convert image to grayscale
- Apply Gaussian blur
- Canny edge detection
- Detect lines with HoughLinesP
- Find longest line (needle)
- Calculate angle → map to speed

🔹 Time & Distance Extraction
- Grayscale conversion & normalization
- Gaussian blur + thresholding
- Define Region of Interest (ROI)
- OCR with Pytesseract
- Post-processing for valid formats

🔹 Fuel Gauge Detection
- Grayscale + normalization
- Gaussian blur + thresholding
- ROI selection
- Pixel counting (cv2.countNonZero)
- Ratio → fuel percentage
  
Input :
<img width="709" height="503" alt="image" src="https://github.com/user-attachments/assets/de5833dd-547b-4242-900a-058c448d1ebe" />

Output : 
<img width="792" height="437" alt="image" src="https://github.com/user-attachments/assets/fd556888-fbab-451f-a134-7897a57af7f7" />

