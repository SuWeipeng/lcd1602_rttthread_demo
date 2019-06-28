#
# Copyright (c) 2014-2015 0xc0170
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

# This project was exported via the project generator.  More information https://github.com/project-generator/project_generator

CPU = cortex-m4

# toolchain specific
TOOLCHAIN = arm-none-eabi-
TOOLCHAIN_BINPATH = 
CC = $(TOOLCHAIN_BINPATH)$(TOOLCHAIN)gcc
CXX = $(TOOLCHAIN_BINPATH)$(TOOLCHAIN)g++
AS = $(TOOLCHAIN_BINPATH)$(TOOLCHAIN)gcc -x assembler-with-cpp
LD = $(TOOLCHAIN_BINPATH)$(TOOLCHAIN)gcc
AR = $(TOOLCHAIN_BINPATH)$(TOOLCHAIN)ar

SIZE = $(TOOLCHAIN_BINPATH)$(TOOLCHAIN)size
OBJCOPY = $(TOOLCHAIN_BINPATH)$(TOOLCHAIN)objcopy
OBJDUMP = $(TOOLCHAIN_BINPATH)$(TOOLCHAIN)objdump
NM = $(TOOLCHAIN_BINPATH)$(TOOLCHAIN)nm

# application specific
INSTRUCTION_MODE = thumb
TARGET = stm32f4discovery-rtt

TARGET_EXT = .elf


LD_SCRIPT = ../IDE/GCC/STM32F407VGTx_FLASH.ld

CC_SYMBOLS =  -DUSE_HAL_DRIVER  -DSTM32F407xx 
ASM_SYMBOLS = $(CC_SYMBOLS)

LIBS =  
 
LIBS += -Wl,--start-group   -lm  -lgcc  -lc  -lnosys  -lstdc++  -Wl,--end-group
 

LIB_PATHS = 


# directories
INC_DIRS =  ../Drivers  ../Drivers/CMSIS  ../Drivers/CMSIS/Device  ../Drivers/CMSIS/Device/ST  ../Drivers/CMSIS/Device/ST/STM32F4xx  ../Drivers/CMSIS/Device/ST/STM32F4xx/Include  ../Drivers/CMSIS/Include  ../Drivers/STM32F4xx_HAL_Driver  ../Drivers/STM32F4xx_HAL_Driver/Inc  ../Drivers/STM32F4xx_HAL_Driver/Inc/Legacy  ../Inc  ../Libraries  ../Libraries/rt-thread  ../Libraries/rt-thread/board-407vg  ../Libraries/rt-thread/components  ../Libraries/rt-thread/components/finsh  ../Libraries/rt-thread/components/drivers  ../Libraries/rt-thread/components/drivers/include  ../Libraries/rt-thread/HAL_Drivers  ../Libraries/rt-thread/include  ../Libraries/rt-thread/include/libc  ../Middlewares  ../Middlewares/ST  ../Middlewares/ST/STM32_USB_Device_Library  ../Middlewares/ST/STM32_USB_Device_Library/Class  ../Middlewares/ST/STM32_USB_Device_Library/Class/CDC  ../Middlewares/ST/STM32_USB_Device_Library/Class/CDC/Inc  ../Middlewares/ST/STM32_USB_Device_Library/Core  ../Middlewares/ST/STM32_USB_Device_Library/Core/Inc  ../Middlewares/Third_Party  ../Middlewares/Third_Party/FatFs  ../Middlewares/Third_Party/FatFs/src 

OUT_DIR = build

INC_DIRS_F = -I. $(patsubst %, -I%, $(INC_DIRS))

SRC_DIRS =  ../Middlewares/ST/STM32_USB_Device_Library/Class/CDC/Src  ../Middlewares/ST/STM32_USB_Device_Library/Core/Src  ../Middlewares/Third_Party/FatFs/src  ../Middlewares/Third_Party/FatFs/src/option  ../Src-rtt  ../Drivers/STM32F4xx_HAL_Driver/Src  ../Libraries/rt-thread/board-407vg  ../Libraries/rt-thread/components/finsh  ../Libraries/rt-thread/HAL_Drivers  ../Libraries/rt-thread/libcpu/arm/cortex-m4  ../Libraries/rt-thread/src  ../IDE/GCC 

ifeq ($(strip $(OUT_DIR)), )
	OBJ_FOLDER =
else
	OBJ_FOLDER = $(strip $(OUT_DIR))/
endif

