# Assignment 5 - Separation of IPython notebook into various files
The single notebook which used to house everything is now divided into the following files...
* S5.ipynb
* model.py
* utils.py

## model.py
This file would contain the Net() class which is basically the model that we are creating.
Fixes to the code include mapping the output parameters to the input of the convolution.
Also, some of the maxpools are shuffled with ReLu.. so that ReLu is applied first and then the Maxpool.
The stride for Maxpool has been explicity specified as 2. Default is None.
The ReLu was also (in some cases) taking a 2nd parameter which was felt unnecessary. Hence removed.

## utils.py
The following functions from the notebook have been moved into this file...
* GetCorrectPredCount
* train
* test
* plot_stats

These seem to be generic and reusable functions and hence can be placed here.

## S5.ipynb notebook
The following are noteable changes done to the notebook apart from the above code that was moved to various files.
* Import statements were added to import from the above 2 files.
* Known fixes like correcting mean/std, setting test_data, train / test = True etc., are all done.
* The train needed a CrossEntropyLoss without reduction parameter. Hence, 2 separate CrossEntropyLoss are created. The test one has reduction='sum' parameter set.
* After 20 epoch, the accuracy stopped around 99.22%

The training / testing concluded with the following stats
![image](https://github.com/tsai-praveen/era1-assignments/assets/498461/bd992b4d-94c8-4720-ad57-79620c0da93d)

