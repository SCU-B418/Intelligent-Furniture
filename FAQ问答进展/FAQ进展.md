# 智能家居FAQ问答系统之项目进展
## FAQ System about Intelligent-Furniture
### **Time：2018.11.12-2018.11.19**      
任务分配：使用百度UNIT平台，制作订票，退票功能  
**反馈**：  
- 在平台上模拟了火车票订票功能，训练出来的沙盒模型比较傻。  
- UNIT平台界面的某个工具栏更新了。在本次版本中的“对话模板”这一块没有“效果优化这一栏”。  
- UNIT平台上是手动对未标注数据进行标注，智能家居这块可以模仿序列标注，将词槽给标注好。  

### **Time：2018.11.21-2018.11.28**  
Option1：家电常见问题数据搜集  
Option2：查询类FAQ问答系统架构   
Tool：爬虫  
**注**：从故障排除、日常保养、常见问题等方面收集数据  
数据如下：  
- [博朗家电](https://www2.braunhousehold.com/zh-cn/customer-support/faq-section?search=+)  
- [海尔家电](https://www.haier.com/cn/services_supports/overview/small_applications/daily_use/troubles/index_1.shtml)  
- [长虹家电](http://cn.changhong.com/fw/cjwt/czzd/)  
  
平台介绍：  
[百度开源 FAQ 问答系统—AnyQ](https://www.jiqizhixin.com/articles/2018-08-24-17)  
**反馈**：  
进展：1.爬取了长虹家电官网 首页>服务>常见问题>操作指导>下的家电信息QA对，并对噪声数据进行删选  
规划：1.爬取以下数据：首页>服务>常见问题>日常保养， 首页>服务>常见问题>故障排除， 首页>服务>自助排障，并对爬取数据进行去噪  

### **Time：2018.12.1-2018.12.15**  
Option1：家电常见问题数据搜集,数据预处理  
Option2：百度AnyQ Docker环境搭建，demo试运行
Option3：FAQ问答系统功能模块实现    
#### 进展：
- Raw data：博朗家电，海尔家电，长虹家电的相关数据已经爬取完
  - 博朗家电数据特点：主要集中在咖啡机等小家电方面的数据，QA结构比较好，问题简短，答案多简短，但数据量少  
  - 海尔家电数据特点：  
  - 长虹家电数据特点：
- Clean data：博朗家电数据已经处理完
- 小米家电数据集处理  

|数据集类型|字段|数量|描述| 
|-|-|-|-|
|train|ids，q1，label，q2|28499|q-q pair|
|test|ids，q1，label，q2|2039|q-q pair|
|qa|ids，questions，answers|1017|q-a pair|  
- 百度AnyQ Docker环境搭建，demo试运行还在进行中，环境搭建比较麻烦
- FAQ问答系统功能模块
  - jieba分词
  - 去停用词
  - 转为BOW
  - tf-idf，lsa，lda
  - whoosh检索
#### 规划：
- 数据搜集
- 百度AnyQ运行demo
- 将分模块组合并进行检索
