################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
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

BUILD_ARTIFACT_NAME := TIM_ULN2003_STEPPER
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX := 
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME).$(BUILD_ARTIFACT_EXTENSION)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
TIM_ULN2003_STEPPER.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
TIM_ULN2003_STEPPER.list \

OBJCOPY_BIN += \
TIM_ULN2003_STEPPER.bin \


# All Target
all: main-build

# Main-build Target
main-build: TIM_ULN2003_STEPPER.elf secondary-outputs

# Tool invocations
TIM_ULN2003_STEPPER.elf: $(OBJS) $(USER_OBJS) C:\Users\Aslan\STM32CubeIDE\workspace_1.1.0\TIM_ULN2003_STEPPER\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "TIM_ULN2003_STEPPER.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\Aslan\STM32CubeIDE\workspace_1.1.0\TIM_ULN2003_STEPPER\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="TIM_ULN2003_STEPPER.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

TIM_ULN2003_STEPPER.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "TIM_ULN2003_STEPPER.list"
	@echo 'Finished building: $@'
	@echo ' '

TIM_ULN2003_STEPPER.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "TIM_ULN2003_STEPPER.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents fail-specified-linker-script-missing warn-no-linker-script-specified
.SECONDARY:

-include ../makefile.targets
