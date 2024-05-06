В Java `Comparable` и `Comparator` - это интерфейсы, которые используются для сравнения объектов и определения порядка сортировки.

Интерфейс `Comparable` содержит метод `compareTo()`, который позволяет сравнивать текущий объект с другим объектом. Метод `compareTo()` возвращает отрицательное целое число, ноль или положительное целое число в зависимости от результата сравнения. Если текущий объект меньше, чем другой объект, то метод должен вернуть отрицательное число. Если они равны, то метод должен вернуть ноль. Если текущий объект больше, чем другой объект, то метод должен вернуть положительное число.

Пример использования `Comparable`:

```
class Person implements Comparable<Person> {
    private String name;
    private int age;
    
    // Конструкторы, геттеры, сеттеры
    
    @Override
    public int compareTo(Person other) {
        return this.age - other.age;
    }
}

public class Main {
    public static void main(String[] args) {
        Person person1 = new Person("Alice", 25);
        Person person2 = new Person("Bob", 30);
        
        int result = person1.compareTo(person2);
        if (result < 0) {
            System.out.println(person1.getName() + " младше, чем " + person2.getName());
        } else if (result > 0) {
            System.out.println(person1.getName() + " старше, чем " + person2.getName());
        } else {
            System.out.println(person1.getName() + " и " + person2.getName() + " одного возраста");
        }
    }
}
```

В данном примере класс `Person` реализует интерфейс `Comparable<Person>`, переопределяя метод `compareTo()`. В данной реализации объекты `Person` сравниваются по возрасту. Метод `compareTo()` возвращает разницу в возрасте между текущим объектом (`this`) и переданным объектом (`other`).

Интерфейс `Comparator` предоставляет возможность определить кастомную логику сравнения объектов. Он содержит метод `compare()`, который принимает два объекта и возвращает отрицательное целое число, ноль или положительное целое число в зависимости от результата сравнения.

Пример использования `Comparator`:

```
class Person {
    private String name;
    private int age;
    
    // Конструкторы, геттеры, сеттеры
}

class AgeComparator implements Comparator<Person> {
    @Override
    public int compare(Person person1, Person person2) {
        return person1.getAge() - person2.getAge();
    }
}

public class Main {
    public static void main(String[] args) {
        Person person1 = new Person("Alice", 25);
        Person person2 = new Person("Bob", 30);
        
        AgeComparator comparator = new AgeComparator();
        
        int result = comparator.compare(person1, person2);
        if (result < 0) {
            System.out.println(person1.getName() + " младше, чем " + person2.getName());
        } else if (result > 0) {
            System.out.println(person1.getName() + " старше, чем " + person2.getName());
        } else {
            System.out.println(person1.getName() + " и " + person2.getName() + " одного возраста");
        }
    }
}
```

В данном примере создается отдельный класс `AgeComparator`, который реализует интерфейс `Comparator<Person>`. В данной реализации объекты `Person` сравниваются по возрасту. Метод `compare()` возвращает разницу в возрасте между двумя переданными объектами.

Интерфейсы `Comparable` и `Comparator` позволяют упорядочить объекты и использовать их для сортировки в различных контекстах.