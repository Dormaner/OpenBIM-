# 1.OpenBIM：An Enabling Solution for Information Interoperability
## 2000-2019年这20年间国际上对于openBIM的研究情况。
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

## openBIM的六大研究方向
1. Information representation（信息表达）
2. Information query（信息查询）
   Mazairac等^[Mazairac, W.; Beetz, J. BIMQL—An open query language for building information models. Adv. Eng. Inform.2013, 27, 444–456.]提出一种基于特定领域的开放语言查询框架，可以用来选择、更新和删除存储在IFC中的数据（这是为bimserve.org开发的）；为了加快构件元素之间的拓扑查询，Khalili等^[Khalili, A.; Chua, D.K.H. IFC-Based Graph Data Model for Topological Queries on Building Elements.J. Comput. Civ. Eng. 2013, 29. ]提出图数据模型（GDM），此外，一个新的基于IFC的算法被用于推导出建筑元素之间的拓扑关系；另外，也可以利用数据库技术、自然语言处理、机器学习等先进技术和openBIM相结合来解决信息查询问题，如，Ghang^[Ghang, L.; Jiyong, J.; Jongsung, W.; Chiyon, C.; Seok-joon, Y.; Sungil, H.; Hoonsig, K. Query Performance of the IFC Model Server Using an Object-Relational Database Approach and a Traditional Relational Database Approach. J. Comput. Civ. Eng. 2014, 28, 210–222.
]等人结合传统关系数据库的优势，开发出一种创新的对象关系IFC服务器，可以提高传统IFC服务器的查询性能。
3. Information exchange（信息交换）
   使用本身格式进行信息交换：IFC、IDM、MVD
   使用平台进行信息交换：BIMserver、xBIM
4. Information extension（信息扩展）
   向桥梁、隧道、景观的扩展等
5. Information integration（信息集成）
   和GIS的集成研究、和先进技术（如机器学习、数据库等技术的）集成研究
## openBIM的展望
1. 规则检查
   目前规则检查可能会导致语法问题、语义错误和意外的几何转换；
2. IFC映射关系不够清晰，IFC所表达的语义过于通用。
3. BIM和GIS的集成
4. IFC向CityGML转换时，BIM于GIS之间的模型信息不匹配将导致几何信息的不匹配。由于BIM模型中存储的庞大而复杂的IFC数据具有各种属性和几何表达式，这将对映射过程形成干扰。
5. 在IFC和CityGML进行数据转换时，可能会出现特征的语义丢失。如一个建筑的外墙和内墙在转换后变成了同一个物体。

# Generating construction schedules through automatic data extraction using open BIM technology
1. 研究目的：利用数据自动生成施工进度表。
1. 五个步骤
BIM模型的构建→ifcXML文件数据的解析（包含几何数据和材料数据）（相较于用STEP标准构建的ifc数据，利用XML构建的ifcXML有更多的数据处理库）→解析BIM数据至工期活动数据→利用Microsoft Project编写时间表。

# Ifc to building energy performance simulation: A systematic review of the main adopted tools and approaches

1. 目的：如何解决BIM和BEPS（building energy performance simulation）的互操作性问题
2. 比较了IFC和gbXML两种格式在建筑模拟中作为通用格式的可能性。
 gbXML（Green Building XML）专注于环境数据，被能源模拟软件普遍采用，成为事实上的标准，但仅能接受矩形的形状。ifc则更加通用，虽然BIM模型在保存为这两种格式都会出现数据丢失的问题（10%左右）。因此，进一步开发ifc比gbXML更有意义。
1. 另外一种方法是，修复IFC文件后，利用转换工具将IFC转换为gbXML。
2. ifc文件通常很庞杂，需要进行清理、校正后才适合导入到能源模拟软件中
3. 结论：本文介绍了BIM和BEPS之间的数据交换，比较了IFC和gbXML两种格式的应用，并选定IFC格式讨论了BIM到BEPS的工作流。

# Development of openBIM-based energy analysis software to improve the interoperability of energy performance assessment
1. 摘要：传统能源性能评估（EPA）方法（手工）容易导致数据错误，但是BIM和能源模拟模型之间的互操作性低下，本研究旨在开发一个平台，来提高基于BIM的EPA的互操作性水平。