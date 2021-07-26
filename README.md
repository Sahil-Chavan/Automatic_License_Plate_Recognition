# Automatic_License_Plate_Recognition

Functionality of this project is that it detects License plates of the vehicles using Object Detection and subsequently perform OCR over the detected number plate to obtain the registration number in the form of text.
      
   In terms of implementation I have used SSD ResNet50 (RetinaNet50) for higher accuracy and other one is SSD MobileNet V2 for higher speed. These models used for transfer learning, where they were trained for 3000 epochs on the dataset obtained on Kaggle (https://www.kaggle.com/andrewmvd/car-plate-detection). Then for OCR I have made the use of open source Tesseract OCR (Pytesseract)  for obtaining the registration numbers in text format.

Dataset : https://www.kaggle.com/andrewmvd/car-plate-detection

Model : SSD ResNet50 (RetinaNet50) and SSD MobileNet V2

End point : One can access the system either by the webpage that I have created using Flask, or by using Postman, by accessing the '/api' endpoint, which receives input image through POST File method and provides output image with predictions in base64 format.

End Result : An system which is capable of identifying License plates from an image or from video and obtain the registration number in text format using OCR.

Future Plans : Here I am using an open source OCR - Tesseract. Next I am going to build an OCR from scratch and use it here in place of Tesseract.

Libraries Used : OpenCV, Pytesseract, TFOD, COCOapi, Tensorflow 2.X, Pillow, Flask, Imutils, etc.

Shout Out to all these references :
- https://towardsdatascience.com/automatic-license-plate-detection-recognition-using-deep-learning-624def07eaaf
- https://tensorflow-object-detection-api-tutorial.readthedocs.io/en/latest/auto_examples/plot_object_detection_saved_model.html#sphx-glr-auto-examples-plot-object-detection-saved-model-py
