# Design Patterns

## [Strategy Pattern](StrategyPatternExample/README.md)

## [Decorator Pattern](DecoratorPatternExample/README.md)

## [Observer Pattern]

### Beispiel

### Problem

### Lösung

### UML

### Code

Als erstes müssen zwei abstrakte Klassen erstellt werden:

* Die Gertaenk Klasse mit der abstrakten methode cost()
* Die AddOnDecorator Klasse die eine Subklasse von Geraenk ist

```java

public abstract class Getraenk{
	public abstract double cost();
}

public abstract class AddOnDecorator extends Getraenk{
	public abstract doube cost();
}

```

Dann werden die eigentlichen Getränke und AddOns implementiert

```java

public class Espresso extends Getraenk{
	public double cost(){
		return 1.50;
	}
}

public class Decaffinated extends Getraenk{
	public double cost(){
		return 1.50;
	}
}

public class CaramelAddOn extends AddOnDecorator{
	private Geraenk getrank;
	
	public CaramelAddOn(Getraenk getrank){
		this.getrank = getrank;
	}

	public double cost(){
		return this.getrank.cost() + 0.3;
	}
}

public class ChocolateAddOn extends AddOnDecorator{
	private Geraenk getrank;
	
	public ChocolateAddOn(Getraenk getrank){
		this.getrank = getrank;
	}

	public double cost(){
		return this.getrank.cost() + 0.2;
	}
}

public class MilkAddOn extends AddOnDecorator{
	private Geraenk getrank;
	
	public MilkAddOn(Getraenk getrank){
		this.getrank = getrank;
	}

	public double cost(){
		return this.getrank.cost() + 0.1;
	}
}

public class ChilliAddOn extends AddOnDecorator{
	private Geraenk getrank;
	
	public ChilliAddOn(Getraenk getrank){
		this.getrank = getrank;
	}

	public double cost(){
		return this.getrank.cost() + 0.5;
	}
}

public class SpinachAddOn extends AddOnDecorator{
	private Geraenk getrank;
	
	public SpinachAddOn(Getraenk getrank){
		this.getrank = getrank;
	}

	public double cost(){
		return this.getrank.cost() + 0.4;
	}
}

```

Letztens können die verschiedenen Kaffes erstellt werden

```java

public class Main{
	public static void main(String[] args){
		Getraenk kaffe1 = new SpinachAddOn(new ChilliAddOn(new Espresso));
		Getraenk kaffe2 = new MilkAddOn(new ChocolateAddOn(new Decaffinated));
	}
}

```

## Factory Pattern (Simple/Abstract)


## Proxy Pattern

## Adapter Pattern

## Command Pattern
