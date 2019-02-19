# Pixfalcon Flight Controller

The Pixfalcon autopilot (designed by [Holybro<sup>&reg;</sup>](http://www.holybro.com/)) is binary-compatible (FMUv2) derivative of the [Pixhawk 1](../flight_controller/pixhawk.md) design that has been optimized for space-constrained applications such as FPV racers. It has less IO to allow for the reduction in size.

![](../../assets/hardware/hardware-pixfalcon.png)

## 总览

    * Main System-on-Chip: [STM32F427](http://www.st.com/web/en/catalog/mmc/FM141/SC1169/SS1577/LN1789)
      * CPU: 180 MHz ARM<sup>&reg;</sup> Cortex<sup>&reg;</sup> M4 with single-precision FPU
      * RAM: 256 KB SRAM (L1)
    * Failsafe System-on-Chip: STM32F100
      * CPU: 24 MHz ARM Cortex M3
      * RAM: 8 KB SRAM
    * GPS: U-Blox<sup>&reg;</sup> M8 (bundled)
    

### Connectivity

    * 1x I2C
    * 2x UART (one for Telemetry / OSD, no flow control)
    * 8x PWM with manual override
    * S.BUS / PPM input
    

## 访问链接:

From manufacturer: [Holybro](http://www.holybro.com/product/8) or from distributor [Hobbyking<sup>&reg;</sup>](http://www.hobbyking.com/hobbyking/store/__86437__PixFalcon_Micro_PX4_Autopilot_plus_Micro_M8N_GPS_and_Mega_PBD_Power_Module.html)

Optional hardware:

* Optical flow: PX4 Flow unit from manufacturer [Holybro](http://www.holybro.com/product/24) or distributor [Hobbyking](http://www.hobbyking.com/hobbyking/store/__66308__HK_Pilot32_Optical_Flow_Kit_With_Sonar.html)
* Digital Airspeed sensor from manufacturer [Holybro](http://www.holybro.com/product/26) or distributor [Hobbyking](http://www.hobbyking.com/hobbyking/store/__62752__HKPilot_32_Digital_Air_Speed_Sensor_And_Pitot_Tube_Set.html)
* On screen display with integrated Telemetry: 
  * [Hobbyking OSD + EU Telemetry (433 MHz)](http://www.hobbyking.com/hobbyking/store/__74650__Micro_HKPilot_Telemetry_Radio_Module_with_On_Screen_Display_OSD_unit_433MHz_.html)
* Pure Telemetry options: 
  * [Hobbyking Wifi Telemetry](http://www.hobbyking.com/hobbyking/store/__87841__APM_Pixhawk_Wireless_Wifi_Radio_Module.html)
  * [Hobbyking EU Micro Telemetry (433 MHz)](http://www.hobbyking.com/hobbyking/store/__74647__Micro_HKPilot_Telemetry_radio_Set_With_Integrated_PCB_Antenna_433Mhz.html)
  * [Hobbyking US Micro Telemetry (915 MHz)](http://www.hobbyking.com/hobbyking/store/__74648__Micro_HKPilot_Telemetry_radio_Set_With_Integrated_PCB_Antenna_915Mhz.html)

## 编译固件

> **Tip**大多数用户将不需要建立此固件! 它是预构建的, 并在连接适当的硬件时由 *QGroundControl* 自动安装。

为此目标 [编译 PX4](https://dev.px4.io/en/setup/building_px4.html)：

    make px4_fmu-v2_default
    

## Key Links

* [User Manual](http://www.holybro.com/manual/pixfalcon.pdf)