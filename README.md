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
  
## Colab Hacks 🌟
* [How to download large data from a link and unzip the data][16]
  * Sometimes download to your local and then upload to colab might change the data format, better do this
* [Real hacks!][12]
  * Keyboard shortcuts
  * How to increase Colab RAM
  * Stop Colab from disconnecting after 30 mins
  * Saved code snippets - it's in python notebook format, can be resued as a whole
  * Modes in Colab - such as dark mode, they even have Corgi and Kitty mode, the puppies and the cats are moving! That's cool!

## Experiments
* [Practicing Optimization Problems with Pyomo][17]
* [About SVD - 3 types of python SVD][2]
* [SVD Application][3]
  * Image Compression
    * It's better to use grey photo for compression, otherwise `VT` won't have enough dimension to be used in decomposition when it's color photo.
    * One thing noticed here is, even when I was trying to use GPU here, a simple notebook like this one will occupy RAM space fast.
  * [Used in Spectral Clustering][4]
    * Not very straightforward to see SVD is used here. The major part in this algorithm is to find eigenvector, which is also the core part in SVD.
    * Spectural Clustering is using dimensional reduction idea to project the data into a new space, so that clustering can be easier. For some onconvex dataset, methods like kmeans own't work well, but spectural clustering can handle well.
    * Also because its iead is similar to dimensional reduction, spectural clustering can be used to cluster high dimensional data.
  * [Used in Spectral CoClustering][5]
    * SVD is used to find singular vectors. It's more straightforward to see SVD used here.
    * But to visualize biclustering here, can be confusing. Biclustering is trying to find the submatrix of the data that has unique patterns. When spectural clustering can be slow, people use biclustering and spectural clustering together.
    
* [Graph Feature Extraction with DeepWalk][6]
  * The basic idea here is to use RandomWalk to extract sequences from the graph, then convert each sequence into a verctor, this vector can be used for model training, such as predict sequences, calculating the similarity between 2 sequences, etc.
  * [Skip-Gram vs CBOW][7]
    * skip-Gram is tring to predict the context (surrounding nodes/text) given the target node/text, while CBOW predicts the target node/word given the context
  * [Params & Relevant Functions for Word2Vec][8]
    * It's using skip-gram
    * When return the similarity or similar sequences, the input sequence/token has to be in the training input
  * [Sample dataset][9]
  
* [Tensorflow 2.0 Use Case][10]
  * Feature engineering and neural network when using Tensorflow 2.0
  * A simple Google BigQuery to query the public data
  * How to use Tensorflow [tf.dataset][11] for data processing
  
* [Graph DB - Link Prediction][13]
  * Train a model to predict whether 2nodes will be connected or not
  * Needs label data and also assumes the unconnected nodes won't be connected...
  
* [Graph DB - Build Directional Graph][14]
  * Some basics aabout how to build directional graph with edge weights
  
* [How to use Pyspark on colab][15]
  * Very basic

[1]:https://medium.com/deep-learning-turkey/google-colab-free-gpu-tutorial-e113627b9f5d
[2]:https://github.com/hanhanwu/Hanhan_COLAB_Experiemnts/blob/master/SVD_intro.ipynb
[3]:https://github.com/hanhanwu/Hanhan_COLAB_Experiemnts/blob/master/SVD_application.ipynb
[4]:https://scikit-learn.org/stable/modules/generated/sklearn.cluster.SpectralClustering.html
[5]:https://scikit-learn.org/stable/modules/generated/sklearn.cluster.bicluster.SpectralCoclustering.html
[6]:https://github.com/hanhanwu/Hanhan_COLAB_Experiemnts/blob/master/Try_DeepWalk.ipynb
[7]:https://www.kdnuggets.com/2018/04/implementing-deep-learning-methods-feature-engineering-text-data-skip-gram.html
[8]:https://radimrehurek.com/gensim/models/word2vec.html#gensim.models.word2vec.Word2Vec
[9]:https://github.com/hanhanwu/Hanhan_COLAB_Experiemnts/blob/master/dataset/environment_wiki_graph.tsv
[10]:https://github.com/hanhanwu/Hanhan_COLAB_Experiemnts/blob/master/tensorflow2_training_day1.ipynb
[11]:https://www.tensorflow.org/api_docs/python/tf/data/Dataset
[12]:https://www.analyticsvidhya.com/blog/2020/04/5-amazing-google-colab-hacks-you-should-try-today/?utm_source=feedburner&utm_medium=email&utm_campaign=Feed%3A+AnalyticsVidhya+%28Analytics+Vidhya%29
[13]:https://github.com/hanhanwu/Hanhan_COLAB_Experiemnts/blob/master/link_prediction.ipynb
[14]:https://github.com/hanhanwu/Hanhan_COLAB_Experiemnts/blob/master/directional_graphDB.ipynb
[15]:https://github.com/hanhanwu/Hanhan_COLAB_Experiemnts/blob/master/spark_colab.ipynb
[16]:https://colab.research.google.com/drive/1JwDl3HZ9SfvV5crtjbuFPaU_T7Q1y34w?usp=sharing#scrollTo=BuM8UGy5lJu2
[17]:https://github.com/hanhanwu/Hanhan_COLAB_Experiemnts/tree/master/optimization_practice
