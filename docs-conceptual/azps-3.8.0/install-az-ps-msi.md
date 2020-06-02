---
title: Установка Azure PowerShell с помощью MSI
description: Сведения о том, как установить Azure PowerShell без PowerShellGet с помощью пакета MSI.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 07abfc9a4277c0d658830c397ad5c1abfbe95abe
ms.sourcegitcommit: 9f5c7d231b069ad501729bf015a829f3fe89bc6a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2020
ms.locfileid: "84122212"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="4e9a7-103">Установка Azure PowerShell в ОС Windows с помощью пакета MSI</span><span class="sxs-lookup"><span data-stu-id="4e9a7-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="4e9a7-104">В этой статье объясняется, как установить Azure PowerShell в ОС Windows с помощью установщика MSI.</span><span class="sxs-lookup"><span data-stu-id="4e9a7-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span> <span data-ttu-id="4e9a7-105">Установщик MSI предоставляется для сред, в которых коллекция PowerShell может блокироваться брандмауэром или требуется автономный установщик.</span><span class="sxs-lookup"><span data-stu-id="4e9a7-105">The MSI installer is provided for environments where the PowerShell Gallery may be blocked by a firewall, or an offline installer is needed.</span></span> <span data-ttu-id="4e9a7-106">Мы рекомендуем устанавливать Azure PowerShell с помощью PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="4e9a7-106">The recommended way to install Azure PowerShell is with PowerShellGet.</span></span> <span data-ttu-id="4e9a7-107">Инструкции по установке Azure PowerShell с помощью PowerShellGet см. в [этой статье](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="4e9a7-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-az-ps.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e9a7-108">Требования</span><span class="sxs-lookup"><span data-stu-id="4e9a7-108">Requirements</span></span>

<span data-ttu-id="4e9a7-109">Установщик MSI в Windows предназначен для только установки Azure PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="4e9a7-109">The MSI installer on Windows is designed to install Azure PowerShell for PowerShell 5.1 only.</span></span> <span data-ttu-id="4e9a7-110">Для установки на платформах, отличающихся от Windows, или более поздних версий PowerShell [выполните установку PowerShellGet](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="4e9a7-110">For installation on non-Windows platforms or later versions of PowerShell, [Install with PowerShellGet](install-az-ps.md).</span></span> <span data-ttu-id="4e9a7-111">Чтобы узнать вашу версию PowerShell, выполните приведенную ниже команду:</span><span class="sxs-lookup"><span data-stu-id="4e9a7-111">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="4e9a7-112">Чтобы использовать Azure PowerShell в PowerShell 5.1, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="4e9a7-112">To use Azure PowerShell in PowerShell 5.1, you need to:</span></span>

1. <span data-ttu-id="4e9a7-113">При необходимости выполните обновление до [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="4e9a7-113">Update to [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="4e9a7-114">Если вы используете Windows 10, среда PowerShell 5.1 уже установлена.</span><span class="sxs-lookup"><span data-stu-id="4e9a7-114">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="4e9a7-115">[Установите платформу .NET Framework версии 4.7.2 или более поздней](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="4e9a7-115">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="4e9a7-116">Установка или обновление в Windows с помощью пакета MSI</span><span class="sxs-lookup"><span data-stu-id="4e9a7-116">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="4e9a7-117">Пакет MSI для Azure PowerShell доступен на [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span><span class="sxs-lookup"><span data-stu-id="4e9a7-117">The MSI package for Azure PowerShell is available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="4e9a7-118">Если вы установили более ранние версии модулей Azure PowerShell с помощью пакета MSI, установщик удалит их автоматически.</span><span class="sxs-lookup"><span data-stu-id="4e9a7-118">If you have installed earlier versions of Azure PowerShell using the MSI, the installer automatically removes them.</span></span> <span data-ttu-id="4e9a7-119">Пакет MSI устанавливает модули в `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="4e9a7-119">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span>

<span data-ttu-id="4e9a7-120">Чтобы начать работу с Azure PowerShell, выполните вход, используя данные своей учетной записи в Azure.</span><span class="sxs-lookup"><span data-stu-id="4e9a7-120">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="4e9a7-121">Если вы отключили автоматическую загрузку модулей, вам нужно вручную импортировать модуль с помощью `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="4e9a7-121">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="4e9a7-122">Из-за структуры модуля эта операция может занять около минуты.</span><span class="sxs-lookup"><span data-stu-id="4e9a7-122">Because of the way the module is structured, this can take up to a minute.</span></span>

<span data-ttu-id="4e9a7-123">Это действие нужно будет повторить для каждого нового сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4e9a7-123">You'll need to repeat this step for every new PowerShell session you start.</span></span> <span data-ttu-id="4e9a7-124">Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах PowerShell, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="4e9a7-124">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="4e9a7-125">Отзывы</span><span class="sxs-lookup"><span data-stu-id="4e9a7-125">Provide feedback</span></span>

<span data-ttu-id="4e9a7-126">Если вы нашли ошибку при работе с Azure PowerShell, [сообщите о проблеме на GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="4e9a7-126">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="4e9a7-127">Чтобы отправить отзыв из командной строки, используйте командлет [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="4e9a7-127">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="4e9a7-128">Next Steps</span><span class="sxs-lookup"><span data-stu-id="4e9a7-128">Next Steps</span></span>

<span data-ttu-id="4e9a7-129">Дополнительные сведения о модулях Azure PowerShell и их функциях см. в статье [Get Started with Azure PowerShell](get-started-azureps.md) (Начало работы с Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="4e9a7-129">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="4e9a7-130">Если вы знакомы с Azure PowerShell и вам необходимо мигрировать из AzureRM, см. статью [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) (Миграция с AzureRM на Az).</span><span class="sxs-lookup"><span data-stu-id="4e9a7-130">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
