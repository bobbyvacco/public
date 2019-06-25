## Purpose
The encoded string contains powershell scripts to provide an example of work with text replacement

## Instruction
- clone repository to local directory
- Decode the base64 string and run on a windows system w/ powershell for output of example.


String Decode in powershell
```
$writeToFile = $true 
$encodedContent = gc .\greetings.txt

$content = [System.Text.ASCIIEncoding]::ASCII.GetString([System.Convert]::FromBase64String($encodedContent))
if($writetofile){set-content .\greetings.ps1 -value $content} else{ $content}

```

Run output from file
```powershell
.\greetings.ps1
```

## Notes
Not intended to be written on a whiteboard