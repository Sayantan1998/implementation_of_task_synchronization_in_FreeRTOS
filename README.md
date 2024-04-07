The "tm4c123-freertos-keil" folder contains four main files i.e "main.c" , "bsp.h", "bsp.h" and "FreeRTOSConfig.h".

The "main.c" contains the code that establishes a system with three tasks that operate LEDs in various ways, utilizing FreeRTOS for task management and coordination. It begins by initializing the hardware and creating a binary semaphore. It then creates and starts two tasks: main_blinky1 and main_blinky2. The first task blinks a green LED, while the second task waits on a semaphore before blinking a blue LED. A commented-out section suggests a third task, main_blinky3, that would blink a red LED independently, but it's not actively created in this version of the code. The code concludes by starting the FreeRTOS scheduler, which manages the execution of the tasks.

The "bsp.h" initializes methods, system clock ticks and semaphores.

The code present in "bsp.c" is for a board support package (BSP) for a development board with a TM4C123GXL microcontroller. It initializes the board including LEDs and a switch, sets up interrupt handling for the switch, and provides functions to control the LEDs. It also includes callbacks for FreeRTOS, a real-time operating system. The code appears to handle some low-power functionality as well. There is an assert function that turns on all LEDs if assertions are enabled for debugging purposes

"FreeRTOSCongig.h" is a configuration file for FreeRTOS, a real-time operating system. It defines various settings for the OS, such as memory allocation, task priorities, and timer behavior. The file allows users to adjust these settings based on their specific hardware and application needs. It also includes comments that explain what each setting does and refer to the FreeRTOS documentation for more details.

The "FreeRTOS" folder contains C code for essentiial components like event groups, list, semaphores, timer, queue, stream buffer and tasks.

The "ek-tm4c123gxl" folder contains the header file and C souce file for the EK-TM4C123GXL Evaluation board.

To run the code follow the directions:-    
Download keil MDk IDE -> open tm4c123-freertos-keil folder -> click on "lesson.uvprojx" file
