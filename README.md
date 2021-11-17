# HandWriteOCR
OCR TASK based on hand input.

# Environments

- PaddlePaddle 2.0.1
- Python 3.7

# [baseline地址](https://aistudio.baidu.com/aistudio/projectdetail/2793088?forkThirdPart=1)
# 运行方法：
1. 下载[2021A_T1_Task1_数据集.zip](http://ailab.aiwin.org.cn/my/datasets/download/125ee28f-f9f7-454f-a43d-3ff8d0d2033c)

2. ```shell
   # 配置环境
   \rm -rf __MACOSX/ 测试集/ 训练集/ dataset/
   unzip 2021A_T1_Task1_数据集含训练集和测试集.zip > out.log
   pip install Levenshtein
   ```

3. ```shell
   # 构造数据集
   mkdir -vp dataset/images
   cp 训练集/date/images/*.jpg dataset/images
   cp 训练集/amount/images/*.jpg dataset/images
   python data_creator.py
   ```

4. ```shell
   # (可选)数据集离线增强
   python expand_datasets.py
   ```

5. ```shell
   # 训练
   python do_train.py
   ```

6. ```shell
   # 评估
   python do_evaluate.py
   ```

   

