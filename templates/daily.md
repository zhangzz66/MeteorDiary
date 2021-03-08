{{ $ppath := nospace (cat "https://b3logfile.com/siyuan/assets/pic" ((randInt 1 32) | toString) ".png")}}
{: id="20210113192100-rgvegn6" updated="20210306234754"}

{{$week := add (mod (div ((toDate "2006-01-02" "2050-03-13").Sub now).Hours 24) 7) 1}}
{: id="20210113192100-kh51gbb"}

![image]({{$ppath}})
{: id="20210113192100-8z7nlt1"}

## 🕐 创建时间：{{now | date "2006-01-02 15:04"}} {{last (slice (list "星期六" "星期五" "星期四" "星期三" "星期二" "星期一" "星期天") 0 $week )}}
{: id="20210113192100-mpyqy1k"}

{: id="20210117205636-cxm9szs"}


{: id="20210113192050-74ldoic" type="doc"}
