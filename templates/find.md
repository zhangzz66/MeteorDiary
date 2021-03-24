!{{SELECT * FROM blocks WHERE (id in (select parent_id from blocks where content like '%{{.title}}%' and type !='l' ) and type='i') or (id in (select parent_id from blocks where content like '%{{.title}}%' ) and type='h') and root_id !='{{.id}}' order by created DESC}}
{: id="20210319205749-uu5y1my" memo="查询逻辑：1列表项块的话就展示该列表项块及其子项  2非列表项块展示其所在的标题块（非文档块）" updated="20210319214354"}

{: id="20210319205749-agdian3" updated="20210319213009"}


{: id="20201207153440-whc3tr3" type="doc"}
