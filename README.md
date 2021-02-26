# Meteor模板介绍
> 适用于思源笔记日记、文档模板，使用方法：在文档中任意位置使用`{{`插入模板；**日记模板**可以在设置中更改配置，修改默认**模板路径**。
## v0.5 更新，新增快速输入时间、日期模板
- 增加完整版日记模板'dailynote.md'
- 改进反链提及逻辑，增加别名搜索
## v0.4 更新，新增快速输入时间、日期模板

## v0.2 模板更新（01/17 21:05）

![del](https://gitee.com/zhangjlsjtu/pic/raw/master/picture/del.png)

主要内容

- 模板拆解成五个：日记、历史待办、链接提及、随机漫游、文档模板。
- 此次模板设计遵循**简约**原则，日记模板只提供简单背景和创建时间，其他功能可通过`{{ `调用，进行功能组合
- 实现类似RR、RE的page提及功能

### 新增截图：

**daily：** 基本日记模板，可与其他模板组合

![daily](https://gitee.com/zhangjlsjtu/pic/raw/master/picture/daily.png)

historyTodo：历史待办模板

![historytodo](https://gitee.com/zhangjlsjtu/pic/raw/master/picture/historytodo.png)

roam：随机复习模板

![roam](https://gitee.com/zhangjlsjtu/pic/raw/master/picture/roam.png)

link：链接与提及模板

![link](https://gitee.com/zhangjlsjtu/pic/raw/master/picture/link.png)

docSign：普通文档模板，能自动加载文档名作为二级标题

![docsign](https://gitee.com/zhangjlsjtu/pic/raw/master/picture/docsign.png)

-------

## 截图
![image](https://raw.githubusercontent.com/zhangjl-sjtu/MeteorDiary/main/preview.png)
## 主要特性
- 每次使用模板都能随机加载一张 页头背景图片
- 可显示创建时间、星期
- 随机展示未完成的 待办列表
- 随机复习：随机展示 一篇文档。如要排除路径，搜索关键词、标签请使用SQL语言
## 文档模板使用示例
![image](https://raw.githubusercontent.com/zhangjl-sjtu/MeteorDiary/main/example.gif)
