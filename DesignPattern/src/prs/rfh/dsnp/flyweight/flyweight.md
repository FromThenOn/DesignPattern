# Flyweight
> 享元模式（蝇量模式）

### 使用场景
主要用于减少创建对象的数量，以减少内存占用和提高性能。这种类型的设计模式属于结构型模式，它提供了减少对象数量从而改善应用所需的对象结构的方式。
在有大量对象时，有可能会造成内存溢出，我们把其中共同的部分抽象出来，如果有相同的业务请求，直接返回在内存中已有的对象，避免重新创建。

1、系统中有大量对象。 2、这些对象消耗大量内存。 3、这些对象的状态大部分可以外部化。 4、这些对象可以按照内蕴状态分为很多组，当把外蕴对象从对象中剔除出来时，每一组对象都可以用一个对象来代替。 5、系统不依赖于这些对象身份，这些对象是不可分辨的。

分为内蕴和外蕴，内蕴是指对于对象有意义的，一旦享元创建就这个内蕴是不可改变的，和享元绑定的，而外蕴则是对于享元无关的对象。无需保存在享元内部。

### 应用实例：
1、JAVA 中的 String，如果有则返回，如果没有则创建一个字符串保存在字符串缓存池里面。 2、数据库的数据池。

### 优点：
大大减少对象的创建，降低系统的内存，使效率提高。

### 缺点：
 提高了系统的复杂度，需要分离出外部状态和内部状态，而且外部状态具有固有化的性质，不应该随着内部状态的变化而变化，否则会造成系统的混乱。

### 使用场景： 1、系统有大量相似对象。 2、需要缓冲池的场景。

### 注意事项：
1、注意划分外部状态和内部状态，否则可能会引起线程安全问题。 2、这些类必须有一个工厂对象加以控制。
