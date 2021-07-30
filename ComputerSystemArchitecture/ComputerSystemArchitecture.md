# 计算机系统结构

## 第1章 计算机系统结构

* 多级层次结构：微程序→机器语言→操作系统→汇编语言→高级语言→应用语言
* 定义：
  * 经典定义：计算机属性
  * 广义定义：指令集结构、组成、硬件
  * 实质：软硬件界面
* 计算机组成和计算机实现
* 分类：
  * Flynn分类法：最大并行度
  * 冯氏分类法：指令流和数据流的多倍性
* 4个定量原理：
  * 经常性事件
  * Amdahl定律
  * CPU性能公式
  * 程序的局部性原理
* 计算机系统结构的发展：
  * 冯·诺依曼结构
  * 软件兼容
  * 模拟和仿真
* 并行性：
  * 并行性等级：
    * 处理数据角度：
      * 字串位串
      * 字串位并
      * 字并位串
      * 字并位并
    * 执行程序角度：
      * 指令内部并行
      * 指令级并行
      * 线程级并行
      * 任务级或过程级并行
      * 作业或程序级并行
  * 提高并行性：
    * 时间重叠：部件功能专用化
    * 资源重复
    * 资源共享

---

## 第2章 计算机指令集结构

* 指令集结构的分类：
  * 堆栈
  * 累加器
  * 通用寄存器组：
    * 操作数个数
    * 存储器操作数的个数
* 寻址方式：
  * 立即数寻址方式
  * ...
  * 偏移寻址方式
* 指令集结构的功能设计：
  * 对指令集的基本要求：
    * 完整性
    * 规整性：对称性，均匀性
    * 高效率
    * 兼容性 
  * CISC：强化指令功能，减少程序的指令条数，以达到提高性能的目的
  * RISC：
    * 指令条数少而简单
    * 采用简单而又统一的指令格式，并减少寻址方式
    * 指令的执行在单个机器周期内完成
    * 只有load和store指令才能访问存储器
    * 大多数指令都采用硬连逻辑来实现
    * 强调优化编译器的作用
    * 充分利用流水技术来提高性能
* 操作数的类型和大小：
  * 表示操作数类型的方法：
    * 由操作码指定
    * 由数据本身给出
* 指令格式的设计：
  * 操作码的编码：
    * Huffman编码法
    * 固定长度的操作码
  * 指令集编码格式：
    * 变长编码格式
    * 定长编码格式
    * 混合型编码格式

---

## 第3章 流水线技术

* 流水线：
  * 概念：
    * 把一个重复的过程分解为若干个子过程，每个子过程由专门的功能部件来实现。
    * 把多个处理过程在时间上错开，依次通过各功能段，这样，每个子过程就可以与其他的子过程并行进行。
  * 特点：
    * 流水线瓶颈
    * 流水寄存器：每一个功能部件的后面的缓冲寄存器
    * 通过时间和排空时间
  * 分类：
    * 单功能流水线与多功能流水线
    * 静态流水线与动态流水线
    * 部件级、处理机级及处理机间流水线
    * 线性流水线与非线性流水线
    * 顺序流水线与乱序流水线
    * 标量处理机与向量流水处理机 
  * 性能：
    * 吞吐率：
      * 实际吞吐率
      * 最大吞吐率
    * 解决流水线瓶颈：
      * 细分瓶颈段
      * 重复设置瓶颈段
    * 加速比
    * 效率
* 流水线的相关与冲突：
  * 相关：两条指令之间存在某种依赖关系
    * 数据相关：写后读
    * 名相关：
      * 反相关：读后写
      * 输出相关：写后写
    * 控制相关
  * 流水线冲突：由于相关的存在，使得指令流中的下一条指令不能在指定的时钟周期执行
    * 结构冲突：资源不够
    * 数据冲突：读/写操作数的顺序与非流水实现不同
      * 类型：
        * 写后读冲突
        * 读后写冲突
        * 写后写冲突
      * 解决：
        * 定向技术
        * 指令调度
    * 控制冲突：
      * 减少分支延迟：
        * 预测分支失败 
        * 预测分支成功 
        * 延迟分支：
          * 延迟槽
          * 三种调度方法

---

## 第4章 指令级并行

* **指令级并行：**
  * **单流出：**减少流水线停顿
    * 数据相关：
      * 静态调度
      * 动态调度：
        * 乱序执行，引入RAW和WAW冲突(名相关)
        * Tomasulo算法：
          * 硬件：
            * 保留站
            * 公共数据总线(CDB)
          * 3段流水线：
            * 流出
            * 执行
            * 写结果
    * 控制相关：
      * 静态分支预测
      * 动态分支预测：
        * 分支历史表(BHT)：保存历史预测情况
        * 分支目标缓冲器(BTB)：保存历史预测情况和跳转目标地址
        * 基于硬件的前瞻执行(ROB)：
          * 前瞻执行，结果放在ROB中
          * 预测成功才确认，乱序执行，顺序确认
  * **多流出：**
    * 超标量：流出指令数不固定
    * 超长指令字VLIW：多指令构成长指令
  * **循环级并行：**
    * 循环展开和指令调度
    * 循环体代码复制多次，循序排列，调整循环结束条件

---

## 第5章 存储系统

### 存储系统

* **三个指标：**
  * 容量大
  * 速度块
  * 价格低
