---
title: Другие способы установки Azure PowerShell
description: Сведения о том, как установить Azure PowerShell без PowerShellGet.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 7148188603e84efbcd784264de4c78819edf6833
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243724"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a>Установка Azure PowerShell в ОС Windows с помощью пакета MSI или установщика веб-платформы

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

В этой статье описывается, как установить Azure PowerShell в ОС Windows с помощью пакета MSI или установщика веб-платформы.
Используйте эти способы установки только в том случае, если это необходимо для вашей системы. Мы рекомендуем устанавливать Azure PowerShell в ОС Windows с помощью PowerShellGet. Инструкции по установке Azure PowerShell с помощью PowerShellGet см. в [этой статье](install-azurerm-ps.md).

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Установка или обновление в Windows с помощью пакета MSI

Azure PowerShell можно установить с помощью MSI-файла из [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018). Если вы установили предыдущие версии модулей Azure с помощью пакета MSI, установщик удалит их автоматически. Пакет MSI устанавливает модули в `${env:ProgramFiles}\WindowsPowerShell\Modules`. Устанавливаются оба модуля: `AzureRM` и `Azure`.

> [!NOTE]
> Используйте модуль `Azure`, только если вы работаете с классической моделью развертывания Azure.

Чтобы приступить к работе с Azure PowerShell, вам нужно загрузить `AzureRM` в текущий сеанс PowerShell. Для этого воспользуйтесь командлетом [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), после чего войдите в систему с помощью своих учетных данных Azure.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Эти действия нужно повторять для каждого нового сеанса PowerShell. Чтобы автоматически импортировать модуль `AzureRM`, необходимо настроить профиль PowerShell. Подробнее об этом рассказывается [здесь](/powershell/module/microsoft.powershell.core/about/about_profiles).
Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a>Установка или обновление в Windows с помощью установщика веб-платформы

Скачайте [пакет Azure PowerShell WebPI](https://aka.ms/webpi-azps) и запустите установку. Если вы установили предыдущие версии модулей Azure с помощью пакета MSI или установщика веб-платформы, установщик удалит их автоматически. Модули устанавливаются в `${env:ProgramFiles}\WindowsPowerShell\Modules`. Устанавливаются оба модуля: `AzureRM` и `Azure`.

> [!NOTE]
> Используйте модуль `Azure`, только если вы работаете с классической моделью развертывания Azure.

Чтобы приступить к работе с Azure PowerShell, вам нужно загрузить `AzureRM` в текущий сеанс PowerShell. Для этого воспользуйтесь командлетом [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), после чего войдите в систему с помощью своих учетных данных Azure.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Эти действия нужно повторять для каждого нового сеанса PowerShell. Чтобы автоматически импортировать модуль `AzureRM`, необходимо настроить профиль PowerShell. Подробнее об этом рассказывается [здесь](/powershell/module/microsoft.powershell.core/about/about_profiles).
Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).
