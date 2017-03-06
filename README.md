## 购物车

### 题目要求：1.	代码要能够覆盖题目所描述的各种正常和异常路径，但是不需要过多考虑题目中没有描述的场景。2.	代码应当组织清晰、符合clean code原则，并且在能够体现面向对象设计原则同时避免过度设计。3.	良好的自动化构建和自动化测试将会是加分项。 ### 需求描述
程序员正在为某电子商务网站实现一个虚拟的购物车，以便让其的用户能够同时购买多件商品，从而获得更好的购物体验。用户在访问该网站的过程中可以一边浏览商品，一边将自己满意的商品添加到购物车中，选购完毕后一次性结清购物车中的所有商品。购物车结算过程涉及到一些折扣和优惠的业务逻辑，程序需要自动计算用户最终支付的实际金额。 
一个影响结算金额的因素是折扣。网站会在一些法定节假日或者其他促销季节推出某些商品的折扣。例如，双十一的时候，会有针对电子产品的折扣，五一假期的时候，会有针对日用品的折扣，在计算购物车结算金额的时候，需要根据结算当天的折扣计算出折后的金额。 
另外，网站为了促销，曾经在过去一年内派发了一些优惠券，这些优惠券只要有效期内，结算的时候都是可以用的，但是每次结算只能用一张。优惠券通常是 “满 1000 减 200” 这样的形式，表示总金额如果超过1000则立减200。 
作为程序员的你需要编写一个程序，根据输入的购物车信息和促销信息来计算用户最终支付的结算金额。为了简化问题，我们一开始支持以下的产品目录: 
* 电子: ipad，iphone，显示器，笔记本电脑，键盘* 食品: 面包，饼干，蛋糕，牛肉，鱼，蔬菜* 日用品: 餐巾纸，收纳箱，咖啡杯，雨伞* 酒类: 啤酒，白酒，伏特加 以下是一些用例，你的程序必须通过这些用例，并编写自动化测试来证明你的程序在其他情形下同样可靠。 

Case A 

```输入2015.11.11 |0.75 | 电子   //折扣信息：日期 | 折扣 | 产品品类。可有多个，每个一行，如果没有则保留一个空行//空行分隔1 * iphone: 4099.00  //商品信息，每种一行，格式为: 数量 * 商品: 单价1 * 小米电视: 4999.0012 * 黑啤: 99.005 * 全麦面包: 12.00//空行分隔2015.11.11  //结算日期2016.2.15 5000 500  //优惠券信息，示例为2016年2月15日到期，满5000返500，空格分隔，如果没有则保留一个空行 输出7259.50  //结算金额：四舍五入到小数点后2位
```Case B

```输入5 * 菠菜 : 5.25 2 * Face纸巾 :7.70 2017.01.01
输出 41.65```
