######################################
#
#######################################
#source file : find all .c/cpp files and subst them to .o files

#target you can change test to what you want ---TBD
#TARGET  := useAccount useScreen
TARGET  := lplay lrecord

#compile and lib parameter
CC      := gcc
LIBS    := -L/usr/lib/x86_64-linux-gnu/libasound.so -lasound
LDFLAGS :=
DEFINES :=
INCLUDE := -I.
CFLAGS  := -g -Wall -O2 $(LIBS) $(INCLUDE)


#i think you should do anything here
.PHONY : everything objs clean veryclean rebuild

all : $(TARGET)

lplay: lplay.o sndwav_common.o wav_parser.o
	$(CC) $(CFLAGS) lplay.o sndwav_common.o wav_parser.o -o lplay $(LIBS)

lplay.o: lplay.c  sndwav_common.h wav_parser.h
	$(CC) $(CFLAGS) -c lplay.c

lrecord: lrecord.o sndwav_common.o wav_parser.o
	$(CC) $(CFLAGS) lrecord.o sndwav_common.o wav_parser.o -o lrecord $(LIBS)

lrecord.o: lrecord.c sndwav_common.h  wav_parser.h
	$(CC) $(CFLAGS) -c lrecord.c 

sndwav_common.o: sndwav_common.c sndwav_common.h
	$(CC) $(CFLAGS) -c sndwav_common.c

wav_parser.o: wav_parser.c wav_parser.h
	$(CC) $(CFLAGS) -c wav_parser.c


#unorderedWordCount: unorderedWordCount.cpp
#	$(CC) $(CPPFLAGS) -std=gnu++11 unorderedWordCount.cpp -o $@

clean :
	rm -fr *.o $(TARGET)
