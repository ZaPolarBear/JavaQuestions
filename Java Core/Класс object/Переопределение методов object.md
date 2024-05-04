В Java вы можете переопределить методы, определенные в классе `Object`, в своих собственных классах. Переопределение позволяет вам изменить поведение методов класса `Object` для соответствия особым требованиям вашего класса.

Вот примеры переопределения некоторых методов класса `Object`:

1. **Метод `toString()`**:

```
public class MyClass {
    private String name;

    // Конструкторы, методы и поля класса...

    @Override
    public String toString() {
        return "MyClass with name: " + name;
    }
}
```

В данном примере мы переопределили метод `toString()`, чтобы возвращалась строка, содержащая имя объекта класса `MyClass`.

2. **Метод `equals(Object obj)`**:

```
public class Point {
    private int x;
    private int y;

    // Конструкторы, методы и поля класса...

    @Override
    public boolean equals(Object obj) {
        if (this == obj) {
            return true;
        }
        if (obj == null || getClass() != obj.getClass()) {
            return false;
        }
        Point other = (Point) obj;
        return x == other.x && y == other.y;
    }
}
```

В данном примере мы переопределили метод `equals()`, чтобы сравнивать два объекта класса `Point` по их координатам `x` и `y`.

3. **Метод `hashCode()`**:

```
public class Person {
    private String name;
    private int age;

    // Конструкторы, методы и поля класса...

    @Override
    public int hashCode() {
        return Objects.hash(name, age);
    }
}
```

В данном примере мы переопределили метод `hashCode()`, используя встроенный метод `hash()` из класса `Objects`, чтобы вычислить хеш-код объекта на основе его имени и возраста.

4. **Метод `clone()`**:


```
public class Circle implements Cloneable {
    private double radius;

    // Конструкторы, методы и поля класса...

    @Override
    public Circle clone() {
        try {
            return (Circle) super.clone();
        } catch (CloneNotSupportedException e) {
            throw new RuntimeException("Cloning failed", e);
        }
    }
}
```

В данном примере мы переопределили метод `clone()`, чтобы создать и вернуть глубокую копию объекта класса `Circle` с использованием метода `clone()` из класса `Object`.

5. **Метод `finalize()`** (устаревший):

```
public class Resource {
    // Конструкторы, методы и поля класса...

    @Override
    protected void finalize() throws Throwable {
        try {
            // Код для освобождения ресурсов
        } finally {
            super.finalize();
        }
    }
}
```

В данном примере мы переопределили метод `finalize()`, который вызывается перед удалением объекта сборщиком мусора, чтобы освободить какие-либо ресурсы, связанные с объектом.