# Hanhan_COLAB_Experiemnts
Experiements using Google COLAB

## About Google COLab
* It's a convenient tool to use ipython in the cloud. Libraries such as tensorflow, pytorch, keras, etc. are all built in. It also supports team collaboration by sharing the ipython notebook. You can also use free GPU. Saved ipython can also connect to your GitHub or Gist as a saved file too. The user experience is very smooth.
* [How to use COLAB with Free GPU][1]
* To exit playground mode, you need to open the notebook through your google drive.
* How to load images
  * Although the ipython notebook is in google drive, it doesn't mean you can put image in the same folder and can load directly.
  * A good way is to put images in the same folder or any folder in google drive, then "mount drive". This will add everything in drive into the path from where notebook can load directly.
  <img src="https://github.com/hanhanwu/Hanhan_COLAB_Experiemnts/blob/master/images/mount_drive.PNG" width="40%">

## Experiments
* [About SVD - 3 types of python SVD][2]
* [SVD Application][3]
  * Image Compression
    * It's better to use grey photo for compression, otherwise `VT` won't have enough dimension to be used in decomposition when it's color photo
    * One thing noticed here is, even when I was trying to use GPU here, a simple notebook like this one will occupy RAM space fast.
  * https://scikit-learn.org/stable/modules/generated/sklearn.cluster.bicluster.SpectralCoclustering.html

[1]:https://medium.com/deep-learning-turkey/google-colab-free-gpu-tutorial-e113627b9f5d
[2]:https://github.com/hanhanwu/Hanhan_COLAB_Experiemnts/blob/master/SVD_intro.ipynb
[3]:https://github.com/hanhanwu/Hanhan_COLAB_Experiemnts/blob/master/SVD_application.ipynb
