{{$week := add (mod (div ((toDate "2006-01-02" "2050-03-13").Sub now).Hours 24) 7) 1}}
{: id="20210117174458-c4u3cmr"}

## 🎉️ 历史待办
{: id="20210117173634-z3gapm0"}

> 截止至 `{{now | date "2006-01-02 15:04"}} {{last (slice (list "星期六" "星期五" "星期四" "星期三" "星期二" "星期一" "星期天") 0 $week )}}`
> {: id="20210117174348-sb8dow5"}
{: id="20210117174346-yrb35qv"}

!{{select * from blocks where markdown like '%[ ]%' and type = 'l' LIMIT 5}}
{: id="20210117173702-t5ifomh"}

{: id="20210117173702-5ixp1d6"}


{: id="20210117173634-zy03er3" type="doc"}