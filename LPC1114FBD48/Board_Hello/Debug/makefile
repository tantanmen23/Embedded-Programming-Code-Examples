################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 

# All Target
all: Board_Hello.axf

# Tool invocations
Board_Hello.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: MCU Linker'
	arm-none-eabi-gcc -nostdlib -L"C:\Users\Yusuke\Documents\LPCXpresso_7.7.2_379\workspace\CMSISv2p00_LPC11xx\Debug" -Xlinker -Map="Board_Hello.map" -Xlinker --gc-sections -mcpu=cortex-m0 -mthumb -T "Board_Hello_Debug.ld" -o "Board_Hello.axf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '
	$(MAKE) --no-print-directory post-build

# Other Targets
clean:
	-$(RM) $(OBJS)$(C_DEPS)$(EXECUTABLES) Board_Hello.axf
	-@echo ' '

post-build:
	-@echo 'Performing post-build steps'
	-arm-none-eabi-size "Board_Hello.axf"; # arm-none-eabi-objcopy -v -O binary "Board_Hello.axf" "Board_Hello.bin" ; # checksum -p LPC1114_303 -d "Board_Hello.bin";
	-@echo ' '

.PHONY: all clean dependents
.SECONDARY: post-build

-include ../makefile.targets
