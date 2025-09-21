# Makefile для компиляции и запуска Kazino-Royal.cpp
# На основе example-2 с адаптацией под один файл

.PHONY: all build run clean

# Компилятор
CC = g++
CFLAGS = -Wall -Wextra -std=c++11

# Имена файлов
SOURCE = Kazino-Royal.cpp
EXEC = kazino-royal

# Цели по умолчанию
all: build run

# Сборка программы
build: $(EXEC)

$(EXEC): $(SOURCE)
	$(CC) $(CFLAGS) $(SOURCE) -o $(EXEC)

# Запуск программы
run: $(EXEC)
	./$(EXEC)

# Отладочная сборка
debug: CFLAGS += -g -O0
debug: $(EXEC)
	@echo "Собрана отладочная версия с debug символами"

# Релизная сборка
release: CFLAGS += -O2 -DNDEBUG
release: $(EXEC)
	@echo "Собрана оптимизированная релизная версия"

# Очистка
clean:
	rm -f $(EXEC) *.o *.out *.gch core

# Показать помощь
help:
	@echo "Доступные цели:"
	@echo "  make all     - собрать и запустить программу"
	@echo "  make build   - только собрать программу"
	@echo "  make run     - только запустить программу"
	@echo "  make debug   - собрать с debug символами"
	@echo "  make release - собрать оптимизированную версию"
	@echo "  make clean   - удалить скомпилированные файлы"
	@echo "  make help    - показать эту справку"

.PHONY: all build run debug release clean help
