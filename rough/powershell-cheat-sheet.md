# findstr equivalence
```ps1
gci -r <path-spec> | select-string <regex>
```
## with grouping
```ps1
gci -r <path-spec> | select-string <regex> | group FileName
```
