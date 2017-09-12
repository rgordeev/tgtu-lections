---

### Подготовка окружения

---

### Системы контроля версий

+++

### Базовые операции при работе с кодом

* Добавить файл
* Удалить файл
* Изменить файл

Как решить проблему конкурентных изменений?

+++

### Примеры версионирования

* Dropbox
* Google Docs
* Microsoft Office

+++

История изменений формируется ревизиями. Ревизия может базироваться как на
моментальных снимках (снепшотах), так и на дельте изменений от предыдущего состояния
(diff).

Между двумя любыми снимками можно вычислить дельту (diff).

+++

Базовый рабочий процесс при работе с СКВ:

1. Инициализация (создание) репозитория
2. Добавление новых файлов
3. Коммит
4. Любые операции с файлами (добавление, удаление или изменение)
5. Коммит
...

+++

### Первое поколение

RCS, SCCS

* Работали с каждым файлом индивидуально
* Только локальная работа

+++

### Второе поколение

CVS, SourceSafe, Subversion

* Многофайловые
* Централизованные
* Требуют наличия сервера

+++

### Третье поколение

Git, Bazaar, Mercurial

* Распределенные
* У каждого свой полноценный репозиторий

---

### Git

+++

### Установка git

* https://git-scm.com
* `apt-get install git` (linux)
* `brew install git` (mac)

+++

Конфигурирование git

```
git config --global user.name = "Some Name"
git config --global user.email = "some@mail.com"
```

+++

Инициализация репозитория

```
git init
```

Посмотреть настройки репозитория
```
cat .git/config
git config --list
```

+++

Фиксирование изменений

```
git add .
git commit -m "some comment"
```

+++

Работа с историей

```
git log
git log -p
git show <commit-id>
```

+++

### Практика

[https://try.github.io/levels/1/challenges/1](https://try.github.io/levels/1/challenges/1)

---

### Состояния рабочей копии

* Untracked
* Tracked
  * unmodified
  * modified
  * staged

+++

Смотрим текущее состояние рабочей копии

```
git status
```

Перевод Untracked -> Tracked
и перевод modified -> staged
```
git add .
```

Перевод staged -> unmodified
```
git commit
```

Перевод staged -> modified
```
git reset <path>
```

Перевод modified -> unmodified

```
git checkout path/to/file
```

+++

### Литература

[https://git-scm.com/book/ru/v2](https://git-scm.com/book/ru/v2)