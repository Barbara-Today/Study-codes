```
import random

num1 = random.randint(1, 100) 
print('Добро пожаловать в числовую угадайку.')
print('Я загадала число от 0 до 100, попробуй отгадать его!')

def is_valid(num2):
    if num2.isdigit() and 0 <= int(num2) <= 100:
        return True
    else:
        return False

count = 0
import math

while True:
    n = input()
    if is_valid(n):
        n = round(int(n))
        if n < num1:
            print('Ваше число меньше загаданного, попробуйте еще разок')
            count = count+1
        elif n > num1:
            print('Ваше число больше загаданного, попробуйте еще разок')
            count = count +1
        elif n == num1:
            print('Вы угадали с',count, 'попытки, поздравляю!')
            break
    else:
        print('А может быть все-таки введем целое число от 1 до 100?')

print("Спасибо, что играли в числовую угадайку. Еще увидимся...")
```
