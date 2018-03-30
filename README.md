# ProtocolKit 

![ProtocolKit](http://og0h689k8.bkt.clouddn.com/18-3-30/70417530.jpg)

上面是对于ProtocolKit的实现流程做了一个小的概括


# ProtocolKit 的实现

ProtocolKit 的主要原理仍然是 runtime 以及宏的；通过宏的使用来隐藏类的声明以及实现的代码，然后在 main 函数运行之前，将类中的方法实现加载到内存，使用 runtime 将实现注入到目标类中。

ProtocolKit 中有两条重要的执行路线：

```
_pk_extension_load 将协议扩展中的方法实现加载到了内存
_pk_extension_inject_entry 负责将扩展协议注入到实现协议的类
```

<font color='red' size='5'>具体的内容可以看作者的博客讲解,代码中也已经加了详细的注释希望对你有帮助</font>

[作者对于ProtocolKit的详解](https://draveness.me/protocol-extension)


