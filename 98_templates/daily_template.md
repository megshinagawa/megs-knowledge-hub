# <%tp.date.now("YYYY-MM-DD ddd") %>

## Created Today
```dataview
LIST
FROM "01_notes"
WHERE dateformat(datecreated, "yyyyMMdd") = this.file.name
```
