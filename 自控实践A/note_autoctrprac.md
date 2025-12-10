## LEC1 绪论

1. 控制系统功能框图
   <img src="note_autoctrprac.assets/image-20250905100312177.png" alt="image-20250905100312177" style="zoom:67%;" />
2. 控制五要素：主体、客体、目标、条件、手段

## LEC2 磁路与电气常识

### 磁场基本理论

1. 磁场基本物理量

   * 磁力线

     右手定律
     <img src="note_autoctrprac.assets/image-20250905101841678.png" alt="image-20250905101841678" style="zoom:50%;" />

   * 磁感应强度B（磁密）
     通过某单位面积的磁力线的条数。方向：磁场方向。

   * 磁通$\Phi$
     $\Phi = \int_A B \cos\theta \, dA$

   * 磁路

     * 电磁元件中，磁通所经过的闭合回路称为磁路。
       通过电磁元件工作磁路路径的磁通称为**主磁通**，除此之外，还有少量的磁通不在此路径通过，称为**漏磁通**。
     * 常见的铁心磁路
       <img src="note_autoctrprac.assets/image-20250905103138451.png" alt="image-20250905103138451" style="zoom:67%;" />

   * 磁场强度$H$

     * $H=B/\mu$   (A/m)
       磁场的特性参数，与介质无关，仅与电流相关。

   * 磁导率 $\mu$

     * 单位：（H/m）
     * 真空磁导率为：$\mu_0=4\pi \times 10^{-7}$
       空气磁导率：近似等于真空磁导率
       相对磁导率：$\mu_r = \mu/\mu_0$
     * 磁导率：表示物质导磁能力大小，并不是磁力大小；物质的磁力由磁能积（B H）表示

2. 磁路的基本定律

   * 高斯定律
     * <img src="note_autoctrprac.assets/image-20250905104507120.png" alt="image-20250905104507120" style="zoom:67%;" />
   * 安培环路定律
     * <img src="note_autoctrprac.assets/image-20250905105757255.png" alt="image-20250905105757255" style="zoom:67%;" />
     * ==磁压降$U_m$、磁动势$F_m$、磁路基尔霍夫第二定律==
       <img src="note_autoctrprac.assets/image-20250905105817199.png" alt="image-20250905105817199" style="zoom:67%;" />
   * ==磁路欧姆定律==
     * <img src="note_autoctrprac.assets/image-20250905105915515.png" alt="image-20250905105915515" style="zoom:67%;" />
     * **磁路与电路的差别**<img src="note_autoctrprac.assets/image-20250905105951084.png" alt="image-20250905105951084" style="zoom:67%;" />
       注意，磁路一般呈饱和非线性，不可使用叠加定律。且直流磁路（内部）无损耗，磁路中的漏磁比电路中严重得多。
   * 法拉第定律
     * <img src="note_autoctrprac.assets/image-20250905110119238.png" alt="image-20250905110119238" style="zoom:67%;" />
     * <img src="note_autoctrprac.assets/image-20250905110214829.png" alt="image-20250905110214829" style="zoom:67%;" />
     * 引起磁链（磁通）变化的原因
       * 磁通由交流电产生，空间中任意一点的磁通随时间变化。（时间）
       * 空间中各点磁通不变化，但线圈位置变化，磁链相应变化。（位移）
       * 总结：$\Psi = \Psi(t, x)$
     * <img src="note_autoctrprac.assets/image-20250905110359586.png" alt="image-20250905110359586" style="zoom:67%;" />
     * <img src="note_autoctrprac.assets/image-20250905111243792.png" alt="image-20250905111243792" style="zoom:67%;" />
   * 安培电磁力定律
     * <img src="note_autoctrprac.assets/image-20250905111257099.png" alt="image-20250905111257099" style="zoom:67%;" />
     * 均匀磁场中导线受力：$F=BIL\sin \theta$
     * <img src="note_autoctrprac.assets/image-20250905112817628.png" alt="image-20250905112817628" style="zoom:67%;" />
     * <img src="note_autoctrprac.assets/image-20250905112912592.png" alt="image-20250905112912592" style="zoom:67%;" />

### 电器控制常识

## LEC3 直流电机原理与结构

1. 直流电机工作原理
   <img src="note_autoctrprac.assets/image-20250909194348569.png" alt="image-20250909194348569" style="zoom:50%;" />

2. 直流电机结构

   * 定子

     * 分类：永磁式（永磁铁）、励磁式（绕线圈，电生磁）

     * 结构
       <img src="note_autoctrprac.assets/image-20250909195314335.png" alt="image-20250909195314335" style="zoom:50%;" />
   
       **组成成分：**

     * 主磁极

       * 作用：建立主磁场
       * 构成：
         主极铁心和套装在铁心上的励磁绕组，大功率场合
         永久磁铁，小功率场合
   
     * 机座
   
       * 作用：主磁路的一部分、电机的结构框架
       * 用厚钢板弯成筒形焊成或铸钢件制成。
   
     * 电刷
       <img src="note_autoctrprac.assets/image-20250909195551494.png" alt="image-20250909195551494" style="zoom:50%;" />
   
   * 转子
   
     * 换向器
       <img src="note_autoctrprac.assets/image-20250909195641812.png" alt="image-20250909195641812" style="zoom:50%;" />
   
     * 电枢铁心
       <img src="note_autoctrprac.assets/image-20250909195657757.png" alt="image-20250909195657757" style="zoom: 50%;" />
   
     * 电枢绕组（**电路部分**）
       <img src="note_autoctrprac.assets/image-20250909195719626.png" alt="image-20250909195719626" style="zoom:50%;" />
   
       * 绕法：简单来说，在基本原理图基础上，增大线圈数量以提高受力时间/效率，同时利用换向片将线圈连接起来，使得所有线圈在任意时刻都通电，增大整体受力。另外，增大线圈的匝数，增大单个线圈受力。
         <img src="note_autoctrprac.assets/image-20250909200056186.png" alt="image-20250909200056186" style="zoom:67%;" />
         <img src="note_autoctrprac.assets/image-20250909200106579.png" alt="image-20250909200106579" style="zoom:67%;" />
         
         核心：最终都要从电刷出去，因此，所有电流最终都要到达电刷所在的换向片。
         <img src="note_autoctrprac.assets/image-20250909200126561.png" alt="image-20250909200126561" style="zoom:67%;" />
         
         除此之外，还有环形绕组、鼓形绕组
   
   * <img src="note_autoctrprac.assets/image-20250909194724509.png" alt="image-20250909194724509" style="zoom:67%;" />
   
3. 电机中的铁磁与永磁材料

   * 电机的材料主要包括

     * 铜——电枢绕组：电机的电路部分

     * 铁——定子铁心：电机的磁路部分

       > 非线性的B-H曲线，磁导率大，是真空磁导率的2000~8000倍

   * 铁磁材料的导磁性能
     <img src="note_autoctrprac.assets/image-20250912213722154.png" alt="image-20250912213722154" style="zoom:67%;" />

   * 磁滞现场与磁滞回线

     * 磁滞现象：磁感应强度B的变化总是落后于外磁场H的变化

     * 重要参数：剩磁$B_r$、矫顽力$H_c$

       <img src="note_autoctrprac.assets/image-20250912214904294.png" alt="image-20250912214904294" style="zoom:67%;" />

       > 解读，顺着曲线箭头来看，H从正降到0，而B却没降到0。

     * 磁滞回线：若反复磁化若干循环后，就可得到一个近似对称于原点的闭合曲线
       基本磁化回线：各磁滞回线顶点的连线
       <img src="note_autoctrprac.assets/image-20250912215120811.png" alt="image-20250912215120811" style="zoom:67%;" />
       
     * 磁滞损耗：
       <img src="note_autoctrprac.assets/image-20251014091914167.png" alt="image-20251014091914167" style="zoom:50%;" />
       <img src="note_autoctrprac.assets/image-20251014092032600.png" alt="image-20251014092032600" style="zoom:50%;" />
   
     * 涡流损耗
       <img src="note_autoctrprac.assets/image-20251014092524357.png" alt="image-20251014092524357" style="zoom:50%;" />
   
       > 分析功率时，涡流的电压认为不变$e=-\frac{d\Phi}{dt}$(单匝分析)
   
   * 软磁材料、硬磁材料/永磁材料
     <img src="note_autoctrprac.assets/image-20250912215218976.png" alt="image-20250912215218976" style="zoom:67%;" />
       * 永磁材料的性能参数
         * 最大磁能积
         * 温度系数（通常为负的）
           当铁磁材料的温度升到一定程度时,铁磁材料会变为弱磁物质。居里点：铁磁材料转化为弱磁物质μr = 1的温度称为 居里点。 
         * 电阻率
           常用的铁氧体、钕铁硼等永磁材料的电阻率是纯铁的 100-1000倍以上，（纯铁）铁耗小。
         * 最强的永磁材料——钕铁硼
   
4. 直流电机的磁场

   * 空载时直流电机的磁场

     * 定义：电枢（转子）电流等于零时，由励磁绕组电流单独作用产生的磁场，又称为主极磁场。

       <img src="note_autoctrprac.assets/image-20250912221225955.png" alt="image-20250912221225955" style="zoom: 67%;" />

     * 例子：
       <img src="note_autoctrprac.assets/image-20250912221330498.png" alt="image-20250912221330498" style="zoom:67%;" />
       <img src="note_autoctrprac.assets/image-20250912221429604.png" alt="image-20250912221429604" style="zoom:67%;" />

     * 气隙磁通密度分布——**礼帽形**、一对极的主磁极磁通分布
       <img src="note_autoctrprac.assets/image-20250912221558870.png" alt="image-20250912221558870" style="zoom:67%;" />

       > 横坐标代表沿着电枢圆周展开的位置，而磁密波形的具体形状，主要是由主磁极（特别是极靴）与电枢之间气隙的形状和大小决定的。磁密即为磁感应强度B。
       
     * 磁通饱和性
       <img src="note_autoctrprac.assets/image-20250912221623412.png" alt="image-20250912221623412" style="zoom:67%;" />

   * 负载时直流电机的磁场

     * 定义：直流电机负载后，电枢电流产生的磁动势，电枢磁动势的出现使电机磁场发生变化。假设励磁电流为零，只有电枢电流，由图可见电枢磁动势产 生的气隙磁场在空间的分布情况
       <img src="note_autoctrprac.assets/image-20250912221741584.png" alt="image-20250912221741584" style="zoom:50%;" />
     * 气隙磁通密度分布——**“马鞍形”**
       <img src="note_autoctrprac.assets/image-20250912221834599.png" alt="image-20250912221834599" style="zoom:67%;" />

   * 直流电机的电枢反应

     * 定义：电机负载运行后，气隙中的磁场是励磁磁动势与电枢磁动势共同作用的结果。**二者磁场对气隙磁场的影响称为电枢反应。**
       <img src="note_autoctrprac.assets/image-20250912222120508.png" alt="image-20250912222120508" style="zoom:67%;" />
       <img src="note_autoctrprac.assets/image-20250912222132765.png" alt="image-20250912222132765" style="zoom:67%;" />
       物理中性线偏离几何中性线！

   * 直流电机磁场的合成
     <img src="note_autoctrprac.assets/image-20250912222221813.png" alt="image-20250912222221813" style="zoom:67%;" />

   * 电刷在几何中性线时，电枢反应的特点：
     <img src="note_autoctrprac.assets/image-20250912222256464.png" alt="image-20250912222256464" style="zoom:67%;" />

5. 直流电机的换向

   * <img src="note_autoctrprac.assets/image-20250912222307967.png" alt="image-20250912222307967" style="zoom:67%;" />
   * <img src="note_autoctrprac.assets/image-20250912222322672.png" alt="image-20250912222322672" style="zoom:67%;" />
   * <img src="note_autoctrprac.assets/image-20250912222332164.png" alt="image-20250912222332164" style="zoom:67%;" />
   * <img src="note_autoctrprac.assets/image-20250912222342309.png" alt="image-20250912222342309" style="zoom:67%;" />
   * <img src="note_autoctrprac.assets/image-20250912222354498.png" alt="image-20250912222354498" style="zoom:67%;" />
   
     > 换向极的目的，就是在电刷所在的位置（几何中性线处）产生一个**方向正好相反**的小磁场，用来**抵消**和补偿由电枢反应造成的磁场扭曲。这样一来，即使在有电枢反应的情况下，电刷下的磁场也能被人为地校正回理想状态。

## LEC4 直流电机基本方程

1. 直流电机的基本关系式

   * 电动势
     <img src="note_autoctrprac.assets/image-20250913101826982.png" alt="image-20250913101826982" style="zoom:67%;" />

     > n是每分钟转速，不是每秒！$\omega$和$\Omega$都是角速度。
     
     > 导体：电枢上，能够切割磁感线并产生感应电动势的单根有效导线。
     > 并联支路：从电刷进入电枢后被分成好几条并行的路径。
     > 示例：<img src="note_autoctrprac.assets/image-20250913105526436.png" alt="image-20250913105526436" style="zoom:50%;" />
     
   * 电磁力矩
     <img src="note_autoctrprac.assets/image-20250913101841492.png" alt="image-20250913101841492" style="zoom:67%;" />
   
2. 直流电动机的基本关系式

   * 电磁转矩与电枢反电势

     $T_{em}=K_tI_a$、$E_a=K_e\omega$、$K_e=K_t$
     <img src="note_autoctrprac.assets/image-20250916194132920.png" alt="image-20250916194132920" style="zoom:67%;" />

     转矩系数和反电势系数是由电机结构决定，对于一个特定电机，为一个常数。

     > 注意看，$C_e\Phi n = K_e w$，并非$K_e = C_e \Phi$，注意别混淆了

   * 转矩平衡方程式

     * 式子：$T_{em}-T_0-T_L=J\frac{dw}{dt}$

       <img src="note_autoctrprac.assets/image-20250916195018347.png" alt="image-20250916195018347" style="zoom:67%;" />

       * <img src="note_autoctrprac.assets/image-20250916195136484.png" alt="image-20250916195136484" style="zoom:67%;" />

       * 由上述式子可推导出，加速、减速、匀速$\frac{dw}{dt}$的大小可推出

         <img src="note_autoctrprac.assets/image-20250916195249300.png" alt="image-20250916195249300" style="zoom:67%;" />

   * 电压平衡方程式

     * 动态电压平衡方程式：$U_a=L_a\frac{dI_a}{dt}+R_aI_a+E_a$
       静态电压平衡方程式：$U_a=R_aI_a+E_a$

       <img src="note_autoctrprac.assets/image-20250916195423794.png" alt="image-20250916195423794" style="zoom:67%;" />

     * 功率平衡方程式

       * 从电路角度看
         <img src="note_autoctrprac.assets/image-20250916200249628.png" alt="image-20250916200249628" style="zoom: 50%;" />
       * 从机械角度看
         <img src="note_autoctrprac.assets/image-20250916200627200.png" alt="image-20250916200627200" style="zoom:67%;" />
         
         * $M$：转矩$T$
         
         * $\Omega$：电机角速度
         * $P=T\omega=M\Omega$
       * 能量流动
         <img src="note_autoctrprac.assets/image-20250916201005137.png" alt="image-20250916201005137" style="zoom:50%;" /><img src="note_autoctrprac.assets/image-20250916200946833.png" alt="image-20250916200946833" style="zoom:50%;" />

   * 直流电动机四大关系式
     <img src="note_autoctrprac.assets/image-20250916201102041.png" alt="image-20250916201102041" style="zoom:67%;" />

3. 额外说明

   * 感应电势
     <img src="note_autoctrprac.assets/image-20250916201603189.png" alt="image-20250916201603189" style="zoom:67%;" />
   * 电磁转矩
     <img src="note_autoctrprac.assets/image-20250916201613516.png" alt="image-20250916201613516" style="zoom:67%;" />
   * $K_e$和$K_t$的关系
     <img src="note_autoctrprac.assets/image-20250916201722508.png" alt="image-20250916201722508" style="zoom:67%;" />
   * 电阻
     <img src="note_autoctrprac.assets/image-20250916201736178.png" alt="image-20250916201736178" style="zoom:67%;" />

4. 发电机的基本关系式（机械能/~——电能）
   <img src="note_autoctrprac.assets/image-20250917094802257.png" alt="image-20250917094802257" style="zoom:67%;" />

5. 直流发电机和直流电动机的基本平衡关系式对比
   <img src="note_autoctrprac.assets/image-20250917094841842.png" alt="image-20250917094841842" style="zoom:67%;" />

