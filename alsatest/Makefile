######################################
#
#######################################
#source file : find all .c/cpp files and subst them to .o files

#target you can change test to what you want ---TBD
#TARGET  := useAccount useScreen
TARGET  := listing1 listing2 listing3-play listing4-rec

#compile and lib parameter
CC      := gcc
LIBS    :=
LDFLAGS :=
DEFINES :=
INCLUDE := -I.
CFLAGS  := -Wall


#i think you should do anything here
.PHONY : everything objs clean veryclean rebuild

all : $(TARGET)

listing1: listing1.c
	$(CC) -o listing1 listing1.c -lasound

listing2: listing2.c
	$(CC) -o listing2 listing2.c -lasound

listing3-play: listing3-play.c
	$(CC) -o listing3-play listing3-play.c -lasound
listing4-rec: listing4-rec.c
	$(CC) -o listing4-rec listing4-rec.c -lasound

#unorderedWordCount: unorderedWordCount.cpp
#	$(CC) $(CPPFLAGS) -std=gnu++11 unorderedWordCount.cpp -o $@

clean :
	rm -fr *.o $(TARGET) *.wav
