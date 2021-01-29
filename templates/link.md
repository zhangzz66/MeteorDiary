{{ $block:= (sql "select * from blocks where type='d' and content='{{.title}}' ") }}
{{ $blocks:=split " " ((first $block)|toString)}}
{{$myID:=(trunc -22 $blocks._0)}}
{: id="20210129211237-309dq0t"}

## 🏷 链接“ {{.title}}”的内容
{: id="20210129211237-b25zmo0"}

!{{SELECT * FROM blocks WHERE markdown LIKE '%{{$myID}}%' and path not LIKE '%{{.title}}%'}}
{: id="20210129211237-jh17cgr"}

## 🏷 提及“ {{.title}}”的内容
{: id="20210117201946-iesarol"}

!{{SELECT * FROM blocks WHERE content LIKE '%{{.title}}%' and path not LIKE '%{{.title}}%' and markdown not LIKE '%{{$myID}}%'}}
{: id="20210129211237-bmqibm2"}


{: id="20210117192611-6c17hv1" type="doc"}
