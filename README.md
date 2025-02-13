# Computer_Vision-Camera-calibration-using-OpenCV-and-Python

# Camera Calibration using OpenCV

This repository contains Python code for calibrating a camera using OpenCV. The code utilizes chessboard images to determine the camera's intrinsic parameters, including the camera matrix and distortion coefficients.

## Description

The `calibrate_chessboard.py` script performs the following steps:

1. **Image Loading:** Reads chessboard images from a specified directory.  The image paths are globbed by a specific pattern.
2. **Chessboard Corner Detection:** Detects chessboard corners in each image using `cv.findChessboardCorners()`.
3. **Corner Refinement:** Refines the detected corners using `cv.cornerSubPix()` for subpixel accuracy.
4. **Object and Image Point Storage:** Stores the 3D object points (representing the chessboard corners in the real world) and the corresponding 2D image points.
5. **Camera Calibration:** Calibrates the camera using `cv.calibrateCamera()` with the collected object and image points. This function returns the camera matrix, distortion coefficients, rotation vectors, and translation vectors.
6. **Output:** Prints the calibration results, including the `retval`, `camera_matrix`, `dist_coefs`, `rvecs`, and `tvecs`.

## Requirements

To run this code, you need the following libraries:

* Python 3
* OpenCV (`cv2`)
* NumPy (`numpy`)
* glob
* Matplotlib (`matplotlib`)

You can install these libraries using pip:

```bash
pip install opencv-python numpy matplotlib
