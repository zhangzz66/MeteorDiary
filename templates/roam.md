{{$dayleft := (div ((toDate "2006-01-02" "2022-01-01").Sub now).Hours 24)}}
{: id="20210117205551-gf9fvzw" updated="20210226144036"}

## 🚴 随机复习
{: id="20210117204808-yqws8cs" updated="20210226143819"}

> 距离 `2022-01-01` 还剩 `{{$dayleft}}` 天，加油！
> {: id="20210117205515-8p7rsx9" updated="20210226144045"}
{: id="20210117205436-61dcsj6"}

!{{SELECT * FROM blocks where type = 'd' and root_id != '{{.id}}' and path not like '%daily%' ORDER BY random() LIMIT 1}}
{: id="20210117204827-z8lk3kf"}

{: id="20210117205434-qw4rjly"}

{: id="20210117205434-6dqfavc"}


{: id="20210117204808-8pkg9iu" type="doc"}
