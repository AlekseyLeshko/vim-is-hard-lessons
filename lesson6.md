# Урок №6

## Презентация

## Практикум

Каждое упражнение в этом занятие лучше выполнять в отдельно запущеной сессии
командного интерпретатора.

Для этого откройте вкладку или отдельное окно

### 1. Пробуем grep

  0. Откройте vim выполнив `vim`.

  1. Наберите `:grep vim *.md`, чтобы запустить поиск `vim` во всех файлах
     уроков.

  2. Используйте `:cnext` и `:cprev` чтобы перемещаться по совпадениям.

### 2. Поиск сначала по открытому, затем по всем файлам

  0. Откройте vim выполнив `vim`.

  1. Начните искать по файлу строку `vim`.

  2. Наберите `:vim /`

  4. Нажмите `<C+r>/`, чтобы вставить в командную стру содержимое
     регистра поиска.

  5. Наберите оставшуюся часть команды `/ *.md`, и нажмите `<Enter>`
     чтобы начать поиск.

  6. Используйте `:cnext` и `:cprev` чтобы перемещаться по совпадениям.


### 3. Рефакторинг с Ack

Для выполнения этого упражнения вам потребуется плагин
[ack.vim](https://github.com/mileszs/ack.vim)
При выполнении задания могут возникнуть проблемы из-за того, что
в системе не установлен сам ack
для убунты: `sudo apt-get install ack`

Задача переименовать метод класса `Animal` из `walk` в `run`

  0. Откройте vim выполнив `vim`.

  1. Наберите `:Ack 'walk' lesson6`, чтобы начать поиск `walk` в папке `lesson`.

  2. Нажимайте `j`, `k`, чтобы перемещатья по результатам.

  3. Поочередно откройте каждый файл с помощью клавиши `o` и выполните задания
     используя ранее полученные знания.

СОВЕТЫ:

  - Заменить слово – `cw`
  - Перемещение между окнами – `Ctrl+w(h|j|k|l)`
  - Закрыть окно поиска – `:q`

### 4. Ctrl+p. Открываем файл.

Для выполнения этого упражнения вам потребуется плагин
[ctrlp.vim](https://github.com/kien/ctrlp.vim)

  0. Откройте vim выполнив `vim`.

  1. Нажмите `Ctrl+p`, чтобы открыть окно поиска.

  2. Наберите `mo`.

  3. Перемещайтесь по результатам с помощью `Ctrl+j`, `Ctrl+k`

  4. Чтобы открыть файл, нажмите `Enter`

### 5. Слепой рефакторинг с :argdo

Заменим во всех файлах объявление класса на модуль.

  1. Выполните команду `:args lesson6/**/*.rb`.

  2. Выполните команду `:agrs` чтобы посмотреть содержимое аргументов.

  3. Выполните команду `:argdo! %s/class/module/gI`

  4. С помощью ранее изученных методов перехода по файлам, убедитесь что все
     верно.

