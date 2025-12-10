# 系统辨识
<img src="note_sys.assets/image-20251015150903678.png" alt="image-20251015150903678" style="zoom:50%;" /><img src="note_sys.assets/image-20251015150843040.png" alt="image-20251015150843040" style="zoom:50%;" />

## 系统辨识——经典辨识

### 相关分析法

> 重要假设：信号是平稳的或周期的；因此，在实验二中，我们从第二个周期开始计算互相关函数，目的是避免受暂态响应的干扰。暂态响应并非由输入信号决定，和系统本身的结构有关。

1. 维纳-霍夫方程

   * $R_{xy}(\tau)=\int^{\infty}_0g(\sigma)R_x(\tau-\sigma)d\sigma$

   * **自相关/互相关函数的计算式：**
     $R_x(\tau)=\int^{\infty}_{-\infty}x(t)x(t+\tau)dt$
     $R_{xy}(\tau)=\int^{\infty}_{-\infty}x(t)y(t+\tau)dt$

     > 并非唯一定义，此为能量信号；后续功率信号/周期信号，有另外的定义，即改为取均值，否则积分不收敛

   * 推导过程：
     <img src="note_sys.assets/image-20250929220029118.png" alt="image-20250929220029118" style="zoom: 67%;" />
     <img src="note_sys.assets/image-20250929220042240.png" alt="image-20250929220042240" style="zoom:67%;" />
     
     > $\tau=t_2-t_1$，稍加整理就成了前面提到的式子
     
   * 在实际应用中，我们常常无法直接测量系统脉冲响应，但可以测量输入和输出，计算$R_x$和$R_{xy}$，利用该方程反解出系统的特性$g(\sigma)$

2. 由维纳霍夫方程求解$g(\tau)$和白噪声

   * 白噪声

     * 概念
       <img src="note_sys.assets/image-20250929221307304.png" alt="image-20250929221307304" style="zoom: 67%;" />
     * 当$x(t)$为白噪声信号时，$R_x(\tau)=K\delta(\tau)$

   * 代入方程，求得
     $g(\tau)=R_{xy}(\tau)/K$

     <img src="note_sys.assets/image-20250929221136452.png" alt="image-20250929221136452" style="zoom:67%;" />

   * 采用白噪声为输入时的辨识结构图
     <img src="note_sys.assets/image-20250929222042339.png" alt="image-20250929222042339" style="zoom:67%;" />

     > 图中结果忽略了时间$T$，但不影响其比例关系

   * 白噪声工程问题

     * 白噪声在工程上人为不可产生
     * 实际工程上，常用M序列来代替白噪声输入信号。

3. M序列——最长线性移位寄存器序列，近似白噪声

   * 定义
     <img src="note_sys.assets/image-20250929222439411.png" alt="image-20250929222439411" style="zoom:67%;" />
     周期为T

   * M序列的产生

     本质上，初始是除了全零之外的状态，然后往前移位，取某些寄存器的值进行异或运算后当作开头的input，最后一个寄存器的移出值为输出。
     <img src="note_sys.assets/image-20250929222457789.png" alt="image-20250929222457789" style="zoom:67%;" />
     <img src="note_sys.assets/image-20250929222510080.png" alt="image-20250929222510080" style="zoom:67%;" /><img src="note_sys.assets/image-20250929222534478.png" alt="image-20250929222534478" style="zoom:67%;" />

   * M序列的自相关函数
     <img src="note_sys.assets/image-20250929223052095.png" alt="image-20250929223052095" style="zoom: 67%;" />
     <img src="note_sys.assets/image-20250930205110020.png" alt="image-20250930205110020" style="zoom:67%;" />
     
     > 上图为M序列连续形式下的自相关函数的图像。呈周期的锯齿状，尖峰为位移$\tau=0$。
     
     > 其中，离散形式尤为重要。上面的将M序列视作连续函数的自相关函数。
     
   * M序列辨识线性系统的脉冲响应
   
     * ==输入伪随机信号$x(t)$下，自相关函数和互相关函数计算==
   
       * $R_{xy}(\tau)=\frac1T\int^T_0x(t)y(t+\tau)dt$
       * $R_x(\tau)=\frac1T\int^T_0x(t)x(t+\tau)dt$
       * 推导：依靠关键性质$x(t)=x(t+T)$
   
     * **离散形式的维纳-霍夫方程**
       $R_{xy}(\tau)=R_{xy}(u\Delta)=\sum^{N_p-1}_{k=0}\Delta g(k\Delta)R_x(u\Delta-k\Delta)$
   
       > $\Delta:$时间离散化精度
       > <img src="note_sys.assets/image-20250930210034099.png" alt="image-20250930210034099" style="zoom: 67%;" />
   
     * 矩阵形式的维纳-霍夫方程
       <img src="note_sys.assets/image-20250930210145128.png" alt="image-20250930210145128" style="zoom:67%;" />
   
     * 求解g
       <img src="note_sys.assets/image-20250930210247453.png" alt="image-20250930210247453" style="zoom:67%;" />
   
       <img src="note_sys.assets/image-20250930210310793.png" alt="image-20250930210310793" style="zoom: 67%;" />
   
     * 总结：相关分析法：
       ![image-20250930210502854](note_sys.assets/image-20250930210502854.png)
   
