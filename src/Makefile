#--------------------------------------------------------------
# Pi Calendar Makefile
# Author: Alan Crispin <crispinalan@gmail.com> 
# Date: February 2025
# Changelog: 0.01
#----------------------------------------------------------------

CC ?= gcc
PKGCONFIG = $(shell which pkg-config)
CFLAGS = $(shell $(PKGCONFIG) --cflags gtk4)
LIBS = $(shell $(PKGCONFIG) --libs gtk4) -lm -lasound -lsqlite3 

SRC = main.c displayitem.c calendarevent.c customcalendar.c dictionary.c dbmanager.c

OBJS = $(SRC:.c=.o)

all: picalendar


%.o: %.c
	$(CC) -c -o $(@F) $(CFLAGS) $<


picalendar: $(OBJS)
	$(CC) -o $(@F) $(OBJS) $(LIBS)

clean:
	rm -f $(OBJS)
	rm -f picalendar


