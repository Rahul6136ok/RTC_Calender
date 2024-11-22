# RTC_Calender
🚀 RTC Calendar Test Project Using STM32 🚀
I recently completed a project implementing a Real-Time Clock (RTC) Calendar system with the STM32F407VGT6 microcontroller. The objective was to configure the RTC to display the current date and time, triggered by a button press, and transmit this data over UART for real-time monitoring.
Key Features:
🔹 RTC Configuration:
Used STM32’s HAL library to set up the RTC in 24-hour mode with accurate timekeeping.
Configured the asynchronous prescaler to 0x7F and synchronous prescaler to 0xF9 to align with the internal LSI clock (32kHz).
🔹 UART Communication:
Configured UART2 at a baud rate of 115200 for sending time and date data to a terminal like TERA TERM.
I utilized a USB UART module and TERA TERM for monitoring, enabling easy data exchange over UART to debug and verify RTC functionality.
🔹 Interrupt-Driven Display:
Implemented external interrupts triggered by a button press (PA0), which fetches and sends the current date and time over UART.
This method minimizes CPU usage and improves efficiency.
🔹 GPIO and Clock Setup:
Initialized GPIO pins for the user button and LEDs, configuring the system clock using the HSE oscillator at 50 MHz for stability.
🔹 Day of the Week Calculation:
Developed a function to display the day of the week based on RTC data, enhancing the calendar representation.
Challenges & Solutions:
🔧 RTC Initialization:
Corrected initial prescaler settings after recalculating based on the LSI clock, resolving time drift.
🔧 UART Communication:
Fixed glitches by fine-tuning settings and expanding the buffer size for stable data transmission.
🔧 Button Handling:
Resolved debouncing issues by adjusting interrupt priority and EXTI configuration, ensuring reliable button press detection.
🔧 Clock Configuration:
Adjusted PLL and flash latency settings for stable system clock operation.
🔧 Data Formatting:
Used sprintf for zero-padded output of RTC data, maintaining clarity in UART transmission.
Project Outcome:
Successfully displayed real-time date and time via UART, triggered by a button press. This project enhanced my skills in RTC management, UART communication, and interrupt handling while deepening my knowledge of embedded systems.
https://www.linkedin.com/posts/rahul-kumar-mahato-11b1611b6_stm32-embeddedsystems-rtc-activity-7254361094092169216-6K8k?utm_source=share&utm_medium=member_desktop
