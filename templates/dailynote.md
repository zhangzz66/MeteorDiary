{: id="20210113192050-7tndnxe"}

{{ $ppath := nospace (cat "https://gitee.com/zhangjlsjtu/pic/raw/master/picture/diary"  ((randInt 1 4) | toString) ".jpg") }}
{: id="20210113192100-rgvegn6"}

{{$after := (div ((toDate "2006-01-02" "2021-03-01").Sub now).Hours 24)}}
{: id="20210113192100-w16ba0f"}

{{$week := add (mod (div ((toDate "2006-01-02" "2050-03-13").Sub now).Hours 24) 7) 1}}
{: id="20210113192100-kh51gbb"}

![image]({{$ppath}})
{: id="20210113192100-8z7nlt1"}

## 🕐 创建时间：{{now | date "2006-01-02 15:04"}} {{last (slice (list "星期六" "星期五" "星期四" "星期三" "星期二" "星期一" "星期天") 0 $week )}}
{: id="20210113192100-mpyqy1k"}

- {: id="20210113192100-70dbtys"}作者：`Zhangjl`
- {: id="20210113192100-r6glcef"}邮箱：`**`
- {: id="20210113192100-o28g16p"}距离 `2021-03-01` 还剩 `{{$after}}` 天
{: id="20210113192100-r8qhlub"}

## 🧱今日待办
{: id="20210113192100-afwcity"}

### 1.
{: id="20210113192100-az05z5s"}

### 2.
{: id="20210113192100-nzsdpey"}

## 🎉️历史待完
{: id="20210113192100-jqlx35n"}

!{{select * from blocks where markdown like '%[ ]%' and type = 'l' LIMIT 3}}
{: id="20210113192100-6tbm7yh"}

---

## 🚴 随机复习
{: id="20210113192100-d7asy70"}

!{{SELECT * FROM blocks ORDER BY random() LIMIT 3}}
{: id="20210113192100-wf069w6"}


{: id="20210113192050-74ldoic" type="doc"}
