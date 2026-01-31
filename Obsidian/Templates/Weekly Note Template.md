---
date: <% moment(tp.file.title, 'YYYY-[W]WW').startOf('week').add(0, 'days').format("YYYY-MM-DD") %>
journal: Journal Weekly
type: weekly
log-week:
tags:
summary:
---

---
```calendar-nav
```
---
![[Journal.base#Weekly Note]]

![[Journal.base#Weekly Stats]]

## Week

```toggl
LIST WEEK 
GROUP BY PROJECT
SORT DESC
```

>[!hightlight]- Highlights!
>```dataview
>TASK
>FROM ""
>WHERE icontains(text, "#log/highlight")
>AND (date <= (date(this.date) + dur(6 days))) and (date >= (date(this.date)))
>GROUP BY file.name as filename
>```

>[!calendar]- Daily Reviews
>```dataview
>TASK
>WHERE icontains(text, "#log/day-review")
>AND (date <= (date(this.date) + dur(6 days))) and (date >= (date(this.date)))
>GROUP BY file.name as filename
>SORT filename ASC
>```

---
## 