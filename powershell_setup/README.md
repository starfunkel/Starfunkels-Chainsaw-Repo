### Path loader for Yara files

Either put the profile.ps1 in the path which is displayed when executing the following ps command

```powershell
echo $PROFILE.CurrentUserCurrentHost
```

### Or modify your existig powershell profile and add the directories containing chainsaw's Yara files

```powershel
# Example contents of C:\Users\%YOURUSERNAME%\Documents\WindowsPowerShell\Microsoft.PowerShell_profile.ps1

$sigma = "\chainsaw\sigma"
$mapping = "\chainsaw\mappings"
$rules = "\chainsaw\rules"
```

### Now one can use these variable in the current powershell user namespace to point to the files

```powershell
chainsaw.exe hunt .\Security.evtx -s $sigma --mapping $mapping\custom.yml --rule $rules --csv -o .\out\
```