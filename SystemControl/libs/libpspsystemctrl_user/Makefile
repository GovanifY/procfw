TARGET=libpspsystemctrl_user.a
all: $(TARGET)
OBJS = SystemCtrlForUser_0000.o SystemCtrlForUser_0001.o SystemCtrlForUser_0002.o SystemCtrlForUser_0003.o SystemCtrlForUser_0004.o SystemCtrlForUser_0005.o SystemCtrlForUser_0006.o SystemCtrlForUser_0007.o SystemCtrlForUser_0008.o SystemCtrlForUser_0009.o SystemCtrlForUser_0010.o SystemCtrlForUser_0011.o SystemCtrlForUser_0012.o SystemCtrlForUser_0013.o SystemCtrlForUser_0014.o SystemCtrlForUser_0015.o SystemCtrlForUser_0016.o SystemCtrlForUser_0017.o SystemCtrlForUser_0018.o SystemCtrlForUser_0019.o SystemCtrlForUser_0020.o SystemCtrlForUser_0021.o SystemCtrlForUser_0022.o SystemCtrlForUser_0023.o SystemCtrlForUser_0024.o SystemCtrlForUser_0025.o SystemCtrlForUser_0026.o SystemCtrlForUser_0027.o SystemCtrlForUser_0028.o SystemCtrlForUser_0029.o SystemCtrlForUser_0030.o SystemCtrlForUser_0031.o SystemCtrlForUser_0032.o SystemCtrlForUser_0033.o SystemCtrlForUser_0034.o SystemCtrlForUser_0035.o SystemCtrlForUser_0036.o SystemCtrlForUser_0037.o SystemCtrlForUser_0038.o SystemCtrlForUser_0039.o SystemCtrlForUser_0040.o SystemCtrlForUser_0041.o SystemCtrlForUser_0042.o SystemCtrlForUser_0043.o SystemCtrlForUser_0044.o SystemCtrlForUser_0045.o SystemCtrlForUser_0046.o 

PSPSDK=$(shell psp-config --pspsdk-path)

clean:
	rm -f $(OBJS) $(TARGET)

CC=psp-gcc
INCDIR = 
CFLAGS = -Os -G0 -Wall -fno-builtin-printf -I$(PSPSDK)/include
CXXFLAGS = $(CFLAGS) -fno-exceptions -fno-rtti
ASFLAGS = $(CFLAGS)
LDFLAGS=-nodefaultlibs

LIBDIR =

$(TARGET): $(OBJS)
	psp-ar q $(TARGET) $(OBJS)
	psp-ranlib $(TARGET)

$(OBJS): SystemCtrlForUser.S
	$(CC) $(CFLAGS) -DF_$* $< -c -o $@

