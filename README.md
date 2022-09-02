# OCR-with-Pyautogui
This is a little simple version of OCR that utilizing pyautogui to detect number and write it out
 
 ## How it work
 The basic idea of this is using a chain of image identifier, that is wrap inside a list. detecting time is a long O(1) but still in a manageable range
 
 2 major concept applied:
  * Recursion to call for detecting phase, if met with unexpected value, the function will do recursion and run the function again
  * Pyautogui detect image, therefore, being binded by the image detecting time of cv2 (can be improved by changing the way this script scan through it image list

 Just a quick-note, this script can autoclick and buy off the object that have the auction amount it feel the best.Hence, a little combination of OCR, Non-Ai-Stimulator autoclick based on a pre-set amount of resource that user feel comfortable to buy and send away without monitoring
 
 This could be considered as one of the most confused script that I've ever written up to now(2022) due to it core-value of dealing with list and iteration

## Demonstration:

Noticed the number value on the right, the purpose me me first making this list is to find something that detecting number in a specific region
 
 ![GifMaker_20220723221816709](https://user-images.githubusercontent.com/76143641/187845632-0d37a06f-1f59-402b-9c79-1ceee54fd13e.gif)
 
 And here is the output from the terminal:
 
![GifMaker_20220723221430999](https://user-images.githubusercontent.com/76143641/187845792-0907677a-3f82-4df1-9929-b657f8c57ccb.gif)
