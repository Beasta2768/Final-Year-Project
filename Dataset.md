# All Notes
```dataview
List 
FROM -"Templates"
WHERE Week > 0
Sort Week
```
# Lectures
## Online Lectures 
```dataview
TABLE Topic, Date, Week
FROM -"Templates"
WHERE Type = "Online"
Sort Week
```

```dataview
TABLE Topic, Date, Week
FROM -"Templates"
WHERE Type = "Tutorial"
Sort Week
```

```dataview
CALENDAR file.ctime
FROM -"Templates" and -"Excalidraw"
```

