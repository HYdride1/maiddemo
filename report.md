## 实验报告

221900110 黄扬昊 221900110@smail.nju.edu.cn

### 指令选择

在实验三中我选择了线性IR，这里指令选择就是直接将其对应到MIPS代码

### 寄存器选择

我采用了朴素的寄存器分配算法

寄存器分为两类：

- `$t0-$t7`：用于临时存储中间计算结果。
- `$s0-$s7`：用于长期保存变量值。

优先分配空闲寄存器，当寄存器不足时，从内存加载/保存变量。

### 栈管理

每个局部变量在函数栈帧中分配固定的偏移量，使用`fp`指针定位。

每次调用新函数时，使用`sp`和`fp`创建新的栈帧。
