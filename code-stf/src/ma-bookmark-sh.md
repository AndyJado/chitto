how many apps out there are able to be replaced with some bash script?

```bash
boma() {
    echo "what is the url?"
    read url
    echo "keywords?"
    read kwd
    echo "["$kwd"]("$url")" | pbcopy
}
```