* **多级存储层次结构：**
  * 原理：程序访问的局部性原理
    * 时间局部性
    * 空间局部性
  * 三级存储系统：
    * Cache，主存，辅存
    * Cache——主存：弥补主存速度不足
    * 主存——辅存：弥补主存容量不足
* **存储器性能参数：**
  * 存储容量
  * 单位价格
  * 命中率和不命中率
  * 平均访问时间：
    * 命中时间
    * 不命中时间
* **存储层次四个问题：**
  * 映像规则：调入高一层存储器
  * 查找算法：在高一层存储器查找
  * 替换算法：不命中
  * 写策略：写访问

---

### Cache

* **Cache：**
  * 地址：分块管理，块地址+块内位移
  * **映像规则：**
    * 全相联映像：空间利用率最高，冲突概率最低，实现最复杂
    * 直接映像：空间利用率最低，冲突概率最高，实现最简单
    * 组相联映像：直接映像和全相联的一种折中
  * **查找算法：**
    * 查找目录表：主存块的块地址高位部分作为标识
    * "主存→Cache"地址变换和访问Cache同时进行，读出所有候选位置再比较
    * 并行查找：
      * 相联存储器：读出一组，按内容查找，标识相联比较
      * 单体多字存储器+比较器
  * **替换算法：**
    * 随机法：
      * 实现简单
    * 先进先出法FIFO
    * 最近最少使用法LRU：
      * 实际选择最久没有被访问过的块
      * 不命中率低
      * 实现：
        * 堆栈法
        * 比较对法
  * **写策略：**
    * 写命中策略：
      * 写直达法：同时写入Cache和主存
      * 写回法：只写入Cache，替换时写入主存
    * 写不命中调块：
      * 按写分配(写时取)
      * 不按写分配(绕写法)
    * 两种结合：
      * 写回法 ── 按写分配
      * 写直达法 ── 不按写分配
  * Cache性能：
    * 不命中率
    * 平均访存时间
    * 程序执行时间
* **提高Cache性能：**
  * **降低不命中率(8)：**
    * 增加Cache块大小：
      * 减少强制性不命中
      * 增加冲突不命中
      * 增加不命中开销
    * 增加Cache容量：
      * 减少容量不命中
      * 增加命中时间
    * 提高相联度：
      * 减少冲突不命中
      * 增加命中时间
    * 伪相联Cache：
      * 命中时间小
      * 不命中率低
    * 预取：减少强制性不命中
      * 硬件预取
      * 编译器控制的预取
    * 编译器优化
    * "牺牲"Cache：全相联的小Cache用于存放被替换出去的块
      * 减少冲突不命中
  * **减少不命中开销(5)：**
    * 两级Cache：
      * 第一级Cache：小而快
      * 第二级Cache：
        * 容量大
        * 较高的相联度或伪相联
        * 较大的块
    * 让读不命中优先于写
    * 写缓冲合并
    * 请求字处理技术：
      * 尽早重启动
      * 请求字优先
    * 非阻塞Cache技术：不命中下命中
  * **减少命中时间(4)**：
    * 容量小、结构简单的Cache
    * 虚拟Cache：
      * 虚拟索引＋虚拟标识
      * 虚拟索引＋物理标识
    * Cache访问流水化
    * 踪迹Cache

---

### 并行主存

* 单体多字存储器：
  * 实现简单
  * 访存效率不高 
* 多体交叉存储器：
  * 高位交叉编址：对存储单元矩阵按列优先进行编址，同体高位相同
  * 低位交叉编址：对存储单元矩阵按行优先进行编址，同体低位相同

---

### 虚拟存储器

* 分类：
  * 页式
  * 段式
* 快速地址转换技术：
  * 地址变换缓冲器TLB(快表)
  * 标识：虚地址的一部分
  * 数据：物理页帧号、有效位、存储保护信息、使用位、修改位等

---

## 第6章 输入/输出系统

* 系统响应时间：
  * I/O响应时间
  * CPU处理时间
* I/O性能：
  * 连接特性
  * 容量
  * 响应时间和吞吐率
* 可靠性：系统从某个初始参考点开始一直连续提供服务的能力
  * 平均无故障时间MTTF
* 可用性：系统正常工作的时间在连续两次正常服务间隔时间中所占的比率
  * MTTF+MTTR：平均失效间隔时间MTBF
* 可信性：服务的质量
* 磁盘冗余阵列RAID：
  * 数据交叉存放的粒度：
    * 细粒度磁盘阵列
    * 粗粒度磁盘阵列
  * 分级：
    * RAID0：非冗余阵列
    * RAID1：镜像盘
    * RAID2：存储器式的磁盘阵列(汉明纠错码)
    * RAID3：位交叉奇偶校验盘阵列
    * RAID4：块交叉奇偶校验磁盘阵列
    * RAID5：块交叉分布奇偶校验磁盘阵列
    * RAID6：P＋Q双校验磁盘阵列
    * RAID10与RAID01
* 总线：
  * 分离事务总线：总线事务分成请求和应答
  * 同步总线
  * 异步总线
  * 编址：
    * 统一编址
    * 独立编址：专用I/O指令
* I/O方式：
  * 程序查询
  * 中断
  * DMA
  * 通道处理机：
    * 4级层次结构I/O：CPU、通道、设备控制器、外设
    * 种类：
      * 字节多路通道
      * 选择通道
      * 数组多路通道