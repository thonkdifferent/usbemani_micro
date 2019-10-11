CC = i686-w64-mingw32-gcc
CFLAGS ?= -O2 -Wall 
all:
	# Don't forget to readd -mwindows when finished!
	i686-w64-mingw32-windres -i resources.rc -o resources.o
	$(CC) $(CFLAGS) -s -DUSE_WIN32 -o USBemaniConfig.exe USBemaniConfig.c Bootloader.c resources.o -lcomdlg32 -lcomctl32 -lhid -lsetupapi -luxtheme

clean:
	rm -f USBemaniConfig.exe resources.o
