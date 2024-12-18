
![YUTING's GitHub stats](https://github-readme-stats.vercel.app/api?username=YUTING0907&show_icons=true&theme=tokyonight)

### 2023TODO 
#### ✅1.Doris
  Doris1.1.4 -> 1.2.6版本问题追踪 (50%）
  1.正则表达式函数会搞挂BE
  2.group by as alias参数
  3.not in的字查询中存在null，查询出来的结果会有问题
  
  总结：跨多个版本升级需要⚠️阅读各个版本的release note
#### ✅2.数据同步模块
  ✅Flinkcdc实时同步mysqltodoris，包含表结构变更通知，表结构变更不停掉作业\
  ​   1.新增表同步不停掉原始的作业（广播流）\
​     2.同步表ddl同步变更\
  ✅Dolpinscheduler源码修改，增加后端同步表接口，以及dorisddl\
  ✅Flinkcdc源代码 Debezium Binlog 日期类型数据解析源码修改\
解决 0000-00-00 00:00:00 时间 数据不能通过校验的问题\
  ✅Doris UDF

  问题总结：
  * 1.从specific-offset模式（binlog）启动后，再从checkpoint启动会报错，升级flinkcdc版本解决
  * 2.mysql 日期数据0000-00-00 00:00:00 scheme字段设置not null会导致报错，flinkcdc将此类日期数据转换成null导致，修改源码将其改为1970-01-01日期解决
  * 3.fastjson导致oom
#### 3.监控
   flinkjob
   ✅flinkcdc表数据监控
   ✅敏感词
#### 4.图像美学
论文阅读
跑实验
#### 5.AI深度学习算法
  * ✅商品分类(Bert) 
  * ✅图片分类(ResNet50、EfficientNet-B2) 
#### 6.数据质量
  * 数据同步数据校验 NineData
  * ✅dolpin调度校验
#### ✅7.数据血缘
    数据采集：使用 Apache Doris 提供的审计日志插件 Doris Audit Plugin 进行数据采集
    1.用Doris审计日志插件将FE的审计日志（fe.audit.log）导入到Doris集群中通过sql查看和分析
    数据存储：对审计日志插件做了定制化开发，使用 Kafka 存储 Doris 审计日志数据
    2.通过filebeat收集审计日志（fe.audit.log）写入Kafka，Flink消费解析
    血缘解析：使用 Druid 进行 Doris SQL 解析
    血缘关系存储：使用 Nebula Graph 存储血缘关系数据

#### ✅8.数据安全扫描
  * 基于dolpin二开插件 

<!--
**YUTING0907/YUTING0907** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

### Visit times
![Visitor Count](https://profile-counter.glitch.me/YUTING0907/count.svg)

### language
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=YUTING0907&layout=compact&theme=tokyonight)
Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
