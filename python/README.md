# MrzhangF1ghterStudio MiniOLED模块
# OLED教程 （Python版本）
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


### 该Python版本是使用开源库Adafruit_Python_SSD1306
https://github.com/MrzhangF1ghter/Adafruit_Python_SSD1306
> 下面是安装教程
> `sudo python setup.py install`<br>
> 终端最后显示`Finished processing dependencies for Adafruit-SSD1306xxxx`则代表安装成功了<br>
请注意 请使用此代码库里的example文件夹，我已经适配好了！
### 使用：
> 在example文件里有很多例子程序 只需要`python xxxx.py &`即可执行了，其中&代表后台执行<br>
> 例子:`python stats.py &`则oled会显示当前系统信息 <br> 
> 注意:每个.py文件引脚号都适配彩虹板了，若需要修改，请找到此段修改RST和DC引脚，引脚为BCM引脚：<br>
```Python
# Raspberry Pi pin configuration:
RST = 25
# Note the following are only used with SPI:
DC = 24
```
> 若需要修改SPI引脚 请找到：<br>
> `# disp = Adafruit_SSD1306.SSD1306_128_32(rst=RST, dc=DC, sclk=18, din=25, cs=22)`将#去掉，并把引脚修改成你oled所对应的引脚 <br>
> 若需要修改成I2C 请将SPI相关代码注释掉并将I2C代码取消注释，详情请看源码注释。<br>

