{{- /* This is comment*/}}
{{ $ppath := nospace (cat "https://b3logfile.com/siyuan/assets/pic" ((randInt 1 32) | toString) ".png")}}
{{ $parent:= (sql "SELECT * FROM blocks WHERE id in (SELECT parent_id FROM blocks WHERE (content LIKE '%{{.title}}%' or name LIKE '%{{.title}}%' or alias LIKE '%{{.title}}%' or ('{{.alias}}' !='' and content LIKE '%{{.alias}}%') or ('{{.alias}}' !='' and name LIKE '%{{.alias}}%') or ('{{.alias}}' !='' and alias LIKE '%{{.alias}}%'))) and root_id !='{{.id}}' order by created DESC") }}
![image.png]({{$ppath}})
{: id="20210308215217-rrq7d6g"}

## ((20210308160748-d36k54r "HOME"))  >  {{len $parent }} blocks related to **{{.title}}**{: style="background-image: linear-gradient(to right, var(--b3-theme-primary), var(--b3-theme-error)); -webkit-background-clip: text; color: transparent;"}
{: id="20210308215217-s9zbhjd"}

{{ $doc:= (sql "SELECT * FROM blocks WHERE id in (SELECT root_id FROM blocks WHERE (content LIKE '%{{.title}}%' or name LIKE '%{{.title}}%' or alias LIKE '%{{.title}}%' or ('{{.alias}}' !='' and content LIKE '%{{.alias}}%') or ('{{.alias}}' !='' and name LIKE '%{{.alias}}%') or ('{{.alias}}' !='' and alias LIKE '%{{.alias}}%'))) and root_id !='{{.id}}' order by created DESC") }}
{{range $i,$v:=$doc}}
{: id="20210308215217-6yepp8t"}

### {{add $i 1}}. 📑 (({{$v.ID}} "{{$v.Content}}")):{{range $ii,$vv :=$parent}} {{if eq $vv.Path $v.Path }}   (({{$vv.ID}} "{{substr 0 20 $vv.Content}}")) {{end}}{{end}}{{end}}
{: id="20210308163842-987rbbh"}


{: id="20210308212427-391q4t6" type="doc"}
