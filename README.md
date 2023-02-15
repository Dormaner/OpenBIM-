# 综合报告
工业数字化程度正在加速，对于OpenBIM解决方案和标准的要求也在增加。
buildingSMART之前常常把精力集中在建筑领域内的数据交换，现在，是时候把它推向更广的领域了。越来越多建筑领域外的用户、开发者和modellers想要在他们的流程和工具里用OpenBIM标准。随着智慧建筑、智慧城市和数据孪生等新概念的出现，人们对于未来的标准和解决方案有了更多的期待，这增加了对于大量数据的处理据交换的低延迟的要求，而当前基于本地文件的信息存储方式和人工智能、机器学习有相当大的脱节。
工业领域间的连接愈发强烈，基于当前现实，buildingSMART需要为数据格式、工具及底层技术创造可扩展的互操作性。
之前的IFC是基于文件的，但数字孪生、传感器、微服务、智慧城市对IFC提出了更高的要求，因此目前IFC新的工作方向是基于通用数据环境的（CDE）

## OpenBIM工作流
## OpenBIM名词解释
### IDS
IDS：IDS的最终目的是为了让人和计算机都能读懂BIM信息需求。使用IDS，我们可以制定哪些数据必须要包含在BIM模型中，并验证是否合规。
IDS是基于XML格式的

如何使用：模型作者可以使用IDS确保自己提供信息的规范性；接收模型的人则可以利用IDS检查IFC模型是否符合规范。

（自己的理解：现实情况中，自己发布的模型会缺失很多信息，比如防火属性、内外属性、承重属性等，如果模型传递给其他专业，如结构专业，这个模型是无法用于计算的，IDS就像模型作者和模型接收者之间的检察官，核算模型是否满足交付规范，实际上就是用编程的手段来对交付的模型属性进行挨个比对，如果结构专业要求有“承重属性”而建筑专业没有提供，那么就告诉建筑设计师：你需要对这面墙体赋予属性）

在没有ids之前，上下游之间进行信息交付的主要方式是通过xlsx、docx、pdf等格式，并由上游的人给下游的人进行解释，常常出现理解偏差，且整体验证阶段时间长。

## 第一步：使用IDS定义需求
这一步，你可以得到一个.xml文件
## 第二步：查看
利用BIM.works打开.xml文件，查看、修改需求
## 第三步：检查
检查后导出一个BCF文件


##使用Sketchup的bSDD的典型案例

不明白的地方：.ids格式和XML格式的区别是什么？

![Alt text](/images/1676442076504.png)

### bSDD（数据字典）
BIM建模员用bSDD来轻松有效地访问所有标准、丰富他们的模型；BIM经理用bSDD检查BIM数据的有效性；高级技术人员使用bSDD去进行合规性检查、查找产品制造商，创建IDS等。
bSDD不是一个标准，而是buildingSMART提供的一项服务，以更简单地去使用BIM和OpenBIM标准。

为什么要有这个东西？

## Oslo Airport

使用软件：Archicad、EDModelServer，Grasshopper,MicroStation V8i,Navigate SImple BIM,Navisworks,Novapoint,ProjectWise,Revit,Solibri Model Checker,StreamBIM,SYNCHROPRO,Tekla BIMsight,Tekla Structures,Trimble Connect,Vectorworks
交付格式：IFC 2*3
设计团队：Team-T
负责人：Aas Jakobsen

## The Pontsteiger Project
使用软件：Allplan,Archicad,BIMcollab,Docstream,Solibri Model Checker,Tekla Structures,Vectorworks
交付格式：IFC2*3,bcf
时间：2014年4月设计，2015年10月开工，2018年5月入住

## The Henderson -面向未来的办公建筑
设计师：扎哈团队