6. 直流电动机的静态特性**概述**

   * 概念：
     * 静态：控制电压和负载转矩不变，电机的电流和转速达到恒定的稳定在时，称电机处于稳态。
     * 静态特性：静态时各变量间的关系。
   * 常用稳态（静态）特性
     * 机械特性：转速与转矩的关系（固有特性）
     * 调节特性：转速与控制量（如电压）的关系（人为控制）
   * 对于直流电机控制系统，根据被控量的补贴，分为：
     * 调速系统
     * 转矩控制系统
     * 机械位移（角位移控制系统）
   * 关系式：电机电流、转速
     <img src="note_autoctrprac.assets/image-20250918220029726.png" alt="image-20250918220029726" style="zoom:67%;" />
   * 调速方法、调速系统要求
     <img src="note_autoctrprac.assets/image-20250918220641325.png" alt="image-20250918220641325" style="zoom:67%;" />

7. 电枢控制

   * 机械特性——转速n与电磁转矩$T_{em}$的关系
     <img src="note_autoctrprac.assets/image-20250918220723045.png" alt="image-20250918220723045" style="zoom:67%;" />
     注意，由于理想空载是不存在的，因此，有实际空载和理想空载的区分。

     机械特性硬度，即抵抗能力。
     <img src="note_autoctrprac.assets/image-20250918220739672.png" alt="image-20250918220739672" style="zoom:67%;" />

     > 电压变换，但转速不会突变，因此，工作状态会有一个过渡态

   * 调节特性——转速n与电枢电压$U_a$
     <img src="note_autoctrprac.assets/image-20250918220913222.png" alt="image-20250918220913222" style="zoom:67%;" />
     <img src="note_autoctrprac.assets/image-20250918220920908.png" alt="image-20250918220920908" style="zoom:67%;" />

8. 磁场控制时的机械特性和调节特性——n与磁通$\Phi$

   <img src="note_autoctrprac.assets/image-20250918220947872.png" alt="image-20250918220947872" style="zoom:67%;" />

9. 电机稳定运行时的功率关系
   <img src="note_autoctrprac.assets/image-20250918221008914.png" alt="image-20250918221008914" style="zoom:67%;" />

10. 直流电机的调速控制

    * 串电阻调速——射线

      <img src="note_autoctrprac.assets/image-20250918222752527.png" alt="image-20250918222752527" style="zoom:67%;" />

      > <img src="note_autoctrprac.assets/image-20250922223745986.png" alt="image-20250922223745986" style="zoom:67%;" />
      > $E_a=C_e\Phi \Omega$，$\Omega$即转速$n$

    * 弱磁调速
      <img src="note_autoctrprac.assets/image-20250918222825462.png" alt="image-20250918222825462" style="zoom:67%;" />
    
      > 无级调速：连续，平滑地调速，通常来源于励磁回路的电阻$R_f$，一个滑线变阻器。
      >
      > 高效率：相较于在电枢回路中串联电阻的降压调速方法，弱磁调速只是调节励磁回路的小电流，能量损耗小，因此效率较高。
      >
      > 调速比：指最高转速与最低转速（基速）的比值。在弱磁调速中，这个范围通常是2到4倍，意味着最高可以调到基速的2至4倍。范围受限于换向性能和机械强度。
      > <img src="note_autoctrprac.assets/image-20250918223645840.png" alt="image-20250918223645840" style="zoom:67%;" />
      
    * 降压调速
      <img src="note_autoctrprac.assets/image-20250922224516477.png" alt="image-20250922224516477" style="zoom:67%;" />
    
11. 直流电机的启动/关闭

    * $U=I_aR_a+E=I_aR_a+C_e\Phi\Omega$

      启动时，转速为0，E为0，此时电流$I_{st}=I_a=U/R_a$过大，因此需要采取措施，分别为：**降压U、增加电阻$R_a$**

      关于串联电阻启动的方式有两种，分别为：

      * 单级电阻启动（左下图）：启动时开关断开，用R来限制电流，转速达到要求后再断开

      * 多级电阻启动（右下图）：电机启动时，所有电阻都串在电路中。随着转速升高，接触器 KM1,KM2,KM3 按顺序依次闭合，逐级地将电阻切除（短路）。
        图中从上到下的多条斜线代表串联不同电阻时的机械特性（电阻越大，直线越陡）。启动过程如红色箭头所示：电机沿着总电阻最大的线（最陡的）启动(①)，当转速升高、电流下降到某个值(I2)时，切除一级电阻，电流瞬间跳变到上限(I1)，电机沿着新的特性曲线继续加速(②→③)，如此反复，直到所有启动电阻被切除，电机最终在固有特性上稳定运行(⑦) 。这种方式能将启动过程中的电流和转矩波动控制在一定范围内。

        <img src="note_autoctrprac.assets/image-20250922225053021.png" alt="image-20250922225053021" style="zoom:67%;" />

    * 正确的启动方式（左下角文字）
      <img src="note_autoctrprac.assets/image-20250922225737419.png" alt="image-20250922225737419" style="zoom:67%;" />

12. 直流电动机的工作状态

    * 总览

      * 四种：电动机、发电机、能耗制动、反接制动
      * 电动机：电磁转矩与转速同向
        发电机/能耗制动/反接制动：电磁转矩与转速反向
        <img src="note_autoctrprac.assets/image-20250922230352316.png" alt="image-20250922230352316" style="zoom:67%;" />

    * 电动机状态
      <img src="note_autoctrprac.assets/image-20250922230442735.png" alt="image-20250922230442735" style="zoom:67%;" />

      > 1、3象限：正转、反转

    * 发电机（反馈/回馈制动）状态（$E_a>U_a$）
      <img src="note_autoctrprac.assets/image-20250922230507507.png" alt="image-20250922230507507" style="zoom:67%;" />

      例子：小车下坡
      <img src="note_autoctrprac.assets/image-20250923092351015.png" alt="image-20250923092351015" style="zoom:67%;" />
      
    * 能耗制动状态（$U_a=0$）
      <img src="note_autoctrprac.assets/image-20250923084630720.png" alt="image-20250923084630720" style="zoom:67%;" />
      <img src="note_autoctrprac.assets/image-20250923090332604.png" alt="image-20250923090332604" style="zoom:67%;" />

      > 公式：$n=-\frac{R_a+R_i}{K_eK_t}T_{em}$，（PPT有误）
      >
      > 优点：最终准确停在原点，不会出现反向启动（反接制动会反向启动）。

    * 反接制动状态（$U_a$反向）
      <img src="note_autoctrprac.assets/image-20250923090924495.png" alt="image-20250923090924495" style="zoom:67%;" />
      <img src="note_autoctrprac.assets/image-20250923090934924.png" alt="image-20250923090934924" style="zoom:67%;" />

    * 实际应用
      <img src="note_autoctrprac.assets/image-20250923093112716.png" alt="image-20250923093112716" style="zoom:50%;" />

      * <img src="note_autoctrprac.assets/image-20250923093141332.png" alt="image-20250923093141332" style="zoom:50%;" />
        <img src="note_autoctrprac.assets/image-20250923093154550.png" alt="image-20250923093154550" style="zoom:67%;" />

    * 直流电机的四象限运行
      <img src="note_autoctrprac.assets/image-20250923093405656.png" alt="image-20250923093405656" style="zoom:50%;" /><img src="note_autoctrprac.assets/image-20250923093337110.png" alt="image-20250923093337110" style="zoom:67%;" />

13. 直流电动机的动态特性
    <img src="note_autoctrprac.assets/image-20250923155134108.png" alt="image-20250923155134108" style="zoom:50%;" />
    <img src="note_autoctrprac.assets/image-20250923155145714.png" alt="image-20250923155145714" style="zoom:50%;" />
    <img src="note_autoctrprac.assets/image-20250923155156582.png" alt="image-20250923155156582" style="zoom:50%;" />
    
    ==机电常数$\tau_m$会考到，结合转动惯量一起出题==
    <img src="note_autoctrprac.assets/image-20250923155206505.png" alt="image-20250923155206505" style="zoom:50%;" />
    <img src="note_autoctrprac.assets/image-20250923155213584.png" alt="image-20250923155213584" style="zoom:50%;" />
    <img src="note_autoctrprac.assets/image-20250923155222006.png" alt="image-20250923155222006" style="zoom:50%;" />

### 做题总结

1. 熟悉各条公式最为关键
   $T_{em}=C_T\Phi I_a$
   $E_a=C_e\Phi n$
   $K_e=K_T$、$C_T \Phi = C_e\Phi *\frac{60}{2\pi}$
   围绕上述关系，结合电路列出方程如$U_a=I_aR_a+E_a$，即可求解
   转变电枢电压并不会影响上述常数与电枢电阻，因此可作为求解电压变化的关键
2. 电动机-发电机机组，本质上是发电机成为了电动机的负载，二者拥有如下关系
   * 转速相同
   * 电动机的负载转矩$T_L$是发电机的动力，即对于发电机来说，$T_L=T_{em}+T_0$
3. 启动：电机转速为0，感应电动势$E_a=0$
   空载：电机启动后未挂载负载，$T_{em}=T_0/T_{em}=0$

## LEC5 直流电机的选用

1. 直流电机的选用

   * 直流电机特点
     <img src="note_autoctrprac.assets/image-20250923155522827.png" alt="image-20250923155522827" style="zoom: 50%;" /><img src="note_autoctrprac.assets/image-20250923155547037.png" alt="image-20250923155547037" style="zoom:50%;" /><img src="note_autoctrprac.assets/image-20250923160422920.png" alt="image-20250923160422920" style="zoom: 50%;" />
     <img src="note_autoctrprac.assets/image-20250923160447913.png" alt="image-20250923160447913" style="zoom:50%;" />
     <img src="note_autoctrprac.assets/image-20250923160456956.png" alt="image-20250923160456956" style="zoom:50%;" />

   * 电机选择

     * 系统组成
       <img src="note_autoctrprac.assets/image-20250923161122140.png" alt="image-20250923161122140" style="zoom:67%;" />

     * 从电机侧看需求：
       <img src="note_autoctrprac.assets/image-20250923161155342.png" alt="image-20250923161155342" style="zoom:67%;" />

       > 上述公式的i来源于两个齿轮传速比，$w_m=i \cdot w_L$
       >
       > 左式：转动惯量，即**总=电机自身+负载**。推导利用能量守恒定律；动能：$\frac12 J w^2$
       >
       > 右式：力矩计算，推导利用功率守恒；功率：$P=Tw$

     * 各项参数
       <img src="note_autoctrprac.assets/image-20250923161941486.png" alt="image-20250923161941486" style="zoom: 50%;" />
     * 


## LEC6-电力电子技术概述

1. 电力电子技术概述

   * 对功率放大环节的要求
     <img src="note_autoctrprac.assets/image-20250925145258645.png" alt="image-20250925145258645" style="zoom:50%;" />

   * 电力交流技术

     * AC--DC
       <img src="note_autoctrprac.assets/image-20250925145359061.png" alt="image-20250925145359061" style="zoom:50%;" />

       > 通过开关结构，将交流电变为等效的直流电。

     * DC--DC
       <img src="note_autoctrprac.assets/image-20250925145411042.png" alt="image-20250925145411042" style="zoom:50%;" />

       > 占空比控制电压大小，电流有一定的增减过程

     * AC--AC
       <img src="note_autoctrprac.assets/image-20250925145421401.png" alt="image-20250925145421401" style="zoom:50%;" />
       <img src="note_autoctrprac.assets/image-20250925145439622.png" alt="image-20250925145439622" style="zoom:50%;" />

     * DC--AC
       <img src="note_autoctrprac.assets/image-20250925145449432.png" alt="image-20250925145449432" style="zoom:50%;" />

     * 开关技术

       电阻技术：耗能，效率低；

       开关技术：效率高，仅在开关切换时有较大功耗。可以用占空比进行调节。
       <img src="note_autoctrprac.assets/image-20250925145459351.png" alt="image-20250925145459351" style="zoom:50%;" />
       <img src="note_autoctrprac.assets/image-20250925145508677.png" alt="image-20250925145508677" style="zoom:50%;" />
   
2. 电力电子器件

   * 按照开关类型分类

     * 不可控器件——不能用控制信号来控制其通断
       如：电力二极管，只有两个端子，器件的通和断是由其在主电路中承受的电压和电流决定的
       <img src="note_autoctrprac.assets/image-20250925195803043.png" alt="image-20250925195803043" style="zoom:50%;" />

     * 半控型器件——通过控制信号可以控制其导通而不能控制其关断
       如：晶闸管及其大部分派生器件，器件的关断由其在主电路中承受的电压和电流决定
       <img src="note_autoctrprac.assets/image-20250925195906457.png" alt="image-20250925195906457" style="zoom:50%;" />
       <img src="note_autoctrprac.assets/image-20250925195921409.png" alt="image-20250925195921409" style="zoom: 67%;" />

     * 全控型器件——通过控制信号可控制导通和关断，又称自关断器件

       * 绝缘栅双极晶体管IGBT
       * 电力场效应晶体管P-MOSFET
       * 门极可关断晶闸管 GTO

       <img src="note_autoctrprac.assets/image-20250925200434034.png" alt="image-20250925200434034" style="zoom:50%;" />

     * 总览

       横坐标：工作频率，代表器件的开关速度，越高表示开关速度越快

       纵坐标：器件容量，代表器件能够处理的功率大小，越高表示功率处理能力越强

       从左到右依次为：TRIAC（晶闸管）、GTO、IGBT、MOSFET
       <img src="note_autoctrprac.assets/image-20250925200817505.png" alt="image-20250925200817505" style="zoom: 67%;" />

   * **MOSFET**场效应晶体管
     <img src="note_autoctrprac.assets/image-20250925201338825.png" alt="image-20250925201338825" style="zoom:67%;" />
     <img src="note_autoctrprac.assets/image-20250925201615139.png" alt="image-20250925201615139" style="zoom:67%;" />
     <img src="note_autoctrprac.assets/image-20250925201643584.png" alt="image-20250925201643584" style="zoom: 67%;" />
     <img src="note_autoctrprac.assets/image-20250925201721555.png" alt="image-20250925201721555" style="zoom:67%;" />

   * IGBT
     <img src="note_autoctrprac.assets/image-20250925201825004.png" alt="image-20250925201825004" style="zoom: 67%;" />
     <img src="note_autoctrprac.assets/image-20250925201841179.png" alt="image-20250925201841179" style="zoom:67%;" />
     <img src="note_autoctrprac.assets/image-20250925201852127.png" alt="image-20250925201852127" style="zoom:67%;" />

3. 电力电子器件—器件保护

   * 过电压保护措施
     <img src="note_autoctrprac.assets/image-20250925201934989.png" alt="image-20250925201934989" style="zoom:67%;" />
   * 过电流——过载和短路
     <img src="note_autoctrprac.assets/image-20250925201954693.png" alt="image-20250925201954693" style="zoom:67%;" />
   * 缓冲电路
     <img src="note_autoctrprac.assets/image-20250925202014311.png" alt="image-20250925202014311" style="zoom:67%;" />
     <img src="note_autoctrprac.assets/image-20250925202022490.png" alt="image-20250925202022490" style="zoom:67%;" />
     <img src="note_autoctrprac.assets/image-20250925202031136.png" alt="image-20250925202031136" style="zoom:67%;" />

## LEC7 脉宽调制驱动技术

1. PWM技术基本原理

   * **冲量相等而形状不同的窄脉冲加在具有惯性的环节上时，其响应效果基本相同**
     <img src="note_autoctrprac.assets/image-20250930105808126.png" alt="image-20250930105808126" style="zoom:50%;" />
     <img src="note_autoctrprac.assets/image-20250930105837518.png" alt="image-20250930105837518" style="zoom:50%;" />

   * PWM信号产生的基本原理

     用一系列等幅不等宽的脉冲来代替一个正弦半波
     $u_r$与$u_c$比较，前者更大时，输出为正，反之为负。

     <img src="note_autoctrprac.assets/image-20250930110007812.png" alt="image-20250930110007812" style="zoom:67%;" />

