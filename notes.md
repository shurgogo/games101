主讲老师: 闫令琪，UCSB
课程主页: https://sites.cs.ucsb.edu/~lingqi/teaching/games101.html
bilibili: https://www.bilibili.com/video/BV1X7411F744/?spm_id_from=333.337.search-card.all.click&vd_source=7ad9867f192de3567ed09c0a484aeb78
作业发布: http://games-cn.org/forums/topic/allhw/

## 变换矩阵

### 平移(translation)、旋转(rotation)、剪切(shearing)

- 平移是非线性的，为了保持同其他变换的一致性，引入齐次坐标(Homogenous Coordinates)


### 旋转矩阵
三维旋转注意绕 y 轴时的方向(正负性)

1. 绕 X 轴旋转 (Roll)

绕 X 轴旋转角度 \( \theta \) 的矩阵为：

$$
R_x(\theta) = \begin{bmatrix}
1 & 0 & 0 \\
0 & \cos \theta & -\sin \theta \\
0 & \sin \theta & \cos \theta
\end{bmatrix}
$$

2. 绕 Y 轴旋转 (Pitch)

绕 Y 轴旋转角度 \( \theta \) 的矩阵为：

$$
R_y(\theta) = \begin{bmatrix}
 \cos \theta & 0 & \sin \theta \\
           0 & 1 &           0 \\
-\sin \theta & 0 & \cos \theta
\end{bmatrix}
$$

3. 绕 Z 轴旋转 (Yaw)

绕 Z 轴旋转角度 \( \theta \) 的矩阵为：

$$
R_z(\theta) = 
\begin{bmatrix}
    \cos \theta & -\sin \theta & 0 \\
    \sin \theta &  \cos \theta & 0 \\
              0 &            0 & 1
\end{bmatrix}
$$

### 旋转矩阵具有正交性(重要性质)

### 罗德里克旋转公式(Rodrigues' rotation formula)
计算三维空间中，一个向量绕旋转轴旋转给定角度以后得到的新向量的计算公式

### 映射矩阵

$$
\text{projection} = 
\begin{bmatrix}
\frac{width}{2} &                0 & 0 &  \frac{width}{2} \\
              0 & \frac{height}{2} & 0 & \frac{height}{2} \\
              0 &                0 & 1 &                0 \\
              0 &                0 & 0 &                1
\end{bmatrix}
$$