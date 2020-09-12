# Отчёт о тестировании приложения "Precision"

## Краткое описание

При попытке присвоить переменной totalBonus типа double значение вычисления regularBonus + specialBonus (типа double) происходит некорректная запись числа.  Ожидаемый результат вычисления должен соответствовать значению 0.9, а фактически получилось 0.8999999999999999. 

```
public class Main {
    public static void main(String[] args) {
        double regularBonus = 0.3;
        double specialBonus = 0.6;
        double totalBonus = regularBonus + specialBonus;
        System.out.println(totalBonus);
    }
}
```
Результат вычисления

```
0.8999999999999999

Process finished with exit code 0
```

## Описание тестов

Проводилось тестирование методом "белого ящика" с помощью режима отладки кода .

## Результаты

1. https://github.com/bakaraml/2Task2Lesson/issues/1

## Общие рекомендации

Необходимо либо изменить тип переменной totalBonus, либо указать количество цифр после точки.

## Тестирование производилось в следующем окружении:

* macOS Catalina 10.15.6 x64 
* java 11.0.8
* IntelliJ IDEA