2. 开关电路驱动——H桥

   * 结构
     <img src="note_autoctrprac.assets/image-20250930111148784.png" alt="image-20250930111148784" style="zoom:67%;" />
     
   * 原理
     * 前提假设
       * 忽略晶体管开关过程，只讨论其稳态阶段。但要分析晶体管开关时，电路中电压电流的瞬态与稳定响应。
       * 一个开关周期内电机转速及反电势为常值。
       * 电枢回路用电阻、电感和电势等效。
       * 电磁转矩平均值和负载转矩相平衡时，是准稳定状态，电枢电流周期性变化。
       * 电机默认为正向转动；电流A到B为正向。
       
     * 双极PWM驱动的输入输出
       * <img src="note_autoctrprac.assets/image-20250930111514429.png" alt="image-20250930111514429" style="zoom:50%;" />
       * <img src="note_autoctrprac.assets/image-20250930111528103.png" alt="image-20250930111528103" style="zoom:67%;" />
       
         > $u_a$即$U_{AB}$，$U_{av}$为$U_{AB}$的有效值，$U_D$为直流电源提供的电压，是恒定值。
       
     * 电动机状态
       ==$i_a>0,U_{av}>E$，电流从A到B==
       <img src="note_autoctrprac.assets/image-20251001153038011.png" alt="image-20251001153038011" style="zoom:50%;" />
     
       * $0<t<t_1$，$T_1、T_4$饱和导通，$T_2、T_3$截至断开
     
         $U_{AB}=U_D$
     
         <img src="note_autoctrprac.assets/image-20251001152817876.png" alt="image-20251001152817876" style="zoom:67%;" />
     
       * $t_1<t<T$，只有$D_2$和$D_3$正常导通
     
         $U_{AB}=-U_D$
         <img src="note_autoctrprac.assets/image-20251001153150459.png" alt="image-20251001153150459" style="zoom:50%;" />
     
         核心在于电枢电感，其维持了电流的走向，产生巨大的自感电动势，使得最终表现为$U_{AB}=-U_D$
         <img src="note_autoctrprac.assets/image-20251001154935989.png" alt="image-20251001154935989" style="zoom:67%;" />
         <img src="note_autoctrprac.assets/image-20251001155733939.png" alt="image-20251001155733939" style="zoom:67%;" />
     
         * $t_1<t<T$时间段，$T_2$、$T_3$基极正向偏压，但$U_{CE}=-0.7V$，故不导通
         * 若无$D_2$、$D_3$，$T_1$、$T_4$截止时将被击穿
     
     * 发电机状态
       ==$i_a<0，U_{av}<E$，电流从B到A==
       <img src="note_autoctrprac.assets/image-20251001161042183.png" alt="image-20251001161042183" style="zoom:67%;" />
     
       * $t_1<t<T$，$T_2、T_3$饱和导通，$T_1、T_4$截至断开
     
         $U_{AB}=-U_D$
         <img src="note_autoctrprac.assets/image-20251001161102177.png" alt="image-20251001161102177" style="zoom:67%;" />
     
       * $0<t<t_1$，只有$D_1$和$D_4$正常导通
         $U_{AB}=U_D$
         <img src="note_autoctrprac.assets/image-20251001162311710.png" alt="image-20251001162311710" style="zoom:67%;" />
     
         * $0<t<t_1$时间段，$T_1$、$T_4$基极正向偏压，但$U_{CE}=-0.7V$，故不导通
         * 若无$D_1$、$D_4$，$T_2$、$T_3$截止时将被击穿
     
     * 轻载状态
       <img src="note_autoctrprac.assets/image-20251001162424960.png" alt="image-20251001162424960" style="zoom:67%;" />
     
   * 双极输出总结：
     <img src="note_autoctrprac.assets/image-20251001162503640.png" alt="image-20251001162503640" style="zoom:67%;" />
     <img src="note_autoctrprac.assets/image-20251001162516651.png" alt="image-20251001162516651" style="zoom:67%;" />

## LEC8 变压器

### 变压器运行原理

1. 变压器运行原理简要概述
   <img src="note_autoctrprac.assets/image-20251009140726826.png" alt="image-20251009140726826" style="zoom:67%;" />

2. 变压器概述

   * 用途
     <img src="note_autoctrprac.assets/image-20251009142356646.png" alt="image-20251009142356646" style="zoom:67%;" />
   * 分类
     <img src="note_autoctrprac.assets/image-20251009142408064.png" alt="image-20251009142408064" style="zoom:67%;" />
   * 结构
     * 铁心
       <img src="note_autoctrprac.assets/image-20251009142511749.png" alt="image-20251009142511749" style="zoom:67%;" />
     * 绕组
       <img src="note_autoctrprac.assets/image-20251009142521211.png" alt="image-20251009142521211" style="zoom:67%;" />
     * 其他
       <img src="note_autoctrprac.assets/image-20251009142530653.png" alt="image-20251009142530653" style="zoom:67%;" />

3. 变压器的空载与负载运行

   * 基本原理概述
     <img src="note_autoctrprac.assets/image-20251009142721028.png" alt="image-20251009142721028" style="zoom:67%;" />

     * 主磁通$\Phi$
       ==$e=-N\frac{d\phi}{dt}$==
       <img src="note_autoctrprac.assets/image-20251009142834944.png" alt="image-20251009142834944" style="zoom: 67%;" />
       方向问题
       <img src="note_autoctrprac.assets/image-20251010094652466.png" alt="image-20251010094652466" style="zoom:67%;" />
       
       > 楞次定律，当正向电流增强，磁场增强，为了削弱磁场，需产生反向磁场，则应有反向的感应电流，感应电流方向与正向电流相反，则感应电动势应为下正上负。
       
     * 漏磁通$\Phi_{1\sigma}$、损耗
       <img src="note_autoctrprac.assets/image-20251009143239730.png" alt="image-20251009143239730" style="zoom:67%;" />

     * 运行时整体情况
       <img src="note_autoctrprac.assets/image-20251009143617432.png" alt="image-20251009143617432" style="zoom:67%;" />
     
       > 漏磁通的介质是空气，因此其不会有铁的饱和特性，故呈线性
     
   * 空载状态
   
     * 主磁通感应的电动势——主电动势
   
       相量关系$\dot{E}_1=-j4.44f_1N_1\dot{\Phi}_m$

       主磁通取决于电网电压、频率、匝数，与负载大小基本无关。
       <img src="note_autoctrprac.assets/image-20251009144034560.png" alt="image-20251009144034560" style="zoom:67%;" />

       * 二次主电动势
         <img src="note_autoctrprac.assets/image-20251009144341428.png" alt="image-20251009144341428" style="zoom:67%;" />
   
         > $2\pi f_1=\omega$
   
     * 漏磁通感应的电动势——漏电动势
       <img src="note_autoctrprac.assets/image-20251009144800226.png" alt="image-20251009144800226" style="zoom:67%;" />
       漏电抗对于一个变压器来说是定值。

     * 空载时电路分析
       <img src="note_autoctrprac.assets/image-20251009150139092.png" alt="image-20251009150139092" style="zoom:67%;" />
   
       attention：将漏电抗和原端绕组电阻合并为原端绕组漏阻抗。

       此时的电流为空载电流$I_0$，
       <img src="note_autoctrprac.assets/image-20251009150340435.png" alt="image-20251009150340435" style="zoom:67%;" />
   
       * 空载电流分析
         <img src="note_autoctrprac.assets/image-20251009150721059.png" alt="image-20251009150721059" style="zoom:67%;" />
       * 电压比例
         <img src="note_autoctrprac.assets/image-20251009151229047.png" alt="image-20251009151229047" style="zoom:67%;" />
       * 波形
         <img src="note_autoctrprac.assets/image-20251009151242379.png" alt="image-20251009151242379" style="zoom:67%;" />
         
         > 理解方式：右上角为磁通与电流的关系，前期线性，后期饱和。
         >
         > 而第二象限为理想的正弦，通过一象限的函数一一映射，有第四象限的图。
       
     * 空载时的等效电路和相量图
     
       * 等效电路
         <img src="note_autoctrprac.assets/image-20251009152056646.png" alt="image-20251009152056646" style="zoom:67%;" />
         <img src="note_autoctrprac.assets/image-20251009152110606.png" alt="image-20251009152110606" style="zoom:67%;" />
       * 相量图
         <img src="note_autoctrprac.assets/image-20251009152123470.png" alt="image-20251009152123470" style="zoom:67%;" />
     
     * 总结
       <img src="note_autoctrprac.assets/image-20251009152139080.png" alt="image-20251009152139080" style="zoom:67%;" />
     
   * 负载状态
   
     > 变压器一次侧接在额定频率、额定电压的交流电源上，二次接上负载的运行状态，称为负载运行
   
     * 电磁关系
       前面提到，$\dot{E}_1=-j4.44f_1N_1\dot{\Phi}_m$，在理想条件下，认为原边的电动势恒等于电网电压，也就是说，**$E_1$为恒定值，则$\Phi_m$也为恒定值。**
       <img src="note_autoctrprac.assets/image-20251009221614207.png" alt="image-20251009221614207" style="zoom: 67%;" />
   
       由于负载存在，导致副边产生了副边电流$I_2$，这个电流产生的磁通方向与主磁通相反，会削弱主磁通。因此，为了维持主磁通不变，原边需要增加相应的电流$I_{1L}$以抵消$I_2$的影响。
       <img src="note_autoctrprac.assets/image-20251009221817600.png" alt="image-20251009221817600" style="zoom:67%;" />
   
       磁通为恒定值，则$F=\Phi R = IN$可知，闭合磁路的磁动势也为恒定值，与空载的时候的情况列等式，有：
       <img src="note_autoctrprac.assets/image-20251009221656421.png" alt="image-20251009221656421" style="zoom:67%;" />
       <img src="note_autoctrprac.assets/image-20251009221728706.png" alt="image-20251009221728706" style="zoom:67%;" />
       由于新增的负载电流$I_{1L}$远大于空载电流，故
       <img src="note_autoctrprac.assets/image-20251009221807140.png" alt="image-20251009221807140" style="zoom:67%;" />
   
       总的来说，**原边绕组从电网吸收的功率传递给副边绕组。副边绕组电流增加或减小的同时，引起原边电流的增加或减小，吸收的功率也增大或减小。**
   
       ==对于电压来说==，<img src="note_autoctrprac.assets/image-20251009221941324.png" alt="image-20251009221941324" style="zoom:67%;" />
       ==对于功率来说==，<img src="note_autoctrprac.assets/image-20251009222001819.png" alt="image-20251009222001819" style="zoom: 67%;" />
       <img src="note_autoctrprac.assets/image-20251009222103359.png" alt="image-20251009222103359" style="zoom:67%;" />
   
     * 方程式
       <img src="note_autoctrprac.assets/image-20251009222749266.png" alt="image-20251009222749266" style="zoom:67%;" />
       <img src="note_autoctrprac.assets/image-20251009222805429.png" alt="image-20251009222805429" style="zoom:50%;" />
       
       > 注意E1的方向，从电动势角度来看，二者均为电压升，但此时电源以负载角度看，故而需取负号，实际情况下，这里真实的压降与E1始终相反。
       
       <img src="note_autoctrprac.assets/image-20251009222814479.png" alt="image-20251009222814479" style="zoom:50%;" />
       
     * 绕组归算/等效电路
     
       > 假设一个新的二次绕组替代原二次绕组，新的二次绕组的匝数等于一次绕组的匝数，同时一次和二次绕组的原有电磁关系不变。
     
       * 原则
         * 归算后二次绕组的磁动势保持不变。
         * 归算后功率、能量不变。
       * 推演
         <img src="note_autoctrprac.assets/image-20251009223048523.png" alt="image-20251009223048523" style="zoom:67%;" />
         <img src="note_autoctrprac.assets/image-20251009223056142.png" alt="image-20251009223056142" style="zoom:67%;" />
         <img src="note_autoctrprac.assets/image-20251009223105991.png" alt="image-20251009223105991" style="zoom:67%;" />
         <img src="note_autoctrprac.assets/image-20251009223122865.png" alt="image-20251009223122865" style="zoom:67%;" />
       * 归算后的基本方程
         <img src="note_autoctrprac.assets/image-20251009223157093.png" alt="image-20251009223157093" style="zoom:67%;" />
       * 归算后的T型等效电路
         <img src="note_autoctrprac.assets/image-20251009223220457.png" alt="image-20251009223220457" style="zoom:67%;" />
   
     * 负载下相量图画法
       <img src="note_autoctrprac.assets/image-20251009223253275.png" alt="image-20251009223253275" style="zoom:67%;" />
     
     * 功率因素
       <img src="note_autoctrprac.assets/image-20251009223304284.png" alt="image-20251009223304284" style="zoom:50%;" />
   
## 步进电机

* 本章节易混淆参数的意义

  * $Z_r$：转子的齿数

  * $N$：总拍数，即完成一个通电周期需要多少个动作/拍

  * m：相数，定子中独立的绕组数量，每一相都是可以单独通电控制的电路

  * p：磁极对数，定子中NS极对数。
    P：P=2p

    > 多对磁极可能是由同一个电路通过不同的绕法控制，因此$p=km$

### 步进电动机原理

1. 以三相反应式步进电机为例
   
   * 原理图及其解读
     <img src="note_autoctrprac.assets/image-20251014192551903.png" alt="image-20251014192551903" style="zoom:50%;" />
     * 定子铁心有六个齿极，每个齿极上绕有线圈，径向相对两个线圈连接在一起。
     * 转子铁心有四个齿极
   * **磁阻最小原理**：磁通总是沿磁阻最小的路径闭合，利用齿极间的吸引力拉动转子旋转。
     <img src="note_autoctrprac.assets/image-20251014192817690.png" alt="image-20251014192817690" style="zoom:50%;" />
   * 错齿是使步进电机旋转的根本原因。
   * 运作过程
     * 从磁场来看，三相反应式步进电动机通过顺序接通和关断各相绕组，形成了一个步进旋转磁场，转子铁心受定子磁场的影响旋转。
     * <img src="note_autoctrprac.assets/image-20251014193155687.png" alt="image-20251014193155687" style="zoom:50%;" />
       <img src="note_autoctrprac.assets/image-20251014193204081.png" alt="image-20251014193204081" style="zoom:50%;" />
       <img src="note_autoctrprac.assets/image-20251014193215519.png" alt="image-20251014193215519" style="zoom:50%;" />
   
2. 依据工作过程进行分类

   * 三相单三拍（前述类型）
     <img src="note_autoctrprac.assets/image-20251014193323139.png" alt="image-20251014193323139" style="zoom:50%;" />

     > 不稳定，因而较下列两种控制较少使用

   * 三相双三拍
     <img src="note_autoctrprac.assets/image-20251014193341962.png" alt="image-20251014193341962" style="zoom:50%;" />

   * 三相单双六拍
     <img src="note_autoctrprac.assets/image-20251014194145554.png" alt="image-20251014194145554" style="zoom:50%;" />
     <img src="note_autoctrprac.assets/image-20251014194212496.png" alt="image-20251014194212496" style="zoom:50%;" />
     <img src="note_autoctrprac.assets/image-20251014194355042.png" alt="image-20251014194355042" style="zoom:50%;" />

3. 原理分析

   * 概念
     齿距角$\theta_t$、步距角$\theta_b$、极距角$\theta_p$

     <img src="note_autoctrprac.assets/image-20251014195038631.png" alt="image-20251014195038631" style="zoom:50%;" />
     <img src="note_autoctrprac.assets/image-20251016193358755.png" alt="image-20251016193358755" style="zoom:50%;" />

     > 注意理解，**一个齿距角就是通电状态完成一个周期，转子转过的角度。**

   * 运动控制

     <img src="note_autoctrprac.assets/image-20251014195134140.png" alt="image-20251014195134140" style="zoom:50%;" />

4. 步进电机定义
   <img src="note_autoctrprac.assets/image-20251014195340901.png" alt="image-20251014195340901" style="zoom:50%;" />

### 步进电动机的分类与结构

1. 分类
   * 反应式/磁阻式
   * 永磁式
   * 混合式
   
