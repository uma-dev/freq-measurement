# Frequency measurement

Simple and efficient solution to measure frequency of a digital signal using **input capture** in oe port of a [Nucleo Board (STMf446RE)](https://www.st.com/en/evaluation-tools/nucleo-f446re.html).
This project was developed using [STM32Cube IDE](https://www.st.com/en/development-tools/stm32cubeide.html). This project can be testes using the complementary part of the [two-minipulses-generator](https://github.com/uma-dev/2-minipulses-generator) repo. 


<p align="center">
	<img alt="Nuicleo board" width="400" src="https://user-images.githubusercontent.com/22565959/215195552-b0238f6d-21b4-4624-b0a7-b71f18466ac9.png">
</p>

## Advantages 
Timmers in STM32 based boards have a lot of functionalities, like internal trigger conections  that can be used to count the time elapsed between a signal. 
Usign STM32 chips is a highly available and _ready to implement_ final products. Chips are capable, have a lot of support, inexpensive (compared to traditional Arduino boards) and inexpensive. It is highly recommended to use 
official STM32Cube IDE instead of Arduino IDE due to peripherals support and hardaware configurations like clocks and IO.

## Principle of function 
**Input capture mode** is a way to record one event duration, the working principle can be used to measure **width** or **frequency** of a PWM signal by: 
1. Record a timestamp between a `RISING EDGE` or `FALLING EDGE` 
2. The signal edges triggers an interrupt service routine in order to show or map the timestamp.

</p>
