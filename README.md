# remove_backgroung_of_picture

You can use this code by downloading OpenCV library in Python

# Usage

Add the following to your page

import cv2

# Load the image
img = cv2.imread('image.jpg')

# Convert the image to grayscale
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

# Apply a threshold to the image to create a mask
ret, mask = cv2.threshold(gray, 240, 255, cv2.THRESH_BINARY_INV)

# Apply the mask to the image to remove the background
masked_img = cv2.bitwise_and(img, img, mask=mask)

# Save the resulting image
cv2.imwrite('result.jpg', masked_img)
