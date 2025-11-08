@Component - говорит о том, что объекты класса будет создавать не программист, а спринг

@Component
public class Sword impements Weapon {
	// логика
}


Spring Bean - объект созданный и управляемый Spring

ApplicationContext(Контекст приложения) - место где хранятся  bean
Spring закидывает bean в виде hashmap, где ключом является строка с названием объекта, а значением этот объект.

Название объекта = название класса с маленькой буквы

Dependency Injection -