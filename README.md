# CSBP441_ASG1_Logo_G14
This is Assignment 1 for our Group (G14) for the Applied Computer Vision class in UAEU.

# Overview
In this project, we used Python and OpenCV to recreate Logo 14 (the Louis Vuitton LV) logo, which is based entirely on letters and text. Since the design relies on textual elements rather than geometric shapes, we decided to use OpenCV’s text-rendering functions (cv2.putText) to implement the logo. We experimented different font styles to achieve the closest possible match, using an italic “L” and a standard “V” in large font sizes to mimic the overlapping LV monogram. Below these letters, we added the full brand name “LOUIS VUITTON” in a smaller plain font as in the original logo. The final output was displayed directly in Google Colab using cv2_imshow and also saved as an image file. This approach demonstrates how OpenCV’s text functions can be adapted to replicate a clean, structured, and professional-looking logo.

## Contents of this Repository
- The PDF file of the assignment report: [CSBP441_ASG1_Logo_G14.pdf](https://github.com/user-attachments/files/22108548/CSBP441_ASG1_Logo_G14.pdf)

- Google Colab Link for the working code: https://colab.research.google.com/drive/1kD6eFPWCfSrDFvy8dJw8JXXEuL-PiMB2?usp=sharing

## The original Logo we are trying to implement
<img width="336" height="335" alt="image" src="https://github.com/user-attachments/assets/f9776dbb-77d2-452c-a946-fc96db597d0c" />


## The Full Code
!pip install opencv-python-headless

import cv2
import numpy as np
from google.colab.patches import cv2_imshow  # for displaying images in Colab


canvas = np.ones((500, 500, 3), dtype="uint8") * 255


font = cv2.FONT_HERSHEY_TRIPLEX
font_italic = cv2.FONT_HERSHEY_TRIPLEX | cv2.FONT_ITALIC


cv2.putText(canvas, "L", (100, 300), font_italic, 10, (0, 0, 0), 10, cv2.LINE_AA)


cv2.putText(canvas, "V", (90, 270), font, 10, (0, 0, 0), 10, cv2.LINE_AA)


cv2.putText(canvas, "LOUIS VUITTON", (100, 330), cv2.FONT_HERSHEY_PLAIN, 1.3, (0, 0, 0), 2, cv2.LINE_AA)


cv2_imshow(canvas)


cv2.imwrite("logo14_lv.png", canvas)

## The output of the code
<img width="500" height="500" alt="logo14_lv" src="https://github.com/user-attachments/assets/553704cb-7f64-42de-9fbf-35a0ad98e713" />


## Group Members
- Mohammed Alnuaimi
- Ahmed Almasiyuli
- Abdullah Al-khamisani

## Course Instructor
- Dr. Munkhjargal Gochoo
