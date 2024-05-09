Add Filters
============


In this activity, you will learn to apply fiters on the camera feed based on the finger's rasied.


<img src= "https://media.slid.es/uploads/1525749/images/10511841/PCP.gif" width = "480" height = "320">



Follow the given steps to complete this activity:
1. Read the finger and set the filter


* Open file main.py.


* Apply various filters to the camera feed based on the right hand fingers.

    `if fingers1[0]== 0:`
    
        `currentFingerUp="Thumb"`
        
        `cameraFeedImg = cv2.cvtColor(cameraFeedImg, cv2.COLOR_BGR2GRAY)`
       
 * If the finger is `index finger` set the filter to `oilpaint`.
        
    `elif fingers1[1] == 1:`
    
        `currentFingerUp = "Index Finger"`
        
        `cameraFeedImg = cv2.xphoto.oilPainting(cameraFeedImg, size=7, dynRatio=1)`
        
  * If the finger is `Middle Finger` the set the filter to `grayscale`.
  
    `elif fingers1[2] == 1:`
    
        `currentFingerUp = "Middle Finger"`
        
        `grayscaleImage = cv2.cvtColor(cameraFeedImg, cv2.COLOR_BGR2GRAY)`
        
        `invertedImg = 255 - grayscaleImage`
        
        `blurredImg = cv2.GaussianBlur(invertedImg, (21, 21), 0)`
        
        `cameraFeedImg = cv2.divide(grayscaleImage, 255 - blurredImg, scale=256)`
                
    `elif fingers1[3] == 1:`
    
        `currentFingerUp = "Ring Finger"`
        
    `elif fingers1[4] == 1:`
    
        `currentFingerUp = "Little Finger"`
        
    `else:`
    
        `currentFingerUp = ""`
        
* Apply various filters to the camera feed based on the left hand fingers.
 
    `if fingers2[0]== 0:`
    
        `currentFingerUp="Thumb"`
        
        `cameraFeedImg = cv2.cvtColor(cameraFeedImg, cv2.COLOR_BGR2GRAY)`
        
    `elif fingers2[1] == 1:`
    
        `currentFingerUp = "Index Finger"`
        
        `cameraFeedImg = cv2.xphoto.oilPainting(cameraFeedImg, size=7, dynRatio=1)`
        
    `elif fingers2[2] == 1:`
    
        `currentFingerUp = "Middle Finger"`
        
        `grayscaleImage = cv2.cvtColor(cameraFeedImg, cv2.COLOR_BGR2GRAY)`
        
        `invertedImg = 255 - grayscaleImage`
        
        `blurredImg = cv2.GaussianBlur(invertedImg, (21, 21), 0)`
        
        `cameraFeedImg = cv2.divide(grayscaleImage, 255 - blurredImg, scale=256)`
        
    `elif fingers2[3] == 1:`
    
        `currentFingerUp = "Ring Finger"`
        
    `elif fingers2[4] == 1:`
    
        `currentFingerUp = "Little Finger"`
        
    `else:`
    
        `currentFingerUp = ""`
* Save and run the code to check the output.
