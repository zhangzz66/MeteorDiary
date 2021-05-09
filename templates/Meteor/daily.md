.action{$ppath := nospace (cat "https://b3logfile.com/siyuan/assets/pic" ((randInt 1 32) | toString) ".png")}
.action{$week := add (mod (div ((toDate "2006-01-02" "2050-03-13").Sub now).Hours 24) 7) 1}
![image](.action{$ppath})

## 🕐 创建时间：.action{now | date "2006-01-02 15:04"} .action{last (slice (list "星期六" "星期五" "星期四" "星期三" "星期二" "星期一" "星期天") 0 $week )}