# MrzhangF1ghterStudio MiniOLED模块
# OLED模块使用教程

<img src="https://github.com/MrzhangF1ghter/miniOLED/blob/master/schematic/view.jpg" width=50% height=50% /><br>

### 新手引导:
> https://github.com/MrzhangF1ghter/RainbowCandyBoard/wiki

> ### 我们的MiniOLED是挂在原生SPI0接口上的，只占用6个引脚，具体引脚如下:
> |引脚|GPIO| wPi |排针号|
> |----|--- |-----|-----|
> |CS  |BCM8 |pin10| 16 |    
> |DC  |BCM24|pin5 | 18 |
> |RST |BCM25|pin6 | 20 |
> |SDA |BCM10|pin12| 22 |
> |SCLK|BCM11|pin14| 24 |
请将模块以右侧插座方向插入排针号为17~24的引脚
### 原理图如下:
[RainbowCandyBoard.pdf](https://github.com/MrzhangF1ghter/miniOLED/blob/master/schematic/miniOLED.pdf)<br>
<img src="https://github.com/MrzhangF1ghter/miniOLED/blob/master/schematic/miniOLED.png" width=50% height=50%/><br>
> 用户可自行更换OLED显示屏，为7pin spi接口的 0.96寸128x64分辨率。
> 相关代码和教程请打开对应文件夹查看 
树莓派的SPI默认是关闭的（这一点和I2C类似），打开方法有多种，在这仅介绍一种
运行raspi-config，找到interface 把spi打开
