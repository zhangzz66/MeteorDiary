{{ $block:= (sql "select * from blocks where type= 'd' and path like '%{{.title}}%' and id !='{{.id}}'") }}
{: id="20210308161205-dad3gpo" memo="新建文件夹名字的文档，然后调用该模板"}

((20210308160748-d36k54r "HOME"))  >  **{{.title}}**{: style="background-image: linear-gradient(to right, var(--b3-theme-primary), var(--b3-theme-error)); -webkit-background-clip: text; color: transparent;"}
{: id="20210308150148-9b4wvs0"}

---
{: id="20210319222824-nu63jjh"}

{{"| 序号 | 内容 | 路径 |"}}
{{"| ------ | ------ | ------ |"}}
{{range $index,$v:=$block}}  | {{add $index 1}} | (({{$v.ID}} "{{$v.Content}}")) | {{$v.Path}} |
{{end}}
{: id="20210308145704-gxwbw46"}


{: id="20210308160554-49pfy1t" type="doc"}
