## 类中的属性

类中的属性定义在.h文件中。属性以@property关键词声明，定义格式为

关键词 + 属性修饰词+属性类型+属性名称；

关键词为@property,

属性修饰词为

1、nonatomic atomic:修饰为原子性。

2、assign表示的是直接复制非指针变量，不会产生内存管理的代码，当属性是一个基本数据类型时使用，如 int float bool等基本类型。

3、copy 用来修饰NSString的对象类型。建立一个引用计数为1的新对象，不对原对象的引用计数做改变，建立新对象释放旧对象。使用copy关键字必须要实现NSXopying协议。copy是内容拷贝。

4、retain用来修饰除了NSString的其他对象类型。释放旧的对象，将旧对象的值赋予输入对象，再提高输入对象的索引计数为1。retain是指针拷贝。

5、weak 对象的弱引用，不会增加对象的引用计数，也不会持有对象，当对象消失后指针自动指向nil,所以这里也就防止了野指针的存在。

6、strong 对象的强引用，会增加对象的引用计数，如果指向了一个空对象，会造成野指针，平常用的最多的也是strong。


