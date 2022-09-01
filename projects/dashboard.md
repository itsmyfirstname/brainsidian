## Current Projects
Return current projects using a `TABLE`, grouped by implicit fields[^1]
```dataview
TABLE
	 file.folder as Name,
	 priority as Priority
FROM "projects" AND #in-progress
```

## Completed Projects
Return completed projects using a `LIST`, using implicit fields[^1]
```dataview
LIST
FROM "projects" AND #completed 
```

## Project Tasks
```dataview
TASK
FROM "projects"
WHERE !completed
GROUP BY file.folder
```


---
###### Footnotes
[^1]:`file.folder` is an [implicit field](https://blacksmithgu.github.io/obsidian-dataview/data-annotation/#implicit-fields) 