### 用脉冲响应求传递函数

* 总结流程：
       <img src="note_sys.assets/image-20250930212113686.png" alt="image-20250930212113686" style="zoom:67%;" />
* 数学推导过程
       <img src="note_sys.assets/image-20250930212132327.png" alt="image-20250930212132327" style="zoom:67%;" />
       <img src="note_sys.assets/image-20250930212144139.png" alt="image-20250930212144139" style="zoom:67%;" />
       <img src="note_sys.assets/image-20250930212158267.png" alt="image-20250930212158267" style="zoom:67%;" />
       <img src="note_sys.assets/image-20250930212207037.png" alt="image-20250930212207037" style="zoom:67%;" />

* 离散系统的脉冲传递函数
  <img src="note_sys.assets/image-20251014090022220.png" alt="image-20251014090022220" style="zoom:50%;" />
  <img src="note_sys.assets/image-20251014090036596.png" alt="image-20251014090036596" style="zoom:50%;" />
  <img src="note_sys.assets/image-20251014090054683.png" alt="image-20251014090054683" style="zoom:50%;" />

### 随机过程

1. 基本概念

   * 随机过程概念与数字特征
     <img src="note_sys.assets/image-20251013104944921.png" alt="image-20251013104944921" style="zoom:50%;" />
     <img src="note_sys.assets/image-20251013104956775.png" alt="image-20251013104956775" style="zoom: 50%;" />

     * 数字特征
       <img src="note_sys.assets/image-20251013105055147.png" alt="image-20251013105055147" style="zoom:67%;" />

   * 平稳随机过程

     > 非平稳随机一般不论

     * **平稳随机过程：一个随机过程的统计性质不随时间改变**，如方差、均值等
       <img src="note_sys.assets/image-20251013105359214.png" alt="image-20251013105359214" style="zoom:50%;" />
     * 各态遍历性
       * 含义：一个样本能充分地代表整个随机过程的特征，可以以一次时间平均值代替集合平均值。
         <img src="note_sys.assets/image-20251013110457740.png" alt="image-20251013110457740" style="zoom:50%;" />
         * **集合平均**是在**某一个固定的时间点**（例如 t1），对所有这些不同的样本函数取平均值。它描述的是整个过程在某个瞬间的统计特性，例如均值 μx 和自相关函数 Rx(τ)。
         * **时间平均**是**只针对某一条样本函数**（例如 x1(t)），在无限长的时间范围内（从 −T 到 T，然后让 T→∞）对其进行平均。
           <img src="note_sys.assets/image-20251013110518182.png" alt="image-20251013110518182" style="zoom:50%;" />
       * 与平稳随机过程的关系：必要不充分条件
       * <img src="note_sys.assets/image-20251013110721096.png" alt="image-20251013110721096" style="zoom:50%;" />

2. 白噪声

   * 白噪声过程是由一系列不相关的随机变量组成的一种理想化**平稳随机过程**。
     <img src="note_sys.assets/image-20251013110935680.png" alt="image-20251013110935680" style="zoom:50%;" />

   * 功率谱密度函数
     <img src="note_sys.assets/image-20251013111003874.png" alt="image-20251013111003874" style="zoom: 50%;" />

   * 为什么叫“白噪声”——类比白色光

     **白噪声功率谱密度函数为常数！**
     <img src="note_sys.assets/image-20251013111123332.png" alt="image-20251013111123332" style="zoom:50%;" />

   * 白噪声序列
     <img src="note_sys.assets/image-20251013112144716.png" alt="image-20251013112144716" style="zoom:67%;" />

   * 白噪声序列产生方法
     <img src="note_sys.assets/image-20251013112215484.png" alt="image-20251013112215484" style="zoom: 50%;" />

     > 白噪声不只有一种，比如高斯白噪声（正态分布）和均匀白噪声（均匀分布）。
     > <img src="note_sys.assets/image-20251013121343602.png" alt="image-20251013121343602" style="zoom:50%;" />
     >
     > **一个独立同分布的随机数序列，就是离散时间域上的白噪声。**
     > <img src="note_sys.assets/image-20251013121314392.png" alt="image-20251013121314392" style="zoom:50%;" />

     * 伪随机数产生方法（计算机）：
       <img src="note_sys.assets/image-20251013112228019.png" alt="image-20251013112228019" style="zoom: 50%;" />
       <img src="note_sys.assets/image-20251013112239461.png" alt="image-20251013112239461" style="zoom:50%;" />

     * 使用均匀分布的伪随机数产生任意分布的随机数

       <img src="note_sys.assets/image-20251013115224449.png" alt="image-20251013115224449" style="zoom: 50%;" />

       * 正态分布随机数产生：**伪随机数+中心极限定理**
         <img src="note_sys.assets/image-20251013115246900.png" alt="image-20251013115246900" style="zoom:50%;" /><img src="note_sys.assets/image-20251013115259663.png" alt="image-20251013115259663" style="zoom:50%;" />

