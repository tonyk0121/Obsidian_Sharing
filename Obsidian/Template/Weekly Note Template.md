---
title: <% tp.file.title %>
category: WeeklyNote
---
# Daily Note link

![[<% tp.date.weekday("YY-MM-DD-dddd", 0, tp.file.title, "YYYY-[W]ww") %>#<% tp.date.weekday("dddd", 0, tp.file.title, "YYYY-[W]ww") %>]]

![[<% tp.date.weekday("YY-MM-DD-dddd", 1, tp.file.title, "YYYY-[W]ww") %>#<% tp.date.weekday("dddd", 1, tp.file.title, "YYYY-[W]ww") %>]]

![[<% tp.date.weekday("YY-MM-DD-dddd", 2, tp.file.title, "YYYY-[W]ww") %>#<% tp.date.weekday("dddd", 2, tp.file.title, "YYYY-[W]ww") %>]]

![[<% tp.date.weekday("YY-MM-DD-dddd", 3, tp.file.title, "YYYY-[W]ww") %>#<% tp.date.weekday("dddd", 3, tp.file.title, "YYYY-[W]ww") %>]]

![[<% tp.date.weekday("YY-MM-DD-dddd", 4, tp.file.title, "YYYY-[W]ww") %>#<% tp.date.weekday("dddd", 4, tp.file.title, "YYYY-[W]ww") %>]]

![[<% tp.date.weekday("YY-MM-DD-dddd", 5, tp.file.title, "YYYY-[W]ww") %>#<% tp.date.weekday("dddd", 5, tp.file.title, "YYYY-[W]ww") %>]]

![[<% tp.date.weekday("YY-MM-DD-dddd", 6, tp.file.title, "YYYY-[W]ww") %>#<% tp.date.weekday("dddd", 6, tp.file.title, "YYYY-[W]ww") %>]]


# File created
```dataview
TABLE
WHERE 
	file.cday >= date("<% tp.date.weekday("YYYY-MM-DD", 0, tp.file.title, "YYYY-[W]ww") %>","yy-MM-dd") and
	file.cday < date("<% tp.date.weekday("YYYY-MM-DD", 7, tp.file.title, "YYYY-[W]ww") %>","yy-MM-dd")
```