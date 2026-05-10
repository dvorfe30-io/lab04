## Lab03
### Матвеев Андрей. ИУ8-23

## Homework

Представьте, что вы стажер в компании "Formatter Inc.".
### Задание 1
Вам поручили перейти на систему автоматизированной сборки **CMake**.
Исходные файлы находятся в директории [formatter_lib](formatter_lib).
В этой директории находятся файлы для статической библиотеки *formatter*.
Создайте `CMakeList.txt` в директории [formatter_lib](formatter_lib),
с помощью которого можно будет собирать статическую библиотеку *formatter*.
[CMakeLists.txt](https://github.com/dvorfe30-io/lab03/blob/main/formatter_lib/CMakeLists.txt)
### Задание 2
У компании "Formatter Inc." есть перспективная библиотека,
которая является расширением предыдущей библиотеки. Т.к. вы уже овладели
навыком созданием `CMakeList.txt` для статической библиотеки *formatter*, ваш 
руководитель поручает заняться созданием `CMakeList.txt` для библиотеки 
*formatter_ex*, которая в свою очередь использует библиотеку *formatter*.
[CMakeLists.txt](https://github.com/dvorfe30-io/lab03/blob/main/formatter_ex_lib/CMakeLists.txt)
### Задание 3
Конечно же ваша компания предоставляет примеры использования своих библиотек.
Чтобы продемонстрировать как работать с библиотекой *formatter_ex*,
вам необходимо создать два `CMakeList.txt` для двух простых приложений:
* *hello_world*, которое использует библиотеку *formatter_ex*;
* *solver*, приложение которое испольует статические библиотеки *formatter_ex* и *solver_lib*.
### main CMakeLists.txt
[CMakeLists.txt](https://github.com/dvorfe30-io/lab03/blob/main/CMakeLists.txt)

### hello_world_application
[CMakeLists.txt](https://github.com/dvorfe30-io/lab03/blob/main/hello_world_application/CMakeLists.txt)

### solver_application
[CMakeLists.txt](https://github.com/dvorfe30-io/lab03/blob/main/solver_application/CMakeLists.txt)

### solver_lib
[CMakeLists.txt](https://github.com/dvorfe30-io/lab03/blob/main/solver_lib/CMakeLists.txt)

<details>
<summary>Вывод сборки</summary>

```bash
$ cmake -B build
-- Configuring done
-- Generating done
-- Build files have been written to: /home/aa44/git/laba3/lab03_hw/build
$ cmake --build build
gmake[1]: вход в каталог «/home/aa44/git/laba3/lab03_hw/build»
gmake[2]: вход в каталог «/home/aa44/git/laba3/lab03_hw/build»
gmake[2]: выход из каталога «/home/aa44/git/laba3/lab03_hw/build»
[ 20%] Built target formatter
gmake[2]: вход в каталог «/home/aa44/git/laba3/lab03_hw/build»
gmake[2]: выход из каталога «/home/aa44/git/laba3/lab03_hw/build»
[ 40%] Built target formatter_ex
gmake[2]: вход в каталог «/home/aa44/git/laba3/lab03_hw/build»
Scanning dependencies of target solver
gmake[2]: выход из каталога «/home/aa44/git/laba3/lab03_hw/build»
gmake[2]: вход в каталог «/home/aa44/git/laba3/lab03_hw/build»
[ 50%] Building CXX object solver_lib/CMakeFiles/solver.dir/solver.cpp.o
[ 60%] Linking CXX static library libsolver.a
gmake[2]: выход из каталога «/home/aa44/git/laba3/lab03_hw/build»
[ 60%] Built target solver
gmake[2]: вход в каталог «/home/aa44/git/laba3/lab03_hw/build»
Scanning dependencies of target hello_world_application
gmake[2]: выход из каталога «/home/aa44/git/laba3/lab03_hw/build»
gmake[2]: вход в каталог «/home/aa44/git/laba3/lab03_hw/build»
[ 70%] Building CXX object hello_world_application/CMakeFiles/hello_world_application.dir/hello_world.cpp.o
[ 80%] Linking CXX executable hello_world_application
gmake[2]: выход из каталога «/home/aa44/git/laba3/lab03_hw/build»
[ 80%] Built target hello_world_application
gmake[2]: вход в каталог «/home/aa44/git/laba3/lab03_hw/build»
Scanning dependencies of target solver_application
gmake[2]: выход из каталога «/home/aa44/git/laba3/lab03_hw/build»
gmake[2]: вход в каталог «/home/aa44/git/laba3/lab03_hw/build»
[ 90%] Building CXX object solver_application/CMakeFiles/solver_application.dir/equation.cpp.o
[100%] Linking CXX executable solver_application
gmake[2]: выход из каталога «/home/aa44/git/laba3/lab03_hw/build»
[100%] Built target solver_application
gmake[1]: выход из каталога «/home/aa44/git/laba3/lab03_hw/build»
```
</details>