### 阶跃响应法

> 前面已经讲过脉冲响应法，但在实际情况中是无法生成一个冲激信号的，因此，方有阶跃响应法

1. 阶跃响应法——非参数模型辨识方法

   * 第一步：测取过程的阶跃响应
   * 第二步：由阶跃响应求过程的传递函数
     * 常用方法：
       * 近似法、切线法、两点法、面积法、半对数法等
       * 当阶跃曲线比较规则时，用近似法、半对数法、切线法和两点法都能比较有效的求得传递函数

2. 第一步：阶跃响应的曲线的实验测定

   * 目标为阶跃响应曲线：当对象的输入量做阶跃变化时，其输出量是随时间而变化的曲线，则称为**阶跃响应曲线**。

   * 注意事项
     <img src="note_sys.assets/image-20251015205246439.png" alt="image-20251015205246439" style="zoom:50%;" />

   * 矩形脉冲响应**复原至阶跃响应**
     <img src="note_sys.assets/image-20251015205406453.png" alt="image-20251015205406453" style="zoom: 25%;" />

     * 数学原理
       <img src="note_sys.assets/image-20251015205443094.png" alt="image-20251015205443094" style="zoom:50%;" />
       ==将脉冲响应视为阶跃信号的叠加！==

     * 图解

       观察二式，可以由矩形脉冲响应和差分的阶跃响应叠加而得。比如2a点为矩形脉冲响应的y值叠加a点时阶跃响应的y值。以此递推，直到复原曲线。
       <img src="note_sys.assets/image-20251015205523529.png" alt="image-20251015205523529" style="zoom:50%;" />

3. 第二步：由阶跃响应求过程的传递函数

   * 近似法

     以一阶系统为例
     <img src="note_sys.assets/image-20251015205841091.png" alt="image-20251015205841091" style="zoom:50%;" />

     * 确定时间常数T：$y(t)=0.63y(\infty)$对应的t值
       <img src="note_sys.assets/image-20251015205944608.png" alt="image-20251015205944608" style="zoom:50%;" />
     * 确定放大系数K：$K=\frac{y(\infty)}{x_0}$

   * 切线法

     * 确定时间常数T
       <img src="note_sys.assets/image-20251015210101187.png" alt="image-20251015210101187" style="zoom:50%;" />
     * 数学原理
       <img src="note_sys.assets/image-20251015210116694.png" alt="image-20251015210116694" style="zoom:50%;" />
     * 一阶关系加纯滞后环节的阶跃响应曲线的T的确定
       <img src="note_sys.assets/image-20251015210211048.png" alt="image-20251015210211048" style="zoom:50%;" />

   * 两点法
   
     * 概述
       <img src="note_sys.assets/image-20251020105029945.png" alt="image-20251020105029945" style="zoom:50%;" />
     * 实际应用时，常取特定点
       <img src="note_sys.assets/image-20251020105103691.png" alt="image-20251020105103691" style="zoom:50%;" />
     * 数学原理
       <img src="note_sys.assets/image-20251020105135736.png" alt="image-20251020105135736" style="zoom:50%;" />
   
   * 面积法
   
     > 复杂，不重要，了解核心思想即可
     
     数学过程：
     <img src="note_sys.assets/image-20251020145854842.png" alt="image-20251020145854842" style="zoom:50%;" />
     
     编程思想：
     <img src="note_sys.assets/image-20251020145927743.png" alt="image-20251020145927743" style="zoom:50%;" />

## 系统辨识—近代辨识法

### 最小二乘法

> 在模型阶次n已知的情况下，根据系统的输入输出数据，估计出系统差分方程的各项系数。

1. 场景建模

   * 任意SISO系统的基本描述
     <img src="note_sys.assets/image-20251021192539521.png" alt="image-20251021192539521" style="zoom:50%;" />
   * 经过整理，则有
     <img src="note_sys.assets/image-20251021192620321.png" alt="image-20251021192620321" style="zoom:50%;" />
     注意，$\xi(k)=v(k)+\sum^n_{i=1}a_iv(k-i)$，是当前和过去噪声的线性组合。
   * 写为向量形式
     <img src="note_sys.assets/image-20251021192635319.png" alt="image-20251021192635319" style="zoom:50%;" />
   * 实际情景：存在噪声、数据长度大于未知数数量——无法求出准确的$\theta$
     <img src="note_sys.assets/image-20251021192711832.png" alt="image-20251021192711832" style="zoom:50%;" />

