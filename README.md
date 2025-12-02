This is a minimal bare-metal C project for an STM32 microcontroller, demonstrating direct hardware control by accessing memory-mapped registers via C structures.

Functionality
The program configures GPIO Pin A5 (PA5) as an output and continuously toggles its state, causing the onboard LED to blink using a simple software delay loop.

Key Techniques Used
Bare-Metal Programming: No HAL or standard libraries are used; peripheral addresses are directly defined.

Struct Pointers: RCC_TypeDef and GPIO_TypeDef structures map register offsets to variables for clear access (e.g., GPIOA->MODER).

Clock Enable: The AHB1 clock for GPIOA is explicitly enabled via the RCC peripheral.
