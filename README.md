<p align="center">
 <img width="100px" src="https://raw.githubusercontent.com/NekoSilverFox/NekoSilverfox/403ab045b7d9adeaaf8186c451af7243f5d8f46d/icons/silverfox.svg" align="center" alt="NekoSilverfox" />
 <h1 align="center">数据挖掘</h1>
 <p align="center"><b>Jupyter、Matplotlib、Numpy、Pandas</b></p>
</p>



<div align=center>



[![License](https://img.shields.io/badge/license-Apache%202.0-brightgreen)](LICENSE)
![Python](https://img.shields.io/badge/Python-3.8+-blue)

</br>

![Library](https://img.shields.io/badge/Library-Matplotlib-orange)
![Library](https://img.shields.io/badge/Library-Numpy-orange)
![Library](https://img.shields.io/badge/Library-Pandas-orange)
![Library](https://img.shields.io/badge/Library-Jupyter-orange)
![Library](https://img.shields.io/badge/Library-Tables-orange)


<div align=left>
<!-- 顶部至此截止 -->



[toc]



# 环境安装

| 库         | 说明                                                         |
| ---------- | ------------------------------------------------------------ |
| Matplotlib | 可以借助它进行绘制柱状图、折线图、散点图、直方图、函数图像等 |
| Numpy      |                                                              |
| Pandas     | 可以用于数据清洗                                             |
| TA-Lib     | 技术指标库                                                   |
| Tables     | 读取 hdf5 数据文件（hdf5 - 经过压缩的一种数据文件，可存储三维数据） |
| Jupyter    | 数据分析与展示的平台                                         |



# Jupyter Notebook

## 简介

**Jupyter Notebook 可以理解为 web 版本的 iPython**

Jupyter项 目是一个非盈利的开源项目，源于2014年的Python项目，并逐渐发为支持跨所有编程语言的交互式数据科学计算的工具。

- JupyterNotebook，原名 ipython Notebook，是 iPython 的加强网页版，一个开源Web应用程序
- 名字源自 Julia、 Python 和 R（数据科学的三种开源语言）
- 是一款程序员和科学工作者的编程/文档/笔记/展示软件
- `ipynb` 文件格式是用于计算型叙述的 **JSON文档格式**的正式规范



**为什么使用 Jupyter Notebook？**

- 画图和展示数据方便



## cell 操作

**cell：一对 In-Out 会话被视作一个代码单元，称为 cell**

Jupyter 支持两种模式：

- 编辑模式（ Enter）
    - 命令模式 下`回车 Enter` 或 `鼠标双击 cell` 进入编辑模式
    - 可以操作 cell 内文本或代码，剪切/复制/粘贴移动等操作
- 命令模式（Esc）
    - 按Esc退出编辑，进入命令模式
    - 可以操作 cell 单元本身进行剪切/复制/粘贴/移动等操作

![image-20220126001603579](doc/pic/README/image-20220126001603579.png)



## 使用 Jupyter Notebook

| 功能                                 | 快捷键                                               |
| ------------------------------------ | ---------------------------------------------------- |
| 打开 Jupyter Notebook                | 终端中输入：`jupyter notebook` 或 `ipython notebook` |
| 运行此单元格的代码，并自动选择下一个 | Shift + Enter                                        |
| 运行此单元格的代码，留在此单元       | Ctrl + Enter                                         |
|                                      |                                                      |



| 命令模式下（ESC 进入） | 操作                        |
| ---------------------- | --------------------------- |
| A                      | 在当前 cell 上面插入新 cell |
| B                      | 在当前 cell 下面插入新 cell |
| 双击D                  | 删除当前 cell               |



| 编辑模式下（Enter 进入）  | 操作       |
| ------------------------- | ---------- |
| Ctrl + / 或 CMD + /       | 添加注释   |
| 按住 Alt 或 Option 点鼠标 | 多光标操作 |
| Tab                       | 补全代码   |



# Matplotlib



## 简介

<img src="doc/pic/README/image-20220126002904416.png" alt="image-20220126002904416" style="zoom:25%;" />

**名字：**

- mat - matrix
- plot - 画图
- lib - library



**功能：**

- 专门用于开发 2D 或 3D 图表的 Python 库
- 使用起来极其简单
- 以渐进、交互式方式实现数据可视化



**为什么学习 Matplotlib**

将数据可视化，更直观的呈现；在我们进行数据挖掘和分析之前可以帮助我们选择一个更加适合的方法。

言外话：在 JavaScript 中好用的数据可视化工具有 D3 和 百度的 echarts



## 图像结构

<img src="doc/pic/README/image-20220126005157777.png" alt="image-20220126005157777" style="zoom: 33%;" />

![image-20200528144651404](doc/pic/image-20200528144651404.png)

```python
import matplotlib.pyplot as plt

plt.(figsize=(8, 10), dpi=?)

plt.plot(x, y, linestyle=':', marker='o', color='red', label='图例')
```

- linestyle - 折线形状

    - 直线： linestyle = ‘-’ 或 省略
    - 破折线： linestyle = ‘–’ 或 linestyle = ‘dashed’
    - 点划线： linestyle = ‘-.’ 或 linestyle = ‘dashdot’
    - 虚线： linestyle = ‘：’ 或 linestyle = ‘dotted’

- marker - 数据点形状

    ‘s’ : 方块状
    ‘o’ : 实心圆
    ‘^’ : 正三角形
    ‘v’ : 反正三角形
    ‘+’ : 加号
    ‘*’ : 星号
    ‘,’：点
    ‘x’ : x号
    ‘p’ : 五角星
    ‘1’ : 三脚架标记
    ‘2’ : 三脚架标记

- 

## Matplotlib 三层结构

![Matplotlib](doc/pic/README/Matplotlib.svg)



**由底向高：**

- **画板层（Canvas）**

​	Canvas 是位于最底层的系统层，在绘图的过程中充当画板的角色，即放置画布（Figure）的工具。



- **画布层（Figure）**

    Figure 是 Canvas 上方的*第一层*，也是需要用户来操作的应用层的第一层，在绘图的过程中充当画布的角色

    **创建或设置画布**：`plt.figure()`

    

- **绘图区/坐标系（Axes）**

    Axes 是应用层的第二层，在绘图的过程中相当于画布上的绘图区的角色

    画布上是默认有一个绘图区，一个绘图区是有 x、y 轴张成的区域

    手动创建新的话：`plt.subplots()`

    - **图像层**

        每一个绘图区上的不同图像层都可以画不同的图表

        图像层指 Axes 内通过 plot、scatter、bar、hist、pie 等函数根据数据绘制出的图像

        

    - **辅助显示层**

        图像上的那些坐标、网格、辅助线等。辅助图像的显示

        辅助显示层为 Axes（绘图区）内的除了根据数据绘制出的图像以外的内容，主要包括 Axes外观（facecolor）、边框线（spines）、坐标轴（axis）、坐标轴名称（axis labe）、坐标轴刻度（tick）、坐标轴刻度标签（tick label）、网格线（grid）、图例（legend）、标题（title）等内容

        该层的设置可使图像显示更加直观更加容易被用户理解，但又不会对图像产生实质的影响



**特点：**

- 一个 figure（画布）可以包含多个 axes（坐标系/绘图区），但是一个 axes 只能属于个 figure
- 一个 axes（坐标系/绘图区）可以包含多个 axis（坐标轴），包含两个即为2d坐标系，3个即为3d坐标系



**总结：**

- Canvas（画板）位于最底层，用户一般接触不到
    - Figure（画布）建立在 Canvas 之上
        - Axes（绘图区）建立在 Figure之上
            - 坐标轴（axis）、图例（legend）等辅助显示层以及图像层都是建立在 Axes 之上

<img src="doc/pic/README/image-20220126171952434.png" alt="image-20220126171952434" style="zoom: 25%;" />

<img src="doc/pic/README/image-20220126171055906.png" alt="image-20220126171055906" style="zoom: 33%;" />



## 绘图

`matplotlib.pytplot` 包含了一系列类似于 matlab 的画图函数。他的函数作用于当前图形（figure）的当前坐标系（axes）

```python
 import matplotlib.pyplot as plt
```



| 中文   | 英文      |
| ------ | --------- |
| 折线图 | plot      |
| 散点图 | scatter   |
| 柱状图 | bar       |
| 直方图 | histogram |
| 饼图   | pie       |



---



## 折线图（plot）与基础绘图功能

### API

| API                                         | 功能                           | 参数                                 |
| ------------------------------------------- | ------------------------------ | ------------------------------------ |
| `plt.figure(figsize=(x, y), dpi=y轴分辨率)` | 创建画布                       |                                      |
| `plt.plot(x轴数据列表, y轴数据列表)`        | 绘制图像                       |                                      |
| `plt.xticks(x要显示的刻度列表, **说明)`     | 添加自定义 x 刻度              |                                      |
| `plt.yticks(y要显示的刻度列表, **说明)`     | 添加自定义 y 刻度              |                                      |
| `plt.title('说明字符串')`                   | 添加标题                       |                                      |
| `plt.xlabel('说明字符串')`                  | 添加 x 轴说明                  |                                      |
| `plt.ylabel('说明字符串')`                  | 添加 y 轴说明                  |                                      |
| `plt.grid(True, linestyle='--', alpha=0.5)` | 添加网格显示                   | `linestyle`-线条风格；`alpha`-透明度 |
| `plt.x/ylim(min, max)`                      | 设置 x 或 y 轴显示范围         |                                      |
|                                             |                                |                                      |
| `plt.savefig('路径')`                       | 保存图像                       |                                      |
| `plt.show()`                                | 显示图像，并释放画布的所有资源 |                                      |



### 图形风格

| 颜色字符 | 风格字符        |
| -------- | --------------- |
| r 红色   | `-` 实线        |
| g 绿色   | `--` 虚线       |
| b 蓝色   | `-.` 点划线     |
| w 白色   | `:` 点虚线      |
| c 青色   | `''` 留空、空格 |
| m 洋红   |                 |
| y 黄色   |                 |
| k 黑色   |                 |





### 显示图例

> 注意:如果只在 `plt.plot()`中设置 label 还不能最终显示出图例，还需要通过 `plt.legend()` 将图例显示出来。

```python
 # 绘制折线图
plt.plot(x, y_shanghai, label="上海")

# 使用多次plot可以画多个折线
plt.plot(x, y_beijing, color='r', linestyle='--', label="北京")

# 显示图例
plt.legend(loc="best")
```



**图例位置：**

| **Location String** | **Location Code** |
| ------------------- | ----------------- |
| 'best'              | 0                 |
| 'upper right'       | 1                 |
| 'upper left'        | 2                 |
| 'lower left'        | 3                 |
| 'lower right'       | 4                 |
| 'right'             | 5                 |
| 'center left'       | 6                 |
| 'center right'      | 7                 |
| 'lower center'      | 8                 |
| 'upper center'      | 9                 |
| 'center'            | 10                |



### 多个坐标系显示 plt.subplots(面向对象的画图方法)

![image-20220126231559287](doc/pic/README/image-20220126231559287.png)



可以通过subplots函数实现(旧的版本中有subplot，使用起来不方便)，推荐subplots函数



**API:**

`matplotlib.pyplot.subplots(nrows=列数, ncols=行数, **fig_kw) ` 创建一个带有多个axes(坐标系/绘图区)的图

返回值：

- figure : 图对象
- axes : 返回相应数量的坐标系

之后在调用的时候，也不能直接使用 `plt.方法名()` 了，要用返回的 `ares[索引].set_方法名()` 

另外，在这种多坐标系显示的情况下，设置标题的方式也有所不同：

技巧：基本是涉及到辅助显示层的都要加 `set_`

- set_xticks 
- set_yticks 
- set_xlabel
- set_ylabel

> 参考：https://matplotlib.org/api/axes_api.html#matplotlib.axes.Axes





### 应用场景

`plt.plot()` 除了画折线图还可以画各种数学函数图像

```python
# 准备数据
import numpy as np
from matplotlib import pyplot as plt

x = np.linspace(-1, 1 , 1000)
y = 2 * x * x

# 创建画布
plt.figure(figsize=(20, 8), dpi=80)

# 绘制图像
plt.plot(x, y)

# 添加网格显示
plt.grid(linestyle='--', alpha=0.7)

# 显示图像
plt.show()
```



---



## 散点图（scatter）

简单示例：

```python
from matplotlib import pyplot as plt

"""
探究房屋面积和房屋价格的关系
x - 房屋面积
y - 房屋价格
"""
# 准备数据
x = [225.98, 247.07, 253.14, 457.85, 241.58, 301.01, 20.67, 288.64, 163.56, 120.06, 207.83, 342.75, 147.9 , 53.06, 224.72, 29.51,
21.61, 483.21, 245.25, 399.25, 343.35]

y = [196.63, 203.88, 210.75, 372.74, 202.41, 247.61, 24.9 , 239.34, 140.32, 104.15, 176.84, 288.23, 128.79, 49.64, 191.74, 33.1 ,
30.74, 400.02, 205.35, 330.64, 283.45]

# 新建画布
plt.figure(figsize=(20, 8), dpi=100)

# 绘制散点图
plt.scatter(x, y)

# 展示图像
plt.show()
```



---



## 柱状图（bar）

```python
from matplotlib import pyplot as plt

# 对比每部电影的票房收入
 
# 准备数据
x_moives = ['雷神3:诸神黄昏','正义联盟','东方快车谋杀案','寻梦环游记','全球风暴', '降魔传','追捕','七十七天','密战','狂兽','其它']
y_tickes = [73853,57767,22354,15969,14839,8725,8716,8318,7916,6764,52222]

# 创建画布
plt.figure(figsize=(20, 8), dpi=80)

# 绘制柱状图
x = range(len(x_moives))
plt.bar(x, y_tickes, width=0.5, color=['b','r','g','y','c','m','y','k','c','g','b'])

# 辅助显示层
plt.title('2017年票房对比')
plt.xticks(x, x_moives)
plt.grid(linestyle='--', alpha=0.5)

# 显示
plt.show()
```



---



### 平移坐标以显示多个柱子



- **如果要想实现在一个分类里显示两个柱状图，本质上是在绘制时把柱子和坐标平移！**

![image-20220127184415002](doc/pic/README/image-20220127184415002.png)

```python
from matplotlib import pyplot as plt


# 准备数据
movie_name = ['雷神3:诸神黄昏','正义联盟', '寻梦环游记']
first_day = [105786.3, 10063.5, 1278.3]
first_weekend = [36224.9, 34486.6, 11863]

# 创建画布
plt.figure(figsize=(20, 8), dpi=80)

# 绘制柱状图
"""
【重点】要想在一个分类里显示两个，其实是把第二个柱状图给平移了一下，避免两个柱状图挡在一起
 这里用一个列表生成式进行书写
""" 
x = range(len(movie_name))
plt.bar(x, first_day, width=0.2, label='首日票房')
plt.bar([i + 0.2 for i in x], first_weekend, width=0.2, label='首周票房')
plt.legend()  # 显示图例

# 辅助显示层
plt.title('第一天及第一周票房')
plt.xticks([i + 0.1 for i in x], movie_name)  # 【重点】修改刻度，这里的列表生成式其实是把刻度给平移了

# 展示
plt.show()
```



---



## 直方图（histogram）

直方图（histogram）用于反映数据的分布状况

直方图，形状类似柱状图却有着与柱状图完全不同的含义。直方图涉统计学的概念，首先要对数据进行分组，然后统计每个分组内数据元的数量。在坐标系中，轴标出每个组的端点，纵轴表示频数，每个矩形的高代表对应的频数，称这样的统计图为频数分布直方图。



**直方图与柱状图分区别：**

- 直方图展示的是数据的分布，柱状图比较数据的大小

- 直方图 x 轴为定量数据、数据是连续的，柱状图 x 轴为分类数据。所以直方图的每根柱子是不可移动的

    <img src="doc/pic/README/image-20220127220536663.png" alt="image-20220127220536663" style="zoom:50%;" />

- 直方图的柱子是无间隔的，柱状图柱子有间隔

- 直方图的柱子宽度可不一样，柱状图柱子宽度必须一样





**API:**

```python
matplotlib.pyplot.hist(x, bins=None, density=False, **kwargs)

其中：
	- `x` 就是我们的数据
    - `bins` 就是组数
    - `density` 是否显示频率
```





**【重要】要绘制直方图的过程**

1. 设置组距
2. 设置组数（通常对于数据较少的情况，分为 5~12 组；数据较多，更换图形显示方式）
    - *组数 = 极差/组距 = (Max - Min) / 组距*
3. 要注意 y 轴表示的是什么



示例：

```python
# 电影时长的分布状况
from matplotlib import pyplot as plt

# 准备数据
time = [131,  98, 125, 131, 124, 139, 131, 117, 128, 108, 135, 138, 131, 102, 107, 114, 119, 128, 121, 142, 127, 130, 124, 101, 110, 116, 117, 110, 128, 128, 115,  99, 136, 126, 134,  95, 138, 117, 111,78, 132, 124, 113, 150, 110, 117,  86,  95, 144, 105, 126, 130,126, 130, 126, 116, 123, 106, 112, 138, 123,  86, 101,  99, 136,123, 117, 119, 105, 137, 123, 128, 125, 104, 109, 134, 125, 127,105, 120, 107, 129, 116, 108, 132, 103, 136, 118, 102, 120, 114,105, 115, 132, 145, 119, 121, 112, 139, 125, 138, 109, 132, 134,156, 106, 117, 127, 144, 139, 139, 119, 140,  83, 110, 102,123,107, 143, 115, 136, 118, 139, 123, 112, 118, 125, 109, 119, 133,112, 114, 122, 109, 106, 123, 116, 131, 127, 115, 118, 112, 135,115, 146, 137, 116, 103, 144,  83, 123, 111, 110, 111, 100, 154,136, 100, 118, 119, 133, 134, 106, 129, 126, 110, 111, 109, 141,120, 117, 106, 149, 122, 122, 110, 118, 127, 121, 114, 125, 126,114, 140, 103, 130, 141, 117, 106, 114, 121, 114, 133, 137,  92,121, 112, 146,  97, 137, 105,  98, 117, 112,  81,  97, 139, 113,134, 106, 144, 110, 137, 137, 111, 104, 117, 100, 111, 101, 110,105, 129, 137, 112, 120, 113, 133, 112,  83,  94, 146, 133, 101,131, 116, 111,  84, 137, 115, 122, 106, 144, 109, 123, 116, 111,111, 133, 150]

# 创建画布
plt.figure(figsize=(20, 8), dpi=80)

# 绘制直方图
distance = 2  # 组距
group_num = int((max(time) - min(time)) / distance)  # 组数
plt.hist(time, bins=group_num, density=True)

x_tickes = range(min(time), max(time) + 2, distance)  # 刻度
plt.xticks(x_tickes)

# 辅助显示层
plt.title('电影时长的分布状况')
plt.xlabel('电影时长')
plt.ylabel('电影数量')
plt.grid(linestyle='--', alpha=0.5)


# 显示图像
plt.show()

```



## 饼图（pie）

**API:**

`plt.pie(x, labels=[] , autopct=如何显示占比, colors=[])`

- `x` 数据（数量），饼图会按照给定的数据自动计算占比

- `labels` 每个 x 中的数据（扇形）对应的名称

- `autopct` 如何显示占比，建议使用**`%1.2f%%`**

    `%%`表示一个百分号、`.2f`表示浮点型并保留两位小数、`1`表示占几个位置

- `colors` 没部分的颜色



**注意：**

- 饼图默认不是圆形的，要想使饼图为圆形，需要添加 axis，保证长宽一致，调用：

```python
plt.axis('equal')
```

- 如果要展示的数量超过 9 个，不建议使用饼图，而应该使用直方图





**示例：**

```python
# 展示各个电影票房的占比
from matplotlib import pyplot as plt

# 准备数据
movie_name = ['雷神3：诸神黄昏','正义联盟','东方快车谋杀案','寻梦环游记','全球风暴','降魔传','追捕','七十七天','密战','狂兽','其它']
place_count = [60605,54546,45819,28243,13270,9945,7679,6799,6101,4621,20105]

# 新建画布
plt.figure(figsize=(20, 8), dpi=80)

# 绘制图像
plt.pie(place_count, labels=movie_name, colors=['b','r','g','y','c','m','y','k','c','g','y'], autopct='%1.2f%%')
plt.legend()

# 将饼图转换为圆形
plt.axis('equal')

# 显示图像
plt.show()
```

---





# Numpy

![upload.wikimedia.org/wikipedia/commons/thumb/3/...](https://upload.wikimedia.org/wikipedia/commons/thumb/3/31/NumPy_logo_2020.svg/800px-NumPy_logo_2020.svg.png)

## 简介

Numpy(Numerical Python) 是一个开源的 Python 科学计算库，用于**快速处理任意维度的数组**（ndarray）。 

Numpy 支持常见的数组和矩阵操作。对于同样的数值计算任务，使用 Numpy 比直接使用 Python 要简洁的多。 

Numpy 使用 **ndarray** 对象来处理多维数组，该对象是一个**快速而灵活的大数据容器**。

Numpy 的底层是使用 C 实现的，所以操作的效率极高。Numpy 专门针对 ndarray 的操作和运算进行了设计，所以数组的存储效率和输入输出性能远优于 Python 中的嵌套列表，数组越大，Numpy 的优势就越明显。



**其中，ndarray 的意思是：**

- n - 任意一个
- d - dimension 维度数组
- array - 数组



**Numpy 的基本操作：**

- `ndarray.方法()` 用它来做逻辑运算、统计运算、数组间运算。
- `numpy.函数名()`



> 注意：合并、分割、IO 操作、数据其实也可以使用 Numpy，但是它做的并不是很好。我们将使用 Pandas



![numpy思维导图](doc/pic/README/Numpy.svg)

## ndarray 内存块

<img src="doc/pic/README/image-20220128175851159.png" alt="image-20220128175851159" style="zoom:50%;" />

从图中我们可以看出 ndarray 在存储数据的时候，**数据与数据的地址都是连续的，且只能同时存储一个类型是数据**，这样就给使得批量操作数组元素时速度更快。而 Python 自带的 list 数据在内存中的位置是分散的，但是可以存储不同的数据

具体的解释：这是因为 ndarray 中的所有元素的类型都是相同的，而 Python 列表中的元素类型是任意的，所以 ndarray 在存储元素时内存可以连续，而 python 原生 list 就只能通过寻址方式找到下一个元素，这虽然也导致了在通用性能方面 Numpy 的 ndarray 不及 Python 原生 list，但**在科学计算中，Numpy 的ndarray 就可以省掉很多循环语句，代码使用方面比 Python 原生 list 简单的多**。



- **ndarray** 支持并行化运算(向量化运算)

    numpy内置了并行运算功能，当系统有多个核心时，做某种计算时，numpy会自动做并行计算

    

- 效率远高于纯 **Python** 代码

    Numpy底层使用C语言编写，内部解除了GIL(全局解释器锁)，其对数组的操作速度不受 Python 解释器的限制，所以，其效率远高于纯 Python 代码



## ndarray 的属性及方法



### numpy.dtype 类型

> 若不指定数据类型，整数默认 int64，小数默认 float64

`dtype` 是 `numpy.dtype` 类型

| 名称          | 描述                                             | 简写  |
| ------------- | ------------------------------------------------ | ----- |
| np.bool       | 用一个字节存储的布尔类型(True或False)            | 'b'   |
| np.int8       | 一个字节大小，-128 至 127                        | 'i'   |
| np.int16      | 整数，-32768 至 32767                            | 'i2'  |
| np.int32      | 整数，-2^31 至 2^32 -1                           | 'i4'  |
| np.int64      | 整数，-2^63 至 2^63 - 1                          | 'i8'  |
| np.uint8      | 无符号整数，0 至 255                             | 'u'   |
| np.uint16     | 无符号整数，0 至 65535                           | 'u2'  |
| np.uint32     | 无符号整数，0 至 2^32 - 1                        | 'u4'  |
| np.uint64     | 无符号整数，0 至 2^64 - 1                        | 'u8'  |
| np.float16    | 半精度浮点数:16位，正负号1位，指数5位，精度10位  | 'f2'  |
| np.float32    | 单精度浮点数:32位，正负号1位，指数8位，精度23位  | 'f4'  |
| np.float64    | 双精度浮点数:64位，正负号1位，指数11位，精度52位 | 'f8'  |
| np.complex64  | 复数，分别用两个32位浮点数表示实部和虚部         | 'c8'  |
| np.complex128 | 复数，分别用两个64位浮点数表示实部和虚部         | 'c16' |
| np.object_    | python对象                                       | 'O'   |
| np.string_    | 字符串                                           | 'S'   |
| np.unicode_   | unicode类型                                      | 'U'   |


​    

---



### 生成数组的方法

- **生成0和1的数组**

    | 方法                       | 描述 |
    | -------------------------- | ---- |
    | **`np.ones(shape=形状, dtype=数据类型)`** | `shape` 可以以列表或者元组的形式传入；`dtype` 可以指定数据类型 |
    | `np.ones_like(a=数组, dtype=数据类型)` | `a` 可以是 ndarray，生成和 `a` **形状一样的新** `ndarray` |
    | **`np.zeros(shape=形状, dtype=数据类型)`** |      |
    | `np.zeros_like(a=数组, dtype=数据类型)` |      |

    

- **从现有数组生成**

    > **这里深拷贝和浅拷贝只有在传入的数组是 np.ndarray ，并且数据类型一致时才有效**。如果传入的是 Python 自带的 list[] 类型，则两者都是深拷贝！
    
    | 方法                                          | 描述                                           |
    | --------------------------------------------- | ---------------------------------------------- |
    | `np.array(object=现有数组, dtype=数据类型)`   | **【深拷贝】**返回跟参数中的数组一样的 ndarray |
    | `np.copy(现有数组)`                           | **【深拷贝】**返回跟参数中的数组一样的 ndarray |
    | `np.asarray(object=现有数组, dtype=数据类型)` | **【浅拷贝】**返回跟参数中的数组一样的 ndarray |
    



- **生成固定范围的数组**

    - 创建**等差**数组 — **指定元素数量**

        生成数组内**指定元素数量**的**等差数组**

        *指定的 start-stop 区间为两侧闭区间：[start, stop]*

        ```python
        np.linspace(start=起始值, stop=结束值, num=要生成的等间隔样例数量，默认50, endpoint=序列中是否包含stop值，默认为ture)
        
        
        # 生成等间隔的数组
        np.linspace(0, 100, 11)
         
        >>> 返回结果:
        array([ 0., 10., 20., 30., 40., 50., 60., 70., 80., 90., 100.])
        ```

        

    - 创建**等差**数组 — **指定步长**

        根据**指定的步长**生成数组

        *指定的 start-stop 区间为左闭右开闭区间：[start, stop)*

        ```python
        np.arange(start=起始值, stop=结束值, step=步长、默认1, dtype=类型)
        
        
        np.arange(10, 50, 2)
            
        >>> 返回结果:
        array([10, 12, 14, 16, 18, 20, 22, 24, 26, 28, 30, 32, 34, 36, 38, 40, 42, 44, 46, 48])
        ```

        

    - 创建**等比**数列 — **指定元素数量**

        *指定的 start-stop 区间为 10^n 次方 两侧闭区间：[10^start, 10^stop]*

        ```python
        np.logspace(start=起始值10^start, stop=结束值10^stop, num=要生成的等比数列中元素的数量，默认为50)
        
        
        np.logspace(0, 2, 3)
        
        >>> 返回结果:
        array([  1.,  10., 100.])
        ```





- **生成随机数组**

    模块 API：

    ```python
    numpy.random
    ```

    - **生成随机数组**

        ```python
        np.random.uniform(low=最小值, high=最大值, size=数量)
        ```

        

    - **正态分布**

> **什么是正态分布？**
>
> 正态分布是一种概率分布。正态分布是具有两个参数 μ 和 σ 的连续型随机变量的分布，第一参数 μ 是服从正态分布的随机变量的均值，第二个参数 σ 是此随机变量的标准差，所以正态分布记作 **N(μ**，**σ)**。
>
> 
>
> **当μ = 0,σ = 1时的正态分布是标准正态分布**
>
> 
>
> - `μ` - 均值，在图像中反映为对称轴
>
> - `σ` - 标准差，标准差 **σ** 决定了分布的幅度
>
> - `σ^2` - 方差，理解为数据的分布密度；**方差越大数据越分散，方差越小数据越向均值集中**
>
>     方差是在概率论和统计方差衡量一组数据时**离散程度的度量**
>
>     
>
>     <img src="doc/pic/README/image-20220129170457084.png" alt="image-20220129170457084" style="zoom:50%;" />
>
>     
>
>     其中M为平均值，n为数据总个数，σ 为标准差，σ^2 可以理解一个整体为方差
>                                                                            
>     <img src="doc/pic/README/image-20220129170536906.png" alt="image-20220129170536906" style="zoom:25%;" />
>
>     
>
>     
>
> <img src="doc/pic/README/image-20220129165930556.png" alt="image-20220129165930556" style="zoom:50%;" />
>
> 



- **正态分布**

    - **返创建并回指定形状的标准正态分布的数组**

        ```python
        np.random.standard_normal(size=数组形状)
        ```

        

    - **创建并返回指定均值和标准差的正态分布**

        ```python
        np.random.normal(loc=float类型的均值, scale=标准差, size=数组形状默认1)
        ```




---







### ndarray 的属性

| 属性名字           | 属性解释                                                     |
| ------------------ | ------------------------------------------------------------ |
| `ndarray.shape`    | 返回数组维度的**元组**，元组中一个元素代表一个维度，如果只有一个维度则用 `(n, )` 表示 |
| `ndarray.ndim`     | 返回数组维数                                                 |
| `ndarray.size`     | 返回数组中的元素数量                                         |
| `ndarray.itemsize` | 返回数组中一个元素的长度（字节）                             |
| `ndarray.dtype`    | 数组元素的类型                                               |



### 数组的索引、切片

一维、二维、三维的数组如何索引？

- 直接进行索引,切片
- 对象[:, :] -- 先行后列



二维数组索引方式：

- 举例：获取第一个股票的前3个交易日的涨跌幅数据

```python
# 二维的数组，两个维度 
stock_change[0, 0:3]
```

返回结果：

```python
array([-0.03862668, -1.46128096, -0.75596237])
```

- 三维数组索引方式：

```python
# 三维
a1 = np.array([ [[1,2,3],[4,5,6]], [[12,3,34],[5,6,7]]])
# 返回结果
array([[[ 1,  2,  3],
        [ 4,  5,  6]],

       [[12,  3, 34],
        [ 5,  6,  7]]])
# 索引、切片
>>> a1[0, 0, 1]   # 输出: 2
```





### 形状变换

| 方法                            | 描述                                                         |
| ------------------------------- | ------------------------------------------------------------ |
| `ndarray.reshape(shape, order)` | **只返回**一个具有相同数据域，但shape不一样的**新视图** ，源数组不进行变换<br />行、列不进行互换<br />也就是把数据分布到新的 shape 当中去<br />在转换形状的时候，一定要注意数组的元素匹配 |
| `ndarray.resize(new_shape)`     | 修改数组本身的形状（需要保持元素个数前后相同），无返回值 <br />行、列不进行互换 |
| `ndarray.T`                     | 数组的转置<br />将数组的行、列进行互换                       |
|                                 |                                                              |





### 类型的修改及数据的本地化

> **python 序列化数据本地存放**
>
> 序列化的概念很简单。内存里面有一个数据结构，你希望将它保存下来，重 用，或者发送给其他人。你会怎么做？嗯, 这取决于你想要怎么保存，怎么重用，发送给谁。很多游戏允许你在退出的时候保存进度，然后你再次启动的时候回到上次退出的地方。(实际上, 很多非游戏程序也会这么干。) 在这个情况下, 一个捕获了当前进度的数据结构需要在你退出的时候保存到磁盘上，接着在你重新启动的时候从磁盘上加载进来。这个数据只会被创建它的程序使用，不会发送到网 络上，也不会被其它程序读取。因此，互操作的问题被限制在保证新版本的程序能够读取以前版本的程序创建的数据。

| 方法                                                         | 描述                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| `ndarray.astype(type)`                                       | **只返回**修改了类型之后的数组，不修改原数组                 |
| `ndarray.tostring([order])` <br />或者<br />`ndarray.tobytes([order])` | (本地化数据) **只返回**构造包含数组中原始数据字节的Python字节 |
|                                                              |                                                              |



### 数组的去重

- 利用 Numpy 提供的方法进行直接去重

    ```python
    numpy.unique(ndarry数组)
    
    
    temp = np.array([[1, 2, 3, 4],[3, 4, 5, 6]])
    np.unique(temp)
    
    >>> 输出：
    array([1, 2, 3, 4, 5, 6])
    ```

    **返回**去重后的**数的数组**

    

    

- 利用将 `ndarray.flatten()` 先转换为一维数组，再利用 Python set集合的方式去重

    ```python
    set(ndarry.flatten())
    
    
    >>> 输出：
    array([1, 2, 3, 4, 5, 6])
    ```

    **返回**去重后的**数的集合**



### 小结

- 创建数组【掌握】
    - 生成0和1的数组
        - `np.ones()`
        - `np.ones_like()`
    - 从现有数组中生成
        - `np.array` -- 深拷贝
        - `np.asarray` -- 浅拷贝
    - 生成固定范围数组
        - `np.linspace()`
            - nun -- 生成**等间隔**的多少个
        - `np.arange()`
            - step -- 每间隔多少生成数据
        - `np.logspace()`
            - 生成以10的N次幂的数据
    - 生层随机数组
        - 正态分布
            - 里面需要关注的参数:均值:u, 标准差:σ
                - u -- 决定了这个图形的左右位置
                - σ -- 决定了这个图形是瘦高还是矮胖
            - `np.random.randn()`
            - `np.random.normal(0, 1, 100)`
        - 均匀
            - `np.random.rand()`
            - `np.random.uniform(0, 1, 100)`
            - `np.random.randint(0, 10, 10)`
- 数组索引【知道】
    - 直接进行索引,切片
    - 对象[:, :] -- 先行后列
- 数组形状改变【掌握】
    - `对象.reshape()`
        - 没有进行行列互换,新产生一个ndarray
    - `对象.resize()`
        - 没有进行行列互换,修改原来的ndarray
    - `对象.T`
        - 进行了行列互换
- 数组去重【知道】
    - `np.unique(对象)`





## ndarry 运算

### 逻辑运算

```python
# 生成10名同学，5门功课的数据
>>> score = np.random.randint(40, 100, (10, 5))

# 取出最后4名同学的成绩，用于逻辑判断
>>> test_score = score[6:, 0:5]

# 逻辑判断, 如果成绩大于60就标记为True 否则为False
>>> test_score > 60
array([[ True,  True,  True, False,  True],
       [ True,  True,  True, False,  True],
       [ True,  True, False, False,  True],
       [False,  True,  True,  True,  True]])

# 【重点】BOOL赋值, 将满足条件的设置为指定的值-布尔索引
>>> test_score[test_score > 60] = 1
>>> test_score
array([[ 1,  1,  1, 52,  1],
       [ 1,  1,  1, 59,  1],
       [ 1,  1, 44, 44,  1],
       [59,  1,  1,  1,  1]])
```



### 通用判断函数

- `no.all(布尔表达式)`

    只有所有的元素满足才返回 true

    ```python
    # 判断前两名同学的成绩是否全及格
    np.all(source[0:2, :] > 60)
    ```

    

- `np.any(布尔表达式)`

    只有要有一个元素满足就返回 true

    ```python
    # 判断前两名同学的成绩[0:2, :]是否有大于 90 分的
    np.any(source[0:2, :] > 90)
    ```

    

### 三元运算符及复合逻辑

- `np.where(布尔表达式, 布尔值为True设置的值, 布尔值为False设置的值)` **返回**新的数组

    ```python
    # 通过使用 np.where 能够进行更加复杂的运算
    # 判断前 4 名学生，前 3 门课程中，成绩中大于 60 的置为 1，否则为 0
    
    temp = source[:4, :3]
    np.where(temp > 60, 1, 0)
    ```

    

    

- 复合逻辑需要结合 `np.logical_and`、 `np.logical_or` 、`np.logical_not` 使用

    格式：`np.logical_and/or/not(布尔表达式1, 布尔表达式2, )`

    ```python
    # 判断前 4 名学生，前 3 门课程中，成绩中大于 60【且】小于 90 的换为 1，否则为 0
    np.where(np.logical_and(temp > 60, temp < 90), 1, 0)
    
    # 判断前 4 名学生，前 3 门课程中，成绩中大于 60【或】小于 90 的换为 1，否则为 0
    np.where(np.logical_or(temp > 60, temp < 90), 1, 0)
    ```



---



### 统计指标

获取数组的最小值、最大值、平均值、中位数等，可以使用:

- `Numpy.函数名(ndarry, axis=按哪一坐标轴)` 如果不指明具体按哪个 axis，那么就是整个数组

- `ndarry.方法名(axis=按哪一坐标轴)` 如果不指明具体按哪个 axis，那么就是整个数组



- **按 `Numpy.函数名(ndarry, axis=按哪一坐标轴)` 的方式**

    | 函数名                         | 描述         |
    | ------------------------------ | ------------ |
    | `np.min(ndarry, axis)`         | 最小值       |
    | `np.max(ndarry, axis)`         | 最大值       |
    | `np.median(ndarry, axis)`      | 中位数       |
    | `np.mean(ndarry, axis, dtype)` | 平均数       |
    | `np.std(ndarry, axis, dtype)`  | 标准差       |
    | `np.var(ndarry, axis, dtype)`  | 方差         |
    | `np.argmax(ndarry, axis)`      | 最大值的下标 |
    | `np.argmin(ndarry, axis)`      | 最小值的下标 |

    ```python
    源数据：
    array([[ 0.94392597, -0.2579331 ,  1.17741713,  0.91106463],
           [-0.22480532, -2.17304257,  0.06689428,  0.20691028],
           [-0.03596233, -0.59718032, -1.23148979, -0.62469026],
           [ 0.58676196, -2.00826884, -0.322707  , -1.02992438]])
    
    
    # 用 Numpy.函数名(ndarry, axis=按哪一坐标轴) 的方式：
    np.min(tmp)
    >>> -2.17304256830656
    
    np.min(tmp, axis=0)  # 这时 axis=0 代表按列，返回每一列的最小值
    >>> array([-0.22480532, -2.17304257, -1.23148979, -1.02992438])
    
    np.median(tmp)
    >>> -0.24136921361245312
    ```

    



- **按 `Numpy.函数名(ndarry, axis=按哪一坐标轴)` 的方式**

    | 函数名                         | 描述   |
    | ------------------------------ | ------ |
    | `ndarry.min(axis)`         | 最小值 |
    | `ndarry.max(axis)`         | 最大值 |
    | `ndarry.median(axis)`      | 中位数 |
    | `ndarry.mean(axis, dtype)` | 平均数 |
    | `ndarry.std(axis, dtype)`  | 标准差 |
    | `ndarry.var(axis, dtype)`  | 方差   |
    | `ndarry.argmax(axis)` | 最大值的下标 |
    | `ndarry.argmin(axis)` | 最小值的下标 |

    ```python
    源数据：
    array([[ 0.94392597, -0.2579331 ,  1.17741713,  0.91106463],
           [-0.22480532, -2.17304257,  0.06689428,  0.20691028],
           [-0.03596233, -0.59718032, -1.23148979, -0.62469026],
           [ 0.58676196, -2.00826884, -0.322707  , -1.02992438]])
    
    
    # 用 `ndarry.方法名(axis=按哪一坐标轴)` 的方式：
    tmp.min()
    >>> -2.17304256830656
    
    tmp.min(axis=1)
    >>> array([-0.2579331 , -2.17304257, -1.23148979, -2.00826884])
    ```




- **其他**

    | 函数                                     | 描述             |
    | ---------------------------------------- | ---------------- |
    | `numpy.count_nonzero(布尔表达式, axis=)` | 返回 True 的数量 |
    |                                          |                  |
    |                                          |                  |

    



## 数组间运算

### 数组与数的运算

直接**用一个 ndarry 加减乘除 另一个数，会作用于 ndarry 中的每一个元素**



例子：

```python
arr = np.array([[1, 2, 3, 2, 1, 4], [5, 6, 1, 2, 3, 1]])

arr + 1
>>> array([[2, 3, 4, 3, 2, 5],
       [6, 7, 2, 3, 4, 2]])

arr / 2
>>> array([[0.5, 1. , 1.5, 1. , 0.5, 2. ],
       [2.5, 3. , 0.5, 1. , 1.5, 0.5]])

```



### broadcast 广播机制

**【重点】**数组在进行矢量化运算（element-wise）时，**要求 ndarry 数组的形状是相等的**。当形状不相等的数组执行算术运算的时候，就会出现广播机制，该机制会对数组进行扩展，使数组的 shape 属性值一样，这样，就可以进行矢量化运算了。



**运算的数组之间满足以下任意的一个条件时才能进行运算：**

- 对应维度的元素数量相同（维度等长）
- 对应维度的元素数量有一个数组的是 1（shape）



广播机制需要**扩展维度小的数组**，使得它与维度最大的数组的shape值相同，以便使用元素级函数或者运算符进行运算。

![image-20220202170405943](doc/pic/README/image-20220202170405943.png)



### 矩阵和向量

#### 矩阵

矩阵，英文matrix，**和array的区别矩阵必须是2维的，但是array可以是多维的。**

如图:这个是 3×2 矩阵，即 3 行 2 列，如 m 为行，n 为列，那么 m×n 即 3×2

<img src="doc/pic/README/image-20220202180433112.png" alt="image-20220202180433112" style="zoom:50%;" />

**矩阵的维数即行数×列数**

矩阵元素(矩阵项):

<img src="doc/pic/README/image-20220202180458486.png" alt="image-20220202180458486" style="zoom:50%;" />

$A_{ij}$ 指第 i 行，第 j 列的元素。



---



#### 向量

**向量是一种特殊的矩阵**，讲义中的向量一般都是列向量，下面展示的就是三维列 向量(3×1)

<img src="doc/pic/README/image-20220202180628597.png" alt="image-20220202180628597" style="zoom:50%;" />



---



#### 加法和标量乘法

- 矩阵的加法:**行列数相等的可以加。**

    例:

<img src="doc/pic/README/image-20220202180842906.png" alt="image-20220202180842906" style="zoom:50%;" />

- 矩阵的乘法:每个元素都要乘。

    例:

    <img src="doc/pic/README/image-20220202180853835.png" alt="image-20220202180853835" style="zoom:50%;" />

    组合算法也类似

    

---



#### 矩阵向量乘法

矩阵和向量的乘法如图：m×n 的矩阵乘以 n×1 的向量，得到的是 m×1 的向量

例:

<img src="doc/pic/README/image-20220202181150181.png" alt="image-20220202181150181" style="zoom:50%;" />

```
1*1+3*5 = 16
4*1+0*5 = 4
2*1+1*5 = 7
```

**矩阵乘法遵循准则：**

**(M行, N列)\*(N行, L列) = (M行, L列)**



---



#### 矩阵乘法

矩阵乘法：

m×n 矩阵乘以 n×l 矩阵，变成 m×l 矩阵。

举例：比如说现在有两个矩阵 A 和 B，那 么它们的乘积就可以表示为图中所示的形式。

![image-20220202181451683](doc/pic/README/image-20220202181451683.png)



例：

![image-20220202181550578](doc/pic/README/image-20220202181550578.png)



---



#### 矩阵乘法的性质

矩阵的乘法不满足交换律：A×B≠B×A

矩阵的乘法满足结合律。即：A×（B×C）=（A×B）×C

单位矩阵：在矩阵的乘法中，有一种矩阵起着特殊的作用，如同数的乘法中的 1，我们称这种矩阵为**单位矩阵**。它是个方阵，一般用 I 或者 E 表示，从 左上角到右下角的对角线（称为主对角线）上的元素均为 1 以外全都为 0。

如：

![image-20220202181751116](doc/pic/README/image-20220202181751116.png)



---



#### 逆、转置

矩阵的逆：如矩阵 A 是一个 m×m 矩阵（方阵），如果有逆矩阵，则：

$$ AA^{-1} = A^{-1}A = I $$



**低阶矩阵求逆的方法:**

 1.待定系数法

 2.初等变换



**矩阵的转置：**

设 A 为 m×n 阶矩阵（即 m 行 n 列），第 i 行 j 列的元素是 a(i,j)，即：A=a(i,j)

定义 A 的转置为这样一个 n×m 阶矩阵 B，满足 B=a(j,i)，即 b(i,j)=a(j,i)（B 的第 i 行第 j 列元素是 A 的第 j 行第 i 列元素），记 AT =B。

直观来看，将 A 的所有元素绕着一条从第 1 行第 1 列的元素出发的右下方 45 度的射线作镜面反转，即得到 A 的转置。

例：

<img src="doc/pic/README/image-20220202182144483.png" alt="image-20220202182144483" style="zoom:50%;" />



---



#### 矩阵运算

假设我们拥有学生的平均成绩和期末成绩，但学生的最终成绩是按照平时成绩和最终成绩加权得到的，平时成绩占 30%、期末成绩占 70%

也就是说：

最终成绩 = (平时成绩 * 0.3) + (最终成绩 * 0.7)

我们可以使用矩阵运算的形式得到所需的结果：

<img src="doc/pic/README/image-20220202184019264.png" alt="image-20220202184019264" style="zoom:50%;" />



#### 矩阵 API

- **定义一个矩阵**

    `Numpy.mat(列表形式的数据或 ndarry)` **返回** Numpy 类型的矩阵；mat 代表 **mat**rix

    

- **矩阵的乘法**

    - `矩阵1 * 矩阵2`
    - `np.matmul(矩阵1, 矩阵2)`

    - `np.dot(矩阵1, 矩阵2)`

    

    **`np.matmul(矩阵1, 矩阵2)` 和 `np.dot(矩阵1, 矩阵2)` 的区别:**

    二者都是矩阵乘法。 `np.matmul(矩阵1, 矩阵2)` 中**禁止矩阵与标量的乘法**。 

    在矢量乘矢量的內积运算中，`np.matmul(矩阵1, 矩阵2)` 与 `np.dot(矩阵1, 矩阵2)` 没有区别。



- **在 ndarry 不转换为矩阵的形式下进行矩阵运算：**

    有时候如果是通过 ndarry 的方式直接相乘，是不可以的，比如 (8, 2) 和 (1, 2) 不符合广播机制！所以不能进行运算

    但是可以使用运算符 `@` 的进行相乘（矩阵相乘）！

    `数组1 @ 数组2`



```python
# 学生成绩
mark_stu = np.array([[80, 86],
[82, 80],
[85, 78],
[90, 90],
[86, 82],
[82, 90],
[78, 80],
[92, 94]])

# 权重
weight = np.array([[0.3], [0.7]])

# 转换为矩阵
matrix_mark_stu = np.mat(mark_stu)
matrix_weight = np.mat(weight)

# 矩阵1 * 矩阵2
matrix_mark_stu * matrix_weight

# 矩阵乘法 `np.matmul(矩阵1, 矩阵2)`
np.matmul(matrix_mark_stu, matrix_weight)

# 矩阵乘法 `np.dot(矩阵1, 矩阵2)` 
np.dot(matrix_mark_stu, matrix_weight)

# 如果是通过 ndarry 的方式直接相乘，是不可以的，因为 (8, 2) 和 (1, 2) 不符合广播机制！所以不能进行运算
# 但是可以使用运算符 `@` 的进行相乘（矩阵相乘）！
mark_stu @ weight


>>> array([[84.2],
       [80.6],
       [80.1],
       [90. ],
       [83.2],
       [87.6],
       [79.4],
       [93.4]])
```



---



### 合并、分割

- **数组的合并**

| 函数                                                       | 描述                            |
| ---------------------------------------------------------- | ------------------------------- |
| `Numpy.hstack(ndarry1, ndarry2 ...)`                       | 横向拼接                        |
| `Numpy.vstack(ndarry1, ndarry2 ...)`                       | 竖向拼接                        |
| `Numpy.concatenate((ndarry1, ndarry2 ...), axis=按哪个轴)` | 按指定的 int 类型的 axis 轴拼接 |

示例：

```python
# `Numpy.hstack(ndarry1, ndarry2 ...)` 
# 注意参数的括号
l = np.array((1, 2, 3))
r = np.array((4, 5, 6))
np.hstack((l, r))

>>> array([1, 2, 3, 4, 5, 6])


l = np.array([[1], [2], [3]])
r = np.array([[4], [5], [6]])
np.hstack((l, r))

>>> array([[1, 4],
       [2, 5],
       [3, 6]])

""""""""""""""""""""""""""""""""""""""""""""""""
# `Numpy.vstack(ndarry1, ndarry2 ...)` 
# 注意参数的括号
l = np.array((1, 2, 3))
r = np.array((4, 5, 6))
np.vstack((l, r))

>>> array([[1, 2, 3],
       [4, 5, 6]])


l = np.array([[1], [2], [3]])
r = np.array([[4], [5], [6]])
np.vstack((l, r))

>>> array([[1],
       [2],
       [3],
       [4],
       [5],
       [6]])

""""""""""""""""""""""""""""""""""""""""""""""""
# `Numpy.concatenate((ndarry1, ndarry2 ...), axis=按哪个轴)`
l = np.array([[1, 2], [3, 4]])
r = np.array([[5, 6]])

# 沿着 x 轴合并
np.concatenate((l, r), axis=0)

>>> array([[1, 2],
       [3, 4],
       [5, 6]])

# 沿着 y 轴合并
np.concatenate((l, r.T), axis=1)

>>> array([[1, 2, 5],
       [3, 4, 6]])
```



- **数组的分割**

    `Numpy.split(ndarry, 数或索引数组)` 

    - 如果第二个参数为数则切分成**等分**

        ```python
        arr = np.arange(9.0)
        arr
        >>> array([0., 1., 2., 3., 4., 5., 6., 7., 8.])
        
        # 等分为 3 份
        np.split(arr, 3)
        >>> [array([0., 1., 2.]), array([3., 4., 5.]), array([6., 7., 8.])]
        ```

        

    - 如果为数组则按数组中的**索引切分**，区间为左闭右开

        ```python
        arr = np.arange(9.0)
        arr
        >>> array([0., 1., 2., 3., 4., 5., 6., 7., 8.])
        
        # 按照数组中的索引切分，区间为左闭右开
        np.split(arr, [3, 5, 6, 10])
        >>> 
        [array([0., 1., 2.]),
         array([3., 4.]),
         array([5.]),
         array([6., 7., 8.]),
         array([], dtype=float64)]
        ```

        







---



## IO 操作

注意：Numpy 只要是一个数据操作的工具，文件的读取或者处理不是非常好。建议使用 Pandas 进行操作，Pandas 里也内置了 Numpy



- **读取操作 API：**

    ```python
    np.genfromtxt('文件路径', delimiter='分隔符')
    ```

    



- **什么是缺失值**

    Numpy 无法处理字符串，当读取字符串或者有缺失值的时候，反映到 ndarry 上就是 `nan`，`nan` 的类型是 numpy.float64

    



- **如何处理缺失值**
    - 直接删除具有缺失值的数据
    - 插补法把缺失值填补（平均值或中位数）






















# Pandas

<img src="doc/pic/README/Pandas_logo.svg" alt="Pandas_logo" style="zoom: 25%;" />

## 简介

- **Pandas 名字的解释：**
    - pan - pandel - 面板
    - da - data
    - panel 面板数据，来源于计量经济学，用于处理三维数据



- **特点**
    - 以 Numpy为基础，借力 Numpy 模块在计算方面性能高的优势
    - 基于 Matplotlib，能够简便的画图
    - 独特的数据结构



- **为什么使用 Pandas**

    Numpy 已经能够帮助我们处理数据，结合 matplotlib 解决部分数据展示等问题

    - 便捷的数据处理能力（比如处理 nan 值）
    - 读取文件方便（可以读取多种数据类型的数据）
    - 封装了 Matplotlib 和 Numpy 的画图和计算



- **Pandas 中的数据结构**
    - Series - 一维数据结构
    - DataFrame - 二维数据结构
    - Multilndex - 三维数据结构



**注意：pandas 在设计之初，默认为一行即为一个样本**

> 因为 Pandas 是内置了 Numpy，所以说 Numpy 所具有的函数 Pandas 也有，甚至做了一些拓展



![Pandas](doc/pic/README/Pandas.svg)

## DataFrame

Frame 是框架的意思

DataFrame 是一个类似于二维数组或表格(如excel)的对象，既有**行索引**，又有**列索引**

- **行索引**，表明不同行，横向索引，叫 `index` ，0轴，**axis=0**
- **列索引**，表名不同列，纵向索引，叫 `columns`，1轴，**axis=1**



**DataFrame 可以看作是，ndarry 外面包了一层行索引（index）和列索引（columns）**

---

### DataFrame 属性

| 属性                | 描述                                 |
| ------------------- | ------------------------------------ |
| `DataFrame.shape`   | DataFrame 的形状                     |
| `DataFrame.index`   | DataFrame 的**行**索引序列           |
| `DataFrame.columns` | DataFrame 的**列**索引序列           |
| `DataFrame.values`  | DataFrame 中的 array（除了行列索引） |
| `DataFrame.T`       | 转置 DataFrame                       |

---

### DataFrame 方法

| 方法                                                         | 描述                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| `pandas.DataFrame(数组或ndarry, index=行索引, columns=列索引)` | **返回**将 index 和 columns 与数组粘合的 DataFrame           |
| `DataFrame.head(N)`                                          | **返回**前 N 行数据，参数中如果不指定，默认 5 行             |
| `DataFrame.tail(N)`                                          | **返回**后 N 行数据，参数中如果不指定，默认 5 行             |
| `DataFrame.any()`                                            | **按列返回**属性（columns）中是否拥有 True<br />如果本属性中有一个 True 则返回 True；否则 False<br />**注意：** 前提 DataFrame 中要全为 Bool 值！ |
|                                                              |                                                              |



---

### DatatFrame 索引的设置

| 方法                                                   | 描述                                                         |
| ------------------------------------------------------ | ------------------------------------------------------------ |
| `DataFrame.index = 新索引值列表`                       | 修改行索引为新列表值                                         |
| `DataFrame.reset_index(drop=False)`                    | **返回**重置索引的 DaraFrame <br />`drop` 默认为 False，即不删除原来的索引，而是作为新的一列；如果为 True 则删除原来索引 |
| `DataFrame.set_index(新索引列名或列名列表, drop=True)` | **返回**把 DataFrame 的某一列作为新索引的新 DataFrame，不修改源数据 <br />`drop` 默认为 True，这一列作为新索引的同时是否删除原来的列 |



**以下是列表中方法的使用示例：**



- **修改行索引为新列表值**

    `DataFrame.index = 新索引值列表`

    

    比如：

    ```python
    # 必须全部修改
    label = ['股票_{}'.format(i) for i in range(10)]
    
    data.index = label
    
    >>> 
    
    			0			1			2			3			4
    股票_0	-1.896033	-0.655515	1.134985	-0.924127	0.565096
    股票_1	0.999411	0.372157	-0.506562	-1.492111	0.248759
    股票_2	0.933810	0.272780	-0.884243	-0.780605	-0.284011
    股票_3	-0.250099	-0.629845	-0.263016	1.014709	0.748039
    股票_4	0.212615	-0.301642	1.295189	-1.567214	-1.329128
    股票_5	0.720322	-0.721216	-0.269405	-0.066149	-0.874942
    股票_6	-0.730422	1.523008	-0.289108	1.446570	-0.422432
    股票_7	1.962097	-1.366396	-0.033190	0.831113	-1.177037
    股票_8	1.225902	-0.509225	-0.428516	-1.130633	-0.225949
    股票_9	-0.616889	1.140765	0.296491	-1.005518	1.494569
    ```

    

    **注意：以下修改方式是错误的**

    ```python
    # 不能直接用列表索引的方式修改！
    data.index[3] = '股票四'
    ```

    

- **重置索引**

    `DataFrame.reset_index(drop=False)`

    - **返回**重设索引的 DaraFrame
    - `drop` 默认为 False，不删除原来的索引，而是作为新的一列；如果为 True 则删除原来索引

    ```python
    data.reset_index()
    
    >>> 可以看到，原本的 index 没有被删除，而是作为了新的一列
    	index		0			1				2			3		4
    0	股票_0	-1.896033	-0.655515	1.134985	-0.924127	0.565096
    1	股票_1	0.999411	0.372157	-0.506562	-1.492111	0.248759
    2	股票_2	0.933810	0.272780	-0.884243	-0.780605	-0.284011
    3	股票_3	-0.250099	-0.629845	-0.263016	1.014709	0.748039
    4	股票_4	0.212615	-0.301642	1.295189	-1.567214	-1.329128
    5	股票_5	0.720322	-0.721216	-0.269405	-0.066149	-0.874942
    6	股票_6	-0.730422	1.523008	-0.289108	1.446570	-0.422432
    7	股票_7	1.962097	-1.366396	-0.033190	0.831113	-1.177037
    8	股票_8	1.225902	-0.509225	-0.428516	-1.130633	-0.225949
    9	股票_9	-0.616889	1.140765	0.296491	-1.005518	1.494569
    
    
    
    data.reset_index(drop=True)
    
    >>> 原本的 index 被删除
    		0			1				2			3		4
    0	-1.896033	-0.655515	1.134985	-0.924127	0.565096
    1	0.999411	0.372157	-0.506562	-1.492111	0.248759
    2	0.933810	0.272780	-0.884243	-0.780605	-0.284011
    3	-0.250099	-0.629845	-0.263016	1.014709	0.748039
    4	0.212615	-0.301642	1.295189	-1.567214	-1.329128
    5	0.720322	-0.721216	-0.269405	-0.066149	-0.874942
    6	-0.730422	1.523008	-0.289108	1.446570	-0.422432
    7	1.962097	-1.366396	-0.033190	0.831113	-1.177037
    8	1.225902	-0.509225	-0.428516	-1.130633	-0.225949
    9	-0.616889	1.140765	0.296491	-1.005518	1.494569
    ```

    

- **将某列设置为新索引**

    `DataFrame.set_index(作为新索引的列名或列名列表, drop=True)`

    - **返回**把 DataFrame 的某一列作为新索引的新 DataFrame，不修改源数据

    - `drop` 默认为 True，这一列作为新索引的同时是否删除原来的列

        ![image-20220205185109760](doc/pic/README/image-20220205185109760.png) 



​	**与此同时，如果设置多个列为索引，这样 DataFrame 就变成了一个具有 MultiIndex 的 DataFrame。**

​	![image-20220205185815739](doc/pic/README/image-20220205185815739.png)



## MultiIndex 与 Panel

### MultiIndex

MultiIndex 是**三维的数据结构**;

**多级索引（也称层次化索引）是 pandas 的重要功能，可以在 Series、DataFrame 对象上拥有 2个以及2个以上的索引。**

MultiIndex 多级索引中包含 index 属性，index 属性下又包含 names 和 levels



```python
tmp.index

>>> 
MultiIndex([( 1, 2012),
            ( 4, 2014),
            ( 7, 2013),
            (10, 2014)],
           names=['month', 'year'])
```



- **`index` 属性**

    - `names`: levels 的名称

        ```python
        tmp.index.names
        
        >>> FrozenList(['month', 'year'])
        ```

        

    - `levels`：每个 level 的元组值

        ```python
        tmp.index.names
        
        >>> FrozenList([[1, 4, 7, 10], [2012, 2013, 2014]])
        ```



- **MultiIndex 的创建**

    ```python
    arrays = [[1, 1, 2, 2], ['red', 'blue', 'red', 'blue']]
    pd.MultiIndex.from_arrays(arrays, names=('number', 'color'))
    
    # 结果
    MultiIndex([(1,  'red'),
                (1, 'blue'),
                (2,  'red'),
                (2, 'blue')],
               names=['number', 'color'])
    ```

​	可以用 `MultiIndex.levers[n]` 的方式查看指定的层面



### Pancel（不建议使用）

> **注：Pandas 从版本 0.20.0 开始弃用：推荐的用于表示 3D 数据的方法是通过 DataFrame 上的 MultiIndex 方法**

- **Panel的创建**
    - *class* `pandas.Panel(*data=None*, *items=None*, *major_axis=None*, *minor_axis=None*)`
        - 作用：存储3维数组的 Panel 结构
        - 参数：
            - **data** : ndarray 或者 dataframe
            - **items** : 索引或类似数组的对象，axis=0
            - **major_axis** : 索引或类似数组的对象，axis=1
            - **minor_axis** : 索引或类似数组的对象，axis=2

```python
p = pd.Panel(data=np.arange(24).reshape(4,3,2),
                 items=list('ABCD'),
                 major_axis=pd.date_range('20130101', periods=3),
                 minor_axis=['first', 'second'])

# 结果
<class 'pandas.core.panel.Panel'>
Dimensions: 4 (items) x 3 (major_axis) x 2 (minor_axis)
Items axis: A to D
Major_axis axis: 2013-01-01 00:00:00 to 2013-01-03 00:00:00
Minor_axis axis: first to second
```



- **查看 Panel 数据**

```
p[:,:,"first"]
p["B",:,:]
```





## Series

Series 是一个类似于**一维数组**的数据结构，它能够保存任何类型的数据，比如整数、字符串、浮点数等，**主要由一组数据和与之相关的索引两部分构成。**

- **Series 是一个带索引的一维数组**
- DataFrame 是 Series 的容器
- Pancel 是 DataFrame 的容器

<img src="doc/pic/README/image-20220205222205344.png" alt="image-20220205222205344" style="zoom:50%;" />

### Series 的创建

`pandas.Series(data=None, index=None, dtype=None)` **返回** Series

- 参数：
    - `data`：传入的数据，可以是 ndarray、list 等
    - `index`：索引，必须是唯一的，且与数据的长度相等。如果没有传入索引参数，则默认会自动创建一个从 0-N 的整数索引。
    - `dtype`：数据的类型



- **通过已有数据创建**

    ```python
    # 指定内容，默认索引
    
    pd.Series(np.arange(10))
    
    >>>
    0    0
    1    1
    2    2
    3    3
    4    4
    5    5
    6    6
    7    7
    8    8
    9    9
    dtype: int64
    ```

    

- **指定索引**

    ```python
    pd.Series([6.7,5.6,3,10,2], index=[1,2,3,4,5])
    
    >>> 
    1     6.7
    2     5.6
    3     3.0
    4    10.0
    5     2.0
    dtype: float64
    ```

    

- **通过字典数据创建**

    ```python
    color_count = pd.Series({'red':100, 'blue':200, 'green': 500, 'yellow':1000})
    color_count
    
    >>> 
    red        100
    blue       200
    green      500
    yellow    1000
    dtype: int64
    ```

---



### Series 的属性

为了更方便地操作 Series 对象中的索引和数据，**Series 中提供了两个属性 index 和 values**



- `index` 表示索引值的 ndarry

    ```python
    color_count.index
    
    >>>
    Index(['red', 'blue', 'green', 'yellow'], dtype='object')
    ```

    

- `values` 值列表

    ```python
    color_count.valuescolor_count.values
    
    >>>
    array([ 100,  200,  500, 1000])
    ```

    

- **使用索引来获取数据**

    ```python
    color_count[2]
    
    >>>
    500
    ```

    

---



## 基本数据操作

### 索引

Numpy 当中我们已经讲过使用索引选取序列和切片选择，Pandas 也支持类似的操作，也可以直接使用列名、行名称，甚至组合使用。

| 方法                                                         | 描述                                                 |
| ------------------------------------------------------------ | ---------------------------------------------------- |
| `DataFrame['列名']['行名']`                                  | 直接使用行列名称索引<br />**注意：先列后行**         |
| `DataFrame.loc['行名']['列名']`<br />`DataFrame.loc['行名', '列名']` | 使用名称索引且**先行后列**                           |
| `DataFrame.iloc[行下标, 列下标]`                             | 使用**下标**索引且**先行后列**                       |
| 【已废弃 API】`DataFrame.ix[下标或名称, 下标或名称]`         | **ix 组合索引**；注意，0.20.0 之后的版本可能不再支持 |



---

- **直接使用行列索引 (先列后行)**

    ```python
    # 直接使用行列索引名字的方式（先列后行）
    data['open']['2018-02-27']
    23.53
    
    # 【ERROR】不支持的操作
    data['2018-02-27']['open']  # 错误
    data[:1, :2]  # 错误
    ```

    

- 使用名称索引且**先行后列**

    ```python
    data.loc['2018-02-27':'2018-02-22']['open']
    
    >>>
    2018-02-27    23.53
    2018-02-26    22.80
    2018-02-23    22.88
    2018-02-22    22.25
    Name: open, dtype: float64
            
            
            
    data.loc['2018-02-27':'2018-02-22', 'open']
    
    >>>
    2018-02-27    23.53
    2018-02-26    22.80
    2018-02-23    22.88
    2018-02-22    22.25
    Name: open, dtype: float64
    ```

    

- 使用**下标**索引且**先行后列**

    ```python
    # 使用iloc可以通过索引的下标去获取
    # 获取前3天数据,前5列的结果
    data.iloc[:3, :5]
    
    >>>
    			open	high	close	low		volume
    2018-02-27	23.53	25.88	24.16	23.53	95578.03
    2018-02-26	22.80	23.78	23.53	22.80	60985.11
    2018-02-23	22.88	23.37	22.82	22.71	52914.01
    ```

    

### 赋值操作

- 将 DataFrame 中的某一列都修改为一个指定的值

    ```python
    data.head()
    >>>
    
    			open	high	close	low	volume	price_change	p_change	turnover
    2018-02-27	23.53	25.88	24.16	23.53	95578.03	0.63	2.68	2.39
    2018-02-26	22.80	23.78	23.53	22.80	60985.11	0.69	3.02	1.53
    2018-02-23	22.88	23.37	22.82	22.71	52914.01	0.54	2.42	1.32
    2018-02-22	22.25	22.76	22.28	22.02	36105.01	0.36	1.64	0.90
    2018-02-14	21.49	21.99	21.92	21.48	23331.04	0.44	2.05	0.58
    
    # 方法 1
    data['open'] = 66
    
    # 方法 2
    data.open = 77
    ```

    



---



### 排序

排序有两种形式，一种按照**索引 (index) 进行排序**，一种**按照内容 (values) 排序**



#### DataFrame 排序

- **按照内容 (values) 排序**

    `DataFrame.sort_values(by='列名', ascending=True)` 按照单个建或多个键进行排序

    - `by` 按哪一列进行排序，可以使用列表来指定按多个列进行排序
    - `ascending` 默认为 True 按升序排列；如果指定为 False 则按降序排列

    ```python
    data.sort_values('high', ascending=False).head()
    
    >>> 
    		open	high	close	low	volume	price_change	p_change	turnover
    2015-06-10	77	36.35	33.85	32.23	269033.12	0.51	1.53	9.21
    2015-06-12	77	35.98	35.21	34.01	159825.88	0.82	2.38	5.47
    2017-10-31	77	35.22	34.44	32.20	361660.88	2.38	7.42	9.05
    2015-06-15	77	34.99	31.69	31.69	199369.53	-3.52	-10.00	6.82
    2015-06-11	77	34.98	34.39	32.51	173075.73	0.54	1.59	5.92
    
    
    # 按照多个键进行排序
    data.sort_values(by=['open', 'high']).head()
    ```



- **按照索引 (index) 排序**

    `DataFrame.sort_index()`

    

    这个股票的日期索引原来是从大到小，现在重新排序，从小到大

    ```python
    data.sort_index().head()
    
    >>>
    
    		open	high	close	low		volume	price_change	p_change	turnover
    2015-03-02	77	12.67	12.52	12.20	96291.73	0.32	2.62	3.30
    2015-03-03	77	13.06	12.70	12.52	139071.61	0.18	1.44	4.76
    2015-03-04	77	12.92	12.90	12.61	67075.44	0.20	1.57	2.30
    2015-03-05	77	13.45	13.16	12.87	93180.39	0.26	2.02	3.19
    2015-03-06	77	14.48	14.28	13.13	179831.72	1.12	8.51	6.16
    ```

    

---

#### Series 排序

- **按照内容 (values) 排序**

    因为 Series 只有一列，所以在排序时不需要参数

    `series.sort_values(ascending=True)`

    - `ascending` 默认为 True 按升序排列；如果指定为 False 则按降序排列

    

    ```python
    data.volume.sort_values().head()  # data.volume 是从 data 中取出了一列
    
    >>>
    2016-07-06     1158.12
    2017-02-03     8275.00
    2017-01-25    10523.48
    2017-01-26    11587.02
    2017-01-23    11590.10
    Name: volume, dtype: float64
    ```

    

- **按照索引 (index) 排序**

    `DataFrame.sort_index()`

    

    ```python
    data['p_change'].sort_index().head()
    
    >>>
    2015-03-02    2.62
    2015-03-03    1.44
    2015-03-04    1.57
    2015-03-05    2.02
    2015-03-06    8.51
    Name: p_change, dtype: float64
    ```

    

### 运算

#### 算数运算

可以使用提供的方法，也可直接使用算术运算符。就像在 Numpy 当中一样，如果不指定哪一行或哪一列，则作用于所有的元素

| 方法                                        | 描述                                |
| ------------------------------------------- | ----------------------------------- |
| `DataFrame.add(num)`<br />`DataFrame + num` | 对 DataFrame 中所有的元素都加上 num |
| `DataFrame.sub(num)`<br />`DataFrame - num` | 对 DataFrame 中所有的元素都减去 num |
| `Series.add(num)`<br />`Series + num`       | 对 Series 中所有的元素都加上 num    |
| `Series.sub(num)`<br />`Series - num`       | 对 Series 中所有的元素都减去 num    |



---



#### 逻辑运算

- **基本操作**

    可以直接使用运算符（`> < = | &`）进行操作，返回对应布尔值的结果

    ```python
    data['high'] > 20
    ```

    

- **【重点】布尔索引**

    逻辑判断的结果可以作为筛选的依据

    ```python
    # 逻辑判断的结果可以作为筛选的依据
    data[data['high'] > 20].head()
    
    >>>
    
    			open	high	close	low	volume	price_change	p_change	turnover
    2018-02-27	77	25.88	24.16	23.53	95578.03	0.63	2.68	2.39
    2018-02-26	77	23.78	23.53	22.80	60985.11	0.69	3.02	1.53
    2018-02-23	77	23.37	22.82	22.71	52914.01	0.54	2.42	1.32
    2018-02-22	77	22.76	22.28	22.02	36105.01	0.36	1.64	0.90
    2018-02-14	77	21.99	21.92	21.48	23331.04	0.44	2.05	0.58
    ```

- 完成多个逻辑判断

    ```python
    # 完成多个逻辑判断
    data[(data['high'] > 20) & (data['high'] < 23)].head()
    
    >>>
    
    		open	high	close	low	volume	price_change	p_change	turnover
    2018-02-22	77	22.76	22.28	22.02	36105.01	0.36	1.64	0.90
    2018-02-14	77	21.99	21.92	21.48	23331.04	0.44	2.05	0.58
    2018-02-13	77	21.90	21.48	21.31	30802.45	0.28	1.32	0.77
    2018-02-12	77	21.40	21.19	20.63	32445.39	0.82	4.03	0.81
    2018-02-09	77	21.46	20.36	20.19	54304.01	-1.50	-6.86	1.36
    ```



- **逻辑运算函数**

    - 【推荐】`data.query(expr)` **返回**符合条件值的表

        - exper 查询**字符串**

        ```python
        data.query('high > 20 & high < 23').head()
        
        >>>
        		open	high	close	low	volume	price_change	p_change	turnover
        2018-02-22	77	22.76	22.28	22.02	36105.01	0.36	1.64	0.90
        2018-02-14	77	21.99	21.92	21.48	23331.04	0.44	2.05	0.58
        2018-02-13	77	21.90	21.48	21.31	30802.45	0.28	1.32	0.77
        2018-02-12	77	21.40	21.19	20.63	32445.39	0.82	4.03	0.81
        2018-02-09	77	21.46	20.36	20.19	54304.01	-1.50	-6.86	1.36
        ```

        

    - `data.isin(values)` **返回**值是否在 values 中的列表

        - values 值或值的列表

        ```python
        data['turnover'].isin([4.19, 2.39])
        
        >>>
        2018-02-27     True
        2018-02-26    False
        2018-02-23    False
        2018-02-22    False
        2018-02-14    False
                      ...  
            
            
        # 可以指定值进行一个判断，从而进行筛选操作
        data[data['turnover'].isin([4.19, 2.39])].head()
        >>>
        		open	high	close	low	volume	price_change	p_change	turnover
        2018-02-27	77	25.88	24.16	23.53	95578.03	0.63	2.68	2.39
        2017-07-25	77	24.20	23.70	22.64	167489.48	0.67	2.91	4.19
        2016-09-28	77	20.98	20.86	19.71	95580.75	0.98	4.93	2.39
        2015-04-07	77	17.98	17.54	16.50	122471.85	0.88	5.28	4.19
        ```



---



#### 统计运算

> 注意：是按列（columns）进行运算的，因为按行（index）是没有意义的



- `DataFrame.describe()` 综合分析

    综合分析: 能够直接得出很多统计结果 `count`, `mean`, `std`, `min`, `max` 等

    ```python
    data.describe()
    
    >>>
    ```
    
    ![image-20220206172810145](doc/pic/README/image-20220206172810145.png)





- Numpy 当中已经详细介绍， min(最小值), max(最大值), mean(平均值), median(中位数), var(方差), std(标准差), mode(众数)

    | 方法     | 描述                                                         |
    | -------- | ------------------------------------------------------------ |
    | `count`  | Number of non-NA observations                                |
    | `sum`    | **Sum of values**                                            |
    | `mean`   | **Mean of values**                                           |
    | `median` | 中位数 Arithmetic median of values                           |
    | `min`    | **Minimum**                                                  |
    | `max`    | **Maximum**                                                  |
    | `mode`   | Mode                                                         |
    | `abs`    | Absolute Value                                               |
    | `prod`   | Product of values                                            |
    | `std`    | 标准差 **Bessel-corrected sample standard deviation**        |
    | `var`    | 方差 **Unbiased variance**                                   |
    | `idxmax` | compute the index labels with the maximum。含义是 idx 的含义是 index |
    | `idxmin` | compute the index labels with the minimum                    |

    **对于单个函数去进行统计的时候，坐标轴还是按照默认列“columns” (axis=0, default)，如果要对行“index” 需要指定(axis=1)**

    

    ```python
    # 使用统计函数：0 代表列求结果， 1 代表行求统计结果
    data.max(axis=0)
    >>>
    open                   34.99
    high                   36.35
    close                  35.21
    low                    34.01
    volume             501915.41
    price_change            3.03
    p_change               10.03
    turnover               12.56
    my_price_change         3.41
    dtype: float64
    
    
    # 求出最大值的位置
    data.idxmax(axis=0)
    >>>
    open               2015-06-15
    high               2015-06-10
    close              2015-06-12
    low                2015-06-12
    volume             2017-10-26
    price_change       2015-06-09
    p_change           2015-08-28
    turnover           2017-10-26
    my_price_change    2015-07-10
    dtype: object
    
    
    # 求出最小值的位置
    data.idxmin(axis=0)
    >>>
    open               2015-03-02
    high               2015-03-02
    close              2015-09-02
    low                2015-03-02
    volume             2016-07-06
    price_change       2015-06-15
    p_change           2015-09-01
    turnover           2016-07-06
    my_price_change    2015-06-15
    dtype: object
    ```



- **累计统计函数**

    | **函数**  | **作用**                    |
    | --------- | --------------------------- |
    | `cumsum`  | 计算前 1/2/3/…/n 个数的和 |
    | `cummax`  | 计算前 1/2/3/…/n 个数的最大值 |
    | `cummin`  | 计算前 1/2/3/…/n 个数的最小值 |
    | `cumprod` | 计算前 1/2/3/…/n 个数的积     |

    

    ```python
    # 先对时间进行排序
    data['p_change'].sort_index().cumsum().plot()  # 可以直接调用 .plot() 进行绘图；但如果想要一个更好的效果，建议导入 plt 绘制
    ```

    ![image-20220206173409914](doc/pic/README/image-20220206173409914.png)

---

#### 自定义运算

- `apply(func, axis=0)`
    - `func`:自定义函数
    - `axis=0`:默认是列，`axis=1` 为行进行运算



```python
data[['open', 'close']].apply(lambda x: x.max() - x.min(), axis=0)

>>>
open      0.00
close    22.85
dtype: float64
```



---



## Pandas 画图

- DataFrame 画图

`DataFrame.plot(x=None, y=None, kind='line')`

- `kind` string 类型
    - `'line'` 折线图
    - `'bar'`柱状图
    - `'scatter'`散点图
    - `'barh'`水平条形图 （http://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.plot.barh.html）
    - `'hist'`直方图
    - `'pie'`饼图

> 更多细节：https://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.plot.html?highlight=plot#pandas.DataFrame.plot



```python
data.plot(x='p_change', y='low', kind='scatter')
```

![image-20220206202248592](doc/pic/README/image-20220206202248592.png)





---



## 文件的读取与存储

我们的数据大部分存在于文件当中，Pandas 支持复杂的IO操作，Pandas 的 API 支持众多的文件格式，如 CSV、SQL、XLS、JSON、HDF5。

> 注：最常用的 HDF5 和 CSV 文件

![Pandes读取存储](doc/pic/README/Pandes读取存储.png)



### CSV

- **CSV 文件的读取**

    `pandas.read_csv(filepath_or_buffer, sep =',', usecols=[])`

    - `filepath_or_buffer` 文件路径
    - `sep`  分隔符，默认用 `,`隔开
    - `usecols` 指定读取的列名，列表形式

    > 注意：如果 CSV 文件中没有存储列名（columns），那么在使用 API 读取的时候就一定要显示的在 `usecols` 中指定列名是什么，否则会把第一行数据作为列名

    ```python
    # 举例：读取之前的股票的数据
    # 读取文件,并且指定只获取'open', 'close'指标
    data = pd.read_csv("./data/stock_day.csv", usecols=['open', 'close'])
    
    >>>
    
    ```

    

- **CSV 文件的写入**

    `DataFrame.to_csv(path_or_buf=None, sep=',', columns=None, header=True, index=True, mode='w', encoding=None)`

    - `path_or_buf` 文件路径

    - `sep` 分隔符，默认用 `,` 隔开

    - `columns` 选择需要写入文件的列索引

    - `header` 默认为 True，是否写进**列（columns）**索引值

    - `index` 是否写进**行（index）**索引

    - `mode` 'w'：重写；'a' 追加在文件末尾

        

    ```python
    # 选取10行数据保存,便于观察数据
    data[:10].to_csv('./data/test/test.csv', columns=['open'])
    
    # 读取，查看结果
    pd.read_csv('./data/test/test.csv')
    >>>
    	Unnamed: 0    open
    0    2018-02-27    23.53
    1    2018-02-26    22.80
    2    2018-02-23    22.88
    3    2018-02-22    22.25
    4    2018-02-14    21.49
    5    2018-02-13    21.40
    6    2018-02-12    20.70
    7    2018-02-09    21.20
    8    2018-02-08    21.79
    9    2018-02-07    22.69
    
    
    # 会发现将索引存入到文件当中，变成单独的一列数据。如果需要删除，可以指定index参数,删除原来的文件，重新保存一次。
    data[:10].to_csv('./data/test/test.csv', columns=['open'], index=False)
    
    >>>
    open
    23.53
    22.8
    22.88
    22.25
    21.49
    21.4
    20.7
    21.2
    21.79
    22.69
    ```

    

---



### HDF5

- **HDF5 特点**
    - **【重点】HDF5 存储的是三维数据，可以说是同时存放多个二维数据**
    - HDF5 是二进制文件
    - 文件后缀是 `h5`



**注意：优先选择使用 HDF5 文件存储**

- HDF5 在存储的时候支持压缩，**使用的方式是 blosc，这个是速度最快**的也是 pandas 默认支持的
- 使用压缩可以**提磁盘利用率，节省空间**
- HDF5 还是跨平台的，可以轻松迁移到 hadoop 上面





- **HDF5 文件的读取**

    `pandas.read_hdf(path_or_buf，key=None，**kwargs)`

    - `path_or_buffer` 文件路径
    - `key` 读取的键（二维数据的名称），如果一个 h5 文件中有**多个**二维数据，则需指定此键。否则报错

    ```python
    # 读取
    data = pd.read_hdf('./data/stock_day/hdf5/day_high.h5')
    data.head()
    
    # 如果文件中有多个二维数据，如果不指定 key 会报错
    data = pd.read_hdf('./data/test/test.h5', key='key2')
    data
    ```

    





- **HDF5 文件的写入**

    `DataFrame.to_hdf(path_or_buf, key, **kwargs)`

    - `path_or_buffer` 文件路径
    - `key` 写入此键的键名称（二维数据的名称），**写入的时候必须指定此键！**

    ```python
    # 后 10 行
    # 写入, 写入的时候必须指定 key ！
    data[-10:].to_hdf('./data/test/test.h5', key='key2')
    ```

    



---



### JSON

JSON 是我们常用的一种数据交换格式，前面在**前后端的交互**经常用到，也会在存储的时候选择这种格式。所以我们需要知道 Pandas 如何进行读取和存储 JSON 格式。



- **JSON 文件的读取**

`json_read = pandas.read_json('路径', orient='records', lines=True)`

将 JSON 格式转换成默认的Pandas DataFrame 格式

- `orient` 指定存储的 json 格式，通常使用 `records`
- `lines` 指定按照行去变成一个样本



- **JSON 文件的写入**

`DataFrame.to_json(path_or_buf=None, orient=None, lines=False)`

将Pandas 对象存储为json格式

- `path_or_bufNone` 文件地址
- `orient` 存储的json形式，{‘split’,’records’,’index’,’columns’,’values’}
- `lines` 一个对象存储为一行





## 缺失值处理

处理缺失值的思路：

- 删除带有缺失值的样本
- 插补/替换



**当我们读取的数据中有缺失值时，pandas 中表示为为 `NaN` (Not a Number，类型为 float)。在处理缺失值时，需要有一下步骤：**

1. **判断数据中是否存在** `NaN` 或 `None`

    > 使用 pandas.isnull(DataFrame) 或 .isnull(DataFrame) 也可以，这两个其实是 isna/notna 的别名

    - `pandas.isna(DataFrame)` 会在**是**缺失值的地方标记为 True
    - `pandas.notna(DataFrame)` 会在**不是**缺失值的地方标记为 True



2. **处理缺失值**

    - **删除含有缺失值的样本**

        `DataFrame.dropna(inplace=False)`

        `inplace` 如果标记为 True 会直接修改本 DataFrame，而如果为 False 则不会直接修改本数组，而是**返回**新数组（默认即为 False）

        

    - **替换/插补**

        `DataFrame.fillna(value=要填补的值, inplace=False)`

        `inplace` 如果标记为 True 会直接修改本 DataFrame，而如果为 False 则不会直接修改本数组，而是**返回**新数组（默认即为 False）

        

3. **如果缺失值没有标记为 `NaN`，比如空格、问号等**

    - 将其他字符换成 `NaN`，也就是 `numpy.nan` 再进行替换；**注意：是 `numpy` 不是 `pandas`！**

        替换的 API：`DataFrame.replace(to_place='要替换的字符', value=NUMPY.nan)`



---



- 处理 `NaN` 的方法

```python
import pandas as pd
import numpy as np

# 1. 读取数据
data = pd.read_csv('./data/IMDB-Movie-Data.csv')


# 2. 判断缺失值是否存在（法一）
pd.isna(data)  # 在是 NaN | None 的地方标记为 True
pd.notna(data)  # 在不是 NaN | None 的地方标记为 True

np.any(pd.isna(data))  # 借助 numpy 的 any 函数进行判断
np.all(pd.notna(data))

pd.isna(data).any()  # 【重点】会按照列进行返回，那些列中有 True
pd.notna(data).all()

# 删除带有缺失值的样本, 参数 inplace 默认为 False 即返回新 DataFrame
data.dropna()


# 3. 处理缺失值
# 使用插补法分别处理含有缺失值的两列（采用平均值）
data['Revenue (Millions)'].fillna(value=data['Revenue (Millions)'].mean(), inplace=True)
# 使用插补法分别处理含有缺失值的两列（采用平均值）
data['Metascore'].fillna(value=data['Metascore'].mean(), inplace=True)

pd.isnull(data).any()

```



- 如果为其他标识的缺失值，比如 `?`

    ```python
    # 全局取消证书验证
    import ssl
    ssl._create_default_https_context = ssl._create_unverified_context
    
    data = pd.read_csv('https://archive.ics.uci.edu/ml/machine-learning-databases/breast-cancer-wisconsin/breast-cancer-wisconsin.data')
    
    # 把一些其它值标记的缺失值，替换成 np.nan
    data = data.replace(to_replace='?', value=np.nan)
    
    # 这里采用删除缺失值的方式
    data = data.dropna()
    ```

    



---





## 数据离散化

- **为什么要数据离散化？** 

    连续属性离散化的目的是为了简化数据结构，**数据离散化技术可以用来减少给定连续属性值的个数**。离散化方法经常作为数据挖掘的工具。



- **什么是数据离散化？**

    **连续属性的离散化就是在连续属性的值域上，将值域划分为若干个离散的区间，最后用不同的符号或整数** **值代表落在每个子区间中的属性值。**

    离散化有很多种方法，这使用一种最简单的方式去操作

    - 原始人的身高数据：165，174，160，180，159，163，192，184

    - 假设按照身高分几个区间段：150~165, 165~180, 180~195

    这样我们将数据分到了三个区间段，我可以对应的标记为矮、中、高三个类别，最终要处理成一个"**哑变量**"矩阵



例子：假如要表示动物狗、猫、狐狸，在计算机中可以表示为：狗-1、猫-2、狐狸-3；这样带来了一个问题**数值的差异导致了类别的不平衡**，会让人或计算机误以为狐狸-3 的优先级大于为 1 的狗。如果要解决这个问题，可以将他们重新表示为：狗-001、猫-010、狐狸-100，这种**编码方式叫做 one-hot 编码或或热编码或哑变量**

|      | 狗   | 猫   | 狐   |
| ---- | ---- | ---- | ---- |
| A    | 0    | 0    | 1    |
| B    | 0    | 1    | 0    |
| C    | 1    | 0    | 0    |





---



**pandas 中进行数据离散化的步骤：**

1. **分组**

    - 自动分组：`Series = pandas.qcut(x=一维数据, q=分成几组)` **返回**离散化的 Series
    - 自定义切分：`Series = pandas.cut(x=一维数据, , bins=[按哪些数值切分])` **返回**离散化的 Series


    - 自定义分组：`Series = pandas.cut(x=一维数据, bins=[])`
    
      > 使用 `Series.value_counts()` 方法可以查看每个分组中元素的数量


​        


2. **将分组好的结果转换为 one-hot 编码或哑变量**
    - `DataFrame = pandas.get_dummies(data=Series, prefix='前缀')` **返回**离散化的 Series 为 DataFrame



**示例：**

```python
# 1. 读取数据
data = pd.read_csv('./data/stock_day/stock_day.csv', usecols=['p_change'])


# 2. 进行分组
sr = pd.qcut(x=data['p_change'], q=10)  # qcut 自动分组
sr = pd.cut(x=data['p_change'], bins=[-100, -7, -5, -3, 0, 3, 5, 7, 100])  # cut 自定义分组

sr
>>> index 没变，但列变成了对应的区间，而不是具体值
2018-02-27      (0, 3]
2018-02-26      (3, 5]
2018-02-23      (0, 3]
2018-02-22      (0, 3]
2018-02-14      (0, 3]
                ...   
2015-03-06    (7, 100]
2015-03-05      (0, 3]
2015-03-04      (0, 3]
2015-03-03      (0, 3]
2015-03-02      (0, 3]
Name: p_change, Length: 643, dtype: category
Categories (8, interval[int64, right]): [(-100, -7] < (-7, -5] < (-5, -3] < (-3, 0] < (0, 3] < (3, 5] < (5, 7] < (7, 100]]


sr.value_counts()  # 查看每个分组中元素的数量
>>>
(0, 3]        215
(-3, 0]       188
(3, 5]         57
(-5, -3]       51
(5, 7]         35
(7, 100]       35
(-100, -7]     34
(-7, -5]       28
Name: p_change, dtype: int64
 
 
 # 3. 将分组好的结果转换为 one-hot 编码或哑变量
sr = pd.get_dummies(data=sr, prefix='股票')
>>> 
股票_(-100, -7]	股票_(-7, -5]	股票_(-5, -3]	股票_(-3, 0]	股票_(0, 3]	股票_(3, 5]	股票_(5, 7]	股票_(7, 100]
2018-02-27	0	0	0	0	1	0	0	0
2018-02-26	0	0	0	0	0	1	0	0
2018-02-23	0	0	0	0	1	0	0	0
2018-02-22	0	0	0	0	1	0	0	0
2018-02-14	0	0	0	0	1	0	0	0
...	...	...	...	...	...	...	...	...
2015-03-06	0	0	0	0	0	0	0	1
2015-03-05	0	0	0	0	1	0	0	0
2015-03-04	0	0	0	0	1	0	0	0
2015-03-03	0	0	0	0	1	0	0	0
2015-03-02	0	0	0	0	1	0	0	0
643 rows × 8 columns
```



## 合并处理

> 回顾 numpy 拼接方法：
>
> - 水平拼接
>
>     `numpy.hstack()`
>
> - 竖直拼接
>
>     `numpy.vstack`
>
> - 指定拼接方向
>
>     `numpy.concatnate()`



### concat

**pandas 按指定轴方向拼接：**

- `pandas.concat([data1, data2, ...], axis=0)` 默认 axis=0 即竖直拼接，指定为 1 可按行拼接

    **注意：**如果索引（index）不一致的情况下进行按列拼接，则效果类似于数据库中的 `FULL JOIN` 效果

    

    **正常拼接：**

    <img src="doc/pic/README/image-20220215185340085.png" alt="image-20220215185340085" style="zoom:30%;" />

    

    **索引（index）不一致的情况下进行按列拼接拼接：**

    <img src="doc/pic/README/image-20220215185418869.png" alt="image-20220215185418869" style="zoom:30%;" />



---



### merge

`pandas.merge(left=左表, right=右表, how='合并方式', on=['键1', '键2', ...])` 将表按照两组数据的共同键值对合并（类似数据库中连接）

- `how` 表示按什么方式连接，可以有：`left` | `right` | `inner` | `outer`，默认为 `inner`



- **内连接（默认）**

    即为按 key 保留左右表共同键

    ```python
    tb_left = pd.DataFrame({'key1': ['K0', 'K0', 'K1', 'K2'],
                            'key2': ['K0', 'K1', 'K0', 'K1'],
                            'A': ['A0', 'A1', 'A2', 'A3'],
                            'B': ['B0', 'B1', 'B2', 'B3']})
    
    tb_right = pd.DataFrame({'key1': ['K0', 'K1', 'K1', 'K2'],
                            'key2': ['K0', 'K0', 'K0', 'K0'],
                            'C': ['C0', 'C1', 'C2', 'C3'],
                            'D': ['D0', 'D1', 'D2', 'D3']})
    
    # 默认内连接
    pd.merge(left=tb_left, right=tb_right, on=['key1', 'key2'])
    ```

    <img src="doc/pic/README/内连接.png" alt="内连接" style="zoom:50%;" />

    

- **左连接**

    保留左表所有键

    ```python
    # 左连接
    pd.merge(left=tb_left, right=tb_right, how='left', on=['key1', 'key2'])
    ```

    <img src="doc/pic/README/左连接.png" alt="左连接" style="zoom:50%;" />

    

- **右连接**

    保留右表所有键

    ```python
    # 右连接
    pd.merge(left=tb_left, right=tb_right, how='right', on=['key1', 'key2'])
    ```

    <img src="doc/pic/README/右连接.png" alt="右连接" style="zoom:50%;" />

    

- **外连接**

    保留左右表所有键
    
    ```python
    # 外连接
    pd.merge(left=tb_left, right=tb_right, how='outer', on=['key1', 'key2'])
    ```
    
    <img src="doc/pic/README/外链接.png" alt="外链接" style="zoom:50%;" />



---



## 交叉表和透视表

**应用场景：找到两个变量之间的关系**

- **交叉表：**

    交叉表用于**计算一列数据对于另外一列数据的分组个数(用于统计分组频率的特殊透视表)**

    也就是**把`参数 index` 的列作为新的 index，`参数 columns` 的列做为新的 columns**

    - `pd.crosstab(index=表[列], columns=表[列])`

    

- **透视表：**

    透视表是将原有的 **DataFrame 的列分别作为行索引和列索引，然后对指定的列应用聚集函数**

    - `DataFrame.pivot_table([], index=[])`





比如：

探究股票的涨跌与星期几有关？

以下图当中表示，week 代表星期几，1,0 代表这一天股票的涨跌幅是好还是坏，里面的数据代表比例

可以理解为所有时间为星期一等等的数据当中涨跌幅好坏的比例

- **使用交叉表**

```python
# 目的：星期几以及涨跌幅是否好坏
# 最终形式：`pd.crosstab(星期数据列, 涨跌幅数据列)`


#  1. 准备数据
stock_day = pd.read_csv('./data/stock_day/stock_day.csv')


# 2. 将日期处理为星期几
date = pd.to_datetime(stock_day.index)
weekday = date.weekday + 1  # 注意，这里的星期是从 0 开始的


# 3. 添加星期几为新数据列
stock_day['weekday'] = weekday


# 4. 将涨跌处理为 0 或 1（0 位跌，1 位涨），并添加为新列
stock_day['pona'] = np.where(stock_day.p_change > 0, 1, 0)


# 5. 调用交叉表 API，输出涨的数量和跌的数量
ct = pd.crosstab(stock_day.weekday, stock_day.pona)


# 6.转换为百分比（每行的总数 / 每行）
ct_div = ct.sum(axis=1)
result = ct.div(ct_div, axis=0)  # 注意行列


# 7. 绘制图像
result.plot(kind='bar', stacked=True)  # 第二个参数为是否堆叠显示
```

<img src="doc/pic/README/image-20220216180227978.png" alt="image-20220216180227978" style="zoom:50%;" />

- **使用透视表**

    ```python
    # 使用透视表，相当于
    
    #  1. 准备数据
    stock_day = pd.read_csv('./data/stock_day/stock_day.csv')
    date = pd.to_datetime(stock_day.index)
    weekday = date.weekday + 1  # 注意，这里的星期是从 0 开始的
    stock_day['weekday'] = weekday
    stock_day['pona'] = np.where(stock_day.p_change > 0, 1, 0)
    
    
    # 2. 调用透视表 API
    stock_day.pivot_table(['pona'], index=['weekday'])  # 透视表直接能出值为 1 所占的比例
    ```

    

---





## 分组与聚合

交叉表和透视表其实也是一种分组与聚合。

**pandas 中的数据很像数据库总的** `GROUP BY`，可以对 DataFrame 和 Series 进行操作。**但在 pandas中，抛开聚合谈分组，无意义**

<img src="doc/pic/README/分组聚合原理.png" alt="分组聚合原理" style="zoom:50%;" />

- `DataFrame.groupby(by=[按哪种index分组], as_index=False)`  **分组**

    - `by` 按哪一（些）列分组，也就是数据库中 `GROUP BY` 哪些属性
    - `as_index` 要分组的列是否作为结果的 `index`，默认为 False

    

    **注意！分组后只会返回一个 GroupBy 对象，并不会返回 DataFrame 或者 Series，必须再调用聚合函数才可以进行显示！**，聚合函数也就是 `min() | max() | count() | sum() ...` 这些

    

- **简单分组演示**

    ```python
    # 案例:不同颜色的不同笔的价格数据
    col =pd.DataFrame({'color': ['white','red','green','red','green'], 'object': ['pen','pencil','pencil','ashtray','pen'],'price1':[5.56,4.20,1.30,0.56,2.75],'price2':[4.75,4.12,1.60,0.75,3.15]})
    
    col.groupby(by=['color'])
    >>>
    <pandas.core.groupby.generic.DataFrameGroupBy object at 0x14ef5f7f0>
    
    # 按照 DataFrame 的方式分组（建议使用此方式）
    col.groupby(by=['color'])['price1'].sum()
    >>>
    color
    green    4.05
    red      4.76
    white    5.56
    Name: price1, dtype: float64
            
            
    # 按照 Series 的方式分组，先取出需要的列
    col['price1'].groupby(by=col['color']).mean()
    >>>
    color
    green    2.025
    red      2.380
    white    5.560
    Name: price1, dtype: float64
    ```



- **【案例】星巴克零售数据**

    现在我们有一组关于全球星巴克店铺的统计数据，如果我想知道美国的星巴克数量和中国的哪个多，或者我想知道中国每个省份星巴克的数量的情况，那么应该怎么办？

    ```python
    starbucks = pd.read_csv('./data/starbucks.csv')
    
    # 按照国家分组，求出每个国家的星巴克零售店数量
    sb_count = starbucks.groupby(by=['Country'])['Brand'].count()
    
    # 进行画图
    sb_count.sort_values(ascending=False).plot(kind='bar', figsize=(20, 8))
    
    # 假设我们加入省市一起进行分组
    sb_sount2 = starbucks.groupby(by=['State/Province', 'City']).count()  # 【重点】会返回类似 MultIndex 的结构
    ```

    ![image-20220216202314435](doc/pic/README/image-20220216202314435.png)



## 案例（电影）

对于这一组电影数据，如果我们希望统计电影分类(genre)的情况，应该如何处理数据？

![image-20220217124002971](doc/pic/README/image-20220217124002971.png)



思路分析：

1、创建一个全为0的dataframe，列索引置为电影的分类，temp_df

2、遍历每一部电影，temp_df中把分类出现的列的值置为1

3、求和



```python
# 1. 拿到电影类型的 Series
movies['Genre']
>>>
0       Action,Adventure,Sci-Fi
1      Adventure,Mystery,Sci-Fi
2               Horror,Thriller
3       Animation,Comedy,Family
4      Action,Adventure,Fantasy
                 ...           
995         Crime,Drama,Mystery
996                      Horror
997         Drama,Music,Romance
998            Adventure,Comedy
999       Comedy,Family,Fantasy
Name: Genre, Length: 1000, dtype: object
            
            
# 2. 转换为列表格式
# 可以使用 for 循环，也可以使用【列表生成式】
genre = [i.split(',') for i in movies['Genre']]  # i 是 string 类型
>>>
[['Action', 'Adventure', 'Sci-Fi'],
 ['Adventure', 'Mystery', 'Sci-Fi'],
 ['Horror', 'Thriller'],
 ['Animation', 'Comedy', 'Family'],
 ['Action', 'Adventure', 'Fantasy'],
 ['Action', 'Adventure', 'Fantasy'],
 
 
 # 3. 统计电影种类共有多少
[j for i in genre for j in i]
>>>
 ['Action',
 'Adventure',
 'Sci-Fi',
 'Adventure',
 'Mystery',
 'Sci-Fi',
 'Horror',
 'Thriller',
  
movies_types = np.unique([j for i in genre for j in i])
>>>
  array(['Action', 'Adventure', 'Animation', 'Biography', 'Comedy', 'Crime',
       'Drama', 'Family', 'Fantasy', 'History', 'Horror', 'Music',
       'Musical', 'Mystery', 'Romance', 'Sci-Fi', 'Sport', 'Thriller',
       'War', 'Western'], dtype='<U9')
  
num_type = len(movies_types)
>>>
  20
  
  
# 4. 创建一个全为 0 的 DataFrame，然后把每一个电影（行）对应的种类（列）置为 1
tmp_zeros_ndarry = np.zeros(shape=(movies.shape[0], num_type), dtype=np.int32)

df_gener = pd.DataFrame(tmp_zeros_ndarry, index=movies['Title'], columns=movies_types)
>>>
  
Action	Adventure	Animation	Biography	Comedy	Crime	Drama	Family	Fantasy	History	Horror	Music	Musical	Mystery	Romance	Sci-Fi	Sport	Thriller	War	Western
Title																				
Guardians of the Galaxy	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0
Prometheus	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0
Split	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0
Sing	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0
Suicide Squad	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0	0

  
# 5. 遍历每一部电影，genre 中把分类出现的列的值置为1
# df_gener.loc[[i for i in movies['Title']], genre] + 1 ERROR，因为一次只能索引一行

for i in range(movies.shape[0]):
    df_gener.loc[movies['Title'][i]][genre[i]] = 1
>>>
  	Action	Adventure	Animation	Biography	Comedy	Crime	Drama	Family	Fantasy	History	Horror	Music	Musical	Mystery	Romance	Sci-Fi	Sport	Thriller	War	Western
Title																				
Guardians of the Galaxy	1	1	0	0	0	0	0	0	0	0	0	0	0	0	0	1	0	0	0	0
Prometheus	0	1	0	0	0	0	0	0	0	0	0	0	0	1	0	1	0	0	0	0
Split	0	0	0	0	0	0	0	0	0	0	1	0	0	0	0	0	0	1	0	0
Sing	0	0	1	0	1	0	0	1	0	0	0	0	0	0	0	0	0	0	0	0
Suicide Squad	1	1	0	0	0	0	0	0	1	0	0	0	0	0	0	0	0	0	0	0
  
  
# 6. 按列统计数量
df_gener.sum().sort_values(ascending=False)
>>>
Drama        512
Action       302
Comedy       278
Adventure    258
Thriller     195
Crime        150
Romance      140
Sci-Fi       120
Horror       118
Mystery      106
Fantasy      101
Biography     81
Family        51
Animation     49
History       29
Sport         18
Music         16
War           13
Western        7
Musical        5
dtype: int64
  
  
# 7. 绘图
df_gener.sum().sort_values(ascending=False).plot(kind='bar', figsize=(20, 8), fontsize=22, colormap='cool')
>>>
```

![image-20220217124600148](doc/pic/README/image-20220217124600148.png)









































































































































































































































































