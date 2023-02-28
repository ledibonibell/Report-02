# Report-02

# Task 1

## 1. Создайте пустой репозиторий на сервисе github.com (или `gitlab.com`, или `bitbucket.com`)

```
https://github.com/ledibonibell/lab-02.git
```

## 2. Выполните инструкцию по созданию первого коммита на странице репозитория, созданного на предыдещем шаге
 
```
$ mkdir lab-02
$ echo "# lab-02" >> README.md
$ git init
$ git add README.md
$ git commit -m "first commit"
$ git remote add origin https://github.com/ledibonibell/lab-02.git
$ git push -u origin master
```

## 3. Создайте файл `hello_world.cpp` в локальной копии репозитория (который должен был появиться на шаге 2). Реализуйте программу `Hello world` на языке C++ используя плохой стиль кода. Например, после заголовочных файлов вставьте строку `using namespace std;`
 
```
#include <iostream>

using namespace std;

int main(int argc, char** argv) {
   cout << "Hello world" << endl;
}
```

## 4. Добавьте этот файл в локальную копию репозитория
 
```
$ git add "Hello world.cpp"
```

## 5. Закоммитьте изменения с осмысленным сообщением
 
```
$ git commit -m "This is first file"
```

## 6. Изменитьте исходный код так, чтобы программа через стандартный поток ввода запрашивалось имя пользователя. А в стандартный поток вывода печаталось сообщение `Hello world` from `@name`, где `@name` имя пользователя
 
```
$ alias edit=subl
$ edit "Hello world.cpp"
```
```
#include <iostream>
#include <string>
 
using namespace std;

int main(int argc, char** argv) {
   string name;
   cin >> name;
   cout << "Hello world from " << name << endl;
}
```

## 7. Закоммитьте новую версию программы. Почему не надо добавлять файл повторно `git add`?

You do not need to re-write the git add command, because the file was already added in step 4
```
$ git commit -a -m "Changed cpp file"
```

## 8. Запуште изменения в удалёный репозиторий
 
```
$ git push -u origin master
```

## 9. Проверьте, что история коммитов доступна в удалёный репозитории
 
The history of changes is available in the repository

# Task 2

## 1. В локальной копии репозитория создайте локальную ветку `patch1`
 
```
$ git checkout -b patch1
```

## 2. Внесите изменения в ветке `patch1` по исправлению кода и избавления от `using namespace std;`
 
```
$ edit "Hello world.cpp"
```
```
#include <iostream>
#include <string>
 
int main(int argc, char** argv){
  string name;
  std::cin >> name;
  std::cout << "Hello world from " << name << std::endl;
}
```

## 3. `commit`, `push` локальную ветку в удалённый репозиторий
 
```
$ git commit -a -m "Fixed cpp file"
$ git push -u origin patch1
```

## 4. Проверьте, что ветка `patch1` доступна в удалёный репозитории
 
The `patch1` branch is available in the remote repository

## 5. Создайте `pull-request` `patch1 -> master`
 
Create a pull-request `patch1 -> master`

## 6. В локальной копии в ветке `patch1` добавьте в исходный код комментарии
 
```
$ edit "Hello world.cpp"
```
```
#include <iostream>
#include <string>
 
int main(int argc, char** argv){
  string name;                                           // Name of @user
  std::cin >> name;                                      // Input name of @user
  std::cout << "Hello world from " << name << std::endl; // Output name of @user
} 
```

## 7. `commit, push`
 
```
$ git commit -a -m "Code with comments"
$ git push -u origin patch1
```

## 8. Проверьте, что новые изменения есть в созданном на шаге 5 `pull-request`
 
There are new changes in the pull-request created in step 5

## 9. В удалённый репозитории выполните слияние `PR` `patch1 -> master` и удалите ветку `patch1` в удаленном репозитории

## 10. Локально выполните `pull`
 
```
$ git pull origin
```

## 11. С помощью команды `git log` просмотрите историю в локальной версии ветки `master`
 
```
$ git log master
```

## 12. Удалите локальную ветку `patch1`

```
$ git checkout -b origin
$ git branch -d patch1
```

# Task 3

## 1.
 
```

```

## 2.
 
```

```

## 3.
 
```

```

## 4.
 
```

```

## 5.
 
```

```

## 6.
 
```

```

## 7.
 
```

```

## 8.
 
```

```

## 9.
 
```

```

## Required libraries

```
$ sudo apt install git
$ sudo snap install sublim-text
```

## References used
- https://habr.com/ru/post/541258/
- https://losst.pro/komandy-linux-dlya-raboty-s-fajlami
- https://ru.stackoverflow.com/questions/134183/Что-такое-pull-request
- 
