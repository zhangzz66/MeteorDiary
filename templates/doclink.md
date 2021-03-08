{{ $parent:= (sql "SELECT * FROM blocks WHERE id in (SELECT parent_id FROM blocks WHERE (content LIKE '%{{.title}}%' or name LIKE '%{{.title}}%' or alias LIKE '%{{.title}}%' or ('{{.alias}}' !='' and content LIKE '%{{.alias}}%') or ('{{.alias}}' !='' and name LIKE '%{{.alias}}%') or ('{{.alias}}' !='' and alias LIKE '%{{.alias}}%'))) and root_id !='{{.id}}' order by created DESC") }}
{{ $cont:= (sql "SELECT * FROM blocks WHERE (content LIKE '%{{.title}}%' or name LIKE '%{{.title}}%' or alias LIKE '%{{.title}}%' or ('{{.alias}}' !='' and content LIKE '%{{.alias}}%') or ('{{.alias}}' !='' and name LIKE '%{{.alias}}%') or ('{{.alias}}' !='' and alias LIKE '%{{.alias}}%')) and root_id !='{{.id}}' order by created DESC") }}
{{- /* This is comment parent*/}}
((20210308160748-d36k54r "HOME"))  >  {{len $cont }} blocks related to **{{.title}}**{: style="background-image: linear-gradient(to right, var(--b3-theme-primary), var(--b3-theme-error)); -webkit-background-clip: text; color: transparent;"}
----------------------------------------------------
{: id="20210308211819-qotumvn"}

{{ $doc:= (sql "SELECT * FROM blocks WHERE id in (SELECT root_id FROM blocks WHERE (content LIKE '%{{.title}}%' or name LIKE '%{{.title}}%' or alias LIKE '%{{.title}}%' or ('{{.alias}}' !='' and content LIKE '%{{.alias}}%') or ('{{.alias}}' !='' and name LIKE '%{{.alias}}%') or ('{{.alias}}' !='' and alias LIKE '%{{.alias}}%'))) and root_id !='{{.id}}' order by created DESC") }}
{{range $ii,$vv :=$parent}}{{range $i,$v:=$doc}}{{if eq $vv.Path $v.Path }}
{: id="20210308211819-z7jdreh"}

### {{add $ii 1}}. 📑 (({{$v.ID}} "{{$v.Content}}"))
{: id="20210308211819-gvlhoqn"}

!(({{$vv.ID}} "{{substr 0 20 $vv.Content}}")) {{end}}{{end}}{{end}}
{: id="20210308163842-987rbbh"}


{: id="20210308163410-3r83c15" type="doc"}
