.action{$block:= (queryBlocks "select * from blocks where type= 'd' and content like '%.title%' and id !='.id'")}
((20210308160748-d36k54r "HOME"))  >  **.action{.title}**
> 请将文档名命名为 文件夹的名称，该模板将自动map该目录下的文档
---

.action{"| 序号 | 内容 | 路径 |"}
.action{"| ------ | ------ | ------ |"}
.action{range $index,$v:=$block}  | .action{add $index 1} | ((.action{$v.ID} ".action{$v.Content}")) | .action{$v.Path} |
.action{end}