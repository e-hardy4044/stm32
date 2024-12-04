CC = arm-none-eabi-gcc
LD = arm-none-eabi-ld
OBJCOPY = arm-none-eabi-objcopy
SIZE = arm-none-eabi-size

CFLAGS = -mcpu=cortex-m3 -mthumb -O2 -I. -nostdlib
LDFLAGS = Tlinker.ld -nostdlib

TARGET = blinky
SRC = main.c startup.s

all: $(TARGET).bin
	$(CC) $(CFLAGS) -o $@ $^ $(LDFLAGS)

$(TARGET).elf: $(SRC)
	$(OBJCOPY) -O binary $< $@


clean:
	rm -f $(TARGET).elf $(TARGET).bin
