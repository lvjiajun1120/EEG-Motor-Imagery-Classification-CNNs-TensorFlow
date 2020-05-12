# EEG Motor Imagery Classification via Convolutional Neural Networks (CNN)

EEG Motor Imagery Tasks Classification (by Channels) via Convolutional Neural Networks (CNN) 

Author: Shuyue Jia

Date: December of 2018

### Download Paper
[A novel approach of decoding EEG four-class motor imagery tasks via scout ESI and CNN](https://iopscience.iop.org/article/10.1088/1741-2552/ab4af6/meta)

NOTICE: The method in our paper is EEG source imaging (ESI) + Morlet wavelet joint time-frequency analysis (JTFA) + CNNs, my job is using CNNs to classify the EEG data after the ESI + JTFA process. The Dataset (.mat Files) preprocessed via the ESI + JTFA process can be found via the [Shared Google Drive](https://drive.google.com/drive/folders/1go7_ba_JNG4shob9MJ826gKY8sDSw3jJ?usp=sharing).

Meanwhile, the codes in this repository are based on the raw EEG data without the ESI and JTFA process and also achieve a good result. The main CNNs Tensorflow framework codes in the "MI_Proposed_CNNs_Architecture.py" are the same for both of the work.

### Installation and Usage

#### 1. Python file: PhysioNet_MI_Dataset/MIND_Get_EDF.py

--- download all the EEG Motor Movement/Imagery Dataset .edf files from [here](https://archive.physionet.org/pn4/eegmmidb/)!

#### 2. Python file: Read_Raw_Data_Save_Into_Matlab_Files.py

--- Read the edf Raw data of different channels and save them into matlab .m files

--- At this stage, the Python file must be processed under a Python 2 environment (I recommend to use Python 2.7 version).

#### 3. Matlab file: Saved_Matlab_Data/Preprocessing_Raw_Data.m

--- Pre-process the dataset (Data Normalization mainly) and save matlab .m files into Excel .xlsx Files

#### 4. Python file: MI_Proposed_CNNs_Architecture.py

--- the proposed CNNs architecture 

--- based on TensorFlow 1.12.0 with CUDA 9.0 or TensorFlow 1.13.1 with CUDA 10.0

--- The trained results are saved in the Tensorboard

--- Open the Tensorboard and save the results into Excel .csv files

--- Draw the graphs using Matlab or Origin

### Citation
If you find our work useful in your research, please consider citing in your publications. We provide a BibTeX entry below.

```
@article{hou2019novel,  
    year = 2020,  
    month = {feb},  
    publisher = {{IOP} Publishing},  
    volume = {17},  
    number = {1},  
    pages = {016048},  
    author = {Yimin Hou and Lu Zhou and Shuyue Jia and Xiangmin Lun},  
    title = {A novel approach of decoding {EEG} four-class motor imagery tasks via scout {ESI} and {CNN}},  
    journal = {Journal of Neural Engineering}  
}  
```

### Acknowledgment

We are very grateful to Prof. Yimin Hou due to his friendly guidance, and the research paper would not have happened without him.

