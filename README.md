# Contrastive-Learning
#### **Blog**

* Contrastive Self-Supervised Learning
  [Local link] (./blog-contrastive self-supervised learning.pdf)
  [Internet link] <https://ankeshanand.com/blog/2020/01/26/contrative-self-supervised-learning.html>

* 对比学习（Contrastive Learning）相关进展梳理

  [Internet link] <https://zhuanlan.zhihu.com/p/141141365>

* 对比学习（Contrastive Learning）:研究进展精要

  [Internet link] <https://zhuanlan.zhihu.com/p/367290573>

* 论文阅读｜浅谈图上的自监督学习——对比学习

  [Internet link] <https://zhuanlan.zhihu.com/p/187247235>

* 深度学习中的互信息

  [Internet link] <[深度学习中的互信息：无监督提取特征 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/46524857)>




#### Note

##### Introduction

```
Contrastive self-supervised learning techniques are a promising class of methods that build representations by learning to encode what makes two things similar or different.
```

其核心思想是学会编码相似事物的不同之处。

* Example

  ![image-20210510101712186](C:\1MyDataDisk\B+research\Contrastive learning\image-20210510101712186.png)

左边是根据记忆画出来的美元，右边是照着实物画出来的，尽管我们看过很多次，依然无法完全一模一样画出来，但是我们可以有足够的特征将其与其它物体区分开。那么我们是否可以不根据元素级别的细节，只通过编码高层次特征来区分不同事物？

* Genrative vs contrastive method

![image-20210510102727001](C:\1MyDataDisk\B+research\Contrastive learning\image-20210510102727001.png)

* How do contrastive methods 

  ![image-20210510154718858](C:\1MyDataDisk\B+research\Contrastive learning\image-20210510154718858.png)

  ​	**InfoNCE loss**

![image-20210510220456327](C:\1MyDataDisk\B+research\Contrastive learning\image-20210510220456327.png)

![image-20210510220600644](C:\1MyDataDisk\B+research\Contrastive learning\image-20210510220600644.png)


##### **Contrastive predictive coding (CPC)**

  * **Problem**: Improving representation learning requires features that are less specialized towards solving a single supervised task.

  * **Intuition**: learn the representations that encode the underlying shared information between different parts of the (high-dimensional) signal.

  * **Method**: CPC learns representations by encoding information that’s shared across data points multiple time steps apart, discarding local information. These features are o􀁸en called “slow features”: features that don’t change too quickly across time. Examples include identity of a speaker in an audio signal, an activity carried out in a video, an object in an image etc.

    <img src="C:/1MyDataDisk/B+research/Contrastive%20learning/Contrastive%20Learning/image-20210511155512953.png" alt="image-20210511155512953" style="zoom:100%;" />

    ![image-20210511155121637](C:/1MyDataDisk/B+research/Contrastive%20learning/Contrastive%20Learning/image-20210511155121637.png)


##### **SimCLR (Hinton)**

  * ![image-20210511200047517](C:/1MyDataDisk/B+research/Contrastive%20learning/Contrastive%20Learning/image-20210511200047517-1620734459090.png)
  * ![image-20210511200226975](C:/1MyDataDisk/B+research/Contrastive%20learning/Contrastive%20Learning/image-20210511200226975.png)
  * ![image-20210511213336667](C:/1MyDataDisk/B+research/Contrastive%20learning/Contrastive%20Learning/image-20210511213336667.png)
  * ![image-20210511214806211](C:/1MyDataDisk/B+research/Contrastive%20learning/Contrastive%20Learning/image-20210511214806211.png)



##### Deep InfoMax (Bengio)

* ![image-20210511211449820](C:/1MyDataDisk/B+research/Contrastive%20learning/Contrastive%20Learning/image-20210511211449820.png)

  

* The contrastive task behind DIM is to classify whether a pair of global features and local features are from the same image or not.

  * global features are the final output of a convolutional encoder (a flat vector, Y)
  * local features are the output of an intermediate layer in the encoder (an M x M feature map)

* ![image-20210511211806348](C:/1MyDataDisk/B+research/Contrastive%20learning/Contrastive%20Learning/image-20210511211806348.png)



##### Deep graph infomax

* ![image-20210511222921989](C:/1MyDataDisk/B+research/Contrastive%20learning/Contrastive%20Learning/image-20210511222921989.png)
* ![image-20210511222954195](C:/1MyDataDisk/B+research/Contrastive%20learning/Contrastive%20Learning/image-20210511222954195.png)
* ![image-20210511223015935](C:/1MyDataDisk/B+research/Contrastive%20learning/Contrastive%20Learning/image-20210511223015935.png)

