Класс `Optional` в Java представляет собой контейнер, который может содержать или не содержать значение. Он предоставляет удобные методы для работы с возможным отсутствием значения и предотвращения ошибок `NullPointerException`. Вот некоторые из основных методов класса `Optional`:

1. `Optional.empty()`: Метод `empty()` возвращает пустой объект `Optional` без значения.

```
Optional<String> emptyOptional = Optional.empty();
```

2. `Optional.of(value)`: Метод `of()` создает объект `Optional`, содержащий заданное значение. Если значение равно `null`, будет выброшено исключение `NullPointerException`.

```
String name = "John";
Optional<String> optional = Optional.of(name);
```

3. `Optional.ofNullable(value)`: Метод `ofNullable()` создает объект `Optional`, содержащий заданное значение, если оно не равно `null`. Если значение равно `null`, будет создан пустой объект `Optional`.


```
String name = null;
Optional<String> optional = Optional.ofNullable(name);
```

4. `orElse(defaultValue)`: Метод `orElse()` возвращает значение, содержащееся в `Optional`, если оно присутствует. Если значение отсутствует (пустой `Optional`), возвращается указанное значение по умолчанию.

```
Optional<String> optional = Optional.empty();
String result = optional.orElse("Default Value");
```

5. `orElseGet(Supplier<? extends T> supplier)`: Метод `orElseGet()` возвращает значение, содержащееся в `Optional`, если оно присутствует. Если значение отсутствует (пустой `Optional`), вызывается переданный `Supplier`, который возвращает значение по умолчанию.

```
Optional<String> optional = Optional.empty();
String result = optional.orElseGet(() -> "Default Value");
```

Основное различие между `orElse()` и `orElseGet()` заключается в том, что `orElse()` всегда вычисляет значение по умолчанию, даже если в `Optional` есть не пустое значение, в то время как `orElseGet()` вычисляет значение по умолчанию только в случае отсутствия значения в `Optional`. Использование `orElseGet()` может быть полезным, когда вычисление значения по умолчанию требует дорогостоящих вычислений или взаимодействия с внешними источниками данных.