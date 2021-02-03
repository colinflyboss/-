# **TensorFlow概念：**

**Tensorflow已被广泛应用于文本处理，语音识别和图像识别等多项机器学习和深度学习领域。****用于机器学习和深度神经网络方面的研究****

**tensor张量：一个多维数组***（**multidimensional array**）

**Tensor的目的是能够创造更高维度的矩阵、向量**

**Tensor**

**张量，是tensorflow中最主要的数据结构，张量用于在计算图中进行数据传递，创建了张量后，需要将其赋值给一个变量或占位符，之后才会将该张量添加到计算图中。**

**session**

**会话，是Tensorflow中计算图的具体执行者，与图进行实际的交互。一个会话中可以有多个图，会话的主要目的是将训练数据添加到图中进行计算，也可以修改图的结构。**



## 涉及概念：

- **IPC（Inter-process communication）：实现单机中运行的进程之间的相互通信**
- **RPC（远程过程调用）：实现单机上的进程可以相互通信，多机器中的进程也可以相互通信**了
- **RPC框架：可以让程序员来调用远程进程上的代码一套工具**
-  **RDMA(Remote Direct Memory Access)技术全称远程直接内存访问，就是为了解决网络传输中服务器端数据处理的延迟而产生的。**
- **Remote：数据通过网络与远程机器间进行数据传输。**
- **Direct：没有内核的参与，有关发送传输的所有内容都卸载到网卡上。**
- **Memory：在用户空间虚拟内存与RNIC网卡直接进行数据传输不涉及到系统内核，没有额外的数据移动和复制。**
- **Access：send、receive、read、write、atomic操作。**
- **迭代是重复反馈过程的活动，其目的通常是为了逼近所需目标或结果。每一次对过程的重复称为一次“迭代”，而每一次迭代得到的结果会作为下一次迭代的初始值。**

# Numpy

**Numpy(numerical python)：主要用于对多维数组执行计算**。

## 主要用于

- **机器学习模型：在编写机器学习算法时，需要对矩阵进行各种数值计算。例如矩阵乘法、换位、加法等。NumPy提供了一个非常好的库，用于简单(在编写代码方面)和快速(在速度方面)计算。NumPy数组用于存储训练数据和机器学习模型的参数。**
- **图像处理和计算机图形学：计算机中的图像表示为多维数字数组。NumPy成为同样情况下最自然的选择。实际上，NumPy提供了一些优秀的库函数来快速处理图像。例如，镜像图像、按特定角度旋转图像等。**
- **数学任务：NumPy对于执行各种数学任务非常有用，如数值积分、微分、内插、外推等。因此，当涉及到数学任务时，它形成了一种基于Python的MATLAB的快速替代。**

# 数学

## **矩阵**

## **是一个按照长方阵列排列的[复数](https://baike.baidu.com/item/复数/254365)或[实数](https://baike.baidu.com/item/实数/296419)集合**

**用E或I来表示单位矩阵**1        0          0

​                                     0      1          0

​                                     0        0          1

**An*n**

**An表示方矩阵n行n列**

**同型矩阵**

**负矩阵**

**如果矩阵里的数都是同一个数，则该矩阵等于该数**

**方阵只有主副对角线**

## 矩阵运算

加法：![image-20210203160542205](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203160542205.png)

同型矩阵才可以加减

减法：

![image-20210203160638992](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203160638992.png)

![image-20210203160804543](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203160804543.png)

**数乘：**

![image-20210203160909758](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203160909758.png)

矩阵所有元素均有公因子，公因子朝外提一次，一次挺完

行列式提公因子：一行提一次，所有元素具有，提n次

**乘法:**

![image-20210203161429094](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203161429094.png)

第一行乘以第一列，每个数对应相乘，再相加，第一行乘完三列，得出新矩阵的第一行



![image-20210203161741147](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203161741147.png)

这种不能相乘

矩阵相乘前提：第一个矩阵的列数，等于第二个矩阵的行数

结果矩阵的形状：结果矩阵的行数=第一个矩阵的行数

​                             结果列数=第二个的列数

七字诀：中间相等，取两边

![image-20210203162510624](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203162510624.png)

![image-20210203162706192](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203162706192.png)

矩阵A*B不等于B*A

![image-20210203162838262](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203162838262.png)

![image-20210203163107464](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203163107464.png)

![image-20210203163227077](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203163227077.png)

矩阵乘法不满足的规律![image-20210203163339142](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203163339142.png)



![image-20210203165316800](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203165316800.png)

**位置**

![image-20210203165548568](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203165548568.png)

![image-20210203165835082](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203165835082.png)

## 矩阵的幂运算

![image-20210203170712345](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203170712345.png)

![image-20210203171227930](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203171227930.png)

![image-20210203172007912](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203172007912.png)

## 矩阵转置

![image-20210203173426825](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203173426825.png)

## 方阵的行列式

![image-20210203174918224](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203174918224.png)

![image-20210203180305409](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203180305409.png)

## 伴随矩阵

**只有方阵才有伴随矩阵**



## 逆矩阵

**一定是方阵**

**逆矩阵唯一**

**未必可逆**

![image-20210203181944464](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210203181944464.png)



## **行列式：坐标系中，图形的缩放比例**

**行数等于列数**



