
# action-recognition

### Dataset used :
 https://www.kaggle.com/mateohervas/dcsass-dataset
 [https://www.crcv.ucf.edu/data/UCF-ARG.php](https://www.crcv.ucf.edu/data/UCF-ARG.php) 
 Merge these datasets into one folder.
 
## 3DCNN

### Requirements :
python3  
opencv3 (with ffmpeg), keras, numpy, tqdm

 ### Options 
 Options of 3dcnn.ipynb are as following:  
`--epoch`: the number of epochs, default is 100  
`--videos`: a name of directory where dataset is stored, default is UCF101  
`--nclass`: the number of classes you want to use, default is 101  
`--output`: a directory where the results described above will be saved  
`--color`: use RGB image or grayscale image, default is False  
`--skip`: get frames at interval or contenuously, default is True  
`--depth`: the number of frames to use, default is 10

To train the model, change the dataset path and output path in 3DCNN.ipynb file and run it

## 2DCNN+LSTM
### Requirements :
python3  
opencv3 (with ffmpeg), keras, numpy, tqdm

 ### Options 
 Options of 2DCNN+LSTM.ipynb are as following:  
`--batch`: batch size, default is 128  
`--epoch`: the number of epochs, default is 100  
`--videos`: a name of directory where dataset is stored, default is UCF101  
`--nclass`: the number of classes you want to use, default is 101  
`--output`: a directory where the results described above will be saved  
`--color`: use RGB image or grayscale image, default is False  
`--skip`: get frames at interval or contenuously, default is True  
`--depth`: the number of frames to use, default is 10

To train the model, change the dataset path and output path in 2DCNN+LSTM.ipynb file and run it.

## TSN
### Requirements
-   Ubuntu
-   PyTorch 1.4.0
-   Pillow 7.0.0
-   a GPU

### Options

`dataset`: dataset name 
`modality`:RGB /RGBDiff /Flow
`trainset`: a name of directory where train dataset is stored
`validationset`: a name of directory where validation dataset is stored
`base_model`: name of the model used from tf_model_zoo, defalut is BNInception
`n_segment`: number of sagments taken for each video
`consensus_type`: type of consensus funtion
`dropout`: dropout ratio for the layers
`epoch`: number of epoch for train the model
`batch_size`: batch size to be processed at a time
`lr`: learning rate 
`lr_step`: [30,  60],
`momentum`:  momentum factor for SGD optimiser, default is 0.9,
`weight_decay`: weight decay for SGD optimiser, default is 5e-4.
`clip_gradient`: max norm of the gradients
`print_every`:  number of data items after which accuracy, loss of the model has to be printed, default is 20.
`validation_every`:  number of epochs after which accuracy, loss of the model has to be printed, default is 5.

To train the model frst split the dataset into train and test data and change the parameters in TSN.ipynb file and run it.

 