2. 磁阻式步进电机的结构
   * 结构
     * 定子
       <img src="note_autoctrprac.assets/image-20251014200243772.png" alt="image-20251014200243772" style="zoom:67%;" />
     * 转子
       <img src="note_autoctrprac.assets/image-20251014200251917.png" alt="image-20251014200251917" style="zoom: 67%;" />
       * 对转子齿数的规定
         <img src="note_autoctrprac.assets/image-20251014200345646.png" alt="image-20251014200345646" style="zoom:67%;" />
         <img src="note_autoctrprac.assets/image-20251014200954987.png" alt="image-20251014200954987" style="zoom:67%;" />
         * 总结 ：公式的含义是在相邻磁极的角度内，当一个定子转子齿对齐时，为了更换通电绕组时能够旋转，那么下一个磁极的定子转子必须要有错位。而我们一个周期内，转子转过的角度就是齿距角$\theta_t$，而分到每一步上则为$\frac1m \theta_t$。那么，公式中的K，则代表一种设计需求，定子相邻磁极之间的角度不能是整数倍，而是在整数倍基础上加一个$\frac 1 m \theta_t$，从而使得相邻磁极定子和转子之间有一个错位。
           <img src="note_autoctrprac.assets/image-20251014201346435.png" alt="image-20251014201346435" style="zoom:67%;" />
           <img src="note_autoctrprac.assets/image-20251014201509718.png" alt="image-20251014201509718" style="zoom:67%;" />
           <img src="note_autoctrprac.assets/image-20251014214822952.png" alt="image-20251014214822952" style="zoom:67%;" />
     
   * 控制
   
     * 控制信号输入
   
       一个脉冲，绕组改变一次通电状态，转子转过一个步距角！
       <img src="note_autoctrprac.assets/image-20251016190443363.png" alt="image-20251016190443363" style="zoom: 33%;" />
   
3. 永磁式步进电机（了解即可）

   对转子引入磁铁，增加输出转矩
   <img src="note_autoctrprac.assets/image-20251016190622719.png" alt="image-20251016190622719" style="zoom:50%;" />

4. 混合式步进电机

   * 结构
     <img src="note_autoctrprac.assets/image-20251016191017189.png" alt="image-20251016191017189" style="zoom:50%;" />

   * 运转过程

     关键在于，转子1的齿对应转子2的槽。由于内部的磁铁，转子1的所有齿是N极，转子2的齿是S极。而转子1和转子2面对的定子的磁性是一致的，假如磁极是N，转子1正好和磁极相对，那么转子1的N极会被推走，而由于转子2此时对着的是槽且为S极，那么转子2会被吸过去。这二者的受力方向是同样的，因此转矩就更大了。<img src="note_autoctrprac.assets/image-20251016192819736.png" alt="image-20251016192819736" style="zoom:50%;" />

     > 结合右下图来理解较好。

   * 参数关系

     * 齿数——遵循同样的错齿关系，因此和磁阻式步进电机一样，$\frac{Z_r}{2p}=K \pm \frac1m$

       常见的组合
       <img src="note_autoctrprac.assets/image-20251016194643051.png" alt="image-20251016194643051" style="zoom:33%;" />

     * 转速
       <img src="note_autoctrprac.assets/image-20251016194814846.png" alt="image-20251016194814846" style="zoom:50%;" />

### 步进电动机的静特性

1. 基本概念

   * 静态：绕组通电状态保持不变，并且转子保持静止的状态。

   * 静态特性：步进电动机在静态时所拥有的性能称为静态特性，主要指转矩和转角的关系。

   * 静转矩：<img src="note_autoctrprac.assets/image-20251016200407048.png" alt="image-20251016200407048" style="zoom:50%;" />

   * 电角度：
     电角度表示齿距角：$\theta_{te}=360°=2\pi\;rad$
     电角度表示步距角$\theta_{be}=\frac{2\pi }{N}$

     > 电角度剥离了电机具体的相数、齿数关系，更通用

   * 平衡位置：步进电机能够静止不动的位置

     * 稳定平衡：当外力矩为0且步进电机单相通电，齿与齿对齐
     * 不稳定平衡：当外力矩为0且步进电机单相通电，齿与槽对齐
       <img src="note_autoctrprac.assets/image-20251016201111293.png" alt="image-20251016201111293" style="zoom:50%;" />

   * 失调角$\Delta \theta_e$：转子偏离稳定平衡位置的角度
     实际角度$\theta_e$，稳定平衡点的角度$\theta_{e0}$，$\Delta\theta_e=\theta_e-\theta_{e0}$

     $\theta_{e0}=0,2\pi,\dots$

   * **矩角特性**：表示的是静转矩与失调角的关系
     静态转矩：步进电机转子静止且绕组通以直流电时，由于失调角存在而引起的电磁转矩

     > 步进电机的静态特性主要指矩角特性。

2. 矩角特性

   > 失调角与电磁转矩同方向为正

   * 矩角特性图
     <img src="note_autoctrprac.assets/image-20251016210851186.png" alt="image-20251016210851186" style="zoom: 67%;" />
   
     * 转矩是失调角的周期函数，周期为$2\pi$，$T=-T_{em}sin\Delta \theta_e$
   
       > $T_{em}$是最大静转矩，由气隙磁导和电流决定。负号表示步进电动机产生的是一种**恢复转矩**，在一定范围内总是反抗转子偏离平衡位置，即：步进电动机的自锁能力
   
     * 如果上电前转子所在位置（失调角）在静稳定区，一通电后，电磁转矩就会把转子拉动到稳定平衡点位置
   
     * $T_m$与绕组的电流$I$的关系
       <img src="note_autoctrprac.assets/image-20251016211330149.png" alt="image-20251016211330149" style="zoom:50%;" />
   
   * 多相通电时的矩角特性
   
     * 曲线族
       <img src="note_autoctrprac.assets/image-20251016211934339.png" alt="image-20251016211934339" style="zoom:50%;" />
   
     * 数学原理
   
       n：同时通电的相数
       <img src="note_autoctrprac.assets/image-20251016212149526.png" alt="image-20251016212149526" style="zoom: 67%;" />
       <img src="note_autoctrprac.assets/image-20251016213112610.png" alt="image-20251016213112610" style="zoom:50%;" />
   
       > 这里的公式似乎默认了相数等于拍数，即$m=N$。
   
     * 例子
       <img src="note_autoctrprac.assets/image-20251016214403753.png" alt="image-20251016214403753" style="zoom:50%;" />
       <img src="note_autoctrprac.assets/image-20251016214412829.png" alt="image-20251016214412829" style="zoom:50%;" />

### 步进电机的运行特性

<img src="note_autoctrprac.assets/image-20251016215202164.png" alt="image-20251016215202164" style="zoom:50%;" />

1. 单步运行

   > 假设:
   >
   > 绕组通电的持续时间大于机电过渡过程时间；
   >
   > 绕组中电流是瞬时建立和消除的

   * 情况举例
     * 三相电机，无负载转矩
       <img src="note_autoctrprac.assets/image-20251016215004410.png" alt="image-20251016215004410" style="zoom: 67%;" />
     * 三相电机，恒定负载转矩，$T_L<T_{st}$
       <img src="note_autoctrprac.assets/image-20251016215106466.png" alt="image-20251016215106466" style="zoom:67%;" />
     * 三相电机，恒定负载转矩，$T'_L>T_{st}$（无法启动！）
       <img src="note_autoctrprac.assets/image-20251016215122686.png" alt="image-20251016215122686" style="zoom:50%;" />
       ==不失步的基本条件$T_L<T_{st}$==
   * $T_{st}$：单步启动的骑电动转矩就是各相邻矩角特性交点对应的转矩
     <img src="note_autoctrprac.assets/image-20251016215416750.png" alt="image-20251016215416750" style="zoom: 67%;" />
     当每拍矩角特性为正弦且等幅值时，交点横坐标为$\frac{\theta_{be}-\pi}{2}$，$T_{st}=T_m\cos \frac \pi N$
     * 拍数越多，并不是越接近最大转矩，比如图中的4相4拍和4相8拍。
       <img src="note_autoctrprac.assets/image-20251016220233993.png" alt="image-20251016220233993" style="zoom:50%;" />
   * 自由震荡过程
     <img src="note_autoctrprac.assets/image-20251016220404146.png" alt="image-20251016220404146" style="zoom:50%;" />

2. 连续运行

   * 基本概念

     **控制频率——输入脉冲信号频率——每个绕组的通电的持续时间**
     <img src="note_autoctrprac.assets/image-20251016220421861.png" alt="image-20251016220421861" style="zoom: 67%;" />

   * 启动频率

     * 场景推导——控制频率必须小于启动频率才能启动，否则如图中b1点
       <img src="note_autoctrprac.assets/image-20251016220814720.png" alt="image-20251016220814720" style="zoom:50%;" />
       <img src="note_autoctrprac.assets/image-20251016220822353.png" alt="image-20251016220822353" style="zoom:50%;" />
     * <img src="note_autoctrprac.assets/image-20251016221529227.png" alt="image-20251016221529227" style="zoom:67%;" />

   * 运行频率
     <img src="note_autoctrprac.assets/image-20251016221636807.png" alt="image-20251016221636807" style="zoom:67%;" />

     动态转矩随频率增加而下降
     <img src="note_autoctrprac.assets/image-20251016221719848.png" alt="image-20251016221719848" style="zoom:67%;" />

   * 不同频率下的连续运行

     * 极低频下运行——单步运行
       <img src="note_autoctrprac.assets/image-20251016221809356.png" alt="image-20251016221809356" style="zoom:50%;" />
     * 低频运行
       <img src="note_autoctrprac.assets/image-20251016221822594.png" alt="image-20251016221822594" style="zoom:50%;" />
     * 低频运行，低频丢步和低频共振
       <img src="note_autoctrprac.assets/image-20251016221859434.png" alt="image-20251016221859434" style="zoom:67%;" />
       <img src="note_autoctrprac.assets/image-20251016221912204.png" alt="image-20251016221912204" style="zoom: 67%;" />
     * 连续脉冲作用下的平稳运行
       <img src="note_autoctrprac.assets/image-20251016221931653.png" alt="image-20251016221931653" style="zoom: 67%;" />

### 步进电机的驱动

1. 步进电机驱动概述

   * **步进电机驱动器=脉冲分配器+功率放大电路**
     <img src="note_autoctrprac.assets/image-20251022100426070.png" alt="image-20251022100426070" style="zoom:50%;" />
   * 脉冲分配器
     * 功能
       <img src="note_autoctrprac.assets/image-20251022100519797.png" alt="image-20251022100519797" style="zoom:50%;" />
   * 功率放大器
     * 功能：将控制脉冲进行电压和的电流放大，使脉冲具有一定的功率驱动能力
     * 要求：提高步进电动机的快速性、提高步进电动机的平稳性
     * 电路：
       * 单电压限流型驱动电路
       * 高低压切换型驱动电路
       * 恒流斩波型驱动电路
       * 分频段调压驱动电路

2. 步进电机的细分驱动

   * 概述

     细分驱动通过改变相电流的大小，以改变合成磁场的夹角来控制步进电机选择。
     <img src="note_autoctrprac.assets/image-20251022101037456.png" alt="image-20251022101037456" style="zoom: 67%;" />

   * 不同驱动方式的过程：

     * 整步驱动
       <img src="note_autoctrprac.assets/image-20251022101624796.png" alt="image-20251022101624796" style="zoom:50%;" />
     * 半步驱动
       <img src="note_autoctrprac.assets/image-20251022101638681.png" alt="image-20251022101638681" style="zoom:50%;" />
       简单来说，在10，01中间，加了个0.5，0.5的组合。控制电机的角度取在原本两个状态中间。可以对照着下面的绕组通电阶梯图看。
     * 1/4步驱动
       <img src="note_autoctrprac.assets/image-20251022101647122.png" alt="image-20251022101647122" style="zoom:50%;" />
     * 进一步细分，到正弦电流曲线情况
       <img src="note_autoctrprac.assets/image-20251022102007405.png" alt="image-20251022102007405" style="zoom:50%;" />

   * 优缺点

     * 优点

       * 消除了电机的低频振荡

       * 同时也提高了电机的输出转矩

         > <img src="note_autoctrprac.assets/image-20251022103502186.png" alt="image-20251022103502186" style="zoom:50%;" />

       * 提高了电机步进运行的分辨率

     * 缺点

       * 每一微步的增量扭矩大大减小

         > 当电机停在某个状态时，遇到扰动会更容易松动，因为细分驱动原因，导致恢复转矩更小。同时，恢复转矩本质受到转子位置的影响，如果转子本身正对着绕组的话，此时恢复转矩最大，而在两个绕组中间时最小。
         >
         > 当磁场到下一个状态时，即合成磁场旋转一个微小的角度，转子输出的即为增量转矩。每一微步的增量转矩不同。接近整步位置时，增量转矩较小；中间时，增量转矩较大。
         >
         > 同时，假如此时负载转矩过大，也可能要出现累计好几步之后才能转的动的情况，这样就与细分驱动追求的高精度相左。
         >
         > <img src="note_autoctrprac.assets/image-20251022104424961.png" alt="image-20251022104424961" style="zoom:50%;" />

       * 细分后每步的步距角不一定相等。
         <img src="note_autoctrprac.assets/image-20251022105020099.png" alt="image-20251022105020099" style="zoom:50%;" />

       * 高速时性能差
         <img src="note_autoctrprac.assets/image-20251022105048360.png" alt="image-20251022105048360" style="zoom: 67%;" />

       * 不一定能够带来更好的精度，只有当负载非常轻，微细步的扭矩足以驱动负载时，才可以提高精度。精度还取决于细分驱动器的细分电流控制精度等其他因素。细分数越大越难控制。

### 步进电机系统的应用

1. 各参数
   * 步距角
     <img src="note_autoctrprac.assets/image-20251022111145350.png" alt="image-20251022111145350" style="zoom:50%;" />
   * 保持转矩
     <img src="note_autoctrprac.assets/image-20251022111156740.png" alt="image-20251022111156740" style="zoom:50%;" />
   * 定位转矩
     <img src="note_autoctrprac.assets/image-20251022111207046.png" alt="image-20251022111207046" style="zoom:50%;" />
2. 应用要求
   * 步距角、步距精度
     <img src="note_autoctrprac.assets/image-20251022111426735.png" alt="image-20251022111426735" style="zoom:50%;" />
   * 最大负载转矩限制
     <img src="note_autoctrprac.assets/image-20251022111921074.png" alt="image-20251022111921074" style="zoom:50%;" />
   * 脉冲信号频率对运行的影响
     <img src="note_autoctrprac.assets/image-20251022111941175.png" alt="image-20251022111941175" style="zoom:50%;" />
   * 其他注意事项
     <img src="note_autoctrprac.assets/image-20251022111956801.png" alt="image-20251022111956801" style="zoom:50%;" />
     <img src="note_autoctrprac.assets/image-20251022112002315.png" alt="image-20251022112002315" style="zoom:50%;" />
3. 闭环控制的步进电机系统
   <img src="note_autoctrprac.assets/image-20251022112026024.png" alt="image-20251022112026024" style="zoom:67%;" />
   <img src="note_autoctrprac.assets/image-20251022112033364.png" alt="image-20251022112033364" style="zoom:67%;" />
   <img src="note_autoctrprac.assets/image-20251022112041564.png" alt="image-20251022112041564" style="zoom:67%;" />
   <img src="note_autoctrprac.assets/image-20251022112048755.png" alt="image-20251022112048755" style="zoom:67%;" />
   <img src="note_autoctrprac.assets/image-20251022112055677.png" alt="image-20251022112055677" style="zoom:67%;" />

## 交流绕组和无刷直流电机

### 交流绕组的基本工作原理

1. 结构
   <img src="note_autoctrprac.assets/image-20251022204157866.png" alt="image-20251022204157866" style="zoom:67%;" />

2. 工作过程

   * 当只给某一相通电时，磁场的变化分析
     <img src="note_autoctrprac.assets/image-20251022204536386.png" alt="image-20251022204536386" style="zoom:50%;" />
     <img src="note_autoctrprac.assets/image-20251022204546334.png" alt="image-20251022204546334" style="zoom:50%;" />
   * 给三相对称绕组接通三相对称交流电
     * 三相电流，相位相差120°
       <img src="note_autoctrprac.assets/image-20251022204708474.png" alt="image-20251022204708474" style="zoom:50%;" />
       <img src="note_autoctrprac.assets/image-20251022204717550.png" alt="image-20251022204717550" style="zoom:50%;" />
     * 在分析时，可以关注几个特殊点，分别是60°、120°、180°等，此时三相绕组中总是只有两条电路处于通路，分析此时合成磁场方向。
       <img src="note_autoctrprac.assets/image-20251022204910781.png" alt="image-20251022204910781" style="zoom:67%;" />
       <img src="note_autoctrprac.assets/image-20251022204924069.png" alt="image-20251022204924069" style="zoom:67%;" />

