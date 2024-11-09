### Dumputer is a quick and efficient app remover for Windows 11, built to get rid of unnecessary pre-installed apps (looking at you, bloatware). Sometimes you just need a tool that works fast, no frills, and with smart recommendations that make the process smoother. 

I created this tool out of frustration — Windows 11 had become sluggish, and the typical debloating tools weren’t cutting it. So, I decided to build something reliable and effective. With Dumputer, youll have a lightweight, no-nonsense solution that works, especially with version 24H2 of Windows 11.

### Background
When Microsoft released Windows 11 version 24H2, they tweaked the Get-AppxPackage command, which broke a some debloater tools. To solve this, I pivoted to a Process-Based Approach. Instead of running the Get-AppxPackage cmdlet directly through the app, I now launch an external PowerShell.exe process that handles the command asynchronously. This not only ensures better stability but also makes the app more compatible with the latest updates.

Initially, I used the .NET PowerShell API to fetch installed Appx packages, but ran into some compatibility issues, notably the "type initializer for '<Module>' threw an exception" error. So, I ditched that approach and went for a more reliable, process-based method.

Dumputer was originally born as a client project where I fine-tuned the tool to track down and efficiently remove unwanted software. Right now, it’s a lean, fast solution — but stay tuned, as I'll be unlocking more features as I continue to optimize it.

Just a heads-up: Older apps like XD-AntiSpy (including the Debloater plugin) and Bloatbox are still broken due to the same issue. I’ll definitely get around to fixing XD-AntiSpy soon, but with older apps like Bloatbox, breaking down the code takes much longer. Sometimes, starting a new project ends up being quicker

And about the name? Well, I was so tired of dealing with a bloated, slow machine that I just had to call it "Dumputer" — a mix of dump and computer. Because sometimes, your computer’s just full of junk. 