# Flags
COMMON_FLAGS =  -O0  -g  -ggdb  -Wall  -fno-strict-aliasing  -ffunction-sections  -fdata-sections  -fno-exceptions  -fno-delete-null-pointer-checks  -fmessage-length=0  -fno-builtin  -mthumb  -gdwarf-2 
COMMON_FLAGS +=  -mcpu=$(CPU) -m$(INSTRUCTION_MODE) -MMD -MP $(CC_SYMBOLS)  

C_FLAGS  =  -std=c99 
CXX_FLAGS  =  -fno-rtti  -std=gnu++98 
ASM_FLAGS  = 

CFLAGS = $(C_FLAGS) $(INC_DIRS_F) -c $(CC_SYMBOLS)
CXXFLAGS = $(CXX_FLAGS) $(INC_DIRS_F) -c $(CC_SYMBOLS)
ASFLAGS = $(ASM_FLAGS) $(INC_DIRS_F) -c $(ASM_SYMBOLS)

# Linker options
LD_OPTIONS +=  -specs=nano.specs  -Wl,--gc-sections 
LD_OPTIONS +=  -mcpu=$(CPU) -m$(INSTRUCTION_MODE) -Wl,-Map=$(OBJ_FOLDER)$(TARGET).map,--cref -T$(LD_SCRIPT)

OBJCPFLAGS = -O ihex

ARFLAGS = cr

ifeq ($(OS),Windows_NT)
	RM = rmdir /s /q
else
	RM = rm -rf
endif

C_SRCS :=  ../Middlewares/Third_Party/FatFs/src/diskio.c  ../Middlewares/Third_Party/FatFs/src/ff.c  ../Middlewares/Third_Party/FatFs/src/ff_gen_drv.c  ../Middlewares/Third_Party/FatFs/src/option/syscall.c  ../Middlewares/ST/STM32_USB_Device_Library/Class/CDC/Src/usbd_cdc.c  ../Middlewares/ST/STM32_USB_Device_Library/Core/Src/usbd_core.c  ../Middlewares/ST/STM32_USB_Device_Library/Core/Src/usbd_ctlreq.c  ../Middlewares/ST/STM32_USB_Device_Library/Core/Src/usbd_ioreq.c  ../Src-rtt/entry.c  ../Src-rtt/fatfs.c  ../Src-rtt/stm32f4xx_hal_msp.c  ../Src-rtt/stm32f4xx_it.c  ../Src-rtt/system_stm32f4xx.c  ../Src-rtt/usb_device.c  ../Src-rtt/usbd_cdc_if.c  ../Src-rtt/usbd_conf.c  ../Src-rtt/usbd_desc.c  ../Src-rtt/user_diskio.c  ../Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal.c  ../Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_cortex.c  ../Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_dma.c  ../Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_dma_ex.c  ../Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_flash.c  ../Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_flash_ex.c  ../Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_flash_ramfunc.c  ../Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_gpio.c  ../Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_pcd.c  ../Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_pcd_ex.c  ../Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_pwr.c  ../Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_pwr_ex.c  ../Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_rcc.c  ../Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_rcc_ex.c  ../Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_tim.c  ../Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_tim_ex.c  ../Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_ll_usb.c  ../Libraries/rt-thread/board-407vg/board.c  ../Libraries/rt-thread/src/clock.c  ../Libraries/rt-thread/components/finsh/cmd.c  ../Libraries/rt-thread/src/components.c  ../Libraries/rt-thread/src/cpu.c  ../Libraries/rt-thread/libcpu/arm/cortex-m4/cpuport.c  ../Libraries/rt-thread/src/device.c  ../Libraries/rt-thread/HAL_Drivers/drv_common.c  ../Libraries/rt-thread/components/finsh/finsh_compiler.c  ../Libraries/rt-thread/components/finsh/finsh_error.c  ../Libraries/rt-thread/components/finsh/finsh_heap.c  ../Libraries/rt-thread/components/finsh/finsh_init.c  ../Libraries/rt-thread/components/finsh/finsh_node.c  ../Libraries/rt-thread/components/finsh/finsh_ops.c  ../Libraries/rt-thread/components/finsh/finsh_parser.c  ../Libraries/rt-thread/components/finsh/finsh_token.c  ../Libraries/rt-thread/components/finsh/finsh_var.c  ../Libraries/rt-thread/components/finsh/finsh_vm.c  ../Libraries/rt-thread/src/idle.c  ../Libraries/rt-thread/src/ipc.c  ../Libraries/rt-thread/src/irq.c  ../Libraries/rt-thread/src/kservice.c  ../Libraries/rt-thread/src/mem.c  ../Libraries/rt-thread/src/memheap.c  ../Libraries/rt-thread/src/mempool.c  ../Libraries/rt-thread/components/finsh/msh.c  ../Libraries/rt-thread/components/finsh/msh_cmd.c  ../Libraries/rt-thread/components/finsh/msh_file.c  ../Libraries/rt-thread/src/object.c  ../Libraries/rt-thread/src/scheduler.c  ../Libraries/rt-thread/components/finsh/shell.c  ../Libraries/rt-thread/src/signal.c  ../Libraries/rt-thread/src/slab.c  ../Libraries/rt-thread/components/finsh/symbol.c  ../Libraries/rt-thread/src/thread.c  ../Libraries/rt-thread/src/timer.c 
C_OBJS := $(patsubst %.c,$(OBJ_FOLDER)%.o,$(notdir $(C_SRCS)))

