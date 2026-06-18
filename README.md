# python-hw-27-tms

1 Напишите функцию multiply_numbers(), которая принимает два
аргумента и возвращает их произведение. Затем вызовите эту функцию
и выведите результат на экран.

```
def multiply_numbers(a, b):
    return a * b 

print(multiply_numbers(3, 4))
```

2 Создайте файл test.txt и запишите в него строку "Это тестовый файл для
домашнего задания по программированию". Затем откройте этот файл в
режиме чтения, прочитайте его содержимое и выведите на экран.

```
file = open('test.txt', 'r')
content = file.read()
print(content)
file.close()
```

3 Создайте пустую директорию mydir в текущей рабочей директории.
Затем перейдите в эту директорию и создайте в ней три пустых файла:
file1.txt, file2.txt и file3.txt. Наконец, выведите список файлов в
директории на экран.

```
import os

files = os.listdir("./")
print(files)
```

4 Создайте шаблон template.html, который будет содержать HTML-код
для отображения списка пользователей. Шаблон должен использовать
цикл for для перебора элементов списка, и выводить имя и email
каждого пользователя. Затем создайте список пользователей в виде
списка словарей, передайте его в шаблон и отобразите результат на
экране.

```
from jinja2 import Environment, FileSystemLoader

users_data = [
    {"name": "Иван Иванов", "email": "ivan.ivanov@example.com"},
    {"name": "Мария Петрова", "email": "maria.petrova@example.com"},
    {"name": "Алексей Сидоров", "email": "alex.sidorov@example.com"},
    {"name": "Елена Смирнова", "email": "elena.smirnova@example.com"}
]

env = Environment(loader=FileSystemLoader('.'))
template = env.get_template('template.html')
rendered_html = template.render(users=users_data)
print(rendered_html)
```