2. LS最小二乘法推导及应用条件

   * 场景
     <img src="note_sys.assets/image-20251021193005793.png" alt="image-20251021193005793" style="zoom:50%;" />

   * 原理推导——基本的最小二乘法（LS）

     * 辨识准则：残差平方和最小

       <img src="note_sys.assets/image-20251021193212861.png" alt="image-20251021193212861" style="zoom:50%;" />

     * 对J求偏导，得到最小二乘法的参数估计
       <img src="note_sys.assets/image-20251021193443546.png" alt="image-20251021193443546" style="zoom:50%;" />

     * 确保上述偏导结果为极小值，要求二阶导数，引出对于输入信号的要求
       <img src="note_sys.assets/image-20251021193703112.png" alt="image-20251021193703112" style="zoom:50%;" />
       <img src="note_sys.assets/image-20251022163016142.png" alt="image-20251022163016142" style="zoom:50%;" />
       <img src="note_sys.assets/image-20251022163023259.png" alt="image-20251022163023259" style="zoom:50%;" />
       <img src="note_sys.assets/image-20251022163030666.png" alt="image-20251022163030666" style="zoom:50%;" />
       
     * 经过一系列推导，我们得到LS最小二乘法对输入信号要求为：**输入序列$u(k)$的n+1阶方阵$R_u$是正定的，即$u(k)$为n+1阶持续激励信号。**
     
       * $$ \mathbf{R}_u = \begin{bmatrix} R_u(0) & R_u(1) & \cdots & R_u(n) \\ R_u(1) & R_u(0) & \cdots & R_u(n-1) \\ \vdots & \vdots & \ddots & \vdots \\ R_u(n) & R_u(n-1) & \cdots & R_u(0) \end{bmatrix} $$
     
       * 若 $\mathbf{R}_u$ 为强对角占优矩阵，则 $\mathbf{R}_u$ 正定。
     
         > 强对角占优矩阵：对角线上元素远大于其他
     
     * 常见的持续激励信号有
     
       * 白噪声序列
       * 伪随机二位式噪声序列
       * 有色噪声随机信号序列
   
3. 最小二乘估计的概率性质

   * **估计的无偏性**

     * 无偏性估计的定义：

       若 $E\{\hat{\theta}\} = E\{\theta\} = \theta$，则称 $\hat{\theta}$ 是参数 $\theta$ 的无偏估计。

     * 下面讨论**无偏估计的条件**
       $$
       \begin{cases}
       \mathbf{Y} = \mathbf{\Phi}\theta + \xi \\
       \hat{\theta} = (\mathbf{\Phi}^\mathrm{T}\mathbf{\Phi})^{-1}\mathbf{\Phi}^\mathrm{T}\mathbf{Y}
       \end{cases}
       \quad (3.3)
       $$

       $$
       E[\hat{\theta}] = E[(\mathbf{\Phi}^\mathrm{T}\mathbf{\Phi})^{-1}\mathbf{\Phi}^\mathrm{T}\mathbf{Y}] = E[(\mathbf{\Phi}^\mathrm{T}\mathbf{\Phi})^{-1}\mathbf{\Phi}^\mathrm{T}(\mathbf{\Phi}\theta + \xi)]
       $$

       $$
       \Rightarrow E[\hat{\theta}] = E[\theta + (\mathbf{\Phi}^\mathrm{T}\mathbf{\Phi})^{-1}\mathbf{\Phi}^\mathrm{T}\xi] = \theta + E[(\mathbf{\Phi}^\mathrm{T}\mathbf{\Phi})^{-1}\mathbf{\Phi}^\mathrm{T}\xi]
       $$

       LS无偏估计的充要条件为：
       $$
       E[(\mathbf{\Phi}^\mathrm{T}\mathbf{\Phi})^{-1}\mathbf{\Phi}^\mathrm{T}\xi] = 0
       $$
       <img src="note_sys.assets/image-20251022164013147.png" alt="image-20251022164013147" style="zoom:50%;" />
       因此LS无偏估计的充分条件为：
       =={$\xi(k)$}为零均值不相干的随机序列，且与{$u(k)$}无关==
   
   * 估计的一致性
   
     * 定义
       <img src="note_sys.assets/image-20251022164223672.png" alt="image-20251022164223672" style="zoom:50%;" />
   
     * 条件推导
       <img src="note_sys.assets/image-20251022164254974.png" alt="image-20251022164254974" style="zoom:50%;" />
       <img src="note_sys.assets/image-20251022164302611.png" alt="image-20251022164302611" style="zoom:50%;" />
   
       一致性估计的充分条件为：
       =={$\xi(k)$}为零均值不相干的随机序列，且与{$u(k)$}无关==
   
   * 估计的有效性
     <img src="note_sys.assets/image-20251022164337176.png" alt="image-20251022164337176" style="zoom:67%;" />
   
   * 估计的渐近正态性
     <img src="note_sys.assets/image-20251022164344706.png" alt="image-20251022164344706" style="zoom:67%;" />
   
