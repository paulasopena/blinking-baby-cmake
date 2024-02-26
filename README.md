# Integration STM32H7 with CMake

## Description
Simple blinking LED code for STM32H743ZI making the build files with CMake. 

## Toolchain commands to compile and flash

For compiling and building the project:

```bash
mkdir build
cd build
cmake ..
make
```

In order to flash the code to STM32 using openocd:

```bash
openocd -f interface/stlink.cfg -f target/stm32h7x.cfg -c "program /home/paulasopenacoello/Desktop/nanosat/test-compiler/build/blinking-baby.elf verify reset exit" 
```

