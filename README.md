#### AntiVA

###### 这是一个检测当前是否运行在VA下的库，通过对va lib重定向的原理进行检测

va在加载app时，会将当前app的存储路径和so库文件复制到自己的虚拟目录下，通过该特征，可以在app运行时进行检测

va中重定向lib库的逻辑代码：

[java层](https://github.com/asLody/VirtualApp/blob/11db690f60b9950895e18f06ff7dd867b8a313a1/VirtualApp/lib/src/main/java/com/lody/virtual/client/VClientImpl.java#L413)

[jni层](https://github.com/asLody/VirtualApp/blob/a3c26ec200d6f18840028fb9717ee7c53f1638ee/VirtualApp/lib/src/main/jni/Jni/VAJni.cpp#L36)

##### VA的作用：

va是一套开源的虚拟沙箱环境，你可以在该沙箱中执行任何root环境下的操作，包括java层和jni层的hook，app免杀等等

###### ps:代码很简单，如有更好的检测方式，欢迎联系wuxiaoqiu1993@gmail.com