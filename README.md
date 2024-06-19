# Mussel Measurement
Amber Waymouth COSC428 project

# Mussel Measurement using Detectron 2 
This project uses Detectron2 to detect and measure mussels to promote sustainable mussel farming. 

## Data 
Data (images) is contained in the data folder. Training images are used to train the model and validation images are used to validate the model. The annotations used are input into the "train.py" file where the path to the validation and training COCO files are required. Annotations can be found in the labels folder within the object detection folder. 

## Training the model. 
The model is already trained and the output file used to inference unseen data is the model_final_p275ba.pkl file in the object_detection/weights folder. To retrain, copy the path of the COCO files containing your validation and training annotations into the train.py file. 

## Inferencing data 
Test images can be found in images/inputs. Paste the path of the desired test image into the imread function for the image variable at the start of the main function in inference_my_dataset.py. Then run. An image containing dimensions for each mussel in the input image will be returned. This is done through obtaining the coordinates of each of the generated bounding boxes and converting the length and width of these in pixels to millimetres. 
