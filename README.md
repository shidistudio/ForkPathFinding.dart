PathFinding.dart
================

A Dart port of https://github.com/qiao/PathFinding.js library

Usage:
------

```
dependencies:
  pathfinding:
    git: git://github.com/pavelgj/PathFinding.dart.git
```

```dart
import 'package:pathfinding/finders/jps.dart';
import 'package:pathfinding/core/grid.dart';

main() {
  var grid = new Grid(4, 4, [
    [0, 0, 1, 1], // 0 - walkable, 1 - not walkable
    [1, 0, 1, 1],
    [1, 0, 1, 1],
    [1, 0, 0, 0]
  ]);
  var jps = new JumpPointFinder();
  var path = jps.findPath(0, 0, 3, 3, grid);
  print(path); // [[0, 0], [1, 1], [1, 2], [2, 3], [3, 3]]
}
```

Available finders:
------------------
 - JumpPointFinder

TODO:
 - AStar
 - BreadthFirst
 - Dijkstra
 - BiBreadthFirst
 - BiDijkstra
 - BiAStarFinder
 - BestFirstFinder
 - BiBestFirstFinder