4. LS最小二乘法存在的问题

   * 无偏性和一致性估计的充分条件均为：{$\xi(k)$}为零均值不相干的随机序列，且与{$u(k)$}无关
     这个条件无法满足！因此，LS最小二乘法是有偏估计，必须改进。
   * <img src="note_sys.assets/image-20251022165024487.png" alt="image-20251022165024487" style="zoom:67%;" />

5. 递推最小二乘法

   > <img src="note_sys.assets/image-20251022165140588.png" alt="image-20251022165140588" style="zoom:50%;" />

   * 数学推导

     <img src="note_sys.assets/image-20251022170630675.png" alt="image-20251022170630675" style="zoom:50%;" />
     <img src="note_sys.assets/image-20251022170638813.png" alt="image-20251022170638813" style="zoom:50%;" />
     <img src="note_sys.assets/image-20251022170648774.png" alt="image-20251022170648774" style="zoom:50%;" />
     <img src="note_sys.assets/image-20251022170656812.png" alt="image-20251022170656812" style="zoom:50%;" />
   
   * 递推最小二乘法在自适应控制的应用
      这块作为了解内容，核心内容在于框图，在PPT中，举了个例子，我们希望系统稳定，因此需要调节他闭环控制的状态反馈的参数，而这个参数又与系统固有未知系数a和b有关，因此，我们通过递推最小二乘法，估计出a和b的估计值，然后就可以计算出正确的反馈系数，实现目标。
      <img src="note_sys.assets/image-20251101204303712.png" alt="image-20251101204303712" style="zoom:67%;" />

### 极大似然辨识

