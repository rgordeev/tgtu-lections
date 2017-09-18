---

### Основы *nix систем и работы с терминалом

hexlet.io

---

### Справка по доступным командам терминала

```
man <command-name>
```

---

### Навигация

+++?image=assets/fs-structure.png

+++

Вывод информации о папках и файлах

```
pwd
ls
```

+++

Смена текущего каталога

```
cd <path>
cd
cd ~/<path in home dir>
cd /<absolute path>
cd <relative-path>
```

---

### Управление файловой структурой

+++

```
mkdir

mkdir <dir name>

mkdir -p <dir name>/<another>/<some more>

touch <path>/<file-name>

tree <path>
```

+++

```
mv <dir1> <dir2>

mv <dir1>/* <dir2>

rm <path-to-file>

rm -f <path-to-dir>

rm -r <path>/*
```

---

### Просмотр содержимого файла

+++

```
cat <file-name>

head <file-name>

tail <file-name>

tail -f <file-name>

grep <reg-exp>
```

---

### Постраничный вывод (пейджинг)

+++

```
less <file-name>

more <file-name>
```

---

### Работа с документацией

+++

```
man man

man ls

man -f man

man 5 man.config
```

---

### Переменные окружения

+++

```
# установить переменную окружения
MY_HOME=$HOME/mydir

# удалить переменную окружения
unset MY_HOME

# список переменных окружения
env

# inline инициализация переменных
MY_VAR=5 ./some_script

# export делает доступной переменную в env
export MY_VAR=5
./some_script
```

---

### Перенаправления и потоки

+++

```
# записать в файл
echo 'Hello!' > my_file

# прочитать файл 
sort < my_file

# перенаправление
sort < my_file > sorted_file

# pipeline
cat my_file | sort

ls | grep 'a' | grep 'b'

ls | grep 'a' | wc
```

---

### Работа с историей

+++

```
# история вызовов
~/.bash_history

# работа с историей
history

# повторить вызов из истории
!<номер вызова>

# повторить последний вызов
!!

# последний вызов совпадающий с шаблоном
!cat

# поиск по истории
CTRL + R
```

---

### Псевдонимы

+++

```
# список псевдонимов
alias

# установить алиас 
alias l='ls -alF' 

# вычислить алиас
type l

# сбросить алиас
unalias l
```