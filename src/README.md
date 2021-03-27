
应用程序目录apps
+ main()
+ only include "board.h" and "radio.h"

Lora芯片平台目录 radio
+ 同一个头文件 "radio.h" 定义统一的函数接口: extern const struct Radio_s Radio; //callback functions
+ 不同的平台代码接口（真正的写好程序），放在不同文件夹下面 ../sx1276, .../sx1272 

system目录 
+ 定义了系统(MCU)统一的函数接口: uart.h, i2c.h, ...

mac目录
+ LoRaWAN协议MAC层，纯逻辑: LoRaMacSendOnChannel() ...
+ 调用了radio.h 里面的接口函数
