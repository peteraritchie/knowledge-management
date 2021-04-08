# findstr equivalence
```ps1
gci -r <path-spec> | select-string <regex>
```
## with grouping
```ps1
gci -r <path-spec> | select-string <regex> | group FileName
```
# dir equivalents

dir /ad

Get-ChildItem | Where-Object {$_.PSIsContainer}

dir /a-d

Get-ChildItem | Where-Object {!$_.PSIsContainer}

dir /od

Get-ChildItem | Sort-Object Date

dir /od /a-d

Get-ChildItem | Where-Object {!$_.PSIsContainer} | Sort-Object Date

dir /ah

Get-ChildItem -force -path C:\ | Where-Object {$_.Mode -match "h"}

dir /a-h

Get-ChildItem -force -path C:\ | Where-Object {!$_.Mode -match "h"}

dir /b

Get-ChildItem | Select-Object Name
