---
title: <% tp.file.title %>
created: <% tp.file.creation_date("YY-MM-DD-dddd") %>
category: DailyNote
---
[[<% tp.date.weekday("YYYY-[W]ww", 0, tp.file.title, "YYYY-MM-DD") %>]]
<< [[<% tp.date.now("YY-MM-DD-dddd", -1, tp.file.title, "YYYY-MM-DD") %>]] | [[<% tp.date.now("YY-MM-DD-dddd", 1, tp.file.title, "YYYY-MM-DD") %>]] >>
# TODO
- [ ] 
--- 
# <% tp.date.now("dddd", 0, tp.file.title, "YYYY-MM-DD")  %>
오늘 하루 정리

# File created
```dataview
TABLE
WHERE 
file.cday = date("<% tp.date.now("YY-MM-DD", 0, tp.file.title, "YYYY-MM-DD-dddd") %>","yy-MM-dd")
```
# File modified
```dataview
TABLE
WHERE 
	file.cday != date("<% tp.date.now("YY-MM-DD", 0, tp.file.title, "YYYY-MM-DD-dddd") %>","yy-MM-dd")
AND	file.mday = date("<% tp.date.now("YY-MM-DD", 0, tp.file.title, "YYYY-MM-DD-dddd") %>","yy-MM-dd")
```