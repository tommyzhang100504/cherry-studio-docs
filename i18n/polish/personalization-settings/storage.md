---
icon: floppy-disk
---

{% hint style="warning" %}
Ten dokument został przetłumaczony z chińskiego przez AI i nie został jeszcze zweryfikowany.
{% endhint %}

# Domyślna lokalizacja przechowywania

Przechowywanie danych w Cherry Studio jest zgodne ze standardami systemowymi. Dane są automatycznie umieszczane w katalogu użytkownika, a dokładna lokalizacja katalogu wygląda następująco:

> macOS: /Users/username/Library/Application Support/CherryStudioDev

> Windows: C:\Users\username\AppData\Roaming\CherryStudio

> Linux: /home/username/.config/CherryStudio

Można również zobaczyć w następującej lokalizacji:
<figure><img src="../../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>



# Zmiana lokalizacji przechowywania (informacyjnie)

**Metoda 1:**

Można to osiągnąć poprzez utworzenie łącza symbolicznego. Zamknij aplikację, przenieś dane do żądanej lokalizacji, a następnie utwórz łącze w oryginalnej lokalizacji wskazujące na nową lokalizację.

Szczegółowe kroki można znaleźć w: [https://github.com/CherryHQ/cherry-studio/issues/621#issuecomment-2588652880](https://github.com/CherryHQ/cherry-studio/issues/621#issuecomment-2588652880)

**Metoda 2:**
Opierając się na charakterystyce aplikacji Electron, lokalizację przechowywania można zmienić poprzez skonfigurowanie parametrów uruchamiania.

> --user-data-dir
> np: Cherry-Studio-*-x64-portable.exe --user-data-dir="%user_data_dir%"

> Przykład:

```shell
PS D:\CherryStudio> dir


    目录: D:\CherryStudio


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         2025/4/18     14:05                user-data-dir
-a----         2025/4/14     23:05       94987175 Cherry-Studio-1.2.4-x64-portable.exe
-a----         2025/4/18     14:05            701 init_cherry_studio.bat
```

> init_cherry_studio.bat (kodowanie: ANSI)

```bash
@title Inicjalizacja CherryStudio
@echo off

set current_path_dir=%~dp0
@echo Bieżąca ścieżka:%current_path_dir%
set user_data_dir=%current_path_dir%user-data-dir
@echo Ścieżka danych CherryStudio:%user_data_dir%

@echo Wyszukiwanie pliku Cherry-Studio-*-portable.exe w bieżącym katalogu
setlocal enabledelayedexpansion

for /f "delims=" %%F in ('dir /b /a-d "Cherry-Studio-*-portable*.exe" 2^>nul') do ( #Ten kod jest dostosowany do wersji z GitHub i oficjalnej strony, dla innych wersji zmodyfikuj samodzielnie
    set "target_file=!cd!\%%F"
    goto :break
)
:break
if defined target_file (
    echo Znaleziono plik: %target_file%
) else (
    echo Nie znaleziono pasującego pliku, zamykanie skryptu
    pause
    exit
)

@echo Potwierdź, aby kontynuować
pause

@echo Uruchamianie CherryStudio
start %target_file% --user-data-dir="%user_data_dir%"

@echo Operacja zakończona
@echo on
exit
```

> Struktura katalogu user-data-dir po inicjalizacji:

```shell
PS D:\CherryStudio> dir .\user-data-dir\


    目录: D:\CherryStudio\user-data-dir


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         2025/4/18     14:29                blob_storage
d-----         2025/4/18     14:07                Cache
d-----         2025/4/18     14:07                Code Cache
d-----         2025/4/18     14:07                Data
d-----         2025/4/18     14:07                DawnGraphiteCache
d-----         2025/4/18     14:07                DawnWebGPUCache
d-----         2025/4/18     14:07                Dictionaries
d-----         2025/4/18     14:07                GPUCache
d-----         2025/4/18     14:07                IndexedDB
d-----         2025/4/18     14:07                Local Storage
d-----         2025/4/18     14:07                logs
d-----         2025/4/18     14:30                Network
d-----         2025/4/18     14:07                Partitions
d-----         2025/4/18     14:29                Session Storage
d-----         2025/4/18     14:07                Shared Dictionary
d-----         2025/4/18     14:07                WebStorage
-a----         2025/4/18     14:07             36 .updaterId
-a----         2025/4/18     14:29             20 config.json
-a----         2025/4/18     14:07            434 Local State
-a----         2025/4/18     14:29             57 Preferences
-a----         2025/4/18     14:09           4096 SharedStorage
-a----         2025/4/18     14:30            140 window-state.json
```