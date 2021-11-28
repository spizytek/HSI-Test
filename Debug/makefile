################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
HSI_Measurement.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
HSI_Measurement.list \

OBJCOPY_BIN += \
HSI_Measurement.bin \


# All Target
all: HSI_Measurement.elf secondary-outputs

# Tool invocations
HSI_Measurement.elf: $(OBJS) $(USER_OBJS) D:\Embedded\ C\My_workspace\class3MCU1\HSI_Measurement\STM32F407VETX_FLASH.ld
	arm-none-eabi-gcc -o "HSI_Measurement.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"D:\Embedded C\My_workspace\class3MCU1\HSI_Measurement\STM32F407VETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="HSI_Measurement.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

HSI_Measurement.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "HSI_Measurement.list"
	@echo 'Finished building: $@'
	@echo ' '

HSI_Measurement.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "HSI_Measurement.bin"
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
