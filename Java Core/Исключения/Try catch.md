`try-catch` - это упрощенная версия конструкции `try-catch-finally`, которая не содержит блока `finally`. Она используется, когда нет необходимости выполнять какой-либо код в блоке `finally`.

```
try {
    // Код, который может вызвать исключение
    int result = 10 / 0; // Деление на ноль, вызовет ArithmeticException
    System.out.println("Результат: " + result);
} catch (ArithmeticException e) {
    // Обработка исключения ArithmeticException
    System.out.println("Произошла ошибка: " + e.getMessage());
}
```

В этом примере блок `finally` отсутствует, и только блок `try` и `catch` используются для обработки исключения.