3. 概念

   * 极对数

     * 一相绕组通直流电形成的磁场的极数就是电机的极数。一般极数是成对出现的，因此也有极对数。
       <img src="note_autoctrprac.assets/image-20251022205522874.png" alt="image-20251022205522874" style="zoom:50%;" />

     * <img src="note_autoctrprac.assets/image-20251022205536739.png" alt="image-20251022205536739" style="zoom:50%;" />

     * <img src="note_autoctrprac.assets/image-20251022205602765.png" alt="image-20251022205602765" style="zoom:67%;" />

       > Y--B--Y’--B‘

   * 磁场转速
     ==$n_s=\frac{60f}{p}(转/分)$==
   
     * 当极对数P=1时，总共进出线圈边为6
       <img src="note_autoctrprac.assets/image-20251022210922855.png" alt="image-20251022210922855" style="zoom:50%;" />
     * 当极对数P=2时，总共进出线圈边为12
       <img src="note_autoctrprac.assets/image-20251022210940233.png" alt="image-20251022210940233" style="zoom:50%;" />
   
     <img src="note_autoctrprac.assets/image-20251022211132655.png" alt="image-20251022211132655" style="zoom: 50%;" />
   
   * 旋转方向

     * 取决于三相电流的相序，即绕组本身不变，改变一下三相电路的ABC相的接法。
       <img src="note_autoctrprac.assets/image-20251022211109758.png" alt="image-20251022211109758" style="zoom:67%;" />

### 交流绕组基本参数

1. 交流绕组

   * 构成原则
     <img src="note_autoctrprac.assets/image-20251023200256675.png" alt="image-20251023200256675" style="zoom:50%;" />
   * 分类：按相数：单相、二相、三相、多相。

2. 基本概念

   * 电角度/机械角度

     > 结合磁场转速公式理解

     **$电角度=p*机械角度$**

   * 极矩

     > 相邻两个磁极轴线之间沿定子内圆周的距离称为极矩

     * 电角度表示：$\tau=180°$
     * 用槽数表示：$\tau=\frac{Q}{2p}$
     * 用长度表示：$\tau=\frac{\pi D}{2p}$
       <img src="note_autoctrprac.assets/image-20251023201234618.png" alt="image-20251023201234618" style="zoom:50%;" />

   * 线圈：构成交流绕组的基本单位是线圈，线圈可以分为单匝和多匝。
     <img src="note_autoctrprac.assets/image-20251023201410665.png" alt="image-20251023201410665" style="zoom:50%;" />

   * 线圈节距：同一个线圈的两个有效边之间的距离称为线圈节距（$y_1$，用槽数表示）

     <img src="note_autoctrprac.assets/image-20251023201637070.png" alt="image-20251023201637070" style="zoom: 50%;" />

   * 绕组的轴线：
     <img src="note_autoctrprac.assets/image-20251023201716248.png" alt="image-20251023201716248" style="zoom:50%;" />

   * 槽矩角
     相邻两槽之间的电角度为槽矩角$\alpha=\frac{p*360°}{Q}$，Q为定子槽数

     > 结合机械角度、电角度来理解。
     
   * 每极每相槽数
     <img src="note_autoctrprac.assets/image-20251023213813955.png" alt="image-20251023213813955" style="zoom:67%;" />

### 无刷直流电机（普通BLDC）

1. 无刷直流电动机原理

   > 概述，根据转子位置控制定子磁场位置，让定子磁场拖动其转动
   > <img src="note_autoctrprac.assets/image-20251023214231415.png" alt="image-20251023214231415" style="zoom: 33%;" />

   * 组件

     * 电动机

       * 无刷直流电机的转子
         <img src="note_autoctrprac.assets/image-20251023214534386.png" alt="image-20251023214534386" style="zoom:50%;" />

     * 位置传感器：霍尔传感器

       > 老师直接跳过了

     * 电子开关线路

   * 运行原理

     * 两极四相电机

       * 简化模型如下
         <img src="note_autoctrprac.assets/image-20251023215519236.png" alt="image-20251023215519236" style="zoom:50%;" />

       > 图中的定子绕组并非真实，只是一种近似。当其通电时，就是S极。

       * 过程：简单来说就是以$\pm45°$为边界，当转子磁铁进入这个区域时，霍尔传感器检测到，立马打开下一个阶段的定子绕组，吸引磁铁继续旋转。定子绕组的通电始终领先转子一个阶段。
         <img src="note_autoctrprac.assets/image-20251023220155760.png" alt="image-20251023220155760" style="zoom:50%;" />

     * 两极三相电机

       * 简化模型
         <img src="note_autoctrprac.assets/image-20251023220351868.png" alt="image-20251023220351868" style="zoom:67%;" />
       * 过程：本质和上述一样，都是定子磁场牵引着转子运动。在此处，每一次换向都会有一组绕组处于正向通电，第二组反相通电，第 三组不通电。
         <img src="note_autoctrprac.assets/image-20251023220611602.png" alt="image-20251023220611602" style="zoom:67%;" />

2. 各参数

   * 磁状态角

     > N是状态数，也可以理解为一个周期内磁场的状态数。
     >
     > 定子磁场旋转一圈时，**相邻两个稳定磁场方向之间的固定夹角**

   * 定子与转子磁势夹角

     > 定子磁场和转子磁场的实际夹角。

     <img src="note_autoctrprac.assets/image-20251023221137784.png" alt="image-20251023221137784" style="zoom:50%;" />

   * 导通角

     <img src="note_autoctrprac.assets/image-20251023221550664.png" alt="image-20251023221550664" style="zoom:50%;" />

## 无刷直流和交流伺服电机基本原理

1. 交流伺服电机概述

   * 概念

     * 伺服：使物体的位置、方位、状态等输出量能够跟随输入目标的任意变化的自动控制系统。
     * 伺服电机：在自动化控制系统中，用作执行元件，把所收到的电信号转换成电动机轴上的角位移或角速度输出。
       控制方式分为**位置控制、速度控制、转矩控制**

   * 分类

     * 以驱动电流为方波为前提设计的电动机（BLDC）
     * 以驱动电流为正弦波为前提设计的电动机（PMSM）

   * 结构

     * 定子绕组

       * 分布式绕组
         <img src="note_autoctrprac.assets/image-20251028202546999.png" alt="image-20251028202546999" style="zoom:67%;" />
       * 集中非叠式绕组
         <img src="note_autoctrprac.assets/image-20251028202557059.png" alt="image-20251028202557059" style="zoom:67%;" />

     * 永磁转子

       > 由铁芯、永磁体组成

       <img src="note_autoctrprac.assets/image-20251028203140654.png" alt="image-20251028203140654" style="zoom:67%;" />

2. 交流伺服电机原理
   * 矩形波电流驱动BLDC（方波伺服BLDC）
   
     > 简单来说，为了实现平稳的转矩输出，首先将电机设计成能产生“梯形波”反电动势的结构，然后再用驱动器给它通入矩形波电流，让二者的“平顶”完美配合，从而达到理想的控制效果
   
     * 电机本体与普通无刷直流电机类似，但配合高精度反馈+伺服驱动器，实现电流、速度、位置闭环，性能更高。
       
     * 永磁转子气隙磁密分布为梯形，匀速转动时，一相绕组的感应电动势与导线处的磁密成正比
       <img src="note_autoctrprac.assets/image-20251028203828753.png" alt="image-20251028203828753" style="zoom: 67%;" />
   
       > 这个图可以看作：横坐标$\theta$为转子静止时，周围一圈气隙的空间角度。纵坐标则代表气隙的磁感应强度，正负代表方向。
   
     * 理论上的控制方式：
       <img src="note_autoctrprac.assets/image-20251028205041617.png" alt="image-20251028205041617" style="zoom:67%;" />
   
       红线为三相绕组的反电动势，在其平坦处，我们施加电流方波(给两相施加相应的电压产生电流)，从而产生一个常理转矩。**每次都只有两相通电，另一相电流为零。因此排列组合总共有6种状态。**因此，看右图的转矩也是同一时刻只有两个。“正正得正、负负得负”，这是电机运动时两相产生同向转矩的原理。
   
       > 同一时刻只通两相电是为梯形波电机产生最大、最平稳转矩的最优解。
   
     * 实际上的缺陷：**由于电感存在，电流不会突变，也就无法形成理想的矩形波，从而引起换相转矩脉动。**适合应用于定速或调速的应用，不能用于位置控制。
   
     * 和前述无刷直流电机类似，只是增加了伺服控制系统和编码器，换相以及电流大小等控制更精确。（PPT没有体现这部分内容）
   
   * 正弦波电流驱动PMSM
   
     > 简单来说，为了实现**最平滑、最精确**的转矩输出，首先将电机设计成能产生**“正弦波”反电动势**的结构，然后再用伺服驱动器（通过复杂的算法如FOC）给它通入**三相正弦波电流**，并**始终保持电流波形与反电动势波形的相位完全一致**，从而达到理论上完全平滑、无任何波动的理想控制效果。
   
     * 结构
   
       * 气隙磁密分布为正弦，产生的反电动势也为正弦。
         <img src="note_autoctrprac.assets/image-20251028210617018.png" alt="image-20251028210617018" style="zoom: 67%;" />
       * 对三相绕组输入相电流，保持相电流与绕组相位相同
         <img src="note_autoctrprac.assets/image-20251028210705797.png" alt="image-20251028210705797" style="zoom:67%;" />
         <img src="note_autoctrprac.assets/image-20251028210742982.png" alt="image-20251028210742982" style="zoom:67%;" />
       * 合成的力矩为常值，实现了最平滑、稳定的转矩输出
         <img src="note_autoctrprac.assets/image-20251028210732519.png" alt="image-20251028210732519" style="zoom: 67%;" />
   
     * 如何实现相电流与反电动势的相位相同？——FOC（矢量控制）
   
       * 原坐标系
         <img src="note_autoctrprac.assets/image-20251028211718991.png" alt="image-20251028211718991" style="zoom: 67%;" />
   
       * 三相电流是线性相关，用两个线性无关的轴$\alpha、\beta$表示——Clarke变换
         <img src="note_autoctrprac.assets/image-20251028211925638.png" alt="image-20251028211925638" style="zoom:67%;" />
   
       * 换成d-q坐标系，Park变换
         <img src="note_autoctrprac.assets/image-20251028211954779.png" alt="image-20251028211954779" style="zoom: 80%;" />
         通过这个变换，让一个正弦波电流变为转子侧看到的、恒定不变的直流量。
         d轴：转子永磁体的N极方向；q轴：始终与d轴保持90°垂直。
   
       * Clarke-Park变换
         <img src="note_autoctrprac.assets/image-20251028212911446.png" alt="image-20251028212911446" style="zoom:80%;" />
   
       * 实际控制
         通过编码器得到当前转子的位置，通过空间换算，得到该坐标系下d轴和q轴的分量。
         让d轴的分量等于0，则所有电流都作用于q轴上。
         由于d轴其代表永磁体N极磁场方向，当d轴和反电动势的关系可以看作是磁通量$\Phi$和$e$的关系，即$e=-\frac{d\Phi}{dt}$，由于磁场本身是正弦变化的，因此，在求导后，可以知道e和$\Phi$本身就相差了90°。因此和d轴垂直的方向，q轴，就是反电动势的方向。
         我们让三相交流电合成向量始终和q轴对齐，交流电合成量就和反电动势合成量对齐，那么，经过Clarke-Park反变换后，各相交流电就始终和各相反电动势对齐。从而实现了FOC的目标。
   
         > 逆变换是确定的、唯一的数学映射。
   
         <img src="note_autoctrprac.assets/image-20251028215225328.png" alt="image-20251028215225328" style="zoom:67%;" />
   
       * 具体控制的实现
   
         * 测量转子位置，得到夹角$\theta_d$
           <img src="note_autoctrprac.assets/image-20251028215258812.png" alt="image-20251028215258812" style="zoom:67%;" />
   
         * 测定定子A和B相的绕组电流，算出C相绕组电流
           <img src="note_autoctrprac.assets/image-20251028215343954.png" alt="image-20251028215343954" style="zoom:67%;" />
   
         * 应用Clarke-Park变换，得到d和q轴的分量
           <img src="note_autoctrprac.assets/image-20251028215425342.png" alt="image-20251028215425342" style="zoom:67%;" />
   
         * 应用PID来调节$i_d$和$i_q$
   
           <img src="note_autoctrprac.assets/image-20251028215935990.png" alt="image-20251028215935990" style="zoom: 80%;" />
   
           从图中，上下分别为id和iq的PI控制器，分别输出对应的电压vd和vq
   
           > 由于实际电机的电路模型是无法准确获得的，因此需要PID来处理误差
   
         * 反变换，将PID获得的vd和vq反推回abc相电压
           <img src="note_autoctrprac.assets/image-20251028220421500.png" alt="image-20251028220421500" style="zoom:67%;" />
   
         * <img src="note_autoctrprac.assets/image-20251028220436716.png" alt="image-20251028220436716" style="zoom:67%;" />
   
         * 整体框图
           <img src="note_autoctrprac.assets/image-20251028220451290.png" alt="image-20251028220451290" style="zoom:67%;" />
   
       * FOC小结
         <img src="note_autoctrprac.assets/image-20251028220517923.png" alt="image-20251028220517923" style="zoom:67%;" />
   
       * PID控制通常采用电流、速度、位置三闭环的结构。电流环/力矩环是最本质的控制，从电流——速度——位置是依次上升的关系，即力--速度的实现方式。
         <img src="note_autoctrprac.assets/image-20251028222025287.png" alt="image-20251028222025287" style="zoom:80%;" />
   
   * PMSM和BLDC对比
     PMSM由于应用了FOC算法，使得定子磁场始终领先于永磁体90°。而BLDC由于是六步换相控制，无法做到始终保持90°的间距，因此没有PMSM控制平滑。
   
     <img src="note_autoctrprac.assets/image-20251028221801392.png" alt="image-20251028221801392" style="zoom:67%;" />
   
3. 直驱电机和直线电机（了解）

   * 直线伺服电机
   
     * 概述：可以理解为一个旋转电机“剖开并展开”。原本封闭的圆形定子被展开成一条直线导轨，而转子则变成了在导轨上滑行的模块。
       <img src="note_autoctrprac.assets/image-20251029095459647.png" alt="image-20251029095459647" style="zoom:67%;" />
     * 工作原理：当三相电流通入展开的定子绕组后，会产生一个沿直线方向移动的行波磁场，这个磁场与动子上的永磁体互相通，从而驱动动子沿着定子导轨做高速直线运动。
     * 核心优势：将电能直接转化为直线运动的动能，省去了滚珠丝杠、联轴器等中间传动环节，减少了损耗，同时还能高速、高精度。
       <img src="note_autoctrprac.assets/image-20251029095621335.png" alt="image-20251029095621335" style="zoom:67%;" />
       <img src="note_autoctrprac.assets/image-20251029095631086.png" alt="image-20251029095631086" style="zoom:67%;" />
       <img src="note_autoctrprac.assets/image-20251029095638717.png" alt="image-20251029095638717" style="zoom:67%;" />
     * 分类
       * 有铁芯直流电机（平板式/T型）
         <img src="note_autoctrprac.assets/image-20251029095714692.png" alt="image-20251029095714692" style="zoom:67%;" />
         <img src="note_autoctrprac.assets/image-20251029095722148.png" alt="image-20251029095722148" style="zoom:67%;" />
       * 无铁芯直流电机
         <img src="note_autoctrprac.assets/image-20251029095656716.png" alt="image-20251029095656716" style="zoom:67%;" />
   
   * 直驱电机
   
     * 概述：直驱电机也叫力矩电机，它是一种将负载直接安装在电机转轴上的旋转电机，完全取消了减速机、联轴器、皮带等中间传动机构
       <img src="note_autoctrprac.assets/image-20251029095828060.png" alt="image-20251029095828060" style="zoom:67%;" />
   
     * 优势
       <img src="note_autoctrprac.assets/image-20251029095849114.png" alt="image-20251029095849114" style="zoom:67%;" />
       <img src="note_autoctrprac.assets/image-20251029100024012.png" alt="image-20251029100024012" style="zoom:67%;" />
       <img src="note_autoctrprac.assets/image-20251029100037406.png" alt="image-20251029100037406" style="zoom:67%;" />
   
     * 转子
   
       * 无芯内转子
       * 带芯内转子
       * 带芯外转子
   
       <img src="note_autoctrprac.assets/image-20251029095952431.png" alt="image-20251029095952431" style="zoom:67%;" />

## 测量元件概述

