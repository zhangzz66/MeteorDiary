.action{$week := add (mod (div ((toDate "2006-01-02" "2050-03-13").Sub now).Hours 24) 7) 1}
## 🎉️ 历史待办

> 截止至 `.action{now | date "2006-01-02 15:04"} .action{last (slice (list "星期六" "星期五" "星期四" "星期三" "星期二" "星期一" "星期天") 0 $week )}`
>

{{select * from blocks where created <'.action{now | date "20060102"}' and subtype = 't' and type = 'l' order by created DESC limit 4}}