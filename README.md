# Dumputer
With the release of version 24H2, Microsoft made some changes to the Get-AppxPackage command, causing many debloater tools to break. To address this, I switched to a Process-Based Approach, where an external PowerShell.exe process runs the same Get-AppxPackage cmdlet. This method captures and processes the output asynchronously, improving stability and compatibility.

Initially, I used the .NET PowerShell API to fetch installed Appx packages by running the Get-AppxPackage cmdlet, pulling both app names and package details. However, I ran into the 'type initializer for '<Module>' threw an exception' error, likely due to compatibility issues with PowerShell modules in certain environments.

This app is designed to quickly identify and remove pre-installed apps on Windows 11 (especially version 24H2). It started as a client project, where I optimized the app to efficiently track down and remove unnecessary software. Some features will still be unlocked as I continue to enhance the app.

I’ve done some tweaking and bundled everything into a lightweight app package now. Just a heads-up—my older apps like XD-AntiSpy and Bloatbox aren't working properly yet either.


