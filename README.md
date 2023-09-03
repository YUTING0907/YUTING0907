![YUTING's GitHub stats](https://github-readme-stats.vercel.app/api?username=YUTING0907&show_icons=true&theme=tokyonight)

### 2023TODO 
####✅ 1.Doris
  Doris1.1.4 -> 1.2.6版本问题追踪 (50%）
  1.正则表达式函数会搞挂BE
  2.group by as alias参数
  3.not in的字查询中存在null，查询出来的结果会有问题
  
  总结：跨多个版本升级需要⚠️阅读各个版本的release note
#### ✅2.数据同步模块
  ✅Flinkcdc实时同步mysqltodoris，包含表结构变更通知，表结构变更不停掉作业\
  ​   1.新增表同步不停掉原始的作业（广播流）\
​     2.同步表ddl同步变更\
  ✅Dolpinscheduler源码修改，增加后端同步表接口，以及dorisddl

  问题总结：
  * 1.从specific-offset模式（binlog）启动后，再从checkpoint启动会报错，升级flinkcdc版本解决
  * 2.mysql 日期数据0000-00-00 00:00:00 scheme字段设置not null会导致报错，flinkcdc将此类日期数据转换成null导致，修改源码将其改为1970-01-01日期解决
  * 3.fastjson导致oom
#### 3.监控
   flinkjob
   ✅flinkcdc表数据监控
   ✅敏感词
#### 4.图像美学
#### 5.AI深度学习算法
  * 商品分类 60%  
  * 语义匹配
#### 6.数据质量
#### ✅7.数据血缘


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
