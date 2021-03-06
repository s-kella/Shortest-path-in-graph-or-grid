# Shortest-path-in-graph-or-grid

Программма находит кратчайший путь и его длину в гриде или графе по одному из следующих алгоритмов: dijkstra, bfs, astar, считывая исходные данные из xml файла.

### Пример запуска
#### Grid

Для использования грида:  
В файле grid_example.xml в строку 3 
```
<algorithm type="алгоритм"/>
```
вместо слова алгоритм впишите один из трёх алгоритмов: dijkstra, bfs, astar.  
  
В строке 4 задайте координаты i и j старта и финиша (впишите их в ковычки).  
Пример, для стартовой точки (3;1) и финишной точки (4;3):
```
<task start.i="3" start.j="1" goal.i="4" goal.j="3"/>
```
В строке 5 задайте ширину и высоту грида, а также связность (4 - можно двигаться только вверх-вниз-влево-вправо, 8 - можно двигаться ещё и по диагонали).  
Пример для 4-связного грида, размером 6*6:
```
<graph type="grid" width="6" height="6" connectedness="4">
```
Задайте грид. Поставьте нолики в местах, где проход есть и единицы, если там прохода нет.  

Запустите программу:

```
main.py  
grid
```
#### Graph 
Для использования графа:  
В файле graph_example.xml в строку 3 
```
<algorithm type="алгоритм"/>
```
вместо слова алгоритм впишите один из трёх алгоритмов: dijkstra, bfs, astar.   
  
В строку 4 впишите стартовую и конечную точки.  
Пример для стартовой точки А и конечной точки L:
```
<task start.id="A" goal.id="L"/>
```
Далее напишите все точки графа в формате:
```
<node id="Буква, обозначающая точку"/>
```
Далее запишите все возможные маршруты и их вес в формате:
```
<edge source="старт" target="финиш" weight="вес"/>
```  

Запустите программу:
```
main.py   
graph
```

### Цель проекта

Код написан в образовательных целях
