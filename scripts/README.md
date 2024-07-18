### Convert-Chainsaw_txt_to_csv.ps1

The `Convert-Chainsaw_txt_to_csv.ps1` script file is an easy to use first impression script to quickly optain a csv file with artefact information.

For example use:
```Powershell
./chainsaw.exe search  -t 'Event.EventData.TargetUserName: $TargetUserName' .\Security.evtx > $TargetUserName.txt
```
To obtain infoomation about a given user.

Or use
```Powershell
chainsaw.exe search  -t 'Event.System.EventID: =EventID' .\Security.evtx > EventID.txt
```

To get all log entries containing given eventlog entries.

Please refer to [the awesome Chainsaw docs](https://github.com/WithSecureLabs/chainsaw/blob/master/README.md) to get the full idea.