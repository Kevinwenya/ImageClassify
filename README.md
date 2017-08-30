# ImageClassify
图像分类--从原理到实现

### 花卉分类
    主要通过CNN进行花卉的分类，训练结束保存模型，最后通过调用模型，输入花卉的图片通过模型来进行类别的预测。
### 运行环境
    python2.7 + tensorflow1.0
### 训练测试
    直接运行：python imageclassify.py 即可

### 损失及准确率
    train loss: 1.607422
    train acc: 0.246875
    validation loss: 1.604662
    validation acc: 0.232955
        ......

    train loss: 0.755110
    train acc: 0.707292
    validation loss: 0.940745
    validation acc: 0.630682

    train loss: 0.701427
    train acc: 0.733681
    validation loss: 1.012621
    validation acc: 0.637784
###### 由上述结果可以看出，模型已经过拟合，为此，在源代码中，加入drop-out防止过拟合：
    dropout = tf.layers.dropout(inputs=re1, rate=0.5)
