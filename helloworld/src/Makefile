OBJS:=helloworld.o
EXEC:=helloworld
all: $(OBJS)
	$(CC) -o $(EXEC) $(OBJS) $(LIBS)
%.o:%.c
	$(CC) -c -o $@ $^
clean:
	rm $(EXEC) *.o
