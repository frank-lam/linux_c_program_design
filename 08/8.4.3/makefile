CC = gcc
FLAGS = -c		# 使用-c选项
FLAGS += -O2	# 编译选项，使用O2优化

objects = main.o kbd.o command.o display.o \
          insert.o search.o files.o utils.o
objects += new.o							# 所有的目标文件

edit : $(objects)
	$(CC) -o –O2 edit $(objects)

main.o: main.c defs.h						# 生成main.o
	$(CC) $(FLAGS) main.c
kbd.o: kbd.c defs.h command.h				# 生成kbd.o
	$(CC) $(FLAGS) kbd.c
command.o: command.c defs.h command.h		# 生成command.o
	$(CC) $(FLAGS) command.c
display.o: display.c defs.h buffer.h		# 生成display.o
	$(CC) $(FLAGS) display.c
insert.o: insert.c defs.h buffer.h			# 生成insert.o
	$(CC) $(FLAGS) insert.c
search.o: search.c defs.h buffer.h			# 生成search.o
	$(CC) $(FLAGS) search.c
files.o: files.c defs.h buffer.h command.h	# 生成files.o
	$(CC) $(FLAGS) files.c
utils.o: utils.c defs.h						# 生成utils.o
	$(CC) $(FLAGS) utils.c
new.o : new.c								# 生成new.o
	$(CC) $(FLAGS) new.c

clean:
	rm edit $(objects)

.PHONY: clean