1. 测量元件的概述
   * 控制系统中的测量元件
     <img src="note_autoctrprac.assets/image-20251030140604437.png" alt="image-20251030140604437" style="zoom: 50%;" />
   * 控制系统中的的不确定性
     <img src="note_autoctrprac.assets/image-20251030140646533.png" alt="image-20251030140646533" style="zoom: 50%;" />
     <img src="note_autoctrprac.assets/image-20251030140751566.png" alt="image-20251030140751566" style="zoom:50%;" />
     **所有不确定性最终在输出上都有所体现**
   * 根据测量元件不同的控制系统
     <img src="note_autoctrprac.assets/image-20251030142201350.png" alt="image-20251030142201350" style="zoom:50%;" />
2. 传感器的定义、组成和分类
   * 定义
     <img src="note_autoctrprac.assets/image-20251030142227019.png" alt="image-20251030142227019" style="zoom: 50%;" />
   * 组成：敏感元件、转换元件、转换电路
     <img src="note_autoctrprac.assets/image-20251030142300251.png" alt="image-20251030142300251" style="zoom:50%;" />
     * 例子
       <img src="note_autoctrprac.assets/image-20251030145331880.png" alt="image-20251030145331880" style="zoom:50%;" />
       <img src="note_autoctrprac.assets/image-20251030145446715.png" alt="image-20251030145446715" style="zoom:50%;" />
   * 测量元件的分类
     <img src="note_autoctrprac.assets/image-20251030145500340.png" alt="image-20251030145500340" style="zoom:50%;" />
3. 测量元件的特性
   * 总体 概述
     * 理想特性：输入和输出一一线性对应。
     * 静态特性：在稳态条件下（输出中无暂态分量，输入量和输出量不再变化）用分析或实验方法所确定的输出输入关系。静特性适用于输入不随着时间变化或变化缓慢的情况。
     * 动态特性：测量元件的输入量由一个数值迅速变到另一个数值的过程中，它呈现的特性就是动特性，此时变量对时间的导数不可忽略。
   * 各项特性
     * 变换函数
       <img src="note_autoctrprac.assets/image-20251031090312872.png" alt="image-20251031090312872" style="zoom:50%;" />
       <img src="note_autoctrprac.assets/image-20251031090336094.png" alt="image-20251031090336094" style="zoom:50%;" />
     * 灵敏度
       <img src="note_autoctrprac.assets/image-20251031090347143.png" alt="image-20251031090347143" style="zoom:50%;" />
     * 非线性误差/线性度
       <img src="note_autoctrprac.assets/image-20251031090357545.png" alt="image-20251031090357545" style="zoom:50%;" />
       <img src="note_autoctrprac.assets/image-20251031090444463.png" alt="image-20251031090444463" style="zoom:50%;" />
     * 滞环
       <img src="note_autoctrprac.assets/image-20251031090522947.png" alt="image-20251031090522947" style="zoom:50%;" />
     * 重复性误差
       <img src="note_autoctrprac.assets/image-20251031090535759.png" alt="image-20251031090535759" style="zoom:50%;" />
     * 静态误差
       <img src="note_autoctrprac.assets/image-20251031090547336.png" alt="image-20251031090547336" style="zoom:50%;" />
       * ==**精度：测量的精确程度。真实值与测量值之差。**==
       * 绝对误差：测量值与被测量真值之差：测量值-真实值，有单位、有正负
       * 相对误差：$\frac{|测量值-真实值|}{|测量值|}*100\%$，用来说明测量结果的准确程度
     * 测量范围和量程
       <img src="note_autoctrprac.assets/image-20251031091019767.png" alt="image-20251031091019767" style="zoom:67%;" />
     * ==分辨率==
       ![image-20251031091059997](note_autoctrprac.assets/image-20251031091059997.png)
       <img src="note_autoctrprac.assets/image-20251031091123684.png" alt="image-20251031091123684" style="zoom:67%;" />
       <img src="note_autoctrprac.assets/image-20251031091140003.png" alt="image-20251031091140003" style="zoom:50%;" />
     * 稳定性
       传感器在较长工作时间内保持其性能参数的能力
     * 漂移
       <img src="note_autoctrprac.assets/image-20251031091223136.png" alt="image-20251031091223136" style="zoom:67%;" />
     * 带宽
       <img src="note_autoctrprac.assets/image-20251031091245029.png" alt="image-20251031091245029" style="zoom:67%;" />
   * 提高传感器性能的技术途径
     <img src="note_autoctrprac.assets/image-20251031091235652.png" alt="image-20251031091235652" style="zoom:67%;" />
   * 选择测量元件时的注意事项
     <img src="note_autoctrprac.assets/image-20251031091257256.png" alt="image-20251031091257256" style="zoom:67%;" />

## 旋转变压器与感应同步器

1. 旋转变压器/感应同步器概述

   * 旋转变压器

     * 基本原理
       <img src="note_autoctrprac.assets/image-20251031094827070.png" alt="image-20251031094827070" style="zoom: 67%;" />
       总结，此处的基本结构可以认为是有刷旋转变压器。输入为转子、输出为定子。转子输入交流电，对定子上的sin和cos的绕组产生电磁感应。通过转子的旋转，改变转子绕组和定子sin、cos绕组的耦合程度。从而改变两个绕组的感应电动势幅值。通过幅值的比值，得到转角$\theta$

       > 产生感应电动势——输入电压本身的交变
       >
       > 感应电动势的大小——原边绕组和副边绕组的耦合程度——转子和定子绕组的相对位置，正对着的时候最大

     * 种类：

       * 极数：两极旋变和多极旋变
       * 结构形式：接触式和非接触式（有刷、无刷）、一体式和分体式

     * 无刷式旋转变压器
       <img src="note_autoctrprac.assets/image-20251031095544192.png" alt="image-20251031095544192" style="zoom:67%;" />
       定子：激磁绕组、sin/cos绕组
       转子：参考绕组、转子绕组
       过程：向定子激磁绕组输入交流电，通过空间结构的紧密贴合，让参考绕组产生对应的交流电。参考绕组和转子绕组相连，直接获得这个交流电。再通过电磁感应让定子上的sin/cos绕组产生交流电。则可获得转子的角度。整个过程也可以反过来，在后续有所讲述。

   * 感应同步器

     * 感应同步器概述
       <img src="note_autoctrprac.assets/image-20251031100009104.png" alt="image-20251031100009104" style="zoom:50%;" />
     * 平面感应同步器/直线式感应同步器
       <img src="note_autoctrprac.assets/image-20251031100921479.png" alt="image-20251031100921479" style="zoom:50%;" />
       <img src="note_autoctrprac.assets/image-20251031100932148.png" alt="image-20251031100932148" style="zoom:50%;" />
       <img src="note_autoctrprac.assets/image-20251031100952616.png" alt="image-20251031100952616" style="zoom:50%;" />
       简单来说，两个PCB，布局在两个平行的平面上，中间有气隙，耦合效率高。
     * 旋转式感应同步器
       <img src="note_autoctrprac.assets/image-20251031102306351.png" alt="image-20251031102306351" style="zoom:50%;" />

   * 用途：作为测量元件；精密机床数字显示、数控机床闭环伺服、测试转台、雷达天线定位等高精度跟踪系统应用广泛。

   * 类别：角位置测量元件、基于变压器原理、结构型的测量元件、模拟型

2. 旋转变压器/感应同步器的信号产生

   * 旋转变压器

     > 信号输出幅值大，抗干扰能力强，简单、灵敏，适应环境能力强，维护简便，应用广泛

     * 工作原理
       <img src="note_autoctrprac.assets/image-20251031192050222.png" alt="image-20251031192050222" style="zoom:67%;" />
       从电路图看，变压器原方和副方电压同相，因为电感的存在，对相位造成的90°的相位差值和法拉第电磁感应定律中对磁通量求导导致的90°的相位差抵消了。
     
   * 直线式感应同步器
   
     * 工作原理概述
       <img src="note_autoctrprac.assets/image-20251031194833250.png" alt="image-20251031194833250" style="zoom:67%;" />
   
     * 具体结构
   
       重点：节距L等于两倍的极距$\tau$(对应一个完整正弦波的半个周期)，同时当正弦绕组正对定尺某个节距，余弦绕组需要正对某个节距的极距的正中心，也就是，正弦绕组和余弦绕组相距$(K\pm1/4)L$
       <img src="note_autoctrprac.assets/image-20251031195655844.png" alt="image-20251031195655844" style="zoom:50%;" />
   
     * 磁场简化分析
   
       我们考虑两根竖向导体，形成磁场如a所示。由于磁场内磁感应强度肯定是不均匀分布的，其磁感应强度的分布类似一个梯形。我们**取其基波分量进行分析，也就是一个正弦波，来代表整个磁场。**
       <img src="note_autoctrprac.assets/image-20251031200853047.png" alt="image-20251031200853047" style="zoom:67%;" />
   
     * 运行过程
       <img src="note_autoctrprac.assets/image-20251031201140627.png" alt="image-20251031201140627" style="zoom:67%;" />
       <img src="note_autoctrprac.assets/image-20251031201155852.png" alt="image-20251031201155852" style="zoom:67%;" />
   
     * 输出电势瞬时值
       <img src="note_autoctrprac.assets/image-20251031201715577.png" alt="image-20251031201715577" style="zoom:67%;" />
   
       > 感应同步器的电路模型可以认为是电阻类型的，因为他没有无刷换向器那样把线绕在一起，因此便没有电感的影响。这也就造成了相位90°的差值。
       
     * 旋转式感应同步器的参数
       <img src="note_autoctrprac.assets/image-20251031201816673.png" alt="image-20251031201816673" style="zoom:67%;" />
     
     * 定义电角度$\theta_e$
       <img src="note_autoctrprac.assets/image-20251031201919674.png" alt="image-20251031201919674" style="zoom:67%;" />
       k根本无所谓！只是一个比值。
     
     * 用电角度表示电压瞬时值
       <img src="note_autoctrprac.assets/image-20251031201938618.png" alt="image-20251031201938618" style="zoom:67%;" />
     
     * 将输入输出反过来作为控制变压器，即设定一个期望的目标角度，然后加到正弦余弦绕组上，以得到当前位置和目标位置的差值。此时，他们的
       <img src="note_autoctrprac.assets/image-20251031202706964.png" alt="image-20251031202706964" style="zoom:50%;" />
   
3. 旋转变压器/感应同步器的信号处理

   * 鉴相型处理方式——电势的相位来鉴别电角
     目标式子：$e_2=kU_m\sin(wt+\theta_e)$

     * 两相激磁式

       较常用的方法，通过向两相输入电压，然后经过合成，直接检测定子绕组输出电压的相位即可得到电角度。
       <img src="note_autoctrprac.assets/image-20251031204101363.png" alt="image-20251031204101363" style="zoom:67%;" />
       <img src="note_autoctrprac.assets/image-20251031204108987.png" alt="image-20251031204108987" style="zoom:67%;" />

     * 单相激磁式

       不常用，因为需要手动为正弦绕组移相以构造出最后的$e_2$表达式（如果不加，那么相位都相同，无法合成$sin(wt+\theta_e)$）
       <img src="note_autoctrprac.assets/image-20251031205548216.png" alt="image-20251031205548216" style="zoom:67%;" />
       <img src="note_autoctrprac.assets/image-20251031205614443.png" alt="image-20251031205614443" style="zoom:67%;" />

   * 鉴幅型处理方式——根据信号的幅值鉴别电角
     目标式子：$e_2=kU_m\sin(\theta_e-\theta_1)\cos wt$
     这里讲的都是伺服误差控制，通过设定输入目标角度来控制。前面讲到的反正切的方法也可以用，在最后有提及，但其需要ADC等环节参与，较其他方法实现起来更复杂。

     * 两相激磁式

       输入目标角度$\theta_1$，然后实际角度为$\theta_e$，当二者相同时，单相连续绕组的感应电势为0。
       <img src="note_autoctrprac.assets/image-20251031205808335.png" alt="image-20251031205808335" style="zoom:67%;" />

     * 单相激磁式

       单相输入，然后需要特殊处理，即乘$\sin \theta_1$等因子，凑出最后的信号输出量，和前面相同。
       <img src="note_autoctrprac.assets/image-20251031205815223.png" alt="image-20251031205815223" style="zoom:67%;" />
       <img src="note_autoctrprac.assets/image-20251031205823856.png" alt="image-20251031205823856" style="zoom:67%;" />

   * 信号处理方式——编码器原理

     * 鉴相型——两相
       <img src="note_autoctrprac.assets/image-20251031210852581.png" alt="image-20251031210852581" style="zoom:67%;" />
       <img src="note_autoctrprac.assets/image-20251031210859785.png" alt="image-20251031210859785" style="zoom:67%;" />
       <img src="note_autoctrprac.assets/image-20251031210908735.png" alt="image-20251031210908735" style="zoom:67%;" />
       <img src="note_autoctrprac.assets/image-20251031210916351.png" alt="image-20251031210916351" style="zoom:67%;" />
       <img src="note_autoctrprac.assets/image-20251031210931983.png" alt="image-20251031210931983" style="zoom:67%;" />
       <img src="note_autoctrprac.assets/image-20251031210945029.png" alt="image-20251031210945029" style="zoom:67%;" />
     * 鉴幅型——单相
       <img src="note_autoctrprac.assets/image-20251031210954070.png" alt="image-20251031210954070" style="zoom:67%;" />
       <img src="note_autoctrprac.assets/image-20251031211002124.png" alt="image-20251031211002124" style="zoom:67%;" />
     * 鉴幅型——反正切法
       <img src="note_autoctrprac.assets/image-20251101090548762.png" alt="image-20251101090548762" style="zoom:50%;" />
   
4. 旋转变压器/感应同步器使用与注意事项

   * 感应同步器与旋转变压器的区别：
     <img src="note_autoctrprac.assets/image-20251103193310048.png" alt="image-20251103193310048" style="zoom: 50%;" />
   * 旋转变压器的主要技术参数
     <img src="note_autoctrprac.assets/image-20251103193404622.png" alt="image-20251103193404622" style="zoom:50%;" />
   * 旋转变压器优点/缺点
     <img src="note_autoctrprac.assets/image-20251103193437345.png" alt="image-20251103193437345" style="zoom:50%;" />
   * 感应同步器优点
     <img src="note_autoctrprac.assets/image-20251103193515916.png" alt="image-20251103193515916" style="zoom: 50%;" />
     <img src="note_autoctrprac.assets/image-20251103193526733.png" alt="image-20251103193526733" style="zoom:50%;" />
   * 感应同步器缺点
     <img src="note_autoctrprac.assets/image-20251103193538079.png" alt="image-20251103193538079" style="zoom:50%;" />
   * 感应同步器使用注意事项
     <img src="note_autoctrprac.assets/image-20251103193556440.png" alt="image-20251103193556440" style="zoom: 50%;" />

## 光电编码器与光栅

1. 位置编码器概述

   * 功能：转角编码器俗称码盘，用来测量转角并把它转换成脉冲或数字形式的输出信号
   * 分类
     * 根据输出信号的基本形式：增量式和绝对式
     * 根据结构和原理：光电式、电磁式

2. 增量式光电传感器

   * 结构（以单圈光栅、错位检测狭缝为例）
     <img src="note_autoctrprac.assets/image-20251103204140435.png" alt="image-20251103204140435" style="zoom:50%;" />

     * 码盘（旋转的，光源进去的第一个大圆盘）
       刻有均匀分布的辐射状窄缝，分布的周期称为节距L。透光的狭缝宽度为1/2L，不透光的也为1/2L。

     * 光阑板（固定的，透光后就是光敏元件）

       上面根据情况有不同狭缝。上面这种情况就是有两条形状和码盘上的一样的狭缝。A和B相狭缝的中心线相差1/4L，造成了输出相位相差90°

   * 工作原理

     * 概述：光电码盘由透明区和不透明区周期排列组成。光纤经过调制后被光电探测器接收，输出电流与透光面积的变化成正比。由于遮光床和光斑大小有线，透光比例随角度连续变化，因此输出信号呈正弦波形。
     * 单通道
       <img src="note_autoctrprac.assets/image-20251103214030404.png" alt="image-20251103214030404" style="zoom:50%;" />
     * 双通道（双圈光栅+独立检测）
       <img src="note_autoctrprac.assets/image-20251103214103892.png" alt="image-20251103214103892" style="zoom:50%;" />
     * 三通道
       <img src="note_autoctrprac.assets/image-20251103214128536.png" alt="image-20251103214128536" style="zoom:50%;" />

   * 信号处理

     微分装置将在信号上升沿产生脉冲，正传时，A相上升沿，B相为低电平；反转时，A相上升沿，B相为高电平。通过电平检测即可判断方向。
     <img src="note_autoctrprac.assets/image-20251103214424370.png" alt="image-20251103214424370" style="zoom:67%;" />

   * 寻零/位置控制
     关键点在于三通道中的Z脉冲。Z脉冲相当于一个昭示绝对位置的标志位。
     所谓寻零，则是寻找这个Z狭缝的位置。有两种情况，一种是直接转到遇到为止；第二种是两侧有限位器，需要先往一个方向转，再往另一个放旋转，直到遇到Z狭缝。
     <img src="note_autoctrprac.assets/image-20251103215153746.png" alt="image-20251103215153746" style="zoom:50%;" /><img src="note_autoctrprac.assets/image-20251103215159118.png" alt="image-20251103215159118" style="zoom:50%;" />

   * 分辨率与倍频电路

     * 未使用倍频技术前，分辨率取决于码盘的狭缝数量。
       <img src="note_autoctrprac.assets/image-20251103215225939.png" alt="image-20251103215225939" style="zoom: 67%;" />
     * 使用倍频技术后，在不增加码盘狭缝（物理实现难度大）情况下，通过增加判定条件，减小了步距角。 比如，原本只测量A的上升沿，采取了4细分技术后，分别有`A1B0,A1B1,A0B1,A0B0`四种情况，分辨率降低到原本的1/4。
       <img src="note_autoctrprac.assets/image-20251103220017044.png" alt="image-20251103220017044" style="zoom: 67%;" />

   * 优点/缺点
     <img src="note_autoctrprac.assets/image-20251103220046758.png" alt="image-20251103220046758" style="zoom:50%;" />

