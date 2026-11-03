# Лабораторная работа №4
## Тема: Основы работы с системой контроля версий Git и веб-сервисом GitHub

**Выполнил:** Замарин Даниил, ст. гр. УТС-251т

## Цель работы
Изучить базовые концепции контроля версий, приобрести практические навыки установки и настройки Git, создания локальных и удаленных репозиториев, а также организации структуры для хранения последующих лабораторных работ по программированию.

## Ход выполнения работы

В процессе выполнения работы были выполнены следующие шаги:
1. **Установка и настройка:** Проверена установка Git, заданы глобальные параметры пользователя (имя и email) с помощью команд `git config --global user.name` и `git config --global user.email`.
2. **Создание локального репозитория:** В папке `programming-labs` выполнена инициализация репозитория командой `git init`.
3. **Создание структуры:** Созданы каталоги для лабораторных работ (например, `lab_01`, `lab_02` и т.д.) и файлы отчетов `README.md` в формате Markdown.
4. **Первый коммит:** Файлы подготовлены к сохранению (`git add .`) и зафиксированы с осмысленным комментарием (`git commit -m "Initial commit"`).
5. **Создание удаленного репозитория:** На платформе GitHub создан публичный репозиторий `programming-labs` (без инициализации README, чтобы избежать конфликтов).
6. **Связывание и отправка:** Локальный репозиторий связан с удаленным (`git remote add origin ...`), ветка переименована в `main`, выполнен пуш всех файлов (`git push -u origin main`).



```bash
PS C:\Users\iulii\OneDrive\Desktop\programming-labs> git init
Initialized empty Git repository in C:/Users/iulii/OneDrive/Desktop/programming-labs/.git/
PS C:\Users\iulii\OneDrive\Desktop\programming-labs> git config --global user.name "Даниил Замарин"
PS C:\Users\iulii\OneDrive\Desktop\programming-labs> git config --global user.email "dazam2707@gmail.com"
PS C:\Users\iulii\OneDrive\Desktop\programming-labs> git remote add origin https://github.com/DanyaToGit/programming-labs.git
PS C:\Users\iulii\OneDrive\Desktop\programming-labs> git branch -M main
PS C:\Users\iulii\OneDrive\Desktop\programming-labs> git add .
PS C:\Users\iulii\OneDrive\Desktop\programming-labs> git commit -m "Initial commit: create structure and labs"
[main (root-commit) aec8a69] Initial commit: create structure and labs
 4 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 lab_01/README.md
 create mode 100644 lab_02/README.md
 create mode 100644 lab_03/README.md
 create mode 100644 lab_04/README.md
PS C:\Users\iulii\OneDrive\Desktop\programming-labs> git push -u origin main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (4/4), 310 bytes | 103.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/DanyaToGit/programming-labs.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
```

## Ответы на контрольные вопросы

**1. В чем разница между локальным репозиторием Git и удаленным репозиторием GitHub?**
Локальный репозиторий — это скрытая папка `.git` на компьютере пользователя, которая хранит всю историю изменений и позволяет работать автономно (без интернета). Удаленный репозиторий (на GitHub) — это копия проекта на сервере, которая служит для резервного копирования, совместной работы и демонстрации кода преподавателю или другим разработчикам.

**2. За что отвечают команды `git add` и `git commit`? Какова последовательность их применения?**
Команда `git add` добавляет измененные или новые файлы в так называемую «область подготовки» (staging area) — буфер, из которого формируется будущий снимок проекта. Команда `git commit` сохраняет содержимое этой области в историю репозитория, создавая новый уникальный снимок с описанием изменений. 
*Последовательность:* сначала `git add` (выбираем, что сохранить), затем `git commit` (фиксируем).

**3. Что делает команда `git push`?**
Команда `git push` отправляет локальные коммиты (снимки проекта) в удаленный репозиторий (на GitHub). Она синхронизирует локальную ветку с удаленной, делая код доступным на сервере.

**4. Зачем нужна команда `git status`?**
Команда `git status` показывает текущее состояние рабочей директории и области подготовки. Она позволяет увидеть, какие файлы были изменены, какие уже добавлены в индекс (`git add`), а какие еще не отслеживаются Git. Это главный инструмент контроля перед созданием коммита.

## Вывод
В ходе лабораторной работы были изучены базовые принципы работы с системой контроля версий Git и сервисом GitHub. Были приобретены практические навыки установки Git, его настройки, создания локального репозитория и синхронизации его с удаленным публичным репозиторием. Созданная структура каталогов и настроенная связь с GitHub позволяют в дальнейшем вести все последующие лабораторные работы в едином репозитории, используя стандартный цикл `add → commit → push`.

## Ссылка на репозиторий
https://github.com/DanyaToGit/programming-labs