
#### ESP-IDF完整项目功能
* 雷达感应、报警
* 继电器通断
* 七彩灯控制
* OTA升级
* AP配网
* 智能配网
* 遥控学习、清码
* Wifi和Mqtt功能
* 温湿度监控

<br /><br />

#### 按键功能分配
通电后灯为红色，联网后灯为绿色，收发消息蓝色灯闪烁一次
* 短按 &emsp;&emsp;&emsp;继电器通断
* 长按3秒 &emsp;配网，绿灯闪烁
* 短按2次 &emsp;打开AP/重启，红灯亮
* 短按3次 &emsp;遥控学习，蓝灯闪烁3次
* 短按4次 &emsp;遥控清码，蓝灯闪烁4次
* 短按5次 &emsp;打开/关闭雷达,蓝灯闪烁5次
* 短按6次 &emsp;离线/联网模式，离线灯为红色，联网灯为绿色
* 短按7次 &emsp;OTA升级，红灯闪烁

<br /><br />

#### 引脚分配参考，基于乐鑫ESP32S2芯片

* GPIO1	ADC1-CH0	    SCL-i2c传感器
* GPIO2	ADC1-CH1	    SDA-i2c传感器
* GPIO3	ADC1-CH2	    引出
* GPIO4	ADC1-CH3	    引出
* GPIO5	ADC1-CH4	    继电器 	
    
##### RGB灯：
* GPIO11	Red电源灯：红色（接通电源）、绿色（已经联网）、蓝色（接收信号、智能配网）
* GPIO12	Green
* GPIO13	Blue

##### 按键：
* GPIO15	控制按钮

##### 433M遥控
* GND
* VCC      3.3V
* GPIO19   信号1
* GPIO20   信号2
* GPIO21   信号3
* GPIO26   信号4
* GPIO33   对码按键

##### 代码烧录
* GPIO43	TXD
* GPIO44	RXD
* GND 
* GPIO0	        启动模式，低电平进入烧录模式
* EN	        重启按键（EN引脚：高电平，芯片使能；低电平，芯片关闭；芯片已默认拉高）
