---
title: Установка Azure PowerShell с помощью PowerShellGet
description: Инструкции по установке Azure PowerShell с помощью PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: d99265c7f156622d876d700106e2b06dd729e8b8
ms.sourcegitcommit: 020c69430358b13cbd99fedd5d56607c9b10047b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "66365746"
---
# <a name="install-the-azure-powershell-module"></a>Установка модуля Azure PowerShell

В этой статье рассказывается, как установить модули Azure PowerShell с помощью PowerShellGet. Эти инструкции применимы для платформ Windows, macOS и Linux. В данный момент другие методы установки не поддерживаются для модуля Az.

## <a name="requirements"></a>Требования

Azure PowerShell работает с PowerShell 5.1 или более поздней версии на платформе Windows или с PowerShell Core 6.x или более поздней версии на любых платформах. Если вы не уверены, установлена ли среда PowerShell, либо используете macOS или Linux, [установите последнюю версию PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).

Чтобы узнать вашу версию PowerShell, выполните приведенную ниже команду:

```powershell-interactive
$PSVersionTable.PSVersion
```

Чтобы запустить Azure PowerShell в PowerShell 5.1 на платформе Windows, сделайте следующее:

1. При необходимости выполните обновление до [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell). Если вы используете Windows 10, среда PowerShell 5.1 уже установлена.
2. [Установите платформу .NET Framework версии 4.7.2 или более поздней](/dotnet/framework/install).

При использовании PowerShell Core для Azure PowerShell нет дополнительных требований.

## <a name="install-the-azure-powershell-module"></a>Установка модуля Azure PowerShell

> [!IMPORTANT]
>
> Модули AzureRM и Az могут быть установлены одновременно. Если у вас установлены оба модуля, __не включайте псевдонимы__.
> Включение псевдонимов приведет к конфликтам между командлетами AzureRM и псевдонимами команд Az с непредсказуемыми результатами.
> Перед установкой модуля Az рекомендуется удалить AzureRM. Удалить AzureRM или включить псевдонимы можно в любое время. Дополнительные сведения о псевдонимах команд AzureRM см. в статье [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) (Миграция с AzureRM на Az для Azure PowerShell).
> Инструкции по удалению см. в разделе [Uninstall the AzureRM module](uninstall-az-ps.md#uninstall-the-azurerm-module) (Удаление модуля AzureRM). 

Чтобы установить модули в глобальной области видимости, необходим более высокий уровень привилегий для установки модулей из коллекции PowerShell. Чтобы установить Azure PowerShell, выполните следующую команду в сеансе с более высоким уровнем привилегий ("Запуск от имени администратора" в Windows или с правами суперпользователя в macOS или Linux):

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

Если у вас нет доступа к привилегиям администратора, можно выполнить установку для текущего пользователя, добавив аргумент `-Scope`.

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

По умолчанию коллекция PowerShell не используется как доверенный репозиторий для PowerShellGet. При первом использовании PSGallery отображается следующее сообщение:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Ответьте `Yes` или `Yes to All`, чтобы продолжить установку.

Модуль Az — это общий модуль для командлетов Azure PowerShell. Во время его установки скачиваются все доступные модули Azure Resource Manager и устанавливаются все соответствующие командлеты.

## <a name="sign-in"></a>Вход

Чтобы начать работу с Azure PowerShell, выполните вход, используя данные своей учетной записи в Azure.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> Если вы отключили автоматическую загрузку модулей, вам нужно вручную импортировать модуль с помощью `Import-Module Az`. Из-за структуры модуля эта операция может занять несколько секунд.

Эти действия нужно повторять для каждого нового сеанса PowerShell. Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах PowerShell, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Обновление модуля Azure PowerShell

Команда [Update-Module](/powershell/module/powershellget/update-module) не обновит установку надлежащим образом из-за способа упаковки модуля Az. С технической точки зрения Az является метамодулем, включающим все подмодули, содержащие командлеты, необходимые для взаимодействия со службами Azure. Это означает, что для обновления модуля Azure PowerShell его необходимо __переустановить__, а не просто __выполнить обновление__. Эта процедура ничем не отличается от установки, но может потребоваться добавить аргумент `-Force`:

```powershell
Install-Module -Name Az -AllowClobber -Force
```

Хотя это может перезаписать установленные модули, в системе по-прежнему могут остаться более старые версии.
Сведения о том, как удалить из системы предыдущие версии Azure PowerShell, см. в статье [Uninstall the Azure PowerShell module](uninstall-az-ps.md) (Удаление модуля Azure PowerShell).

## <a name="use-multiple-versions-of-azure-powershell"></a>Использование нескольких версий Azure PowerShell

Вы можете установить несколько версий Azure PowerShell. Чтобы проверить наличие нескольких установленных версий Azure PowerShell, используйте следующую команду:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

Сведения о том, как удалить версию Azure PowerShell, см. в статье [Удаление модуля Azure PowerShell](uninstall-az-ps.md).

Определенную версию модуля `Az` можно установить или загрузить с помощью аргумента `-RequiredVersion`.

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

Если у вас установлено несколько версий модуля, модуль автозагрузки и `Import-Module` загрузит последнюю версию по умолчанию.

## <a name="provide-feedback"></a>Отзывы

Если вы нашли ошибку при работе с Azure Powershell, сообщите о ней [на сайте GitHub](https://github.com/Azure/azure-powershell/issues).
Чтобы отправить отзыв из командной строки, используйте командлет [Send-Feedback](/powershell/module/az.accounts/send-feedback).

## <a name="next-steps"></a>Дальнейшие действия

Дополнительные сведения о модулях Azure PowerShell и их функциях см. в статье [Get Started with Azure PowerShell](get-started-azureps.md) (Начало работы с Azure PowerShell).
Если вы знакомы с Azure PowerShell и вам необходимо мигрировать из AzureRM, см. статью [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) (Миграция с AzureRM на Az).