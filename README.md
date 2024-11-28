# deskhopbox
该工程源自**hrvach**的**deskhop**，再次基础上修改了PCB以及外壳。

工程详情请及英文版说明请访问原工程链接。

(For project details and English explanations, please visit the original project link.)

原工程访问：**[hrvach/deskhop](https://github.com/hrvach/deskhop)**

该工程当前基于原工程 **[v0.68](https://github.com/hrvach/deskhop/releases/tag/v0.68)** 制作。

## 作用

仅使用**1套键盘鼠标**，即可控制**2台电脑**，在一台电脑上将鼠标移动至屏幕边缘，**自动穿越到另一台电脑**上，并且键盘也跟随穿越，这就和操作一台电脑一样。是提升跨电脑操作的一大神器。

2台电脑之间**不共享任何数据**，盒子也不会记录任何数据，纯硬件方案，无需安装任何驱动及软件，安全、稳定、高效。

支持在Windows、Linux、macOS之间无缝切换。

支持带接收器的无线键盘、鼠标。***兼容性请在原项目中了解***

## 修改项

对比原项目，我重新绘制了PCB，并匹配金属外壳，修改少量代码用于适配新的PCB硬件。

**特别说明** 由于硬件和软件有少量修改，所以该硬件**不兼容原工程固件**，仅可使用当前工程提供的固件。

## 快捷键说明


## 软硬件制作
### 固件编译
在Debian/Ubuntu系统上，确保安装这些依赖项：
```
sudo apt install cmake gcc-arm-none-eabi libnewlib-arm-none-eabi build-essential
```
运行以下命令来编译固件：
```
cmake -S . -B build
cmake --build build
```
### 也可以使用预先编译好的固件

下载地址：

### 升级固件

**方法一** 将需要升级的一侧插入键盘并连接至电脑，使用快捷键**左边Ctrl+右边Shift+c+o**进入升级模式，将deskhop.uf2复制进去，升级完成后会自动重启，然后将另一侧按照同样方式升级即可。

**方法二(强制刷机)** 拆机后，将一侧boot区域的两个圆孔短接，然后再将USB插入电脑，将deskhop.uf2复制进去即可。然后将另一侧按照同样方式升级即可。

### 硬件制作

PCB主板板厚1.6mm，挡板板厚1mm。黑色阻焊，沉金或喷锡都可以。

PCB焊接及BOM表，参考工程下xxxx/xxxx.html

螺丝使用M2圆头螺丝。