1. 极大似然估计法

   > 既然样本已经发生了，认为该样本发生的概率应该是最大的。

   * 背景定义

     * 联合概率密度函数
       <img src="note_sys.assets/image-20251027104353159.png" alt="image-20251027104353159" style="zoom:50%;" />

     * 似然函数
       <img src="note_sys.assets/image-20251027104413422.png" alt="image-20251027104413422" style="zoom:50%;" />

       > L也可以从概率/概率密度函数组合而来。

   * 算法核心
     <img src="note_sys.assets/image-20251027104432462.png" alt="image-20251027104432462" style="zoom:67%;" />
     为了计算方便，取对数，有==对数似然函数==
     <img src="note_sys.assets/image-20251027104458314.png" alt="image-20251027104458314" style="zoom:50%;" />

   * 算法运算流程
     <img src="note_sys.assets/image-20251027110813608.png" alt="image-20251027110813608" style="zoom:50%;" />

   * **噪声为高斯白噪声时，辨识线性差分方程**

     简单来说，就是**对噪声/误差进行极大似然估计**。
   
     * 模型：
       <img src="note_sys.assets/image-20251027112813054.png" alt="image-20251027112813054" style="zoom: 33%;" />
       <img src="note_sys.assets/image-20251027112824407.png" alt="image-20251027112824407" style="zoom:50%;" />

     > $\theta$只与a、b有关，因为噪声是高斯白噪声，无记忆性。这是理想状况
   
     <img src="note_sys.assets/image-20251027112835734.png" alt="image-20251027112835734" style="zoom:50%;" />
   
     > 这里$e^2$写成了$(Y-\Phi\theta)^T(Y-\Phi\theta)$的形式，后者是线性的，可以通过求导直接得到极大值对于的估计值。
   
     <img src="note_sys.assets/image-20251027112846985.png" alt="image-20251027112846985" style="zoom:50%;" />
   
   * **噪声为有色噪声时：**
   
     * 模型：<img src="note_sys.assets/image-20251027220650217.png" alt="image-20251027220650217" style="zoom:50%;" />
   
     * 将有色噪声分为**过去的白噪声+当前白噪声**，其中当前白噪声即$\varepsilon(k)$就是前面一样的理想的高斯白噪声，不具有相关性。
   
       > 注意，这里只是拆分了有色噪声，有色噪声依然是具有相关性的。我们只是提取出理想的无噪声部分。
   
       <img src="note_sys.assets/image-20251027222326280.png" alt="image-20251027222326280" style="zoom:50%;" />
   
     * 在此方程式基础上，和上例相同，构造方程组
       <img src="note_sys.assets/image-20251027222359735.png" alt="image-20251027222359735" style="zoom:50%;" />
       注意，这里的$\theta$包含了a、b、c，$\Phi$也因此包含了u，y和$\varepsilon(k-i)$。在前面的噪声为高斯白噪声的情况下，$\Phi$和$\theta$无关，因为u、y和$\theta$没关系。但在此处，由于包含了$\varepsilon(k-i)$的关系，误差本身是不可知的，依赖于$\theta$的估计值来填充，因此才有$\Phi(\theta)$。
   
     * 这里，我们发现，$\varepsilon=Y-\Phi(\theta)\theta$变成了关于$\theta$的**非线性方程，无法按照一般的流程，求偏导然后直接通过代数运算直接求解。**
       因此，我们需要应用高斯-牛顿法，通过迭代逼近最优解。
   
       下面介绍的是高斯-牛顿法：
       <img src="note_sys.assets/image-20251027223858546.png" alt="image-20251027223858546" style="zoom:50%;" />
   
       最终得到上面地迭代式$x_{k+1}=x_k-[J(x)^TJ(x)]^{-1}\nabla f$
   
     * 按照原本流程，算出最大似然估计，得到噪声方差的估计值。
       <img src="note_sys.assets/image-20251027225441781.png" alt="image-20251027225441781" style="zoom:50%;" />
   
       > 这里的似然方程建立的原则，和前面一样，都是建立在一个高斯白噪声的基础上的。只是前面可以化简成线性方程直接求导，这里更复杂而已。
       >
       > 目标是求ln L对于$\theta$的导数，求出极大值点。因此这里需要求方差的偏导，代回去消除未知数。得到纯净的关于$\theta$的方程。
   
     * 将噪声方差的极大似然估计值，代回原式子$ln L$中，得到关键式子
       <img src="note_sys.assets/image-20251027225750448.png" alt="image-20251027225750448" style="zoom:50%;" />
   
     * 从上式我们知道，当$v^2(k)$取得最小时，相应的$\hat{\theta_{ML}}$则就是此时的极大似然估计值。
       而这个$\min V(\hat{\theta_{ML}})$就是前述的非线性函数，可以用前面提到的迭代法来求解
       
     * 迭代的初值选取，a和b用前面白噪声的最小二乘法求得，c随机选取，一般取0.
       <img src="note_sys.assets/image-20251027230019934.png" alt="image-20251027230019934" style="zoom:50%;" />
       
     * 计算目标函数的梯度，在计算J梯度这一块需要用迭代法，即先计算v（n+m）的梯度时，要顺序把前面n+1到n+m-1的梯度都算出来。
       <img src="note_sys.assets/image-20251101195326243.png" alt="image-20251101195326243" style="zoom: 67%;" /><img src="note_sys.assets/image-20251027230028158.png" alt="image-20251027230028158" style="zoom: 50%;" />
       
     * 再计算J的二阶偏导
       <img src="note_sys.assets/image-20251027230036597.png" alt="image-20251027230036597" style="zoom:50%;" />
       
       > 二阶导对$\theta^T$求偏导，一个m\*1的向量，对1\*m的行向量求偏导，最终得到的是m\*m的Hessian矩阵。
       
       Newton-Raphson法，前面可以看到，省略了二阶偏导的小数项，那么其本质和前面提到的牛顿-高斯法是一样的。将前面两项结合起来即可得到迭代式子。
       
       **整个迭代过程是批处理的过程，就是，同一批数据反复使用，反复迭代，并不需要边递推边获取新数据。**
       <img src="note_sys.assets/image-20251027230044694.png" alt="image-20251027230044694" style="zoom:50%;" />
     
   * 在线递推
   
     * 和前面的批处理递推不同，这个是每来一个新数据就递推一次，因此称为在线算法。
       <img src="note_sys.assets/image-20251101202514557.png" alt="image-20251101202514557" style="zoom:67%;" />

# 系统仿真

## 经典连续系统仿真建模方法学

### 连续系统离散化原理

