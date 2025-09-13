implements - ключевое слово, которое используется для реализации интерфейсов классом. Когда [[Класс]] реализует [[Интерфейс]], он обязан предоставить реализацию всех абстрактных методов этого интерфейса.

# Основной синтаксис
class MyClass implements MyInterface {
	// реализация методов интерфейса
}


# Зачем используется?
# 1.Реализация контракта - интерфейс определяет контракт, который класс обязан выполнить
interface Drawable {
	void draw();
}

class Circle implements Drawable {
	@Override
	public void draw() 
		System.out.println("Drawing circle");
	}
}

# 2.Множественное наследование - класс может реализовывать несколько интерфейсов
interface Flyable {
	void fly();
}

interface Swimmable {
	void swim();
}

class Duck implements Flyable, Swimmable {
	@Override
	public void fly() {
		System.out.println("Duck is flying");
	}
	@Override
	public void swim() {
		System.out.println("Duck is swimming");
	}
}

# 3.Полиморфизм
interface Animal {
	void makeSound();
}

class Dog implements Animal {
	@Override
	public void makeSound() {
		System.out.println("Гав-гав");
	}
}

class Cat implements Animal {
	@Override
	public void makeSound() {
		System.out.println("Мяу");
	}
}

public class Main {
	public static void main(String[] args) {
		Cat myCat = new Cat();
		Dog myDog = new Dog();
		myCat.makeSound();
		myDog.makeSound();
	}
}