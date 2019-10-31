src=$(wildcard ./*.c)
obj=$(patsubst ./%.c, ./%.o, $(src))

target=video
CC=gcc

$(target):$(obj)
	$(CC) $^ -o $@ -shared -fPIC

%.o:%.c
	$(CC) -c $< -o $@

.PHONY: clean
clean:
	-rm $(obj) $(target) -f