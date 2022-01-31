LIBUSB = libusb-1.0
LIBPCAP = libpcap

CFLAGS = -W -Wall -O -g
CFLAGS += $(shell pkg-config $(LIBUSB) --cflags) $(shell pkg-config $(LIBPCAP) --cflags)
LDFLAGS = $(shell pkg-config $(LIBUSB) --libs)  $(shell pkg-config $(LIBPCAP) --libs) 
# CFLAGS += -I/usr/include/libusb-1.0
# LDFLAGS += -L/lib/x86_64-linux-gnu -lusb-1.0 -lpcap 


all: rawsniff

rawsniff: rawsniff.c
	$(CC) $(CFLAGS) -o rawsniff rawsniff.c $(LDFLAGS)
clean:
	rm -f rawsniff

