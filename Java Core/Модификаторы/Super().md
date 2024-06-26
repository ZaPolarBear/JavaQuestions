Ключевое слово `super` в Java используется для обращения к членам суперкласса (родительского класса) из подкласса. Оно может применяться в конструкторах и методах подкласса для вызова конструкторов, методов или доступа к переменным суперкласса.

Вот несколько случаев, когда используется `super`:

1. Вызов конструктора суперкласса: В конструкторе подкласса можно использовать `super` для вызова конструктора суперкласса. Это позволяет инициализировать члены суперкласса перед инициализацией членов подкласса.

```
public class Subclass extends Superclass {
    public Subclass() {
        super(); // вызов конструктора суперкласса
        // остальные операции инициализации подкласса
    }
}
```

2. Доступ к методам суперкласса: В методе подкласса можно использовать `super` для вызова методов суперкласса с тем же именем. Это позволяет переопределенному методу подкласса обратиться к реализации метода в суперклассе.


```
public class Subclass extends Superclass {
    public void someMethod() {
        super.someMethod(); // вызов метода суперкласса
        // остальная логика метода подкласса
    }
}
```

3. Доступ к переменным суперкласса: В подклассе можно использовать `super` для доступа к переменным суперкласса. Это позволяет подклассу использовать или переопределить значения переменных суперкласса.


```
public class Subclass extends Superclass {
    public void someMethod() {
        int value = super.someVariable; // доступ к переменной суперкласса
        // остальная логика метода подкласса
    }
}
```

Использование `super` позволяет подклассу работать с членами суперкласса и расширять их функциональность или изменять поведение в соответствии с требованиями подкласса.