3. 绝对式光电编码器

   * 概述：绝对式脉冲编码盘是一种绝对角度位置检测装置，它的位置输出信号是某种制式的数码信号，它表示当前绝对位置信息。运行中用起点和终点的绝对位置，经运算后可得到位移量的大小。

   * 结构：旋转的码盘、光源和光电敏感元件。光学码道，每个码道上按一定规律分布着透明区和不透明区。

   * 原理

     * 基本原理：
       <img src="note_autoctrprac.assets/image-20251103220848946.png" alt="image-20251103220848946" style="zoom:50%;" />

     * 16位绝对式编码器 

       对每一个位置，给定一个唯一的编码，再用传感器去识别每个位置的编码，输出与之对应的唯一信号，用来表示特定的位置。
       四圈码盘，代表四位二进制数，总共有16个数值，因此每一圈有16个格子。
       <img src="note_autoctrprac.assets/image-20251103220914852.png" alt="image-20251103220914852" style="zoom:67%;" />

     * 编码方式

       * 码道布局：二进制码盘，每一个码道代表二进制的一位。
       * 分辨率：用N表示码盘的码道数目，即二进制位数，则角度分辨率位$\Delta \theta=360°/2^N$

       <img src="note_autoctrprac.assets/image-20251103221244425.png" alt="image-20251103221244425" style="zoom:50%;" />

       * 目前布局的隐患

         在交界处，由于工艺限制，多个码道并不是完全对齐，可能会存在某些位变化而某些位不变，得到的编码就会存在较大偏差。
         <img src="note_autoctrprac.assets/image-20251103221807263.png" alt="image-20251103221807263" style="zoom: 50%;" />

       * 解决方式——格雷码

         相邻代码间，只有一位数变化，大大减小了误读的风险。
         <img src="note_autoctrprac.assets/image-20251103221931830.png" alt="image-20251103221931830" style="zoom: 67%;" />
         <img src="note_autoctrprac.assets/image-20251103222554067.png" alt="image-20251103222554067" style="zoom:67%;" />
         <img src="note_autoctrprac.assets/image-20251103222801784.png" alt="image-20251103222801784" style="zoom:67%;" />

   * 绝对码盘的优缺点
     <img src="note_autoctrprac.assets/image-20251103222633824.png" alt="image-20251103222633824" style="zoom:50%;" />

4. 光栅

   * 概述
     * 作用：检测线位移和角位移，精度很高
     * 分类：
       * 直线光栅、圆光栅
       * 投射光栅、反射光栅
         <img src="note_autoctrprac.assets/image-20251103222937322.png" alt="image-20251103222937322" style="zoom: 67%;" />
   * 结构
     <img src="note_autoctrprac.assets/image-20251103223006916.png" alt="image-20251103223006916" style="zoom:67%;" />
   * 莫尔条纹
     
     光栅的关键原理，就是通过摩尔条纹，将微小的位移放大。整个场景就是两片光栅叠在一起，将短边a映射位长边W。
     <img src="note_autoctrprac.assets/image-20251103223446380.png" alt="image-20251103223446380" style="zoom:67%;" />
     
     将小位移a换成了大位移W
     <img src="note_autoctrprac.assets/image-20251103223501931.png" alt="image-20251103223501931" style="zoom:67%;" />
     
     例子如下：
     <img src="note_autoctrprac.assets/image-20251103223512477.png" alt="image-20251103223512477" style="zoom:67%;" />
     
     特性：
     <img src="note_autoctrprac.assets/image-20251103223525430.png" alt="image-20251103223525430" style="zoom:67%;" />
   * 光栅信号处理
     <img src="note_autoctrprac.assets/image-20251103223549624.png" alt="image-20251103223549624" style="zoom: 50%;" />
   * 光栅尺的优缺点
     <img src="note_autoctrprac.assets/image-20251103223555630.png" alt="image-20251103223555630" style="zoom:50%;" />

5. 转速测量

   * 概述：将脉冲个数变为速度
     <img src="note_autoctrprac.assets/image-20251103223813930.png" alt="image-20251103223813930" style="zoom:50%;" />
     
   * M法测速
     
     测量一定时间内的脉冲数目，但可能出现，刚好漏掉一个脉冲数目的情况。
     <img src="note_autoctrprac.assets/image-20251103223836537.png" alt="image-20251103223836537" style="zoom:50%;" />
     
     
     <img src="note_autoctrprac.assets/image-20251103224530643.png" alt="image-20251103224530643" style="zoom:50%;" /><img src="note_autoctrprac.assets/image-20251103224049070.png" alt="image-20251103224049070" style="zoom:50%;" />
     
   * T法测速
     测量两个脉冲相隔的时间T。在相邻的两个传感器脉冲内，不断产生高频时钟脉冲，记录高频时钟脉冲的数目，即可得到传感器脉冲时间T和时钟脉冲的关系，进而得到转速。
     <img src="note_autoctrprac.assets/image-20251103224120922.png" alt="image-20251103224120922" style="zoom:50%;" />
     但既然同样是记录脉冲数目，那么一样会面临和M法相同的问题，即刚好计数少了一个
     <img src="note_autoctrprac.assets/image-20251103224458677.png" alt="image-20251103224458677" style="zoom:50%;" />
   
   * M/T法测速
   
     记录的方法是，规定一个时间Tg，然后结束后检测下一个传感器脉冲的下降沿，从而得到整数倍的脉冲间隔，获得准确的$m_1$。配合T法记录的总体时间T，即可计算转速。
     <img src="note_autoctrprac.assets/image-20251103224656300.png" alt="image-20251103224656300" style="zoom:50%;" />
     误差来源于T，也就是T法记录的脉冲数目。
     <img src="note_autoctrprac.assets/image-20251103224934548.png" alt="image-20251103224934548" style="zoom:50%;" />
     <img src="note_autoctrprac.assets/image-20251103224949081.png" alt="image-20251103224949081" style="zoom:50%;" />
   
     * M/T方法通过设定测量速度的最小时间，保证了高速时的相对速率精度，通过限定低速时传感器的脉冲个数(至少1个)，保证了低速的速率精度，它综合M法和T法的优点，应用更为广泛。

## 交流电机的旋转磁场与感应电势

### 异步电机的概述与原理

<img src="note_autoctrprac.assets/image-20251106163834677.png" alt="image-20251106163834677" style="zoom:50%;" />
<img src="note_autoctrprac.assets/image-20251106163843470.png" alt="image-20251106163843470" style="zoom: 50%;" />

### 异步电动机结构

1. 感应电机定子
   * 结构
     <img src="note_autoctrprac.assets/image-20251106164441958.png" alt="image-20251106164441958" style="zoom:50%;" />
     <img src="note_autoctrprac.assets/image-20251106164451380.png" alt="image-20251106164451380" style="zoom:50%;" />
     <img src="note_autoctrprac.assets/image-20251106164457267.png" alt="image-20251106164457267" style="zoom:50%;" />
   * 绕组
     <img src="note_autoctrprac.assets/image-20251106164518036.png" alt="image-20251106164518036" style="zoom:50%;" />
2. 感应电机转子
   * 结构
     <img src="note_autoctrprac.assets/image-20251106164528887.png" alt="image-20251106164528887" style="zoom:50%;" />
   * 绕组
     * 笼型
     
       转子自成一体。
       <img src="note_autoctrprac.assets/image-20251106164606798.png" alt="image-20251106164606798" style="zoom:50%;" />
     * 绕线型
     
       可以在外部接入电阻等进行调节，但成本高。
       <img src="note_autoctrprac.assets/image-20251106164618305.png" alt="image-20251106164618305" style="zoom:50%;" />
3. 气隙
   <img src="note_autoctrprac.assets/image-20251106164639124.png" alt="image-20251106164639124" style="zoom:50%;" />

### 多相对称绕组产生的旋转磁场

1. 单相集中绕组的磁场

   * 假设
     <img src="note_autoctrprac.assets/image-20251106164955737.png" alt="image-20251106164955737" style="zoom:50%;" />

   * 磁动势建模

     根据安培环路定理与磁动势定义：
     <img src="note_autoctrprac.assets/image-20250905105757255.png" alt="image-20250905105757255" style="zoom: 33%;" />
     <img src="note_autoctrprac.assets/image-20250905105817199.png" alt="image-20250905105817199" style="zoom: 33%;" />

     我们可以以图中的磁力线为路径积分，应用安培环路定理，每条环路的磁动势都等于$W_x\;i$。由于忽略铁芯的磁压降，因此，磁动势认为**均分**在环路经过的两侧气隙中。定义从转子进入定子的磁势为正，从定子进入转子的磁势为负，**将气隙展开成直线**，即b图，纵轴为磁动势，那么磁动势的波形就是一个矩形波。由于电流是正弦交流电，因此矩形波的幅值也将随时间按照正弦规律变化。
     <img src="note_autoctrprac.assets/image-20251106165330947.png" alt="image-20251106165330947" style="zoom: 67%;" />

   * 代入电流式子到$F=\frac{W_x i}{2}$中，得到==**脉振磁动势**==，即“空间位置不变，幅值随时间变化”。这里，$-\frac{\pi}2\leq x\leq\frac{\pi}{2}$，已经表明了这里用的是**电角度**了！
     <img src="note_autoctrprac.assets/image-20251106170448575.png" alt="image-20251106170448575" style="zoom: 67%;" />
     <img src="note_autoctrprac.assets/image-20251106170857223.png" alt="image-20251106170857223" style="zoom:50%;" />

   * 多极的情况

     <img src="note_autoctrprac.assets/image-20251106170757782.png" alt="image-20251106170757782" style="zoom: 67%;" />

   * 对矩形波进行傅里叶变化，得到基本与i次谐波
     <img src="note_autoctrprac.assets/image-20251106170933435.png" alt="image-20251106170933435" style="zoom:50%;" />

2. 单相分布式绕组

   * 磁动势波形建模

     所谓分布式绕组，就是好多个相同方向的线圈紧挨着排布。由于空间位置想错，但每个线圈和前面分析过程都相同，因此，矩形波错位相加的结果就是一个阶梯形波。
     <img src="note_autoctrprac.assets/image-20251106171010306.png" alt="image-20251106171010306" style="zoom: 67%;" />

   * 分布式绕组合成磁动势

     以中间的线圈为基，分别列出三个线圈的基波磁动势，进行矢量合成。
     <img src="note_autoctrprac.assets/image-20251106172032164.png" alt="image-20251106172032164" style="zoom:50%;" />

     根据基波矢量关系，求出分布系数$k_{b1}$，进而列出合成磁动势最大值$A_1$
     <img src="note_autoctrprac.assets/image-20251106172136495.png" alt="image-20251106172136495" style="zoom: 67%;" />
     推广至谐波
     <img src="note_autoctrprac.assets/image-20251106172556085.png" alt="image-20251106172556085" style="zoom:50%;" />

   * 进行系数换算$W=pqW_x$，即单个线圈绕组和一相绕组匝数的换算
     <img src="note_autoctrprac.assets/image-20251106172721340.png" alt="image-20251106172721340" style="zoom:50%;" />
     ==谐波的幅值很小，线圈的磁动势可以用基波磁动势表示==

   * 对原本的基波磁动势式子进行一些化简，提出绕组系数$k$
     <img src="note_autoctrprac.assets/image-20251106172839560.png" alt="image-20251106172839560" style="zoom:50%;" />

   * 旋转磁动势与脉振磁动势的关系

     将原式利用三角函数积化和差公式，分为正向和负向正弦波。注意，这里只是对原本脉振磁动势的数学划分，不影响整体的空间不变性。
     <img src="note_autoctrprac.assets/image-20251106173038450.png" alt="image-20251106173038450" style="zoom: 67%;" />
     <img src="note_autoctrprac.assets/image-20251106173215661.png" alt="image-20251106173215661" style="zoom:67%;" />

   * 总结
     <img src="note_autoctrprac.assets/image-20251106173243454.png" alt="image-20251106173243454" style="zoom:67%;" />

3. 两相绕组合成磁场
   <img src="note_autoctrprac.assets/image-20251106195053365.png" alt="image-20251106195053365" style="zoom: 67%;" />
   <img src="note_autoctrprac.assets/image-20251106195119184.png" alt="image-20251106195119184" style="zoom:67%;" />
   <img src="note_autoctrprac.assets/image-20251106195340183.png" alt="image-20251106195340183" style="zoom:67%;" />
   <img src="note_autoctrprac.assets/image-20251106200649695.png" alt="image-20251106200649695" style="zoom:67%;" />
   <img src="note_autoctrprac.assets/image-20251106200702829.png" alt="image-20251106200702829" style="zoom:67%;" />

4. 三相绕组合成磁场
   <img src="note_autoctrprac.assets/image-20251106200737721.png" alt="image-20251106200737721" style="zoom:67%;" />
   <img src="note_autoctrprac.assets/image-20251106201039735.png" alt="image-20251106201039735" style="zoom:67%;" />
   <img src="note_autoctrprac.assets/image-20251106201057827.png" alt="image-20251106201057827" style="zoom:67%;" />
   <img src="note_autoctrprac.assets/image-20251106201129500.png" alt="image-20251106201129500" style="zoom:67%;" />
   前面是正序电流，三个反向抵消，三相合称为正向推移的圆形磁场。
   现在通入负序电流，三个正向抵消，三相合成为反向推移的圆形磁场。
   <img src="note_autoctrprac.assets/image-20251106201257340.png" alt="image-20251106201257340" style="zoom:67%;" />

### 正弦磁场下交流绕组的磁感应电势

1. 前述
   * 旋转磁场类型
     <img src="note_autoctrprac.assets/image-20251106202002922.png" alt="image-20251106202002922" style="zoom:50%;" />
   * 只要电机气隙中有旋转磁场，则异步电机定转子绕组中的磁通会发生变化，这个变化的磁通必然在定转子绕组中产生感应电势。
2. 推导
   * 磁密$B$表达式
     <img src="note_autoctrprac.assets/image-20251106202745412.png" alt="image-20251106202745412" style="zoom:50%;" />
   * 磁场运动的线速度
     <img src="note_autoctrprac.assets/image-20251106203319152.png" alt="image-20251106203319152" style="zoom: 67%;" />
   * 求单根导线的感应电动势E=Blv
     <img src="note_autoctrprac.assets/image-20251106203331285.png" alt="image-20251106203331285" style="zoom:67%;" />
     <img src="note_autoctrprac.assets/image-20251106203445427.png" alt="image-20251106203445427" style="zoom:50%;" />
   * 整距线圈的电动势
     <img src="note_autoctrprac.assets/image-20251106203601359.png" alt="image-20251106203601359" style="zoom:67%;" />
   * 感应电动势的相位与磁密相差90°，源于法拉第电磁感应定律
     <img src="note_autoctrprac.assets/image-20251106204606753.png" alt="image-20251106204606753" style="zoom:67%;" />
   * 分布绕组与短距绕组对感应电势的影响
     <img src="note_autoctrprac.assets/image-20251106204634321.png" alt="image-20251106204634321" style="zoom:67%;" />
   * 相电动势
     <img src="note_autoctrprac.assets/image-20251106204655553.png" alt="image-20251106204655553" style="zoom:50%;" />

