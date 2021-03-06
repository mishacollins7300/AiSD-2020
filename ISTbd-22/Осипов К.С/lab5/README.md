# Отчёт по лабораторной работе №5 #

## Что называется внешней сортировкой ##

Внешняя сортировка – это сортировка данных, которые расположены на внешних устройствах и не вмещающихся в оперативную память.

## На основе каких процедур основываются алгоритмы внешней сортировки ##

В основе большинства методов внешних сортировок лежит процедура слияния и процедура распределения.

## Определения характеристик алгоритмов: Распределение, Слияние, Серия, Фаза, Виды слияния (двухпутевое и многопутевое) ##

Серия – это последовательность элементов, которая упорядочена по ключу.

Фаза – это действия по однократной обработке всей последовательности элементов. Например, двухфазная сортировка – это сортировка, в которой отдельно реализуется две фазы: распределение и слияние.

Распределение – это процесс разделения упорядоченных серий на два или несколько вспомогательных файла.

Слияние – это процесс объединения двух или более упорядоченных серий в одну упорядоченную последовательность при помощи циклического выбора элементов, доступных в данный момент.

Двухпутевым слиянием называется сортировка, в которой данные распределяются на два вспомогательных файла. Многопутевое слияние - данные распределяются на N > 2 вспомогательных файлов.

## Характеристики алгоритма простого слияния ##

Алгоритм сортировки простым слияния является простейшим алгоритмом внешней сортировки, который основан на процедуре слияния серией.

Алгоритм сортировки простым слиянием:

1. Исходный файл разбивается на два вспомогательных файла.
2. Вспомогательные файлы сливаются в исходный файл, при этом одиночные элементы образуют упорядоченные пары.
3. Полученный файл вновь обрабатывается, как указано в шагах 1 и 2. При этом упорядоченные пары переходят в упорядоченные четверки.
4. Повторяя шаги, сливаем четверки в восьмерки и т.д., каждый раз удваивая длину слитых последовательностей до тех пор, пока не будет упорядочен целиком весь файл.

Для выполнения внешней сортировки методом простого слияния в оперативной памяти требуется расположить всего лишь две переменные – для размещения очередных элементов (записей) из вспомогательных файлов. Исходный и вспомогательные файлы будут O(log₂ n) раз прочитаны и столько же раз записаны.
