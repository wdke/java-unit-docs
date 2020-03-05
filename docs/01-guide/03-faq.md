---
order: 3
group: 
  title: 介绍
  order: 1
---

# FAQ

## 技术选型

​		现在市场上的mock框架有，`Mockito`，`EasyMock`，`Jmock`。而`PowerMock`实际上是对`Mockito`以及`EasyMock`的扩展。针对他们不具备模拟静态，私有方法等功能做的扩展，扩展的语法与各自的mock框架语法一致。下面简单介绍一下这些mock框架。

- **Jmock**

  > `Jmock`是一个利用mock对象来测试`JAVA`代码的轻量级测试工具，他是`xUnit`的一员，它从`JUnit`发展而来，是`JUnit`的一个增强库。通过expect-run-verify （期望-运行-验证）的方式来完成测试过程。这种方式需要在运行前记录严格的期望，这常常会导致您被迫查看无关的交互。

- **EasyMock**

  > `EasyMock `是早期比较流行的mock框架。它也是通过expect-run-verify （期望-运行-验证）的方式完成测试过程，它可以验证方法的调用种类、次数、顺序，可以令 mock 对象返回指定的值或抛出指定异常。

- **Mockito**

  > `Mockito`是一个针对Java的mock框架。它与`EasyMock`和`JMock`很相似，是一套通过简单的方法对于指定的接口或类生成mock对象的类库，避免了手工编写mock对象。但`Mockito`是通过在执行后校验哪些行为已经被调用，它消除了对期望行为的需要。使用`Mockito`在准备阶段只需花费很少的时间，可以使用`简洁的API`编写出漂亮的测试，可以对具体的类创建mock对象，并且有“监视”非Mock对象的能力。 

  通过表格我们来看一下他们的能力对比。

|                                  | `JMock` | `EasyMock` | `Mockito` | `PowerMock(EasyMock)` | `PowerMock(Mockito) ` |
| :------------------------------: | :-----: | :--------: | :-------: | :-------------------: | :-------------------: |
|            调用数限制            |    √    |     √      |     √     |           √           |           √           |
|        记录严格的预期结果        |    √    |     √      |           |           √           |                       |
|             显式验证             |         |            |     √     |                       |           √           |
|             部分mock             |    √    |            |     √     |           √           |           √           |
|             级联mock             |         |            |     √     |                       |           √           |
|            多接口mock            |         |            |     √     |                       |           √           |
|           注释类型mock           |         |     √      |     √     |                       |           √           |
|          mock的自动注入          |         |            |     √     |                       |           √           |
| final、static和private方法的mock |         |            |           |           √           |           √           |

​		`Mockito`使用起来简单，学习成本很低，功能强大，并且具有非常`简洁的API`，测试代码的可读性很高，所以它十分受欢迎，用户群体也非常多，很多开源软件也选择了`Mockito`。因此，我们选择了`Mockito`做为我们的mock框架。如果想了解更多有关`Mockito`的信息，可以访问其[官方网站](https://site.mockito.org/)。