# use "gcc" to compile source files.
CC = g++
# the linker is also "gcc". It might be something else with other compilers.
LD = g++
# Compiler flags go here.
CFLAGS = -Wall -O2
# Linker flags go here. Currently there aren't any, but if we'll switch to
# code optimization, we might add "-s" here to strip debug info and symbols.
LDFLAGS = -Wall -s -O2
# use this command to erase files.
RM = rm -f 
# list of souces
SOURCE = peakfit.cpp
# list of generated object files.
OBJS = peakfit.o 
# OBJS2 = xps.cfg
# command to port program in working folder
PORT = sudo cp 
DIR = /usr/local/bin/

# CD
CD = cd

# program executable file name.
PROG = peakfit

# top-level rule, to compile everything.
all: $(PROG)
	$(RM) $(OBJS) 

# rule to link the program
$(PROG): $(OBJS)
	$(LD) $(LDFLAGS) $(OBJS) -o $(PROG)
#	$(PORT) $(PROG) $(DIR)

# rule for file "OBJS".
$(OBJS): $(SOURCE)
	$(CC) $(CFLAGS) -c $(SOURCE)

# rule for final build
build: $(PROG)
	$(RM) $(OBJS) 

# rule for cleaning re-compilable files.
clean:
	$(RM) $(PROG) $(OBJS)
#	$(RM) $(DIR)$(PROG)

# rule to port ipadd in the working folder
install:
	$(PORT) $(PROG) $(DIR)
	sudo chmod 755 $(PROG)

# rule to port ipadd in the working folder
uninstall:
	sudo $(RM) $(DIR)$(PROG) 