1. 数值积分法

   * 数值积分法原理
     <img src="note_sys.assets/image-20251103105618322.png" alt="image-20251103105618322" style="zoom:50%;" />
     **$f(t,y)$是系统固有属性，是已知函数，只要知道t和y就能得到确切值。**

     采用迭代法求解$y_i$，关键在于求解积分$Q_k$
     <img src="note_sys.assets/image-20251103105629854.png" alt="image-20251103105629854" style="zoom:50%;" />

   * 欧拉法

     * 方法
       <img src="note_sys.assets/image-20251103105823606.png" alt="image-20251103105823606" style="zoom:50%;" />
       <img src="note_sys.assets/image-20251103105838535.png" alt="image-20251103105838535" style="zoom:50%;" />

     * 误差

       * 理论
         <img src="note_sys.assets/image-20251103105858485.png" alt="image-20251103105858485" style="zoom:50%;" />

         > $m=O(\frac1h),O(\frac1h)*O(h^2)=O(h)$

       * 分类

         * 截断误差：由算法精度引起的误差，通常步长越小，截断误差越小
         * 舍入误差：由计算机精度（有限位数）产生的误差，通常步长越小，计算次数越多，舍入误差越大

       * 误差权衡
         <img src="note_sys.assets/image-20251103110109566.png" alt="image-20251103110109566" style="zoom:50%;" />

     * 特点
       <img src="note_sys.assets/image-20251103110129923.png" alt="image-20251103110129923" style="zoom:50%;" />

   * 梯形法

     > 在欧拉法基础上，从矩形近似改为梯形近似

     * 原理

       由于$f(t_{k+1},y_{k+1})$是未知的，因此需要先用欧拉法预估，然后再用此数值进行矫正。
       <img src="note_sys.assets/image-20251103110414543.png" alt="image-20251103110414543" style="zoom:67%;" />

     * 特点
       <img src="note_sys.assets/image-20251103110552998.png" alt="image-20251103110552998" style="zoom:50%;" />

   * 二阶龙格-库塔法

     * 算法
       <img src="note_sys.assets/image-20251103113150497.png" alt="image-20251103113150497" style="zoom:50%;" />

     * 推导

       yk对t泰勒展开到二阶，假设出一个解。
       <img src="note_sys.assets/image-20251103113203164.png" alt="image-20251103113203164" style="zoom: 50%;" />

       将K2展开，然后重新代入解的形式里，和原本的泰勒展开式子做对比，得到等式。
       <img src="note_sys.assets/image-20251103113215091.png" alt="image-20251103113215091" style="zoom:50%;" />

       解出未知数
       <img src="note_sys.assets/image-20251103113226269.png" alt="image-20251103113226269" style="zoom:50%;" />

   * 四阶龙格-库塔法
     <img src="note_sys.assets/image-20251103114734176.png" alt="image-20251103114734176" style="zoom:50%;" />
     <img src="note_sys.assets/image-20251103114748578.png" alt="image-20251103114748578" style="zoom:50%;" />

   * 龙格库塔法（一般）
     <img src="note_sys.assets/image-20251103114819440.png" alt="image-20251103114819440" style="zoom:50%;" />
     <img src="note_sys.assets/image-20251103114831034.png" alt="image-20251103114831034" style="zoom:50%;" />

   * 数值积分法的讨论
     <img src="note_sys.assets/image-20251103114843404.png" alt="image-20251103114843404" style="zoom:50%;" />
     <img src="note_sys.assets/image-20251103115539338.png" alt="image-20251103115539338" style="zoom:50%;" />
     
   * 龙格—库塔法的误差估计与步长控制
     
     步长的选取关乎精度和计算效率。这里使用一个反馈控制来调节步长。
     
     至于为何要误差估计，首先，真实的误差是无法得知的，计算机无法解积分，这也是我们数值积分法存在的意义。那么，只能用高阶的估计，近似这个真实值，估计一个误差用于反馈控制。选取高一阶的方法的原因是让估计误差与真实误差同阶。
     <img src="note_sys.assets/image-20251103150742352.png" alt="image-20251103150742352" style="zoom:50%;" />
     
     **龙格—库塔法的误差估计**
     方法：找另一个低阶的龙格—库塔法，两个公式计算结果之差作为估计的误差。
     
     * RKM4法
       <img src="note_sys.assets/image-20251105203313159.png" alt="image-20251105203313159" style="zoom:50%;" />
       <img src="note_sys.assets/image-20251105203320561.png" alt="image-20251105203320561" style="zoom:50%;" />
     
       > 级数不一定小于阶数，本质上，阶数的作用是提供相应数量的基于泰勒展开系数的等式，如果无法满足级数的未知数要求，那么通常会自设条件求解，因此级数是可以大于阶数。
     
     * RKFI—2法
       <img src="note_sys.assets/image-20251105203357028.png" alt="image-20251105203357028" style="zoom:50%;" />
       <img src="note_sys.assets/image-20251105203405266.png" alt="image-20251105203405266" style="zoom:50%;" />
     
     * 其他方法
       <img src="note_sys.assets/image-20251105203416306.png" alt="image-20251105203416306" style="zoom:50%;" />
     
     **步长控制**
     <img src="note_sys.assets/image-20251105203433096.png" alt="image-20251105203433096" style="zoom:50%;" />
     
     > 局部误差$e_k$的公式含义为归一化，变为“当前步和前步的相对局部误差”，+1则是为了避免yk太小，数值不稳定。
   
