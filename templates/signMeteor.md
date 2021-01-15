{{ $ppath := nospace (cat "https://gitee.com/zhangjlsjtu/pic/raw/master/picture/diary" ((randInt 1 4) | toString) ".jpg")}}
{: id="20210114214719-tsvh1d9"}

{{$week := add (mod (div ((toDate "2006-01-02" "2050-03-13").Sub now).Hours 24) 7) 1}}
{: id="20210115135134-466hl9y"}

![img]({{$ppath}})
{: id="20210114214719-avwwfdm"}

## {{.title}}简介
{: id="20210114214719-75hg5gx"}

- {: id="20210114214719-1qw5wit"}作者：`name`
- {: id="20210114214719-5fvr267"}邮箱：`@`
- {: id="20210114214719-m6k4zcd"}创建时间：`{{now | date "2006-01-02 15:04"}} {{last (slice (list "星期六" "星期五" "星期四" "星期三" "星期二" "星期一" "星期天") 0 $week )}}`
{: id="20210114214719-6g9uvj5"}

---


{: id="20210114214704-4mqtidw" type="doc"}
