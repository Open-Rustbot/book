# Getting Started

## Install 

Install rust https://www.rust-lang.org/tools/install

Add the the thumbv7m target `rustup target add thumbv7m-none-eabi`

Install cargo-generate and cargo-binutils `cargo install cargo-generate cargo-binutils`

Install llvm-tools-preview component `rustup component add llvm-tools-preview`

Install openocd and gdb-multiarch using your OS's package manager

## Hello World

After installing the required software we can perform the "Hello World" of the hardware world, a blinking LED.
To begin clone the stm32_starter_rs repository. Take a look at src/main.rs and make an effort to understand the script.
When you're finished, open a terminal and navigate to the repository and launch `openocd`. It is important to be in the
same directory of the repository so that openocd can read the openocd.cfg file in the directory. In another terminal,
navigate to the directory again and this time execute `cargo run`. This will compile the rust source code, flash it
onto the microcontroller, and open a gdb prompt. Enter a `c` to continue the program. You should see the led on the
microcontroller periodically blinking. This program is now flashed onto the microcontroller, so pressing the reset
button will restart the program. Congratulations! You have successfully run your first embedded rust program!

