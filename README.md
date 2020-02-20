# Lenovo-Ren7000-2017-Hackintosh
**适配机型：**拯救者 刃7000 （2017年版本 `B250+7400`）

> 通用适配（请自行测试）：**200系列**主板+**A卡**

**适配版本**：`macOS High Sierra 10.13.6(17G2112)`

**刃7000安装教程**：

1.要一个兼容USB2.0的U盘，然后烧录镜像

2.替换EFI为本库EFI

3.U盘插入机箱背后USB2.0，键盘鼠标也要插入USB2.0才能使用

>机箱背后只有两个USB2.0，使用键盘鼠标的时候要来回插，不能拔U盘！

4.引导安装并进入安装界面

5.安装界面打开终端输入：`date 1212122012`（**必须做**）

6.安装

7.开机[安装英伟达驱动](#安装英伟达驱动)

## 配置信息

| 硬件     |                                          |
| -------- | ---------------------------------------- |
| 主板     | 联想 B250 缩水版                         |
| 处理器   | Intel(R) Core(TM) i5-7400（屏蔽核显）    |
| 内存     | DDR4 8GB 2400MHz（记忆科技和海盗船混用） |
| 硬盘     | INTEL SSDPEKKW128G7（600P）              |
| 独立显卡 | NVIDIA GeForce GTX 1060 3GB              |
| 声卡     | ACL 662                                  |
| 网卡     | Realtek RTL8168H/8111H                   |

## 问题和情况

#### 存在问题

**1.声卡**

- 输入：麦克风（MIC）无法使用 

#### 功能情况
| 情况 | 名称    | 说明                       |
| :--: | ------- | -------------------------- |
|  ✔   | CPU睿频       | 通过CPU-S查询                                   |
| ✔ | 显卡 | 英伟达驱动（[安装方法点我](#安装英伟达驱动)） |
|  ✔   | 扬声器（输出） | 仿冒ID `15` 内建，插入耳机自动切换 |
| ✔ | 网卡 | 千兆正常，`RealtekRTL8111.kext`驱动 |
|  ✔   | USB接口 | 未定制（以便适应其他主板） |
| ✔ | 睡眠 | 睡眠正常，可睡死，电源键闪光，按下后启动 |
| ❌ | 麦克风（输入） | 仿冒ID `15` 内建，无效！ |

**刃7000 2017 USB端口**

| 端口名称 | 类型   | 备注     |
| -------- | ------ | -------- |
| HS03     | USB2.0 | 背面左   |
| HS04     | USB2.0 | 背面右   |
| HS07     | USB3.0 | 电源键左 |
| HS08     | USB3.0 | 电源键右 |
| HS11     | USB3.0 | 背面上   |
| SS01     | USB3.0 | 背面下   |

## 安装英伟达驱动

```bash
bash <(curl -s https://raw.githubusercontent.com/Benjamin-Dobell/nvidia-update/master/nvidia-update.sh)
```

安装完毕后重启，如果驱动没有启用就点右上角的英伟达图标，选择`Nvidia Web Dirver`重启即可！

> ***Tips：安装不了请xx上网！***
>
> *方法来自：[黑果小兵](https://blog.daliansky.net/macOS-High-Sierra-10.13.6-17G2112-Release-Special-with-Clover-4606-original-mirror.html)*

## 测试截图

![1](https://github.com/Tamshen/Lenovo-Ren7000-2017-Hackintosh/raw/master/_doc/pic.png)]

## 系统镜像下载

[黑果小兵的博客 macOS High Sierra 10.13.6(17G2112) 镜像下载](https://blog.daliansky.net/macOS-High-Sierra-10.13.6-17G2112-Release-Special-with-Clover-4606-original-mirror.html#下载链接)

