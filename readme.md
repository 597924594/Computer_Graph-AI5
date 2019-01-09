AI5:  王明达，郑宏锴，王晨

共有三个模型四种方法point net++用于分类，point net++用于分割两种方法，和point CNN
环境配置详见Point net++和point netCNN的环境配置
运行Model Based on PointNet++ Classiﬁcation Branch：进入pointnet文件夹，直接运行python train.py
运行Point-Focused Model Based on PointNet++ Segmentation Branch ：进入pointnet文件夹中，指令python train.py --model pointnet2_sem_seg
运行Tooth-Focused Model Based on PointNet++ Segmentation Branch ，指令python train.py --model pointnet2_sem_seg --seg_version=2
point net++的acc都直接输出，也可以在train.txt中查看预测正确的个数，

PointCNN 的环境应当与Pointnet相同，如果有差错详见PointCNN的环境配置
运行Model based on X-Conv 进入PointCNN/pointcnn_cls 中，执行./train_val_mnist.sh -g 0 -x cls_teeth, 运行的结果保存在上一级目录的models/cls中，其中有pointcnn_cls_teeth.txt显示一次运行的反馈，和文件夹里保存的每一次运行保存的参数和log信息等，可以看到保存的每一次训练的acc