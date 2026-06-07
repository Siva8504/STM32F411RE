\# Push Button Controlled LED using STM32F411RE



\## About Project



In this project I interfaced a push button and LED with STM32F411RE board.



When the push button is pressed, LED turns ON.



When the push button is released, LED turns OFF.



This project helped me understand GPIO input and output configuration in STM32.



\## Components Used



\* STM32 NUCLEO-F411RE

\* Push Button

\* LED

\* 976 Ohm Resistor

\* Breadboard

\* Jumper Wires



\## Connections



\### Push Button



PA0 (A0) ---> Push Button ---> GND



\### LED



PA6 (D12) ---> 976 Ohm Resistor ---> LED ---> GND



\## GPIO Configuration



PA0:



\* GPIO Input

\* Internal Pull-up Enabled



PA6:



\* GPIO Output Push Pull



\## Code Logic



```c

while(1)

{

\&#x20;   if(HAL\\\_GPIO\\\_ReadPin(GPIOA, GPIO\\\_PIN\\\_0) == GPIO\\\_PIN\\\_RESET)

\&#x20;   {

\&#x20;       HAL\\\_GPIO\\\_WritePin(GPIOA, GPIO\\\_PIN\\\_6, GPIO\\\_PIN\\\_SET);

\&#x20;   }

\&#x20;   else

\&#x20;   {

\&#x20;       HAL\\\_GPIO\\\_WritePin(GPIOA, GPIO\\\_PIN\\\_6, GPIO\\\_PIN\\\_RESET);

\&#x20;   }

}

```



\## Working



\* Button not pressed -> LED OFF

\* Button pressed -> LED ON



\## What I Learned



\* GPIO Input Configuration

\* GPIO Output Configuration

\* Internal Pull-up Resistor

\* Push Button Interfacing

\* LED Interfacing

\* STM32CubeMX Configuration

\* STM32CubeIDE Build and Flash Process



\## Demo



Project demo video is available in the images folder.

