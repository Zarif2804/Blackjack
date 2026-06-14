CC = gcc
CFLAGS = -Wall -g -D_POSIX_C_SOURCE=199309L
LDFLAGS = -pthread -lrt

all: server client

server: server.c PokerStructure.c cards.c
	$(CC) $(CFLAGS) -o server server.c PokerStructure.c cards.c $(LDFLAGS)

client: client.c cards.c
	$(CC) $(CFLAGS) -o client client.c cards.c

clean:
	rm -f server client *.o game.log scores.txt