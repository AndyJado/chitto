```
je.filter(|c| c.is_some())

// returns Some(a)? or a?
je.filter_map(|c| c.ok())
```