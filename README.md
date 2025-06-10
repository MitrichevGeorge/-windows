# То что нужно установить на винду:

## Для начала установим пакетные менеджеры:
### Chocolatey
Выполните в `PowerShell` от имени администратора
```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

### Scoop
```powershell
iwr -useb get.scoop.sh | iex
```
> [!IMPORTANT]
> Возможно будет следущая проблема:
> <details>
>  <summary>Текст который может вывестись</summary>
>  <p> <img src="https://github.com/MitrichevGeorge/-windows/blob/main/img/1.png"/>
> </details>
