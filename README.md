# То что полезно установить на винду:

## Пакетные менеджеры:
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
>  <p> <img src="https://github.com/MitrichevGeorge/-windows/blob/main/img/2.png"/>
> </details>
> Тогда надо прописать
> ``` Set-ExecutionPolicy RemoteSigned -scope CurrentUser -Force ```

### UV
```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

## Оконные утилиты
### Powertoys
![изображение](https://github.com/user-attachments/assets/5cd3f3b8-2bd5-41b7-9dea-dae17b3cf948)
Мощная программа с кучей мелких функций. Среди них:
- Крепление окна поверх других
- Пипетка по всему экрану
- Палитра команд
- Экранная линейка
- ...
Установка:
```powershell
winget install Microsoft.PowerToys -s winget
```
Если у вас нет `winget` пропишите:
```powershell
Install-PackageProvider -Name NuGet -Force | Out-Null
Install-Module -Name Microsoft.WinGet.Client -Force -Repository PSGallery | Out-Null
Repair-WinGetPackageManager
```

### Windhawk
встраивание кода в куски системы
```powershell
Invoke-WebRequest 'https://ramensoftware.com/downloads/windhawk_setup.exe' -OutFile 'windhawk_setup.exe'; Start-Process 'windhawk_setup.exe'
```

### Fluent terminal
прокачанный прозрачный терминал
```powershell
scoop install fluentterminal
```

## консольные утилиты
### MSYS2
Оболочка работающая похоже на Arch
```powershell
scoop install msys2
msys2
```

### mpv
Воспроизведение видео из консоли
```powershell
scoop bucket add extras
scoop install extras/mpv
```

### fzf
удобства поиска папок
```powershell
choco install fzf
```

### ffmpeg
Редактор видео
```powershell
choco install ffmpeg
```

## Просто так
### Ani-cli
Понадобится [mpv](#mpv)
```powershell
uv tool install anicli-ru
```
