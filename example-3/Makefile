# Makefile для example-3
# На основе example-2 с улучшениями

.PHONY: all debug release clean

# Компилятор
CC = g++
CFLAGS = -Wall -Wextra

# Переменные для разных версий
RELEASE_FLAGS = -O2 -DNDEBUG
DEBUG_FLAGS   = -g -O0

# Имена исполняемых файлов
RELEASE_EXEC = program-release
DEBUG_EXEC   = program-debug

# Исходные файлы (адаптируйте под файлы example-3)
SOURCES = main.cpp helper.cpp
OBJECTS = $(SOURCES:.cpp=.o)

# Цели по умолчанию
all: debug release

# Debug версия
debug: $(DEBUG_EXEC)

$(DEBUG_EXEC): $(OBJECTS)
	$(CC) $(DEBUG_FLAGS) $(OBJECTS) -o $(DEBUG_EXEC)

# Release версия
release: $(RELEASE_EXEC)

$(RELEASE_EXEC): $(OBJECTS)
	$(CC) $(RELEASE_FLAGS) $(OBJECTS) -o $(RELEASE_EXEC)

# Компиляция объектных файлов
%.o: %.cpp
	$(CC) $(CFLAGS) -c $< -o $@

# Очистка
clean:
	rm -f $(RELEASE_EXEC) $(DEBUG_EXEC) $(OBJECTS) *.out *.gch core

.PHONY: all debug release clean
