[English](README.md)
### 知乎验证码
使用TensorFlow破解知乎验证码


### 基础知识
1. Python3
2. PIL库和numpy库
3. TensorFlow
4. CNN(卷积神经网络)


### 如何运行
1. 标记足够多的验证码放到[captcha_base64.txt](captcha_base64.txt)文件中（图片为base64编码的字符串）
2. 运行[model.py](model.py)脚本，`python3 model.py`
3. 在其他模块中导入[__init__.py](__init__.py)的`predict_captcha`函数，传入base64编码的图片字符串，得到预测值


### 训练过程
1. 使用Python3和TensorFlow构建一个卷积神经网络
2. 为了提高识别准确率，标记足够过的知乎[验证码](https://www.zhihu.com/captcha.gif)，并存储到本地
3. 使用PIL和numpy库将标记好的[验证码](https://www.zhihu.com/captcha.gif)转化成图片和标签数组
4. 把图片和标签数据feed到卷积神经网络中，不断的训练，直到达到满意的准确率
5. 保存训练好的网络模型
6. 恢复网络模型，拉取知乎线上[验证码](https://www.zhihu.com/captcha.gif)转换成图片数组feed到神经网络中进行预测
7. Boom!:boom:


### CNN
使用TensorFlow构建一个简单的卷积神经网络，该网络包含一个输入层、三个卷积层+池化层和最后一个全连接层。
TensorBoard显示整个网络结构如下图所示：  
![CNN网络结构](screenshot/graph.png)  
购买打码服务标记足够多的验证码，不断输入到CNN网络中进行训练，我跑了一个晚上准确率达到了95%左右，走势图如下：  
![准确率](screenshot/accuracy.png)  
loss曲线如下：  
![loss](screenshot/loss.png)

***
关注微信公众号：**Python实验课**，后台回复 **"知乎验证码"** 免费分享一份10万张标记好的验证码文件用于训练  
![Python实验课](screenshot/qrcode_small.jpg)
