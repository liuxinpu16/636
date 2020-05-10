# 636
Set up:
1,Creat a folder in C: named 'tensorflow1'

2,Download:https://github.com/tensorflow/models

3,Unzip the downloaded zip file into C:\tensorflow1

4,Rename folder 'models-master' to 'models'

5,Then go to C:\tensorflow1\models\research\object_detection

6,Go to my google drive:https://drive.google.com/drive/folders/1zBY1Ho4upCBiLz40McRmMAeOu9mE56oa?usp=sharing

7,Dowload Rar file:"636_object_detection" 
  
8,Unzip the downloaded file into object_detection folder.

  Make sure every file go to it's place.
  
  The model file go to C:\tensorflow1\models\research\object_detection\inference_graph
  
  labelmap.pbttxt go to C:\tensorflow1\models\research\object_detection\training
  
  visualization_utils.py go to C:\tensorflow1\models\research\object_detection\utils
  
  test.ipynb stay in C:\tensorflow1\models\research\object_detection\

9,Set up the enviroment:

10,Open anaconda prompt and run the following commands:

conda create -n tensorflow1 pip python=3.6

activate tensorflow1

python -m pip install --upgrade pip

conda install tensorflow-gpu==1.15

conda install -c anaconda protobuf

pip install pillow

pip install lxml

pip install Cython

pip install contextlib2

pip install jupyter

pip install matplotlib

pip install pandas

pip install opencv-python

conda install git   

pip3 install "git+https://github.com/philferriere/cocoapi.git#egg=pycocotools&subdirectory=PythonAPI"

cd C:\tensorflow1\models\research

protoc --python_out=. .\object_detection\protos\anchor_generator.proto .\object_detection\protos\argmax_matcher.proto .\object_detection\protos\bipartite_matcher.proto .\object_detection\protos\box_coder.proto .\object_detection\protos\box_predictor.proto .\object_detection\protos\eval.proto .\object_detection\protos\faster_rcnn.proto .\object_detection\protos\faster_rcnn_box_coder.proto .\object_detection\protos\grid_anchor_generator.proto .\object_detection\protos\hyperparams.proto .\object_detection\protos\image_resizer.proto .\object_detection\protos\input_reader.proto .\object_detection\protos\losses.proto .\object_detection\protos\matcher.proto .\object_detection\protos\mean_stddev_box_coder.proto .\object_detection\protos\model.proto .\object_detection\protos\optimizer.proto .\object_detection\protos\pipeline.proto .\object_detection\protos\post_processing.proto .\object_detection\protos\preprocessor.proto .\object_detection\protos\region_similarity_calculator.proto .\object_detection\protos\square_box_coder.proto .\object_detection\protos\ssd.proto .\object_detection\protos\ssd_anchor_generator.proto .\object_detection\protos\string_int_label_map.proto .\object_detection\protos\train.proto .\object_detection\protos\keypoint_box_coder.proto .\object_detection\protos\multiscale_anchor_generator.proto .\object_detection\protos\graph_rewriter.proto .\object_detection\protos\calibration.proto .\object_detection\protos\flexible_grid_anchor_generator.proto

python setup.py build

python setup.py install



To test on video and webcam:

put the test video at:  C:\tensorflow1\models\research\object_detection\

run the following commands in anaconda prompt with 'tensorflow1' enviroment:

cd C:\tensorflow1\models\research\object_detection\

jupyter notebook test.ipynb




