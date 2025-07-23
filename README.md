# STM32F411 Nucleo UART Interrupt Mode

![STM32F411](https://img.shields.io/badge/STM32F411-Nucleo-blue) 
![UART](https://img.shields.io/badge/USART1-Interrupt_Mode-green)


UART communication using interrupts on STM32F411 Nucleo.

## Features
- **USART1** at 115200 baud
- **Interrupt-Driven** TX/RX
- **10-byte Buffers** (tx_buffer/rx_buffer)
- **Completion Counters** (tx_counter/rx_counter)
- **84MHz System Clock** (HSI-based PLL)

## Hardware Setup
| Signal | Nucleo Pin | Connection |
|--------|------------|------------|
| USART1_TX | PA9 (D8)  | → External RX |
| USART1_RX | PA10 (D2) | ← External TX |
| GND       | GND       | ↔ External GND |

*Note: Requires external USB-TTL converter or second UART device*

## Technical Details
### UART Configuration 
```c
Baud Rate: 115200 (84MHz clock)
Data Format: 8-bit, No Parity, 1 Stop Bit
Oversampling: 16x
Mode: TX/RX with interrupts
