* http://www.iocoder.cn/Spring/DesignPattern-2/?vip
## spring中的设计模式2
* 代理模式
  * spring aop
* 复合模式(组合模式)
  * 复合模式是新建一个类，类里面的一些其他工具由set方法写入。比如Html().setTag(new Body()).setTag(new Header())
* 策略模式
  * 达到同一目标可能由很多方法，策略模式可以根据条件选择合适的方法(途径)
* 模板模式
  * 模板模式是由abstract类预定义好构建对象需要做的一系列事情，然后由子类来实现。比如搭建一个房子，需要地基，需要1层，2层。
```
public class TemplateMethod {

  public static void main(String[] args) {
    HouseAbstract house = new SeaHouse();
    house.construct();
  }

}

abstract class HouseAbstract {
  protected abstract void constructFoundations();
  protected abstract void constructWall();

  // template method
  public final void construct() {
    constructFoundations();
    constructWall();
  }
}

class EcologicalHouse extends HouseAbstract {

  @Override
  protected void constructFoundations() {
    System.out.println("Making foundations with wood");
  }

  @Override
  protected void constructWall() {
    System.out.println("Making wall with wood");
  }

}

class SeaHouse extends HouseAbstract {

  @Override
  protected void constructFoundations() {
    System.out.println("Constructing very strong foundations");
  }

  @Override
  protected void constructWall() {
    System.out.println("Constructing very strong wall");
  }

}
```