2. 线性多步法

   > 龙格-库塔法在计算时要反复调用函数f，而且计算结果复用效率低，因此计算量较大。线性多步法就是将过去的信息利用起来。
   >
   > 多步：用了前r步的信息，而不仅是前一步。
   >
   > <img src="note_sys.assets/image-20251105210227174.png" alt="image-20251105210227174" style="zoom: 50%;" />
   > 核心：等式右端是否存在待求解的未知数。

   * 数学推导

     目的：用一个m阶的多项式去近似真实函数。同时，为了让计算最简化，用了$\tau=\frac{t_{n+k}-t}{h}$而不是普通的t，使得代入目标点t后，得到的是$jh$.
     <img src="note_sys.assets/image-20251105210346916.png" alt="image-20251105210346916" style="zoom: 67%;" />

     ==核心式子==
     <img src="note_sys.assets/image-20251105210356437.png" alt="image-20251105210356437" style="zoom: 67%;" />

     * 预报公式：显示公式，计算$y_{n+k}$

       方程是将已知的2k个条件，带入到多项式的通用表达式中得到的。
       观察式子，总共有m+1个未知数，方程数量有2k个，为了让未知数有唯一解，令m=2k-1。

       ==更一般地，m=条件数-1。应用时给的条件并不一定是对称的，但不影响整个推理过程==
       <img src="note_sys.assets/image-20251105210409595.png" alt="image-20251105210409595" style="zoom:67%;" />

       写出矩阵形式

       * 方法一：直接解出所有d，但是因为只有d0是有效的，所以计算效率低
         <img src="note_sys.assets/image-20251105210423981.png" alt="image-20251105210423981" style="zoom:67%;" />
       * 方法二：引入辅助向量$\phi^p$
         <img src="note_sys.assets/image-20251105210436190.png" alt="image-20251105210436190" style="zoom: 67%;" />

     * 矫正公式：隐式公式，计算$\dot{y}_{n+k}$

       <img src="note_sys.assets/image-20251105215236676.png" alt="image-20251105215236676" style="zoom:67%;" />

       > m应该取2k，PPT似乎有误，因为这里有2k+1个方程。

       <img src="note_sys.assets/image-20251105215243029.png" alt="image-20251105215243029" style="zoom:67%;" />
       <img src="note_sys.assets/image-20251105215251431.png" alt="image-20251105215251431" style="zoom:50%;" />

     * 统一表达式
       <img src="note_sys.assets/image-20251105215350940.png" alt="image-20251105215350940" style="zoom:67%;" />

   * 例子
     <img src="note_sys.assets/image-20251105221807884.png" alt="image-20251105221807884" style="zoom: 67%;" />
     <img src="note_sys.assets/image-20251105221819640.png" alt="image-20251105221819640" style="zoom:67%;" />
     <img src="note_sys.assets/image-20251105221840835.png" alt="image-20251105221840835" style="zoom:67%;" />

3. 总结
   <img src="note_sys.assets/image-20251105222133376.png" alt="image-20251105222133376" style="zoom:67%;" />
   

## 一级倒立摆控制

1. 系统建模

   * 物理定律
     <img src="note_sys.assets/image-20251110113037171.png" alt="image-20251110113037171" style="zoom:50%;" />
   * 数学近似与整理
     <img src="note_sys.assets/image-20251110113059418.png" alt="image-20251110113059418" style="zoom:50%;" />
   * 化为状态空间模型
     <img src="note_sys.assets/image-20251110113116057.png" alt="image-20251110113116057" style="zoom:50%;" />
     <img src="note_sys.assets/image-20251110113128483.png" alt="image-20251110113128483" style="zoom:50%;" />
   * 设定参数数值并列出具体的传递函数
     <img src="note_sys.assets/image-20251110113201130.png" alt="image-20251110113201130" style="zoom:50%;" />
     <img src="note_sys.assets/image-20251110113212057.png" alt="image-20251110113212057" style="zoom:50%;" />

2. LQR控制器理论

   * 控制目的
     <img src="note_sys.assets/image-20251110113928592.png" alt="image-20251110113928592" style="zoom:50%;" />

   * 概述
     <img src="note_sys.assets/image-20251110114513540.png" alt="image-20251110114513540" style="zoom:50%;" />
     <img src="note_sys.assets/image-20251110114522680.png" alt="image-20251110114522680" style="zoom:50%;" />

   * LQR理论的特点
     <img src="note_sys.assets/image-20251110114538496.png" alt="image-20251110114538496" style="zoom:50%;" />

   * LQR控制a定义
     <img src="note_sys.assets/image-20251110115322594.png" alt="image-20251110115322594" style="zoom:50%;" />
     <img src="note_sys.assets/image-20251110115335052.png" alt="image-20251110115335052" style="zoom:50%;" />

     > $x^TQx$为对状态的惩罚，Q越大，系统越倾向于快速减小误差；$u^TRu$：对控制量的惩罚，R越大，系统越倾向于使用更小的控制力。

     <img src="note_sys.assets/image-20251110115847052.png" alt="image-20251110115847052" style="zoom:50%;" />
     <img src="note_sys.assets/image-20251110115939175.png" alt="image-20251110115939175" style="zoom:50%;" />

3. 

