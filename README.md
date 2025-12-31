# 👋 Hi, I'm mdgrs.

- I love making fun, cool, and useful things with PowerShell
- I develop games at work
- I blog at https://mdgrs.hashnode.dev
- I'm active on Bluesky [@mdgrs.bsky.social](https://bsky.app/profile/mdgrs.bsky.social)
- I'm mostly just reading it but active on the [PowerShell Discord](https://discord.gg/powershell) too

## Projects I'm working on

### PowerShellRun

Terminal Based Launcher and Fuzzy Finder for PowerShell ([GitHub Repo](https://github.com/mdgrs-mei/PowerShellRun))

![GitHub Repo stars](https://img.shields.io/github/stars/mdgrs-mei/PowerShellRun)

![PowerShellRun](https://github.com/user-attachments/assets/fb817310-540c-4e54-b34d-1bf0d3759246)

*PowerShellRun* is a launcher application released as a PowerShell module. You can launch applications, utilities and PowerShell script blocks from your terminal. Add everything you need to PowerShellRun, the fuzzy finder helps you run them with ease.

```powershell
Enable-PSRunEntry -Category All
Add-PSRunScriptBlock -Name 'GitPullRebase' -ScriptBlock {
    git pull --rebase --prune
}
Invoke-PSRun
```

### WinUIShell

Scripting WinUI 3 with PowerShell ([GitHub Repo](https://github.com/mdgrs-mei/WinUIShell))

![GitHub Repo stars](https://img.shields.io/github/stars/mdgrs-mei/WinUIShell)

![WinUIShell](https://github.com/user-attachments/assets/a4cc4bf3-0ca6-41f6-94bf-f039c5a5e48e)

*WinUIShell* is a PowerShell module that allows you to create WinUI 3 applications in PowerShell. The goal is to give script authors a framework to create modern and simple GUIs for their scripts.

```powershell
using namespace WinUIShell
Import-Module WinUIShell

$win = [Window]::new()
$win.Title = 'Hello from PowerShell!'
$win.AppWindow.ResizeClient(400, 200)

$button = [Button]::new()
$button.Content = 'Click Me'
$button.HorizontalAlignment = 'Center'
$button.VerticalAlignment = 'Center'
$button.AddClick({
    $button.Content = 'Clicked!'
})

$win.Content = $button
$win.Activate()
$win.WaitForClosed()
```


