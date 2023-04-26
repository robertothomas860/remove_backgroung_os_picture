# remove_backgroung_of_picture

You can use this code by downloading OpenCV library in Python

# Usage

Add the following to your page


```html
import cv2

img = cv2.imread('image.jpg')

gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

ret, mask = cv2.threshold(gray, 240, 255, cv2.THRESH_BINARY_INV)

masked_img = cv2.bitwise_and(img, img, mask=mask)

cv2.imwrite('result.jpg', masked_img)
```

# Author
 Roberto Thomas - https://metroroutes.in/


# Contact Us

If you have any query or suggestion please reach us at
info@metroroutes.in
