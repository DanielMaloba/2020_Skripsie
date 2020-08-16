################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
Radiometer.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Radiometer.list \

OBJCOPY_BIN += \
Radiometer.bin \


# All Target
all: Radiometer.elf secondary-outputs

# Tool invocations
Radiometer.elf: $(OBJS) $(USER_OBJS) /Users/user/Desktop/SU\ 2020\ /2020_skripsie/Programming/stm32/Radiometer/STM32F446RETX_FLASH.ld
	arm-none-eabi-gcc -o "Radiometer.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"/Users/user/Desktop/SU 2020 /2020_skripsie/Programming/stm32/Radiometer/STM32F446RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Radiometer.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Radiometer.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Radiometer.list"
	@echo 'Finished building: $@'
	@echo ' '

Radiometer.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "Radiometer.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
