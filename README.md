# Сортировка данных на магнитной ленте

Устройство хранения данных типа лента (Tape) предназначено для последовательной записи и
чтения данных. Считывающая/записывающая магнитная головка неподвижна во время чтения и
записи, а лента имеет возможность двигаться в обоих направлениях. Запись и чтение информации
возможны в ячейку ленты, на которой в данный момент находится магнитная головка.
Перемещения ленты – затратная по времени операция – лента не предназначена для
произвольного доступа.

Имеется входная лента длины N (где N – велико), содержащая элементы типа integer (2^32).
Имеется выходная лента такой же длины. Необходимо записать в выходную ленту
отсортированные по возрастанию элементы с входной ленты. Есть ограничение по использованию
оперативной памяти – не более M байт (M может быть < N, т.е. загрузить все данные с ленты в
оперативную память не получится). Для реализации алгоритма можно использовать разумное
количество временных лент, т.е. лент, на которых можно хранить какую-то временную
информацию, необходимую в процессе работы алгоритма.

Для решения задания используются временные ленты в каталоге сборки ```build/tmp/```, которые после сортировки удаляются. Временные ленты имеют размер небольший размера указанной доступной оперативной памяти в командной строке.

## Сборка и запуск

* Для сборки проекта требуется перейти в корень проекта и выполнить следующую команду:
**Linux:**
```bash
sudo chmod +x build.sh
./build.sh
```

* После сборки для запуска требуется из корня проекта выполнить следующие команды:
**Linux:**
```bash
cd /build/src
./yadro_task <файл неотсортированной ленты> <файл отсортированной ленты> <конфигурационный файл> <размер доступной ОП>
```


Файлы с неотсортиированной и отсортированной лентами находятся в папке ```resources/```, конфигурационные файлы должны находиться в папке ```resources/config/```
