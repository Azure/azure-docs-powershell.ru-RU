---
title: Установка Azure PowerShell в ОС Windows с помощью PowerShellGet
description: Инструкции по установке Azure PowerShell с помощью PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: b04d4070e420f2d1e64f233eda6b3e250f8bb68c
ms.sourcegitcommit: 9f5c7d231b069ad501729bf015a829f3fe89bc6a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2020
ms.locfileid: "84122037"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="974a9-103">Установка Azure PowerShell в ОС Windows с помощью PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="974a9-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="974a9-104">В этой статье содержатся инструкции по установке модулей Azure PowerShell для PowerShell 5.x для Windows с помощью PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="974a9-104">This article explains the steps to install the Azure PowerShell modules for PowerShell 5.x for Windows using PowerShellGet.</span></span> <span data-ttu-id="974a9-105">PowerShellGet и управление модулями — это предпочтительный способ установки Azure PowerShell, но если вы хотите использовать для установки пакет MSI или установщик веб-платформы, см. статью о [других способах установки](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="974a9-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="974a9-106">Эта версия Azure PowerShell не поддерживает классическую модель развертывания Azure.</span><span class="sxs-lookup"><span data-stu-id="974a9-106">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="974a9-107">Если вам нужна поддержка классического развертывания, см. статью [Установка модуля управления службами Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="974a9-107">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="974a9-108">Модуль AzureRM не поддерживается в macOS и Linux.</span><span class="sxs-lookup"><span data-stu-id="974a9-108">The AzureRM module is not supported for macOS or Linux.</span></span> <span data-ttu-id="974a9-109">Чтобы использовать командлеты Azure PowerShell на этих платформах, [установите модуль Az](/powershell/azure/install-az-ps).</span><span class="sxs-lookup"><span data-stu-id="974a9-109">To use Azure PowerShell cmdlets on these platforms, [Install the Az module](/powershell/azure/install-az-ps).</span></span>

## <a name="requirements"></a><span data-ttu-id="974a9-110">Требования</span><span class="sxs-lookup"><span data-stu-id="974a9-110">Requirements</span></span>

<span data-ttu-id="974a9-111">Чтобы использовать Azure PowerShell версии 6.0 и выше, требуется установить PowerShell 5.0.</span><span class="sxs-lookup"><span data-stu-id="974a9-111">Starting with Azure PowerShell version 6.0, Azure PowerShell requires PowerShell version 5.0.</span></span> <span data-ttu-id="974a9-112">Чтобы проверить установленную на своем компьютере версию PowerShell, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="974a9-112">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="974a9-113">Если у вас более старая версия, см. раздел [Обновление существующей версии Windows PowerShell](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="974a9-113">If you have an outdated version, see [Upgrading existing Windows PowerShell](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="974a9-114">Для модуля AzureRM, описанном в этом документе, используется .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="974a9-114">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="974a9-115">Из-за этого модуль несовместимым с PowerShell версии 6.0, для которой используется .NET Core.</span><span class="sxs-lookup"><span data-stu-id="974a9-115">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="974a9-116">Если вы используете PowerShell 6.0, изучите [инструкции по установке для macOS и Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="974a9-116">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="974a9-117">Установка модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="974a9-117">Install the Azure PowerShell module</span></span>

<span data-ttu-id="974a9-118">Для установки модулей из коллекции PowerShell требуется более высокий уровень привилегий.</span><span class="sxs-lookup"><span data-stu-id="974a9-118">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="974a9-119">Чтобы установить Azure PowerShell, в сеансе с более высоким уровнем привилегий выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="974a9-119">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```azurepowershell-interactive
Install-Module -Name AzureRM -AllowClobber
```

> [!NOTE]
> <span data-ttu-id="974a9-120">Если установленная версия NuGet предшествует версии 2.8.5.201, вам будет предложено скачать и установить последнюю версию NuGet.</span><span class="sxs-lookup"><span data-stu-id="974a9-120">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="974a9-121">По умолчанию коллекция PowerShell не используется как доверенный репозиторий для PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="974a9-121">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="974a9-122">При первом использовании PSGallery отображается следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="974a9-122">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="974a9-123">Ответьте `Yes` или `Yes to All`, чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="974a9-123">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="974a9-124">Модуль `AzureRM` — это общий модуль для командлетов Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="974a9-124">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="974a9-125">Во время его установки скачиваются все доступные модули Azure Resource Manager и устанавливаются все соответствующие командлеты.</span><span class="sxs-lookup"><span data-stu-id="974a9-125">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="974a9-126">Вход</span><span class="sxs-lookup"><span data-stu-id="974a9-126">Sign in</span></span>

<span data-ttu-id="974a9-127">Чтобы начать работу с Azure PowerShell, выполните вход, используя данные своей учетной записи в Azure.</span><span class="sxs-lookup"><span data-stu-id="974a9-127">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```azurepowershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
> <span data-ttu-id="974a9-128">Если вы отключили автоматическую загрузку модулей, вам нужно вручную импортировать модуль с помощью `Import-Module AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="974a9-128">If you've disabled module autoloading, you need to manually import the module with `Import-Module AzureRM`.</span></span> <span data-ttu-id="974a9-129">Из-за структуры модуля эта операция может занять несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="974a9-129">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="974a9-130">Эти действия нужно повторять для каждого нового сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="974a9-130">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="974a9-131">Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах PowerShell, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="974a9-131">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="974a9-132">Обновление модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="974a9-132">Update the Azure PowerShell module</span></span>

<span data-ttu-id="974a9-133">Чтобы обновить версию Azure PowerShell, выполните команду [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="974a9-133">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="974a9-134">Эта команда **не** удаляет предыдущие версии.</span><span class="sxs-lookup"><span data-stu-id="974a9-134">This command does **not** uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

<span data-ttu-id="974a9-135">Сведения о том, как удалить из системы предыдущие версии Azure PowerShell, см. в статье [Удаление модуля Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="974a9-135">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="974a9-136">Использование нескольких версий Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="974a9-136">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="974a9-137">Вы можете установить несколько версий Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="974a9-137">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="974a9-138">Чтобы проверить наличие нескольких установленных версий Azure PowerShell, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="974a9-138">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```azurepowershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions | select Name,Version
```

<span data-ttu-id="974a9-139">Сведения о том, как удалить версию Azure PowerShell, см. в статье [Удаление модуля Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="974a9-139">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="974a9-140">Несколько версий могут понадобиться, если вы работаете с локальными ресурсами Azure Stack, пользуетесь более ранней версией Windows или используете классическую модель развертывания Azure.</span><span class="sxs-lookup"><span data-stu-id="974a9-140">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows, or use the Azure classic deployment model.</span></span> <span data-ttu-id="974a9-141">Чтобы установить более раннюю версию, при установке укажите аргумент `-RequiredVersion`.</span><span class="sxs-lookup"><span data-stu-id="974a9-141">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```azurepowershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="974a9-142">По умолчанию всегда загружается модуль Azure PowerShell последней версии.</span><span class="sxs-lookup"><span data-stu-id="974a9-142">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="974a9-143">Чтобы загрузить другую версию, укажите аргумент `-RequiredVersion`.</span><span class="sxs-lookup"><span data-stu-id="974a9-143">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```azurepowershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a><span data-ttu-id="974a9-144">Отзывы</span><span class="sxs-lookup"><span data-stu-id="974a9-144">Provide feedback</span></span>

<span data-ttu-id="974a9-145">Если вы нашли ошибку при работе с Azure Powershell, [сообщите о ней на сайте GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="974a9-145">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="974a9-146">Чтобы отправить отзыв из командной строки, используйте командлет [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="974a9-146">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="974a9-147">Next Steps</span><span class="sxs-lookup"><span data-stu-id="974a9-147">Next Steps</span></span>

<span data-ttu-id="974a9-148">Сведения о начале работы с Azure PowerShell см. в [этой статье](get-started-azureps.md). Она содержит более подробную информацию о модуле и его компонентах.</span><span class="sxs-lookup"><span data-stu-id="974a9-148">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
