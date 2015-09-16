# Методы программирования 2: Множества на основе битовых полей

[![Build Status](https://travis-ci.org/UNN-VMK-Software/mp2-lab1-set.svg)][travis]

<!-- TODO
  -
-->

## Цели и задачи

__Цель данной работы__  — разработка структуры данных для хранения множеств с
использованием битовых полей, а также освоение таких инструментов разработки
программного обеспечения, как система контроля версий [Git][git] и фрэймворк для
разработки автоматических тестов [Google Test][gtest].

Предполагается, что перед выполнением работы студенты получают данный
проект-шаблон, содержащий следующее:

 - Интерфейсы классов битового поля и множества (h-файлы)
 - Готовый набор тестов для каждого из указанных классов
 - Пример использования класса битового поля и множества для решения задачи
   поиска простых чисел с помощью алгоритма ["Решето Эратосфена"][sieve]

Выполнение работы предполагает решение следующих задач:

  1. Реализация класса битового поля `TBitField` согласно заданному интерфейсу.
  1. Реализация класса множества `TSet` согласно заданному интерфейсу.
  1. Обеспечение работоспособности тестов и примера использования.

## Используемые инструменты

  - Система контроля версий [Git][git]. Рекомендуется использовать один из
    следующих клиентов на выбор студента:
    - [Git](https://git-scm.com/downloads)
    - [GitHub Desktop](https://desktop.github.com)
  - Фреймворк для написания автоматических тестов [Google Test][gtest]. Не
    требует установки, идет вместе с проектом-шаблоном.
  - Среда разработки Microsoft Visual Studio (2008 или старше).
  - Опционально. Утилита [CMake](http://www.cmake.org) для генерации проектов по
    сборке исходных кодов. Она может быть использована для генерации решения для
    среды разработки, отличной от Microsoft Visual Studio 2008 или 2010, предоставленных в данном проекте-шаблоне.

## Общая структура проекта

Структура проекта:

  - `docs` — инструкции по выполнению лабораторной работы, полезные документы.
  - `gtest` — библиотека Google Test.
  - `include` — директория для размещения заголовочных файлов.
  - `samples` — директория для размещения демо-приложений.
  - `sln` — директория с файлами решений и проектов для VS 2008 и VS 2010,
    вложенные директории `vc9` и `vc10` соответственно.
  - `src` — директория с исходными кодами (cpp-файлы).
  - `test` — директория с модульными тестами и основным приложением,
    инициализирующим запуск тестов.
  - `README.md` — информация о проекте, которую вы сейчас читаете.
  - Служебные файлы
    - `.gitignore` — перечень расширений файлов, игнорируемых Git при добавлении
      файлов в репозиторий.
    - `CMakeLists.txt` — корневой файл для сборки проекта с помощью CMake. Может
      быть использован для генерации проекта в среде разработки, отличной от
      Microsoft Visual Studio.
    - `.travis.yml` — конфигурационный файл для системы автоматического
      тестирования Travis-CI. Тесты, входящие в состав шаблонного проекта,
      регулярно запускаются на удаленной [инфраструктуре][travis].

В решении содержатся следующие модули:

  - Модуль `tbitfield`, содержащий реализацию класса битового поля (файлы
    `./include/tbitfield.h`, `./src/tbitfield.cpp`). Предполагается, что в ходе
    выполнения работы реализуются методы класса в файле `./src/tbitfield.cpp`,
    при этом заголовочный файл `./include/tbitfield.h` с объявлениями должен
    оставаться неизменным.
  - Модуль `tset`, содержащий реализацию класса множества (файлы
    `./include/tset.h`, `./src/tset.cpp`). При выполнении работы так же, как и в
    случае класса битового поля, разрабатывается только реализация методов
    класса.
  - Тесты для классов битовое поле и множество (файлы
    `./test/test_tbitfield.cpp`, `./test/test_tset.cpp`).
  - Пример использования класса битового поля и множества для поиска простых
    чисел с использованием алгоритма, называемого ["Решетом Эратосфена"][sieve]
    (файл `./samples/sample_prime_numbers.cpp`).

## Инструкция по выполнению работы

Предполагается выполнение лабораторной работы в несколько шагов:

  1. Освоение общих принципов работы с Git и GitHub. Последовательность
     действий, которую необходимо выполнить перед началом работы с
     проектом, описана в документе, посвященному [Git][git-guide].
  1. Освоение общих принципов работы с Google Test. Инструкции приведены в
     разделе, посвященному [Google Test][gtest-guide].
  1. Создание полноценных реализаций классов `TBitField` и `TSet`, проходящих
     все автоматические тесты.

<!-- LINKS -->

[git]:         https://git-scm.com/book/ru/v2
[gtest]:       https://github.com/google/googletest
[sieve]:       http://habrahabr.ru/post/91112
[travis]:      https://travis-ci.org/UNN-VMK-Software/mp2-lab1-set
[git-guide]:   https://github.com/UNN-VMK-Software/mp2-lab1-set/blob/master/docs/part1-git.md
[gtest-guide]: https://github.com/UNN-VMK-Software/mp2-lab1-set/blob/master/docs/part2-google-test.md
