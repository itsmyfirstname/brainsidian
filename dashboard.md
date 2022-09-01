## `Active`
```dataview
Table
	type,
	priority,
	topic,
	subject
FROM #in-progress AND -"_templates"
```

## `Tasks`
### Working on
```dataview
TASK 
FROM #in-progress AND -"_templates"
WHERE !completed
GROUP BY file.folder
```


### Completed
```dataview
TASK
WHERE completed
GROUP BY file.folder
```