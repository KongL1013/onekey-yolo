# onekey-yolo
特性：
支持三种模式：train,test,re_train
支持yolo和yolo-tiny
支持图片增强 库安装：http://202.120.54.12/?p=913
对图片格式无特殊要求，保持一致即可

使用方法：

1.下载yolo
git clone https://github.com/pjreddie/darknet
cd darknet

2.配置Makefile，使用GPU，CUDN以及Opencv
GPU=1
CUDNN=1
OPENCV=1
OPENMP=0
DEBUG=0

3.在darknet文件夹下编译
make

4.下载训练权重到darknet文件夹下：
yolo: wget https://pjreddie.com/media/files/darknet53.conv.74
yolo-tiny: wget https://pjreddie.com/media/files/yolov3-tiny.weights
5.在darknet/data/下新建yolo_data文件夹

6.在yolo_data文件夹下新建三个文件夹
pic:用来装你的图片
xml:用来装你的标注结果.xml
yolo_script:用来装脚本，下载下面的文件并解压即可

7.在yolo_script中的configer.py中修改你的参数，参数含义有注释

8.在yolo_script文件夹下运行pyhton main_yolo.py即可开始训练

如果后续有bug，请联系我及时修改
