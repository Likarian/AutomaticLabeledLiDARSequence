# Learning-Based Human Segmentation and Velocity Estimation Using Automatic Labeled LiDAR Sequence for Training

Automatic Labeled LiDAR Sequence Data are novel data with human label. The data contain various generated LiDAR sequence with human label. To download the data, please check your free disk space enough and run 'DownloadAndUnzip.sh'. You can also download the data by the following URL.

* TrainData (27.2GB) : http://www.ok.sc.e.titech.ac.jp/res/LHD/TrainData.tar.gz
* TrainDataAddit (166GB) : https://data.airc.aist.go.jp/AutomaticLabeledLiDARData/TrainDataAddit.tar.gz
* TestSet (4.6GB) : https://data.airc.aist.go.jp/AutomaticLabeledLiDARData/TestSet.tar.gz
  
The paper of the Automatic Labeled LiDAR Sequence Data :  
 **Wonjik Kim, Masayuki Tanaka, Masatoshi Okutomi, Yoko Sasaki, "Learning-Based Human Segmentation and Velocity Estimation Using Automatic Labeled LiDAR Sequence for Training", IEEE Access, 2020.** ([link](https://ieeexplore.ieee.org/abstract/document/9090135))

---
# How to use
### Dependencies
* Python 3.6.6
* Tensorflow 1.13.0-rc0
* Keras 2.2.4
* Cuda 10.0

### Run DownloadAndUnzip.sh
In your own directory, please run the following command in terminal.
<br>
> bash ./DownloadAndUnzip.sh 

### Sample code
In directory of './TestSet', you can see sample code for performance evaluation. When you want to check sample code, please run the following command in that directory.
<br>
> python Test_Real(or Gen)Data.py --test Real (or Gen) --network 16_frame.hdf5 --gpu 0 --frame 16

---
### Directory Specification

* TrainData
    * Train_h5file
        * h5file : *containing 32K (32 frames, 1K sequences) hdf5 files*

* TrainDataAddit
    * h5file : *containing 32K (32 frames, 6K sequences) hdf5 files*
    * xml : *containing 32K (32 frames, 6K sequences) xml files*

* TestSet
    * TestCode
        * 16_frame.hdf5 : *trained network using 16 frames*
        * architecture.py : *network architecture description*
        * mtutil.py
        * Test_RealData.py : *sample code for test with real data*
        * Test_GenData.py : *sample code for test with simulation data*
    * Data
        * Real : *3,200 (32 frames, 100 sequences) hdf5 files*
        * Gen : *3,456 (32 frames, 108 sequences) hdf5 files*

---
# License
Automatic Labeled LiDAR Sequence Data are allowed only for noncommercial usage. Please cite our paper if our data were used in your work.
You can see specific terms of use in the LICENSE.md.

