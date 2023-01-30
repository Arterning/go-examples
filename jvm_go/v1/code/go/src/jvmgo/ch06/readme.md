符号引用（Symbolic References）：

符号引用以一组符号来描述所引用的目标，符号可以是任何形式的字面量，
只要使用时能够无歧义的定位到目标即可。
例如，在Class文件中它以CONSTANT_Class_info、
CONSTANT_Fieldref_info、CONSTANT_Methodref_info
等类型的常量出现。符号引用与虚拟机的内存布局无关，
引用的目标并不一定加载到内存中。在Java中，一个java类将会编译成一个class文件。
在编译时，java类并不知道所引用的类的实际地址，因此只能使用符号引用来代替。
比如org.simple.People类引用了org.simple.Language类，
在编译时People类并不知道Language类的实际内存地址，
因此只能使用符号org.simple.Language
（假设是这个，当然实际中是由类似于CONSTANT_Class_info的常量来表示的）
来表示Language类的地址。各种虚拟机实现的内存布局可能有所不同
，但是它们能接受的符号引用都是一致的，
因为符号引用的字面量形式明确定义在Java虚拟机规范的Class文件格式中。
