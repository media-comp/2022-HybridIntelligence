# 2022-HybridIntelligence

1/ install Ananaconda 

2/ run conda-env create -f environment.yml

3/ run conda activate basalt

4/ run pip install -r requirements.txt (it might be better to install packages seperately when running each code because there has been some issues of incompatible versions) make sure that minerl version is 0.4.4

5/ run downloadBasaltDataset.py to download dataset ( it will be downloaded in the file data )

6/ run dataProcessing.py to extract images and actions from the recorded videos 

7/ run labelDataGUI.pyto open GUI to label image frames. ( you can skip this an djust use the labels folder in the repository after extracting it)

8/ run compileLabels.py to create training data for state classifier ( I forgot that when i worked on this i manually copied images from /data to the corresponding folder in /labels before running this code.  I should have written a code for that)

9/run stateClassifier for training

10/ run train.py for cloning behavior 

11/ test.py still doesn't work as there was weirdly an issue with CUDA just there
