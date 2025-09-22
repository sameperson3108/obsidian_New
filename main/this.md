this - слово, которое указывает на конкретный объект

public class Dragon {
	String color;
	public void setColor(String color) {
	this.color = color
	}
}

public class Main {
	public void Main(String[] args) {
	Dragon blackDragon = new Dragon();
	blackDragon.setColor("Black");
	} 
}

В данном случае в классе Main мы создаём объекта класса Dragon. То есть создали дракона по шаблону, а в момент создания на него же создаётся ссылка. Color("Black") изначально ни к чему не привязан и существует сам по себе.

this.color - поле конкретно для нашего дракона, который только что родился. И именно в это поле мы передаем Black