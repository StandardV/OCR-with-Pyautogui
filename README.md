# OCR-with-Pyautogui
This is a little simple version of OCR that utilizing pyautogui to detect number and write it out
 
 ## How it work
 The basic idea of this is using a chain of image identifier, that is wrap inside a list. detecting time is a long O(1) but still in a manageable range
 
 2 major concept applied:
      * Recursion to call for detecting phase, if met with unexpected value, the function will do recursion and run the function again
      * Pyautogui detecting image, therefore, being binded by the detecting of cv2 (can be improved by changing the way this script scan through it image list
