# Параллельный алгоритм сортировки вставками
Данный алгоритм в классическом его исполнении является последовательным, поэтому для его распараллеливания был использован метод "разделяй и властвуй". Данный метод заключается в разбиении задачи на более мелкие подзадачи, решение которых происходит независимо, а затем объединении
результатов этих подзадач в окончательный результат.

Для распараллеливании программы использован стандарт OpenMP
## Сборка и запуск
Эксперименты проводились на следующей конфигурации:

**Процессор 4-х ядерный**: Intel(R) Core(TM) i7-7700 CPU @ 3.60GHz

**ОЗУ**: 6 Gb DDR4

**ОС**: Linux Debian 6.1.38-4 (2023-08-08) x86_64 GNU/Linux

**Компилятор**: g++ (Debian 12.2.0-14) 12.2.0

Компиляция: ``g++ omp_is.coo -fopenmp -o main.bin``

Запуск: ``./main.bin``

## Сравнительная оценка эффектиновсти 

![image](https://github.com/deathlokmike/parallel_insertion_sort/assets/45070165/61dc7cf7-c4ce-42f3-9726-63b74377dd11)

![image](https://github.com/deathlokmike/parallel_insertion_sort/assets/45070165/984b3467-375f-4997-ad88-fa902c82f785)

Для подробного ознакомления, рекомендую статью:
https://www3.cs.stonybrook.edu/%7Epramod.ganapathi/doc/papers/2021-ComputerJournal-Sorting.pdf