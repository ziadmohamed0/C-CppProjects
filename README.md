# C_programming_Projects

Created By Ziad Mohammed Fathi

CC=gcc
CFLAGS=-I.

# Define your projects here
PROJECTS=school_management payment_system login_system

all: $(PROJECTS)

school_management: school_management.o
    $(CC) -o $@ $^ $(CFLAGS)

payment_system: payment_system.o
    $(CC) -o $@ $^ $(CFLAGS)

login_system: login_system.o
    $(CC) -o $@ $^ $(CFLAGS)

%.o: %.c
    $(CC) -c -o $@ $< $(CFLAGS)

clean:
    rm -f *.o $(PROJECTS)
