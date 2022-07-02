# 2022-HybridIntelligence

## Notes
   test_submission_code.py and train_submission_code.py are templates provided at the competition 
   basalt_utils and kairos_minerl are packages prepared by the authors and are included  in requirements.txt 
   folder "data" is where the dataset will be downloaded 
   "train.zip" include trained models so feel free to use them

## Instructions:

### install Ananaconda 

### Prepare the Environment
   ```
   conda-env create -f environment_gpu.yml # with gpu
   conda-env create -f environment_cpu.yml # without gpu
   ```

   ```
   conda activate basalt
   ```
   ```
   pip install -r requirements.txt
   ```

   (it might be better to install packages seperately when running each code because there has been some issues of incompatible versions) make sure that minerl version is 0.4.4



### Data Processing
1. download dataset
   ```
   python downloadBasaltDataset.py
   ```

2. extract images and actions from the recorded videos 
   ```
   python dataProcessing.py
   ```

3. (optimal) open GUI to label image frames. 
   
   you can skip this and just use the labels folder in the repository after extracting it
   ```
   python labelDataGUI.py
   ```

4. create training data for state classifier ( I forgot that when i worked on this i manually copied images from /data to the corresponding folder in /labels before running this code.  I should have written a code for that)
   ```
   python compileLabels.py
   ```

5. training
   ```
   python stateClassifier.py
   ```

6. cloning behavior 
   ```
   python train.py
   ```

7. still doesn't work as there was weirdly an issue with CUDA just there
   ```
   python test.py 
   ```


## Supply
Original repository: https://github.com/viniciusguigo/kairos_minerl_basalt.git

paper citation: https://arxiv.org/abs/2112.03482
