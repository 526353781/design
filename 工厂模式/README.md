# 工厂模式

##  优点：
算法实体的创建被延迟到了工厂子类里，我们不在工厂里直接创建对象，而是直接封装一个一个的小工厂，每个工厂负责创建自己的子类，这样就不存在switch的情况，也就不存违反开闭原则的问题。

##  缺点：
如果算法种类很多，那么继承抽象工厂的子类也就会很多，不是很好维护，同时不支持产品切换，比如我们要开发PC，分为多个系统，那么我们可以把所有的系统都抽象出来（类似上面的加减乘除），然后我们在抽象出来工厂，但是如果这个时候我们有两个硬件呢，PC和Phone，虽然我们可以保证只有这两个硬件了，但是如果用基本的抽象工厂去实现的话还是很别扭。