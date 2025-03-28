# Документация к модулю логирования
Модуль pyloggering предоставляет функции для логирования действий в Python. Он позволяет создавать файл логов и записывать в него сообщения различных уровней, а также выводить эти сообщения в консоль.



![PyPI - Version](https://img.shields.io/pypi/v/colorama?style=flat&label=colorama)


# Подключение
Прежде чем использовать модуль, убедитесь, что у вас установлен Python версии 3.10.9 и выше.
```python
import pyloggering
```
# Функции модуля
## 1. Создание файла для логирования:
Создает файл логов с указанным именем. Если файл уже существует, он будет дописыватся
Убедитесь, что у вас имеются права на запись в директорию, где вы хотите создать файл логов.(Если при использовании функций логирования writing = False, то файл создавать не обязятельно)
 ```python
pyloggering.create_file(name,location,type)
```
### Параметры:

name -> Имя файла для логирования


location -> путь до директории файла логов


type -> тип выходного файла. txt либо log



## Пример 1:
```python
import pyloggering

pyloggering.create_file("log","./assets","log")
```
### Вывод:


![image](https://github.com/user-attachments/assets/46ca7094-5031-45cf-b1d9-e2c61175dabd)



# 2. Уровень логирования INFO и его функция:

Выводит в консоль лог с уровнем INFO и записывает его в файл.


```python
pyloggering.log.info(text,writing)
```
### Параметры:


text -> Текст который будет выведен в консоль и записан в файл


writing -> Записывать ли в файл логи(дефолт True(при false создавать файл не обязательно))




## Пример 1:
```python
import pyloggering

pyloggering.create_file("log", "./assets", ".log")
pyloggering.log.info("Test, check file and console")
```
### Вывод:


![image](https://github.com/user-attachments/assets/8b97093e-06a2-4918-bd97-0e18875a2494)

## Пример 2:
```python
import pyloggering

pyloggering.log.info("Test, check console",False)
```


### Вывод:

![image](https://github.com/user-attachments/assets/6431e5af-4383-469c-ae07-a66871f0515b)


# 3. Уровень логирования WARN и его функция:


Выводит в консоль лог с уровнем warning и записывает его в файл.

```python
pyloggering.log.warning(text,writing)
```
### Параметры:


text -> Текст который будет выведен в консоль и записан в файл


writing -> Записывать ли в файл логи(дефолт True(при false создавать файл не обязательно))

## Пример 1:


```python
import pyloggering

pyloggering.create_file("log", "./assets", ".log")
pyloggering.log.warn("Test, check file and console")
```
### Вывод:


![image](https://github.com/user-attachments/assets/812c10a8-4e28-43c9-99c4-e02fce24c9d5)

## Пример 2:
```python
import pyloggering

pyloggering.log.warn("Test, check console",False)
```

### Вывод:

![image](https://github.com/user-attachments/assets/7f3c9f25-81d1-48f8-8caf-1457a691552a)



# 4. Уровень логирования SUCCESS и его функция:
Выводит в консоль лог с уровнем success и записывает его в файл.

```python
pyloggering.log.success(text,writing)
```
### Параметры:


text -> Текст который будет выведен в консоль и записан в файл


writing -> Записывать ли в файл логи(дефолт True(при false создавать файл не обязательно))


## Пример 1:


```python
import pyloggering

pyloggering.create_file("log", "./assets", ".log")
pyloggering.log.success("Test, check file and console")
```
### Вывод:

![image](https://github.com/user-attachments/assets/0e103fe1-865b-4427-aad1-df8b5d3446a8)

## Пример 2:

```python
import pyloggering


pyloggering.log.success("Test, console", False)
```

### Вывод:

![image](https://github.com/user-attachments/assets/ab0c6ef3-a397-489a-b740-0e0b34d77b71)


# 5. Уровень логирования CRIT и его функция:
Выводит в консоль лог с уровнем critical и записывает его в файл.

```python
pyloggering.log.critical(text,writing)
```
### Параметры:


text -> Текст который будет выведен в консоль и записан в файл


writing -> Записывать ли в файл логи(дефолт True(при false создавать файл не обязательно))


## Пример 1:


```python
import pyloggering

pyloggering.create_file("log", "./assets", ".log")
logger.log.critical("Test, check file and console")
```
### Вывод:

![image](https://github.com/user-attachments/assets/4ea60f10-8b9f-4356-bbc3-fa5a2d00a41d)

## Пример 2:
```python
import pyloggering


logger.log.critical("Test, console", False)
```

### Вывод:

![image](https://github.com/user-attachments/assets/2e424cd7-deda-4c98-8a12-969919c7d0b1)



# 6. Уровень логирования DEBUG и его функция:
Выводит в консоль лог с уровнем debug и записывает его в файл.


```python
pyloggering.log.debug(text,writing)
```
### Параметры:


text -> Текст который будет выведен в консоль и записан в файл


writing -> Записывать ли в файл логи(дефолт True(при false создавать файл не обязательно))


## Пример 1:


```python
import pyloggering

logger.create_file("log", "./assets", ".log")
logger.log.debug("Test, check file and console")
```
### Вывод:

![image](https://github.com/user-attachments/assets/1cafbe8c-58d3-4ed2-ade4-77034763e05a)



## Пример 2:

```python
import pyloggering

logger.log.debug("Test, console",False)
```
### Вывод:

![image](https://github.com/user-attachments/assets/530a55c3-018d-4efa-ae5c-934b873ae3df)



## Заключение

Эта документация охватывает основные функции модуля логирования и даёт вам возможность начать с ним работать без особых трудностей.



