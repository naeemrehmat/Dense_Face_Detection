# Dense Face Detection in All Orientation
<p >

Aim of this project was to detect faces from image irrespective of face orientation and 
number of faces in an image. Furthermore, draw boundingboxes on face and landmarks on eyes, nose, and 
mouth. RetinaFace has state-of-the-art results on WIDER FACE dataset but it is 
unable to detect faces in a rotated image like the exmaple in below image.

</p>

![alt text](https://raw.githubusercontent.com/naeemrehmat/Dense_Face_Detection/master/r35_Old_Model.jpg)

To solve this problem, I modified the RetinaFace implementation by introducing a new input layer 
which randomly rotate an image at an angle of 0, 90, 180, and 270. This improved the results significantly.
After training the resultant model has output like below:

![alt text](https://raw.githubusercontent.com/naeemrehmat/Dense_Face_Detection/master/r180_35.jpg)

Trained model weights can be accessed from the <a href= "https://drive.google.com/open?id=1cUnpwQpCLA87g1twhXx0TgEGAgf3Zeo2" >  link </a>.
Clone this repo, install requirements as mentioned in "RetinaFace/requirements.txt" and use the following command to test the model.

```
python RetinaFace/detect.py --model_path model.pt --image_path file_name.jpeg
```

Done.

