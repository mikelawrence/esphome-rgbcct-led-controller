---
description: Using the Multi-Sensor in Home Assistant
---

![Sensor](https://raw.githubusercontent.com/mikelawrence/esphome-rgbcct-led-controller/main/pcb/meta/esphome-rgbcct-led-controller-top-view.png)

# Home Assistant

There are numerous entities presented to Home Assistant here is a complete list of each with a description.

## Controls

- **Fan** (*Fan*): Provides Fan control in percentage. This is the offboard muffin fan used to circulate air.

- **Light** (*RGBWW Light*): Light control for the LED light strips connected to the controller. Supports 5 channels of PWM for Red, Green, Blue, Warm White and Cool White LED channels.

## Sensors

- **Current** (*Sensor*): This measures the current (A) the entire unit is using including LED lights strips. Updates every minute.

- **Energy** (*Sensor*): This measures the accumulated energy (W Hr) the entire unit has used including LED lights strips. Updates every minute. Resets ant midnight.

- **Fan RPM** (*Sensor*): Current Fan RPM reading. Updates every minute.

- **Humidity** (*Sensor*): Current Humidity sensor reading from the offboard temperature sensor stalk. This is part of a SHT3X sensor. Updates every minute.

- **LED Blue** (*Sensor*): This is the current Blue LED channel intensity in percentage. Updates every change of RGBWW light. Not enabled by default.

- **LED Green** (*Sensor*): This is the current Blue LED channel intensity in percentage. Updates every change of RGBWW light. Not enabled by default.

- **LED Red** (*Sensor*): This is the current Blue LED channel intensity in percentage. Updates every change of RGBWW light. Not enabled by default.

- **LED White Cool** (*Sensor*): This is the current Cool White LED channel intensity in percentage. Updates every change of RGBWW light. Not enabled by default.

- **LED White Warm** (*Sensor*): This is the current Warm White LED channel intensity in percentage. Updates every change of RGBWW light. Not enabled by default.

- **Power** (*Sensor*): This measures the current (A) the entire unit is using including LED lights strips. Updates every minute.

- **Temperature** (*Sensor*): Current Temperature sensor reading from the offboard temperature sensor stalk. This is part of a SHT3X sensor. Updates every minute.

- **Voltage** (*Sensor*): This measures the voltage (V) applied to the unit. Updates every minute.

## Configuration

- **Max Power** (*Number*): Provide the means to limit the total power the RGBWW Light. In some cases a LED Light strip with 5 channels of LED control will
get too hot if all channels are on. By lowering this number from 100% you can effectively limit the total output power. The following equation is used to
determine the brightness level of the RGBWW light.

Brightness = 100 * (RLED(%) + GLED(%) + BLED(%) + WWLED(%) + CW(%)) / (RLED(100%) + GLED(100%) + BLED(100%) + WWLED(100%) + CW(100%))

Adjusting brightness will keep the light color consistent for the most part.

- **Restart** (*Button*): Will restart RGBCCT LED Controller

[back](./)
