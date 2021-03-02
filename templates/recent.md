> 24h为一天，默认72h是3天前的笔记
> {: id="20210302163323-ypqz9yt" updated="20210302163400"}
{: id="20210302163320-r3fqsuw" updated="20210302163323"}

!{{SELECT * FROM blocks WHERE type='d' and created >'{{(now | date_modify "-72h") | date "20060102"}}' order by created DESC}}
{: id="20210302163300-6rx9wm6" updated="20210302163312"}

{: id="20210302163300-1fk68q4"}


{: id="20210302163258-5l2pkft" type="doc"}
