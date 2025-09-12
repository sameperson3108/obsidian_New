# @Override - аннотация(метка), которая указывает, что метод переопределяет метод родительского класса или реализует метод интерфейса.



Лучшие практики:
- Всегда использовать @Override при переопределении методов
- Проверять сигнатуру метода - она должна точно совпадать с родительской
- Обращать внимание на модификаторы доступа - нельзя сужать видимость метода
- Использование для методов Object - equals(), hashCode(), toString()


# Основное назначение:
# 1.Проверка компилятором на наличие метода в родительском классе

class Animal {
	public void makeSound() {
		System.out.println("Ауууууууу");
	}
}

class Dog extends Animal {
	@Override //Компилятор проверит, что такой метод существует в родительском классе
	public void makeSound() {
		System.out.println("Гав-гав");
	}
}


# Когда использовать:
# 1.Переопределение методов класса
class Vehicle {
	public void start() {
		System.out.println("Vehicle starting");
	}
}

class Car extends Vehicle {
	@Override
	public void start() {
		System.out.println("Car starting with key");
	}
}
# 2.Реализация методов интерфейса
interface Drawable {
	void draw();
}

class Circle implements Drawable {
	@Override
	void draw() {
		System.out.println("Drawing circle");
	}
}
# 3.Переопределение методов Object
class Person {
	private String name;
	private int age;
	
	 @Override
	 public boolean equals(Object obj) {
	 if (this == obj) return true;
	 if (obj == null || getClass() != obj.getClass()) return false;
	 Person person = (Person) obj;
	 return age == person.age && name.equals(person.name);
	 }
	 
	 @Override
	 public int hashCode() {
		 return Objects.hash(name, age)
	 }
	 
	 @Override
	 public String toString() {
	 return "Person{name'" + name + "', age=" + age + "}";
	 }
}