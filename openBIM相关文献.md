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

# 基于知识图谱的国内IFC研究综述
## 作者：赖华辉，侯铁
## 研究热点方向：
###  数据交互
如IFC与城市数据（CityGML）^[王建龙, 何望君, 刘纪平. IFC 与 CityGML 建筑几何语义信息转换[ J]. 科学技术创新, 2018, ( 2):150-151.] ^[ 虞铭尧, 庞浩宇, Wardle E. LOD2 和 LOD3 细节层次下 IFC 至 CityGML 的模型转换[J]. 扬州大学学报(自然科学版), 2017, 20(3): 26-30.]，与地理信息之间的转换研究 ^[武鹏飞, 刘玉身, 谭 毅, 等. GIS 与 BIM 融合的研究进展与发展趋势[ J]. 测绘与空间地理信息,2019, 42(1): 1-6.] ^[刘金岩, 刘云锋, 李 浩, 等. 基于 BIM 和 GIS 的数据集成在水利工程中的应用框架[ J]. 工程管理学报, 2016, 30(4): 95-99.]
### 数据集成
IFC数据量大，这方面，国内学者的研究方向主要是信息集成^[ 胡振中, 田佩龙, 李久林. 基于 IFC 的传感器信息存储与应用研究[ J]. 图学学报, 2018, 39 ( 3):522-529.]、信息化^[孙增强. 基于 BIM 信息化技术的建筑项目成本管理系统[D]. 天津: 天津大学, 2016.]、数据库^[周 颖, 郭红领, 罗柱邦. IFC 数据到关系型数据库的自动映射方法研究[C] / / 第四届全国 BIM 学术会议论文集. 北京: 中国建筑工业出版社, 2018:311-317]等
### 数据应用
如进度管理^[ 张晓勇. 基于 Unity 3D 的施工进度管理系统在河南三淅高速公路中的应用[ J]. 公路交通科技(应用技术版), 2016, (8): 152-153]、成本控制^[ 陈向上, 刘金旭. 基于 IFC 标准的造价模型在医院工程中的应用[ J]. 建筑技术, 2019, 50( 2): 213-216]、施工管理^[ 徐圆圆. 基于 BIM 与 IFC 的多目标施工信息优化模型建立及管理研究[ D]. 邯郸: 河北工程大学,2017.]等
### 和新技术的结合
如云计算^[徐 照, 康 蕊, 孙 宁. 基于 IFC 标准的建筑构件点云信息处理方法[ J]. 东南大学学报(自然科学版), 2018, 48(6): 1068-1075]、神经网络^[李柄静. 基于 BIM 的建筑工程施工质量可视化评价方法研究[D]. 南京: 东南大学, 2017.]、本体^[周文韬. 基于本体的绿色施工评价方法研究[D].南京: 东南大学, 2018.]等
>备注：以上文章，仅有扬州大学学报、东南大学学报、图学学报为核心期刊，作者整体引用质量有待商榷，或者说国内没有关于IFC的高质量研究

## IFC国内研究的3个阶段
### 2003-2010年：基础研究阶段
如国家“十五”重点科技攻关项目专题“基于IFC标准和工程信息模型的建筑施工4D管理系统”、十一五科技支撑计划项目“现代建筑设计与施工关键技术研究”，并设立“建筑协同设计平台研究与应用”、“建筑设计与施工一体化平台信息共享技术研究”、“绿色建筑全生命周期信息模型研究”
### 2010-2015年：深入研究阶段
随着2011年住建部《2011-2015年建筑业信息化发展纲要》的颁布，国内学者对IFC的数据结构开展了深入研究，如文本挖掘^[姜韶华, 张海燕. 基于 BIM 的建设领域文本信息管理研究[J]. 工程管理学报, 2013, 27(4): 16-20.]、IDM^[ 丘衍航, 高光林, 曹 国. 语义交换对象在交换模型中的使用[J]. 土木建筑工程信息技术, 2013, 5(5): 107-109]、MVD^[明 星. 基于 MVD 的建筑与结构模型转换研究[D]. 上海: 上海交通大学, 2014]，为建筑项目多方基于IFC标准的数据共享与交换提供了技术支撑
### 2015至今：项目应用阶段
国内学者深入研究了IFC在建筑项目全生命周期的应用问题，如协同设计^[ 赖华辉, 邓雪原, 刘西拉. 基于 IFC 标准的 BIM 数据共享与交换[ J]. 土木工程学报, 2018, 51( 4):121-128.]、施工监测^[ 刘训房. 基于 BIM 和 WEB 的隧道动态施工监测信息系统研究[D]. 大连: 大连海事大学, 2017.]、运维管理^[张建平, 何田丰, 林佳瑞, 等. 基于 BIM 的建筑空间与设备拓扑信息提取及应用[ J]. 清华大学学报
(自然科学版), 2018, 58(6): 587-592.]等。国内早期的研究主要集中在民用建筑，后期向轨道工程、输变电工程、水利水电工程等领域扩展
## 收录IFC的核心期刊（2003-2019）
图学学报（12）、建筑科学（7）、清华大学学报（自然科学版）（7）、计算机应用与软件（5）、工业建筑、土木工程学报、同济大学学报（自然科学版）
