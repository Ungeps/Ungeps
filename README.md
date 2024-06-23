# Проект - фрагментации HTML

# Команда 7: Проект Advanced C

# Участники команды:

- Бибиков Никита, группа 4.307-1
- Кравченко Михаил, группа 4.307-1
- Шмаков Григорий, группа 4.307-1
- Ляпин Ермак, группа 4.307-1
- Буренкин Егор, группа 4.307-1
- Пашин Унан, группа 4.307-1

# Описание
Проект предназначен для разделения HTML-сообщений на фрагменты, которые не превышают максимальную допустимую длину.
Это необходимо для корректной работы корпоративного мессенджера, который накладывает ограничение на длину сообщений в 4096 символов.
Программа сохраняет корректную HTML-структуру при разделении сообщений.

# Функциональные возможности

## Разделение HTML-сообщений

- Сохранение корректной структуры тегов при разделении.
- Возможность задать максимальную длину фрагмента.

### Обработка ошибок

- Исключение в случае невозможности разделения фрагмента.

## Параметры командной строки

- `--max-len`: Максимальная длина фрагмента.
- `<file>`: Путь к HTML-файлу, который необходимо разделить.

## Установка

### Зависимости кода

- Компилятор для языка Си gcc

### Сборка

1. Клонируйте репозиторий:
2. Скомпилируйте проект:
    ```bash
    gcc -o split_msg split_msg.c msg_split.c
    ```

3. Запустите приложение:
    ```bash
    ./split_msg --max-len=3072 ./test-1.html
    ```

## Использование

### Примеры использования

1. Разделение HTML-сообщения:
    ```bash
    ./split_msg --max-len=3072 ./test-1.html
    ```

    ## Тестирование

Для запуска unit-тестов выполните:
```bash
gcc -o test_msg_split test_msg_split.c msg_split.c
./test_msg_split
