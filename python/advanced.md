## Python — продвинутый уровень

🏆 Правильных ответов: 12 из 16.

#### Q1. Укажите, каким будет вывод этой программы в случае, если на вход подаются две строки — сначала «Python», потом «exit».

```
name = ''
while True:
   c = input()
   if c == 'exit':
      break
   name = name + c
print('I’m', name)
```

- [x] I’m Python

#### Q2. Следующий код выводит ошибку. Почему?

```
tuple_ex = ('a', 'b', 'c', {'d': 4})
tuple_ex.append('e', 'f')
new_elements = ('g', 'h')
new_tuple = tuple_ex + new_elements


print(len(tuple_ex))
print(len(new_tuple))
```

- [x] Метод append ожидает только один аргумент

#### Q3. Какой результат выведет этот код?

```
def add(a=[]):
   a.append('A')
   return a

print(add())
print(add())
```

- [x] ['A'] и ['A', 'A']

#### Q4. Какая процедура или функция заранее НЕ определена в модуле os?

- [x] Создание нового потока

#### Q5. Какой результат выведет этот код?

```
class A:
   counter = 0
   def meth(self):
      return 'method'
a = A()
a.counter = 100

print('Equals' if a.counter == A.counter else 'Not Equals')
print('Equals' if a.meth() == A.meth(a) else 'Not Equals')
```

- [x] Not Equals и Equals

#### Q6. Какой из утверждений НЕВЕРНО?

- [x] Как seek(), так и truncate() применимы к файлам, открытым в режиме добавления (‘a’)

#### Q7. Следующий код выводит результат: ['0: a = x', '1: b = y', '2: c = z']. Что пропущено в print()?

```
keys = ['a', 'b', 'c']
values = ['x', 'y', 'z']
idxs = enumerate(zip(keys, values))
print(...)
```

- [x] `list(f'{i}: {k} = {v}' for i, (k, v) in idxs)`

#### Q8. Выберите НЕВЕРНОЕ утверждение.

- [x] Reduce возвращает массив элементов, а map — одно значение

#### Q9. Выберите верное утверждение о блоке try-except-finally в Python.

- [x] Код в блоке finally будет выполнен независимо от того, возникло исключение в блоке try или нет

#### Q10. Какой из встроенных типов данных Python лучше всего подходит для реализации стека?

- [x] Списки

#### Q11. Выберите операцию, которую НЕЛЬЗЯ выполнить с помощью библиотеки requests.

- [x] Использовать асинхронные HTTP-запросы

#### Q12. Какой функции из модуля itertools соответствует по смыслу код ниже?

```
def func(*iterables):
   for it in iterables:
      for e in it:
         yield e
```

- [x] chain

#### Q13. Укажите, какое число тестов будет завершено c успехом при использовании библиотеки pytest для кода, представленного ниже:

```
import pytest, unittest

def should_skip():
   return True

class Test(unittest.TestCase):
   def a(self):
      self.assertEqual(1 + 1, 2)
   def test_b(self):
      self.assertEqual(1 + 2, 3)


   @pytest.mark.skip
   def test_c(self):
      self.assertEqual(1 + 3, 4)

   @pytest.mark.skipif('should_skip')
   def test_d(self):
      self.assertEqual(1 + 4, 5)
```

- [x] 2

#### Q14. Выберите ответ, в котором указаны только те варианты, для которых следующее выражение вернет значение True.

```
re.match(r"^\+7-(\d{3,5})-\d{3,5}?", text) is not None

A. +7-(123)-45678
B. +7-123-45678
C. +7-12-345678
D. +7-(1234)-5678
E. +7-12345-678
```

- [x] B, E

#### Q15. В каком из вариантов генератор реализован НЕВЕРНО?

- [x] `list(i*i for i in range(5))[3]`

#### Q16. Какое утверждение о декораторе lru_cache НЕВЕРНО?

- [x] По умолчанию lru_cache предназначен для кэширования результатов функции в пределах одного процесса Python

