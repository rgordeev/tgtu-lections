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