## 异步电机的运行分析与等效电路

### 异步电机的运行分析

1. 转差率$s=\frac{n_s-n}{n_s}$
   <img src="note_autoctrprac.assets/image-20251111083542296.png" alt="image-20251111083542296" style="zoom:50%;" />
2. 电动机运行状态分析
   * $n<n_s$，电动机
     <img src="note_autoctrprac.assets/image-20251111083624811.png" alt="image-20251111083624811" style="zoom:50%;" />
   * 发电机
     <img src="note_autoctrprac.assets/image-20251111083640307.png" alt="image-20251111083640307" style="zoom:50%;" />
   * 电磁制动
     <img src="note_autoctrprac.assets/image-20251111083653766.png" alt="image-20251111083653766" style="zoom:50%;" />
   * 总结
     <img src="note_autoctrprac.assets/image-20251111083708216.png" alt="image-20251111083708216" style="zoom:50%;" />

### 异步电机的等效电路

1. 结论

   异步电机等效电路图
   <img src="note_autoctrprac.assets/image-20251111111227955.png" alt="image-20251111111227955" style="zoom: 67%;" />

   基本方程
   <img src="note_autoctrprac.assets/image-20251111111300172.png" alt="image-20251111111300172" style="zoom:50%;" />

2. 推导过程

   * 核心问题：

     * 定子转子频率不同——频率归算
     * 电路不直连，感应电动势不相等——电压归算

   * 简化模型（定子侧）

     * 原本：电路分为两个主体，即定子和转子。先分析空载装填，专门分析定子侧。
     * 空载运行的定义：核心在于，无负载情况下，$n \approx n_s$，转子转速近似为与定子磁场同速
       <img src="note_autoctrprac.assets/image-20251111112410327.png" alt="image-20251111112410327" style="zoom:50%;" />
     * 定子侧分为：定子绕组自身的电阻和漏感、产生主磁场的励磁支路
       * 背景：漏磁通、主磁通
         <img src="note_autoctrprac.assets/image-20251111112839034.png" alt="image-20251111112839034" style="zoom:50%;" />
         <img src="note_autoctrprac.assets/image-20251111112851248.png" alt="image-20251111112851248" style="zoom:50%;" />
       * 励磁支路：主磁通、励磁电抗、励磁电阻等
         <img src="note_autoctrprac.assets/image-20251111112921191.png" alt="image-20251111112921191" style="zoom:67%;" />
       * 漏电势：漏磁通
         <img src="note_autoctrprac.assets/image-20251111113002624.png" alt="image-20251111113002624" style="zoom:50%;" />
       * 定子电压方程
         <img src="note_autoctrprac.assets/image-20251111113026677.png" alt="image-20251111113026677" style="zoom:50%;" />
     * 空载时的特点：**感应电机中，若外施电压一定，主磁通赋值基本为定值。**
       <img src="note_autoctrprac.assets/image-20251111113059844.png" alt="image-20251111113059844" style="zoom: 67%;" />

   * 转子侧电路分析：有负债

     * 转子感应电动势的频率$f_2=sf_1$

       感应电动势的频率取决于相对于磁场的切割磁场的频率，对于转子来说，磁场由定子产生，转速为$n_s$，而转子自身的转速为$n$，因而，这里$f_2=\frac{p(n_s-n)}{60}$。
       <img src="note_autoctrprac.assets/image-20251111125147814.png" alt="image-20251111125147814" style="zoom: 67%;" />

     * 转子旋转的磁动势

       **无论转子转速为多少，定、转子磁动势在空间上保持相对静止**
       <img src="note_autoctrprac.assets/image-20251111125757901.png" alt="image-20251111125757901" style="zoom:50%;" />

     * 转子磁动势的赋值
       <img src="note_autoctrprac.assets/image-20251111150142641.png" alt="image-20251111150142641" style="zoom:50%;" />

     * **磁势平衡方程**
       <img src="note_autoctrprac.assets/image-20251111150154393.png" alt="image-20251111150154393" style="zoom:50%;" />

     * 有负载时的电磁关系
       <img src="note_autoctrprac.assets/image-20251111150701223.png" alt="image-20251111150701223" style="zoom:50%;" />

     *  初始的定转子耦合模型
       <img src="note_autoctrprac.assets/image-20251111150905721.png" alt="image-20251111150905721" style="zoom:50%;" />

     * 定义转子电路真实参数，定义了转子静止时的值作为系数，比如$E_2,x_2$，真实的是下标带s的。静止时，转子的频率$f_2=n_s-0=f_1$
       <img src="note_autoctrprac.assets/image-20251111150928651.png" alt="image-20251111150928651" style="zoom:50%;" />

       <img src="note_autoctrprac.assets/image-20251111150937665.png" alt="image-20251111150937665" style="zoom:50%;" />
       <img src="note_autoctrprac.assets/image-20251111150952273.png" alt="image-20251111150952273" style="zoom:50%;" />

     * 频率归算：$I_2、E_2$是$f_2=f_1$情况下的电势和电流
       <img src="note_autoctrprac.assets/image-20251111151438463.png" alt="image-20251111151438463" style="zoom:50%;" />
       理论依据：转子通过磁动势来影响定子，而磁动势$F_2$始终与F1保持相对静止，F2本身与真实的$f_2$无关，只需要保持转子电流大小和转子阻抗角两个参数不变，那么转子就可以进行上述等效

       这里则验证了这两个参数的不变性，因此等效成立。虚拟的转子侧和真实的转子侧对于定子的影响相同。
       <img src="note_autoctrprac.assets/image-20251111152433330.png" alt="image-20251111152433330" style="zoom: 67%;" />

     * 频率归算后的转子电阻
       <img src="note_autoctrprac.assets/image-20251111152537801.png" alt="image-20251111152537801" style="zoom:50%;" />

     * 频率归算后的电路图
       <img src="note_autoctrprac.assets/image-20251111152555873.png" alt="image-20251111152555873" style="zoom:50%;" />

     * 由于转子和定子的感应电动势不同，想要将他们合并到一个电路上，还需要进行类似变压器的归算的处理
       <img src="note_autoctrprac.assets/image-20251111152706488.png" alt="image-20251111152706488" style="zoom:50%;" />
       <img src="note_autoctrprac.assets/image-20251111152721942.png" alt="image-20251111152721942" style="zoom:50%;" />
       <img src="note_autoctrprac.assets/image-20251111152728123.png" alt="image-20251111152728123" style="zoom: 50%;" />
       <img src="note_autoctrprac.assets/image-20251111152738330.png" alt="image-20251111152738330" style="zoom:50%;" />

     * 归算结果，推导完毕
       <img src="note_autoctrprac.assets/image-20251111152758843.png" alt="image-20251111152758843" style="zoom:50%;" />
       <img src="note_autoctrprac.assets/image-20251111152807490.png" alt="image-20251111152807490" style="zoom:50%;" />

3. 等效电路运行情况分析
   <img src="note_autoctrprac.assets/image-20251111152853441.png" alt="image-20251111152853441" style="zoom:50%;" />

## 异步电机的机械特性和调速运动

### 异步电机的功率传输关系

1. 概述
   <img src="note_autoctrprac.assets/image-20251111153453723.png" alt="image-20251111153453723" style="zoom:50%;" />
   <img src="note_autoctrprac.assets/image-20251111153519494.png" alt="image-20251111153519494" style="zoom:50%;" />
2. 各功率分析
   * 输入功率
     <img src="note_autoctrprac.assets/image-20251111153609231.png" alt="image-20251111153609231" style="zoom:50%;" />
     <img src="note_autoctrprac.assets/image-20251111153630937.png" alt="image-20251111153630937" style="zoom:50%;" />
   * 电磁功率
     <img src="note_autoctrprac.assets/image-20251111153637933.png" alt="image-20251111153637933" style="zoom:50%;" />
   * 转轴上的机械功率
     <img src="note_autoctrprac.assets/image-20251111153729248.png" alt="image-20251111153729248" style="zoom:50%;" />
   * 输出功率
     <img src="note_autoctrprac.assets/image-20251111153741286.png" alt="image-20251111153741286" style="zoom:50%;" />
3. 转矩方程---由功率推出
   <img src="note_autoctrprac.assets/image-20251111153822558.png" alt="image-20251111153822558" style="zoom:50%;" />
4. 额定功率等概念
   <img src="note_autoctrprac.assets/image-20251111154201595.png" alt="image-20251111154201595" style="zoom:50%;" /><img src="note_autoctrprac.assets/image-20251111154132599.png" alt="image-20251111154132599" style="zoom:50%;" />
   <img src="note_autoctrprac.assets/image-20251111154224995.png" alt="image-20251111154224995" style="zoom:50%;" />
   <img src="note_autoctrprac.assets/image-20251111154237143.png" alt="image-20251111154237143" style="zoom:50%;" />
   <img src="note_autoctrprac.assets/image-20251111154244810.png" alt="image-20251111154244810" style="zoom:50%;" />

### 异步电机的机械特性

<img src="note_autoctrprac.assets/image-20251111154316714.png" alt="image-20251111154316714" style="zoom:50%;" />
<img src="note_autoctrprac.assets/image-20251111154330920.png" alt="image-20251111154330920" style="zoom: 50%;" />
<img src="note_autoctrprac.assets/image-20251111154339741.png" alt="image-20251111154339741" style="zoom:50%;" />
<img src="note_autoctrprac.assets/image-20251111154346766.png" alt="image-20251111154346766" style="zoom:50%;" />
<img src="note_autoctrprac.assets/image-20251111154353518.png" alt="image-20251111154353518" style="zoom:50%;" />
<img src="note_autoctrprac.assets/image-20251111154401445.png" alt="image-20251111154401445" style="zoom:50%;" />
<img src="note_autoctrprac.assets/image-20251111154410151.png" alt="image-20251111154410151" style="zoom:50%;" />

### 异步电动机的调速控制

1. 概述
   <img src="note_autoctrprac.assets/image-20251117192722298.png" alt="image-20251117192722298" style="zoom:50%;" />

2. 变频调速
   <img src="note_autoctrprac.assets/image-20251117193523986.png" alt="image-20251117193523986" style="zoom:50%;" />

   * 恒压频比控制
     <img src="note_autoctrprac.assets/image-20251117194403448.png" alt="image-20251117194403448" style="zoom:67%;" />

     * 基频以下
       <img src="note_autoctrprac.assets/image-20251117194422453.png" alt="image-20251117194422453" style="zoom:50%;" />

       基频以下，频率较高时，电机转矩不变。频率过小时，定子电阻不可忽略，线性关系被打破，需要适当提高U1以进行补偿
       <img src="note_autoctrprac.assets/image-20251117194431985.png" alt="image-20251117194431985" style="zoom:50%;" />
       <img src="note_autoctrprac.assets/image-20251117194443401.png" alt="image-20251117194443401" style="zoom:50%;" />

     * 基频以上
       <img src="note_autoctrprac.assets/image-20251117194505698.png" alt="image-20251117194505698" style="zoom:50%;" />
       <img src="note_autoctrprac.assets/image-20251117194515996.png" alt="image-20251117194515996" style="zoom:50%;" />
       <img src="note_autoctrprac.assets/image-20251117194539846.png" alt="image-20251117194539846" style="zoom:50%;" />

3. <img src="note_autoctrprac.assets/image-20251117194555715.png" alt="image-20251117194555715" style="zoom:50%;" />

### 单相异步电动机

1. 单相异步电动机本身的特性和局限性
   <img src="note_autoctrprac.assets/image-20251117200058772.png" alt="image-20251117200058772" style="zoom:50%;" />
   <img src="note_autoctrprac.assets/image-20251117200111446.png" alt="image-20251117200111446" style="zoom:50%;" />
2. 获取启动转矩的方式
   * 电容分相式
     <img src="note_autoctrprac.assets/image-20251117200146595.png" alt="image-20251117200146595" style="zoom: 50%;" />
     <img src="note_autoctrprac.assets/image-20251117200153956.png" alt="image-20251117200153956" style="zoom:50%;" />
     <img src="note_autoctrprac.assets/image-20251117200212546.png" alt="image-20251117200212546" style="zoom:50%;" />
   * 电阻式分相异步电动机
     <img src="note_autoctrprac.assets/image-20251117200229589.png" alt="image-20251117200229589" style="zoom:50%;" />
   * 罩极式单相异步电机
     <img src="note_autoctrprac.assets/image-20251117200256873.png" alt="image-20251117200256873" style="zoom:50%;" />

## 附录

1. 交流电路分析
   
      * 电抗/感抗：$X_L=\omega L$
        容抗：$X_C=\frac{-1}{\omega C}$
      
        阻抗：$Z=R+j(X_L+X_C)$
      
      * $\frac U I = |Z|$
        $\psi_u-\psi_i=\psi$
        $\frac{\dot{U}}{\dot{I}}=\dot Z$
      
2. 电机总结分析

      > 本质：磁场中的磁性体受力而运动。
      >
      > 明确两个要素：
      >
      > * 谁产生磁场？
      > * 谁处于磁场中受力？
      >
      > 确定两个因素：
      >
      > * 磁场的空间与时间的分布
      > * 磁体或磁化铁心在磁场中的位置与运动规律

      * 有刷直流电机
        * 谁产生磁场：由固定的永磁体产生磁场或者由励磁线圈通电产生，磁场本身是静止的
        * 谁在磁场中运动：绕有线圈的电磁铁，通电后产生自身磁场
        * 如何控制相互作用：通过换向器（电刷），当转子转动到某个角度，自动切换转子线圈中的电流方向，使得转子的磁场的方向相对于定子磁场始终保持一个能产生转矩的角度。
      * 步进电机
        * 谁产生磁场：定子上有很多齿和线圈，通过外部控制器供电，产生一个位置可控的磁场
        * 谁在磁场中运动：转子通常是永磁体或带齿的铁芯
        * 如何控制相互作用：控制是**外部的、数字的、开环的**。控制器按特定顺序依次给不同的定子线圈通电，定子磁场的方向会“一步一步”地改变。转子磁体为了与定子磁场对齐，就会跟着“一步一步”地转动。它通过精确控制定子磁场的**空间位置**来实现角度控制。
      * 无刷直流电机BLDC
        * 谁产生磁场：定子是电磁铁。
        * 谁在磁场中运动：转子是永磁体。
        * 如何控制相互作用：这是它与有刷电机的核心区别。它抛弃了机械换向器，改用**电子换向**。通过霍尔传感器等元件检测转子的大致位置（例如，在哪一个60°扇区内），然后控制器给对应的定子线圈通电，产生一个领先于转子磁场的磁场，拉着转子转动。这种控制是**外部的、电子的、分步的（六步换相法）**。
      * 交流伺服电机PMSM
        * 谁产生磁场：定子是电磁铁。
        * 谁在磁场中运动：转子是永磁体。
        * 如何控制相互作用：FOC。编码器可以实时、精确地知道转子磁场的**确切角度**。控制器不再是简单的“开/关”线圈，而是通过计算，向三相线圈中注入**平滑的正弦波电流**。这三相正弦电流合成的定子磁场是一个**平滑旋转的矢量**，FOC算法的核心任务就是**始终让这个定子磁场矢量精确地领先转子磁场矢量90°**。这个90°角是产生最大转矩的理想角度。

3. 步进电机和BLDC、PMSM的区别

      * 三者的结构、运行原理都类似。均属于无刷电机
      * 区分点：
        * 步进电机是开环控制，其目的就是让转子到达某个位置，并不需要霍尔传感器去测量其位置。
        * BLDC分为普通BLDC和伺服方波BLDC，两者都是两极三相结构，六步控制方式。前者使用霍尔编码器来定位然后粗暴换相，后者较前者加入了伺服系统和编码器等，可以更精细控制换相和电流大小。
          BLDC和步进电机区别：BLDC需要测量转子位置，而步进电机不需要。因而BLDC更适合连续运动，而步进电机适合定位（只要够快，也可以近似连续运动，但效果不好）。
        * PMSM的三相电流是交流电，是FOC控制，是最精确的控制方式。
      * 应用场景
        * 步进电机控制简单，且在静止状态下有着较强的保持转矩。成本低。但不适用于精密的控制。
        * PMSM和BLDC都可以实现转子位置的控制，在这点上和步进电机类似，但其更重要的能力是让转子能够稳定的旋转，输出转矩。位置环只是其中最高层的应用。为了维持一个位置，控制器需要不断微调，控制较为复杂。

