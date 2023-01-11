# sudoku-dart





## 关于 about

 [![License](https://img.shields.io/badge/License-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE)[![License](https://img.shields.io/badge/BSD-3-Clause.svg)](https://opensource.org/licenses/BSD-3-Clause)

数独 **解题器** 和 **生成器** 开源库 `dart` 版

支持对 唯一/非唯一解数独进行解题 以及 唯一解数独随机生成

opensource sudoku solver and puzzle generator `dart` library

## 安装 install
### with flutter :
`flutter pub add sudoku_dart`

### only dart:
This will add a line like this to your package's `pubspec.yaml`
```
dependencies:
  sudoku_dart: ^1.0.0
```
import
```
import 'package:sudoku_dart/sudoku_dart.dart';
```

## 使用 tutorial

### 解题 solver
```dart
// 支持数独解题
// 输入一维数组的puzzle,-1为待填空
  List<int> puzzle = [
    -1,-1,8,    9,-1,6,     -1,-1,5,
    -1,4,3,     -1,-1,-1,   -1,2,-1,
    -1,-1,-1,   -1,-1,-1,   -1,-1,-1,

    -1,-1,4,    -1,-1,-1,   9,-1,-1,
    5,-1,-1,    -1,4,-1,    6,8,-1,
    -1,-1,-1,   1,-1,-1,    -1,-1,-1,

    2,-1,-1,    -1,8,-1,    -1,7,-1,
    -1,-1,-1,   -1,3,4,     1,-1,-1,
    -1,6,-1,    -1,-1,9,    -1,-1,-1,
  ];

sudoku = Sudoku(puzzle);
// if you need check this puzzle is one-solution sudoku or not,use  strict:true 
// sudoku = Sudoku(puzzle, strict: true);
// 打印调试信息
sudoku.debug();
// origin puzzle
sudoku.puzzle;
// full answer sudoku
sudoku.answer;
```

### 随机生成数独 generator
```dart
import 'package:sudoku_dart/sudoku_dart.dart';
// generate random puzzle with one-solution
// LEVEL : EASY(简单), MEDIUM(中等), HARD(困难), EXPERT(专家)
Sudoku sudoku = Sudoku.generator(LEVEL.EXPERT);
```

## more
this library use on `sudoku-flutter` , support for android and iOS app  , if interesting welcome visit this repository : 

[einsitang/sudoku-flutter](https://github.com/einsitang/sudoku-flutter)