CPP_SRCS := 
CPP_OBJS := $(patsubst %.cpp,$(OBJ_FOLDER)%.o,$(notdir $(CPP_SRCS)))

S_SRCS :=  ../IDE/GCC/startup_stm32f407xx-rtt.S  ../Libraries/rt-thread/libcpu/arm/cortex-m4/context_gcc.S 
S_OBJS = $(patsubst %.s,$(OBJ_FOLDER)%.o,$(filter %.s,$(notdir $(S_SRCS))))
S_OBJS += $(patsubst %.S,$(OBJ_FOLDER)%.o,$(filter %.S,$(notdir $(S_SRCS))))

O_OBJS := 

VPATH := $(SRC_DIRS)

$(OBJ_FOLDER)%.o : %.c
	@echo 'Building file: $(@F)'
	@echo 'Invoking: MCU C Compiler'
	$(CC) $(CFLAGS) $(COMMON_FLAGS) $< -o $@
	@echo 'Finished building: $(@F)'
	@echo ' '

$(OBJ_FOLDER)%.o : %.cpp
	@echo 'Building file: $(@F)'
	@echo 'Invoking: MCU C++ Compiler'
	$(CXX) $(CXXFLAGS) $(COMMON_FLAGS) $< -o $@
	@echo 'Finished building: $(@F)'
	@echo ' '

$(OBJ_FOLDER)%.o : %.s
	@echo 'Building file: $(@F)'
	@echo 'Invoking: MCU Assembler'
	$(AS) $(ASFLAGS) $(COMMON_FLAGS) $< -o $@
	@echo 'Finished building: $(@F)'
	@echo ' '

PRE_BUILD_SCRIPT := $(shell true)

all: create_outputdir $(OBJ_FOLDER)$(TARGET)$(TARGET_EXT) print_info
	 true

create_outputdir:
ifeq ($(OS),Windows_NT)
	-mkdir $(OUT_DIR)
else
	$(shell mkdir $(OBJ_FOLDER) 2>/dev/null)
endif


# Tool invocations
$(OBJ_FOLDER)$(TARGET)$(TARGET_EXT): $(LD_SCRIPT) $(C_OBJS) $(CPP_OBJS) $(S_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: MCU Linker'
	$(LD) $(LIB_PATHS) -o $@ $(CPP_OBJS) $(C_OBJS) $(S_OBJS) $(O_OBJS) $(LIBS) $(LD_OPTIONS) 
	@echo 'Finished building target: $@'
	@echo ' '

print_info: $(OBJ_FOLDER)$(TARGET)$(TARGET_EXT)
	@echo 'Printing size'
	$(SIZE) --totals $(OBJ_FOLDER)$(TARGET)$(TARGET_EXT)
	$(OBJCOPY) -O ihex $(OBJ_FOLDER)$(TARGET)$(TARGET_EXT)  $(OBJ_FOLDER)$(TARGET).hex
	$(OBJCOPY) -O binary -v $(OBJ_FOLDER)$(TARGET)$(TARGET_EXT)  $(OBJ_FOLDER)$(TARGET).bin
	-$(OBJDUMP) -D $(OBJ_FOLDER)$(TARGET)$(TARGET_EXT) > $(OBJ_FOLDER)$(TARGET).lst
	-$(NM) $(OBJ_FOLDER)$(TARGET)$(TARGET_EXT) > $(OBJ_FOLDER)$(TARGET)-symbol-table.txt
	@echo ' '



# Other Targets
clean:
	@echo 'Removing entire out directory'
	$(RM) $(TARGET)$(TARGET_EXT) $(TARGET).bin $(TARGET).map $(OBJ_FOLDER)*.* $(OBJ_FOLDER)
	@echo ' '

.PHONY: clean print_info