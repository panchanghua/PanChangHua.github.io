# JDK组成
![JDK JRE JVM](./image/JDK.png)
## JDK：Java Development Kit
	JDK是Java开发工具包，是sun针对Java开发人员开发的产品。
	JDK是整个Java的核心，其中包括Java运行环境JRE（Java Runtime Eneirnment）、一些Java工具（解释器Java/编译器Javac/文档生成器Java Doc/归档器Jar等）和Java基础的类库（Java API包括tools.jar、rt.jar、dt.jar等）。
	JDK安装目录下有一个名为JRE的目录，里面有两个文件夹bin和lib，可以认为bin就是JVM，lib就是JVM工作所需要的类库，JVM和lib合起来称为Jre。
	①SE(J2SE)，standard edition，标准版，是我们通常用的一个版本，从JDK 5.0开始，改名为Java SE。
	②EE(J2EE)，enterprise edition，企业版，使用这种JDK开发J2EE应用程序，从JDK 5.0开始，改名为Java EE。
	③ME(J2ME)，micro edition，主要用于移动设备、嵌入式设备上的java应用程序，从JDK 5.0开始，改名为Java ME。

## JRE：Java Runtime Eneirnment
	JRE是Java运行环境，可以用来运行Java文件，包括JVM以及常用类库和一些模块，解释class时JVM需要调用所需要解释的类库lib。
	与JDK不同，JRE是Java运行环境，并不是开发环境，没有包含任何开发工具（如编译器和调试器），只针对Java程序的用户。

## JVM：Java Virtual Machine
	JVM是Java虚拟机，他是Java实现跨平台最核心的部分，所有Java程序会首先被编译为.class后缀的类文件，这种类文件可以在Java虚拟机上运行。
	class类文件不是直接运行在操作系统上，而是经过虚拟机间接与操作系统交互，由虚拟机将程序解释给本地操作系统执行，映射到本地CPU指令集和操作系统的系统调用。
	只有JVM不能解释执行class，因为解析class需要类库lib，lib类库在JRE中。
	JVM屏蔽了与具体操作系统平台的相关信息，相当于将不同操作系统之间的差异屏蔽了，这些差异由JVM自身解释完成，Java程序只需要生成Java虚拟机上运行的目标代码（字节码），就可以在多种操作系统平台不加修改的运行，不同操作系统有不同版本的JVM。
