``` kusto
let ASAEvents=    
(
    externaldata(ASA: string, DeviceEventClassID: string,description: string)
    [
        h@"https://raw.githubusercontent.com/qc-gordon/AzureSentinelHelpers/master/ASA%20EventIDs.csv"
    ]
    with(format="csv")
);
```