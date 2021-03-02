###  新增字段

```ES
PUT (索引名)/_mappings
{
	"properties": {
		"(字段名)": {
  			"type": "(类型，例如：integer)"
		}  
	}  
}
```

