## Practice 2(15)

**Object-oriented Programming**：The  vapor-compression refrigeration cycle simulator 

Apply `computational thinking` to model and solve the industrial system problems

**Deadline:**  2021.05.24

## Contents and Requirements

以[SimVCCE](https://github.com/PySEE/SimVCCE)中的Python语言版本为基础，编写代码，使其可计算如下2个循环：

* Thuan Ke Nguyen, [CHE 302 Chemical and Materials Engineering Thermodynamics I: chap7-2](https://www.cpp.edu/~tknguyen/che302/Notes/chap7-2.pdf)

### 1. Example 7.2-5 Page4 

Refrigerant 134a is the working fluid in an ideal vapor-compression refrigeration cycle that communicates thermally with

* a cold region at -10°C 

* Saturated vapor enters the compressor at -10°C 

* liquid leaves the condenser at 0.9MPa and 30°C 

* The compressor has **an efficiency of 80%** 

* The mass flow rate of the refrigerant is 0.08kg/s 

**Determine**

 * the compressor power, in kW
 
 * the refrigeration capacity, in tons
 
 * the coefficient of performance

### 2 Modified Example 7.2-5 Page4 

Refrigerant 134a is the working fluid in an ideal vapor-compression refrigeration cycle that communicates thermally with

* a cold region at -10°C 

* Saturated vapor enters the compressor at -10°C and **Superheated vapor leaves the compressor at 50°C** 

* liquid leaves the condenser at 0.9MPa and 30°C

* The mass flow rate of the refrigerant is 0.08kg/s

**Determine**

* **the efficiency of compressor, in %** 

* the compressor power, in kW
 
* the refrigeration capacity, in tons
 
* the coefficient of performance

 ![](img/example725.jpg) 

### 练习提示

[SimVCCE](https://github.com/PySEE/SimVCCE) 示例中压缩机类的压缩过程是等熵过程，练习中的循环不是等熵过程。

程序要处理：等熵过程、不同已知参数的不可逆非等熵过程，练习需做以下编码工作：

1. compressor压缩机类模块修改：属性、计算及输出

   * 循环Example 7.2-5：已知`压缩机效率`
 
   * 修改了已知参数的循环Example 7.2-5：已知`压缩机出口温度`，计算`压缩机效率`

2. 循环数据Python模块

   * `设备`和`端口连接器`字典

3. 其他修改和完善

**建议工作步骤**，

* 首先，分析 **循环Example 7.2-5**，修改代码，实现其计算

* 进一步，分析 **修改了已知参数的循环Example 7.2-5**，修改代码，实现其计算

### Python源码(6)

* 循环数据Python模块(2)

* 设备类(4)

### 软件设计工作Markdown文档(9)

* 设计任务简要描述

* 设计方案简要描述
  * 端口、设备、端口连接关系和循环输入数据变量的数据结构
  * 端口、设备、连接器、循环分析类
  * 端口连接、连接节点物性和循环计算等算法(主要算法、循环分析流程图)
  
* 练习中遇到的问题及解决过程 
  
* 工作小结：从练习工作相关的以下2个方面做小结
   * 对工业过程仿真软件市场及开发现状的思考？
   * 如果基于练习代码，研究问题求解的数据结构和算法，进而开发更通用的循环分析软件，是什么开发模式？ 对软件项目中如何使用开发模式的思考？

**文档提示** ：

* 数学公式可使用：`LaTex` ( 在VS Code中**需**[Markdown Preview Enhanced](https://shd101wyy.github.io/markdown-preview-enhanced/#/zh-cn/)插件支持显示)

>* LaTex数学公式: $z=\frac{x}{y}$

* 流程图: Microsoft Visio 或者 [Markdown Preview Enhanced支持的图像类型](https://shd101wyy.github.io/markdown-preview-enhanced/#/zh-cn/diagrams),如：[flowchart](https://flowchart.js.org/

flowchart常用的元素：
```
start
end
operation
condition
inputoutput
subroutine
```
示例：

```flow
start=>start: 开始
loginInfo=>inputoutput: 登录数据
verifyLogin=>subroutine: 登录验证
isSuccess=>condition: 验证成功？
respondSuccess=>operation: 响应成功
responseFailure=>operation: 响应失败
end=>end: 结束

start->loginInfo->verifyLogin->isSuccess
isSuccess(yes)->respondSuccess->end
isSuccess(no)->responseFailure->end
```

## 建议工作目录

```txt
 
|── <P2>
     │ 
     │── README.md: 软件设计工作Markdown文档
     | 
     |── <img> Markdown文档使用的图形文件
     |
     |── vccapp.py
     |
     |── <components> 
     |        
     |── <vccmodel> 
     |
     |── <vcc> 
     |
     |── <result> 计算结果数据文件 
```  

## 提交：

* 电邮： cmh@seu.edu.cn
  * 主题：学号-姓名-2
  * 附件：工作目录压缩文件： **学号-姓名-2.zip**； 其中，必须有**计算结果文件**

* 截至时间：2021.05.24
  * 截至时间后可补交，补交得分<=9. (2021.06.21)


