fore - цвет текста
back - цвет фона
style - стиль текста
reset - cброс



result = []

def divider(a, b):
    if a < b:
        raise ValueError("Первое число меньше второго.")
    if b > 100:
        raise IndexError("Второе число больше 100.")
    return a / b

data = {10: 2, 2: 5, "123": 4, 18: 0, "list_key": 15, 8: 4}

for key in data:
    try:
        res = divider(key, data[key])
        result.append(res)
    except ZeroDivisionError:
        print(f"Ошибка: Деление на ноль для ключа {key}")
    except TypeError:
        print(f"Ошибка: Неподдерживаемый тип данных для ключа {key}")
    except ValueError as ve:
        print(f"Ошибка значения для ключа {key}: {ve}")
    except IndexError as ie:
        print(f"Ошибка индекса для ключа {key}: {ie}")

print(result)
