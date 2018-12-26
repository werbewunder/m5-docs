# BUTTON - 单按键Unit

<img src="assets/img/product_pics/unit/M5GO_Unit_button.png" width="30%" height="30%"><img src="assets/img/product_pics/unit/unit_button_grove_b.png" width="30%" height="30%">

***

:memo:**[描述](#描述)**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:octocat:**[例程](#例程)**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:electric_plug:**[原理图](#原理图)**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;🛒**[购买链接](https://item.taobao.com/item.htm?spm=a1z10.3-c.w4002-1172588106.49.3a93425e5PQbBs&id=577636117298)**

## 描述

BUTTON是一个单按键unit，这个Unit能检测你是否按下了.

## 特性

-  GROVE接口，支持[UiFlow](http://flow.m5stack.com)编程，[Arduino](http://www.arduino.cc)编程
-  Unit内置两个Lego插件孔，方便与Lego件结合

## 相关链接

- **[官方频道视频](https://i.youku.com/i/UNjE1ODA2MzE0OA==?spm=a2hzp.8253869.0.0)**

- **[官方论坛](http://forum.m5stack.com/)**

## 例程

### 1. Arduino IDE

*以下仅为用法示意，并不完整。如果需要完整例程请点击[这里](https://github.com/m5stack/M5-ProductExampleCodes/tree/master/Unit/BUTTON/Arduino)。*

```arduino
#include <M5Stack.h>

void setup() {
  M5.begin();// init
  Serial.begin(115200);
  pinMode(36, INPUT);// BUTTON Pin
}

void loop() {
  cur_value = digitalRead(36);// read the value of BUTTON
  Serial.println(cur_value);
  M5.update();
}
```


### 2. UIFlow

<!-- <img src="assets/img/product_pics/unit/unit_example/DUAL_BUTTON/1.png" width="30%" height="30%"> <img src="assets/img/product_pics/unit/unit_example/DUAL_BUTTON/2.png" width="55%" height="55%"><img src="assets/img/product_pics/unit/unit_example/DUAL_BUTTON/3.png" width="55%" height="55%"> -->

<img src="assets/img/product_pics/unit/unit_example/BUTTON/example_unit_button_04.png" width="55%" height="55%">

 <!-- width="30%" height="30%" -->

具体例程请点击[这里](https://github.com/m5stack/M5-ProductExampleCodes/tree/master/Unit/BUTTON/UIFlow)。

## 原理图

<img src="assets/img/product_pics/unit/button_sch.JPG">

### 管脚映射

<table>
 <tr><td>M5Core(GROVE接口B)</td><td>GPIO36</td><td>GPIO26</td><td>5V</td><td>GND</td></tr>
 <tr><td>单按键Unit</td></td><td>按键引脚</td><td> </td><td>5V</td><td>GND</td></tr>
</table>