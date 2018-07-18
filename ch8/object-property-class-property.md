#对象属性和类属性

类属性：用类名调用的属性

Person.name

对象属性的优先级高于类属性，可同名

动态的给对象添加类属性，至针对当前的对象生效，对于其他类创建的对象没有作用

当删除掉了对象中的属性，则使用类中的同名属性。

注意：尽量不要重名

```
class Person(Object):
    pass

```

动态添加属性：

class.name

如何动态添加方法：

from types import MethodType

思考：限制实例的属性怎么处理？

定义类时候定义__slots__属性来限制动态添加的属性。

__slots__ = ('name','height')





