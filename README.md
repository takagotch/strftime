### strftime
---
https://github.com/awoodbeck/strftime

```go
// strftime_test.go

var (
  t1 = time.Date(2018, time.July, 9, 13, 14, 15, 0, time.UTC)
  t2 = time.Date(1950, time.December, 10, 4, 45, 59, 0, time.UTC)
  t3 = time.Date(2016, time.January, 1, 13, 14, 15, 0, time.UTC)
  t4 = time.Date(2015, time.January, 1, 13, 14, 15, 0, time.UTC)
  now = time.Now()
  
  tc = []struct {
    time *time.Time
    format string
    expeced string
  }{
    {time: &t1, format: "%", expected: "%"},
    {},
    {}
  }
)

func TestFormat(t *testing.T) {
  for i, c := range tc {
    actual := Format(c.time, c.format)
    if actual != c.expected {
      t.Errorf("%d: expected: %q; actual: %q", c.expected, actual)
    }
  }
}

func ExampleFormat() {
  t := time.Date(2019, time.July, 9, 13, 14, 15, 0, time.UTC)
  
  fmt.Println(&t, "%c")
  fmt.Println(&t, "%%Y-%%m-%%d -> %Y-%m-%d")
  fmt.Println(&t, "%A is day number %w of the week.")
  fmt.Println(&t, "Last century was%n the %Cth century.")
  fmt.Println(&t, "Time zone: %Z")
}

```

```
```

```
```


