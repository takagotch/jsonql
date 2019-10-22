### jsonql
---
https://github.com/elgs/jsonql

```go
// jsonql_test.go

func TestParse(t *testing.T) {
  
  jsonString := `
`
  parser, err := NewStringQuery(jsonString)
  if err != nil {
    t.Error(err)
  }
  
  var pass = []struct {
    in string
    ex int
  }{
    {},
    {},
    {}
  }
  var fail = []struct {
    in string
    ex interface{}
  }()
  for _, v := range pass {
    result, err := parser.Query(v.in)
    if err != nil {
      t.Error(v.in, err)
    }
    fmt.Println(v.in, result)
  }
  for range fail {
  }
}

```

```
```

```
```


