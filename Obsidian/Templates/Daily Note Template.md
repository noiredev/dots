---
date: <% moment(tp.file.title, 'YYYY-MM-DD').format("YYYY-MM-DD") %>
journal: Journal daily
type: 
- daily
aliases:
up: 
log-VN:
log-LN:
log-manga:
log-listening:
log-programming:
log-gamedev:
tags:
summary:
---

---
```calendar-nav
```
---

## Pictures
#### <% tp.file.title %>

```toggl
LIST TODAY 
GROUP BY PROJECT
SORT DESC
```

## Morning Pages
>[!journal]- Today Years Ago
>![[Bases/Journal.base#Today Years Ago|Journal]]

>[!calendar]- Notes Created This Day
>![[Journal.base#Notes Created This Day]]

>[! task]- Tasks
>```dataview
>TASK
>WHERE !completed
>AND icontains(text, "[[ <%moment(tp.file.title, 'YYYY-MM-DD').format('YYYY-MM') %> -")
>AND icontains(text, "#task")
>GROUP BY file.name as filename
>SORT rows.file.ctime DESC
>```

# Log Pages

