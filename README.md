# Age and Gender Estimation
This is a Keras implementation of a CNN for estimating age and gender from a face image .
In training, [the IMDB-WIKI dataset](https://data.vision.ee.ethz.ch/cvl/rrothe/imdb-wiki/) is used.

## Dependencies
- Python 3
- Keras2.0+
- scipy, numpy, Pandas, tqdm
- OpenCV

Tested on:
- CPU ,GPU:k80 (colab)
- Python 3.6.0, Keras 2.0.2, Tensorflow 1.0.0

#### Download the dataset
The dataset is downloaded and extracted to the `data` directory.

!wget https://data.vision.ee.ethz.ch/cvl/rrothe/imdb-wiki/static/imdb_crop.tar


#### Train network
Train the network using the training data created above.
 
#### Plot training curves from history file

```sh
python3 plot_history.py --input models/history_16_8.h5 
```


##### Results with data
The val_loss was 4.7



## Network architecture

Here the Wide Residual Network (WideResNet) is trained from scratch.
The implementation of the WideResNet; two classification layers (for age and gender estimation) are added on the top of the WideResNet.

While age and gender are independently estimated by different two CNNs ,they are simultaneously estimated using a single CNN.


## Results
Trained on imdb, tested on imdb

## Refrences 
https://www.openu.ac.il/home/hassner/projects/cnn_agegender



