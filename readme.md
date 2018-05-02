Caffe结构
https://blog.csdn.net/ture_dream/article/details/53348301

├── build -> .build_release  //编译结果存放处，.build_release不是一个目录找不到  
├── cmake             //cmake编译用  
│   ├── External  
│   ├── Modules  
│   └── Templates  
├── data               //存放原始数据以及数据获取脚本  
│   ├── cifar10      //存放cifar10小图片原始数据  
│   ├── ilsvrc12    //存放ImageNet Meta数据，原始数据要另外下载  
│   ├── mnist      //存放MNIST手写数字图像数据  
│   └── myself    //存放我的数据，自己建立的  
├── distribute     //编译后生成发布包的位置，用于迁移  
│   ├── bin  
│   └── lib  
├── docker        //用于迁移的工具  
│   ├── standalone  
│   │   ├── cpu  
│   │   └── gpu  
│   └── templates  
├── docs        //doxygen工程文件放这里，可生成Caffe ref_man.pdf  
│   ├── images  
│   ├── _layouts  
│   ├── stylesheets  
│   └── tutorial  
│       └── fig  
├── examples     //存放Caffe简单例程  
│   ├── cifar10   //存放cifar10例程   
│   ├── cpp_classification   //图像分类例程  
│   ├── feature_extraction  //特征提取例程  
│   ├── finetune_flickr_style   //finetune例程  
│   ├── finetune_pascal_detection  //finetune例程  
│   ├── hdf5_classification     //使用HDF5的分类例程  
│   ├── imagenet           //Imagenet例程，使用bvlc_reference_caffenet  
│   ├── images        
│   ├── mnist     //mnist手写字符识别例程  
│   │   ├── mnist_test_lmdb  
│   │   └── mnist_train_lmdb  
│   ├── myself  
│   │   ├── ilsvrc12_train_lmdb  
│   │   └── ilsvrc12_val_lmdb  
│   ├── net_surgery  
│   ├── pycaffe  
│   │   └── layers  
│   ├── siamese  
│   ├── _temp  
│   │   └── features  
│   └── web_demo   //一个Web Server +分类例程  
│       └── templates  
├── include            //Caffe头文件集中存放目录  
│   └── caffe  
│       ├── layers  
│       ├── test  
│       └── util  
├── matlab      //Matlab做Wrapper，具体参考RCNN源码  
│   ├── +caffe  
│   │   ├── imagenet  
│   │   ├── private  
│   │   └── +test  
│   ├── demo  
│   └── hdf5creation  
├── models   //存放示例模型  
│   ├── bvlc_alexnet   //Alexnet模型  
│   ├── bvlc_googlenet  //GoogleNet  
│   ├── bvlc_reference_caffenet  //caffe模拟的Alexnet模型  
│   ├── bvlc_reference_rcnn_ilsvrc13 //Rcnn模型  
│   └── finetune_flickr_style  
├── python               //用于Python wrapper  
│   └── caffe  
│       ├── imagenet  
│       ├── proto  
│       └── test  
├── scripts     //一些文档和数据用到的脚本  
│   └── travis  
├── src          //caffe源码  
│   ├── caffe     
│   │   ├── layers  //各个层具体实现  
│   │   ├── proto   //即所谓的“Protobuf”，帮助caffe提速描述文集，学习数据结果先从这里开始  
│   │   ├── solvers //优化方法类Solver  
│   │   ├── test  
│   │   │   └── test_data  
  
│   │   └── util  //数据转换时用的一些代码。caffe速度快，很大程度得益于内存设计上的优化（blob数据结构采用proto）  
  
                          //  和对卷积的优化（部分与im2col相关）及cudnn加速  
│   └── gtest  
└── tools       //常用学习源码  
    └── extra  