# Object_size_detection
Object size detection is nothing but calculating height and width of an object. This project can find the height and width of an object by taking some reference ie, with an object of known dimensions. Since the object in an image may appear big when object is close to the camera and small when it is far, so by taking reference object in an image the size of any other objects can be detected in this project

# How to use
Add target images in the Input_images folder    
Run the size_detection file and enter the name of image in Input_images that you want to work on  
Enter the name of image with extension   
Make sure that the reference object in the image should be the first object in the image ie, it should be on the left side   
Now enter the width and height of the reference object which is used in the image  
The output will be displayed in separate window and that output will be saved in Results folder with the name "marked"+image name  

# How it works
First the image will be converted to gray scale  
To detect the object first we need to eliminate back ground so that adaptiveThreshold mask will be applied to the image   
After that contours of the objects will be detected  
Based on area some unwanted contours will be neglected and a close bounding box will be created to the remaining contours  
Since reference object is the first object in the image, the height and width of the bounding box which is having minimum x co-ordinate will be divided by the reference objects height and width to get the ratio  
With that ratio all the remaining bounding boxes dimensions will be decided  
Finally those bounding boxes and dimensions will be drawn on the original image 
