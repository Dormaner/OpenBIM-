# 1.OpenBIM：An Enabling Solution for Information Interoperability
主要研究了2000-2019年这20年间国际上对于openBIM的研究情况。
1. 对于openBIM的研究集中于IFC。
![Alt text](images/openBIM%E7%A0%94%E7%A9%B6%E6%96%B9%E5%90%91.png)
1. 研究openBIM的期刊主要有：
    Automation in Construction（51%）
    Ework and Ebusiness in Architecture Engineering and Construction（17%）
    Advanced Engineering Informatics（14%）
    Journal of Computing in Civil Engineering（7%）
2. 研究openBIM的国家主要有：美（22%）、德国（17%）、中国（15%）、英国（11%）、韩国（9%）、荷兰、澳大利亚、法国、意大利、比利时、加拿大
3. openBIM的五大标准：
   IFC：信息传递格式。
   IDM：流程描述
   MVD：将流程转化为技术要求
   BCF：变更协调
   bSDD：定义BIM对象及其属性
4. 介绍了两个开源软件平台：BIMserver、xBIM。
   目前，BIM软件由Autodesk、Bentley、图软系类，同公司软件之间具有很高的兼容性，但不同公司软件之间的互操作性相对较低，这就导致了软件之间信息共享的困难，所以我们需要一款开源的BIM软件平台。
   1.1 BIMserver（BIMserver.org）：这一平台能使得用户创建自己的操作系统，且软件核心式基于IFC的。平台下有以下几个开源库，IfcOpenShell（ifc解析库）、bimvie.ws、BIM Surfer、BCFier
   2、xBIM
5. 介绍了五款openBIM工具
   IfcDoc：用于生成IFC文档、开发MVD的软件，基于mvdXML。
   BCF Manager（其实就是BIMcollab系列软件、插件）：允许用户创建、过滤、发现BIM模型问题，且可以保存、加载问题，或从BIMcollab同步问题。
   ![Alt text](images/BIMcollab%E7%B3%BB%E5%88%97.png)
   BIMQL：用于BIM模型的特定领域查询语言。
   Apstex IFC是一个基于Java的工具包，提供对基于IFC的BIM模型的完全访问，可用于读取、写入、修改、创建IFC模型，且有可视化的界面
   IFC Engine DLL式一个STEP工具箱，能生成最新版本的IFC模型。

openBIM的六大研究方向
1. Information representation（信息表达）
2. Information query（信息查询）
3. Information exchange（信息交换）
4. Information extension（信息扩展）
5. Information integration（信息集成）

   