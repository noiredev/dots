---
date: <% moment(tp.file.title, 'YYYY-MM-DD').format("YYYY-MM-DD") %>
journal: Journal daily
type: 
- daily
aliases:
japanese-reading:
japanese-listening:
programming:
gamedev:
tags:
summary:
---

---
```calendar-nav
```
---

```dataview
TABLE 
  japanese-reading as "Reading",
  japanese-listening as "Listening",
  programming as "Programming",
  gamedev as "Gamedev",
  number(japanese-listening) + number(japanese-reading) + number(programming) + number(gamedev) as "Total"
WHERE file = this.file
```

## Pictures
#### <% tp.file.title %>

```toggl
LIST TODAY 
GROUP BY PROJECT
SORT DESC
```

---

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

