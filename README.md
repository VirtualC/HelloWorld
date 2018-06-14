# HelloWorld
TestRepository

using System;

public abstract class Shape{
  public abstract int Perimeter();
  public abstract int Area();
}


public class Rectangle :Shape{
  private int intHeight;
  private int intWidth;
  
  public Rectangle(int intH, intW){
    this.intHeight = intH;
    this.intWidth = intW;
  }
  
  public override int Perimeter(){
    return (intHeight + intWidth) * 2;
  }
  
  public override int Area(){
    return intHeight * intWidth;
  }
}


public class Square :Shape{
  private int intLength;
  
  public Square(int intL){
    this.intLength = intL;
  }
  
  public override int Perimeter(){
    return intLength * 4;
  }
  
  public override int Area(){
    return intLength ^ 2;
  }
}


public class TestClass{
  public static void Main(string[] args){
    Console.WriteLine("HelloWorld!");
    
    Rectangle recOne = new Rectangle(5,7);
    Square squOne = new Square(5);
    
    Console.WriteLine("Rectangle's Perimeter is : {0}", recOne.Perimeter());
    Console.WriteLine("Rectangle's Area is : {0}", recOne.Area());
    Console.WriteLine("Square's Perimeter is : {0}", squOne.Perimeter());
    Console.WriteLine("Square's Area is : {0}", squOne.Area());
    
    Console.ReadKey();
  }
}
