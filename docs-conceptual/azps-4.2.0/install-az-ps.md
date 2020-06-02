---
title: Установка Azure PowerShell с помощью PowerShellGet
description: Инструкции по установке Azure PowerShell с помощью PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/14/2020
ms.openlocfilehash: caa0c2fbba8b8b7e07424481360a60f3da163e66
ms.sourcegitcommit: cef87acc9f2a0d296bef74f526afd2e067e8146b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/02/2020
ms.locfileid: "84299202"
---
# <a name="install-azure-powershell"></a><span data-ttu-id="33b44-103">Установите Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="33b44-103">Install Azure PowerShell</span></span>

<span data-ttu-id="33b44-104">В этой статье показано, как установить модули Azure PowerShell с помощью [PowerShellGet](/powershell/scripting/gallery/installing-psget).</span><span class="sxs-lookup"><span data-stu-id="33b44-104">This article explains how to install the Azure PowerShell modules using [PowerShellGet](/powershell/scripting/gallery/installing-psget).</span></span> <span data-ttu-id="33b44-105">Эти инструкции применимы для платформ Windows, macOS и Linux.</span><span class="sxs-lookup"><span data-stu-id="33b44-105">These instructions work on Windows, macOS, and Linux platforms.</span></span>

<span data-ttu-id="33b44-106">Azure PowerShell также предоставляется в Azure [Cloud Shell](/azure/cloud-shell/overview) и предустанавливается в [образах Docker](azureps-in-docker.md).</span><span class="sxs-lookup"><span data-stu-id="33b44-106">Azure PowerShell is also available in Azure [Cloud Shell](/azure/cloud-shell/overview) and is now preinstalled in [Docker images](azureps-in-docker.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="33b44-107">Требования</span><span class="sxs-lookup"><span data-stu-id="33b44-107">Requirements</span></span>

> [!NOTE]
> <span data-ttu-id="33b44-108">Для работы в Azure PowerShell на всех платформах мы рекомендуем использовать PowerShell версии 7.x и выше.</span><span class="sxs-lookup"><span data-stu-id="33b44-108">PowerShell 7.x and later is the recommended version of PowerShell for use with Azure PowerShell on all platforms.</span></span>

<span data-ttu-id="33b44-109">Azure PowerShell работает с PowerShell версии 6.2.4 и выше на любой платформе.</span><span class="sxs-lookup"><span data-stu-id="33b44-109">Azure PowerShell works with PowerShell 6.2.4 and later on all platforms.</span></span> <span data-ttu-id="33b44-110">Кроме того, в Windows также поддерживается использование в PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="33b44-110">It is also supported with PowerShell 5.1 on Windows.</span></span> <span data-ttu-id="33b44-111">Установите [последнюю версию PowerShell](/powershell/scripting/install/installing-powershell) для своей операционной системы.</span><span class="sxs-lookup"><span data-stu-id="33b44-111">Install the [latest version of PowerShell](/powershell/scripting/install/installing-powershell) available for your operating system.</span></span> <span data-ttu-id="33b44-112">Дополнительных требований для использования Azure PowerShell в PowerShell версии 6.2.4 и выше нет.</span><span class="sxs-lookup"><span data-stu-id="33b44-112">Azure PowerShell has no additional requirements when run on PowerShell 6.2.4 and later.</span></span>

<span data-ttu-id="33b44-113">Чтобы узнать вашу версию PowerShell, выполните приведенную ниже команду:</span><span class="sxs-lookup"><span data-stu-id="33b44-113">To check your PowerShell version, run the command:</span></span>

```azurepowershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="33b44-114">Чтобы использовать Azure PowerShell в PowerShell 5.1 в Windows, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="33b44-114">To use Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="33b44-115">Выполните обновление до [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="33b44-115">Update to [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span></span>
   <span data-ttu-id="33b44-116">Если вы используете Windows 10 версии 1607 и выше, у вас уже есть PowerShell версии 5.1.</span><span class="sxs-lookup"><span data-stu-id="33b44-116">If you're on Windows 10 version 1607 or higher, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="33b44-117">[Установите платформу .NET Framework версии 4.7.2 или более поздней](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="33b44-117">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>
3. <span data-ttu-id="33b44-118">Убедитесь, что у вас установлена последняя версия PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="33b44-118">Make sure you have the latest version of PowerShellGet.</span></span> <span data-ttu-id="33b44-119">Выполните `Install-Module -Name PowerShellGet -Force`.</span><span class="sxs-lookup"><span data-stu-id="33b44-119">Run `Install-Module -Name PowerShellGet -Force`.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="33b44-120">Установка модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="33b44-120">Install the Azure PowerShell module</span></span>

> [!WARNING]
> <span data-ttu-id="33b44-121">В Windows нельзя одновременно установить модули AzureRM и Az для PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="33b44-121">We do not support having both the AzureRM and Az modules installed for PowerShell 5.1 on Windows at the same time.</span></span> <span data-ttu-id="33b44-122">Если в системе нужно оставить модуль AzureRM, установите модуль Az для PowerShell версии 6.2.4 и выше.</span><span class="sxs-lookup"><span data-stu-id="33b44-122">If you need to keep AzureRM available on your system, install the Az module for PowerShell 6.2.4 or later.</span></span>

<span data-ttu-id="33b44-123">Использование командлетов PowerShellGet — предпочтительный метод установки.</span><span class="sxs-lookup"><span data-stu-id="33b44-123">Using the PowerShellGet cmdlets is the preferred installation method.</span></span> <span data-ttu-id="33b44-124">Установите модуль Az только для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="33b44-124">Install the Az module for the current user only.</span></span> <span data-ttu-id="33b44-125">Это рекомендуемая область установки.</span><span class="sxs-lookup"><span data-stu-id="33b44-125">This is the recommended installation scope.</span></span> <span data-ttu-id="33b44-126">Этот метод работает одинаково на платформах Windows, macOS и Linux.</span><span class="sxs-lookup"><span data-stu-id="33b44-126">This method works the same on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="33b44-127">Выполните следующую команду из сеанса PowerShell:</span><span class="sxs-lookup"><span data-stu-id="33b44-127">Run the following command from a PowerShell session:</span></span>

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope CurrentUser
}
```

<span data-ttu-id="33b44-128">По умолчанию коллекция PowerShell не используется как доверенный репозиторий для PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="33b44-128">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="33b44-129">При первом использовании PSGallery отображается следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="33b44-129">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="33b44-130">Ответьте `Yes` или `Yes to All`, чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="33b44-130">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="33b44-131">Для установки модуля для всех пользователей системы требуются повышенные права.</span><span class="sxs-lookup"><span data-stu-id="33b44-131">Installing the module for all users on a system requires elevated privileges.</span></span> <span data-ttu-id="33b44-132">Запустите сеанс PowerShell **от имени администратора** в Windows либо выполните команду `sudo` в macOS или Linux:</span><span class="sxs-lookup"><span data-stu-id="33b44-132">Start the PowerShell session using **Run as administrator** in Windows or use the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope AllUsers
}
```

<span data-ttu-id="33b44-133">Модуль Az — это общий модуль для командлетов Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="33b44-133">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="33b44-134">Во время его установки скачиваются все общедоступные модули Az PowerShell, а после этого становятся доступными все соответствующие командлеты.</span><span class="sxs-lookup"><span data-stu-id="33b44-134">Installing it downloads all of the generally available Az PowerShell modules, and makes their cmdlets available for use.</span></span>

## <a name="install-offline"></a><span data-ttu-id="33b44-135">Установка в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="33b44-135">Install offline</span></span>

<span data-ttu-id="33b44-136">В некоторых средах невозможно подключиться к коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="33b44-136">In some environments, it's not possible to connect to the PowerShell Gallery.</span></span> <span data-ttu-id="33b44-137">В таких случаях все же можно выполнить установку в автономном режиме, используя один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="33b44-137">In those situations, you can still install offline using one of these methods:</span></span>

* <span data-ttu-id="33b44-138">Скачайте модули в другое сетевое расположение и используйте его в качестве источника установки.</span><span class="sxs-lookup"><span data-stu-id="33b44-138">Download the modules to another location in your network and use that as an installation source.</span></span>
  <span data-ttu-id="33b44-139">Так вы сможете кэшировать модули PowerShell на отдельном сервере или в общей папке, чтобы развернуть их с помощью PowerShellGet в любой системе в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="33b44-139">This method allows you to cache PowerShell modules on a single server or file share to be deployed with PowerShellGet to any disconnected systems.</span></span> <span data-ttu-id="33b44-140">Сведения о том, как настроить локальный репозиторий и установить его в системах без подключения к сети, см. в статье [Работа с локальными хранилищами PowerShellGet](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span><span class="sxs-lookup"><span data-stu-id="33b44-140">Learn how to set up a local repository and install on disconnected systems with [Working with local PowerShellGet repositories](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span></span>
* <span data-ttu-id="33b44-141">[Скачайте MSI для Azure PowerShell](install-az-ps-msi.md) на компьютер, подключенный к сети, а затем скопируйте установщик в системы без доступа к коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="33b44-141">[Download the Azure PowerShell MSI](install-az-ps-msi.md) to a machine connected to the network, and then copy the installer to systems without access to PowerShell Gallery.</span></span> <span data-ttu-id="33b44-142">Помните, что установщик MSI работает только с PowerShell 5.1 в Windows.</span><span class="sxs-lookup"><span data-stu-id="33b44-142">Keep in mind that the MSI installer only works for PowerShell 5.1 on Windows.</span></span>
* <span data-ttu-id="33b44-143">С помощью команды [Save-Module](/powershell/module/PowershellGet/Save-Module) сохраните модуль в общую папку или в другом источнике и вручную скопируйте на другие компьютеры.</span><span class="sxs-lookup"><span data-stu-id="33b44-143">Save the module with [Save-Module](/powershell/module/PowershellGet/Save-Module) to a file share, or save it to another source and manually copy it to other machines:</span></span>

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a><span data-ttu-id="33b44-144">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="33b44-144">Troubleshooting</span></span>

<span data-ttu-id="33b44-145">Ниже описаны некоторые распространенные проблемы с установкой модуля Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="33b44-145">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="33b44-146">Если у вас возникла проблема, не описанная здесь, [сообщите о ней на сайте GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="33b44-146">If you experience a problem not listed here, [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="33b44-147">Прокси-сервер блокирует подключения</span><span class="sxs-lookup"><span data-stu-id="33b44-147">Proxy blocks connection</span></span>

<span data-ttu-id="33b44-148">Если командлет `Install-Module` возвращает ошибки о том, что коллекция PowerShell недоступна, возможно, ваша система находится за прокси-сервером.</span><span class="sxs-lookup"><span data-stu-id="33b44-148">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="33b44-149">Разные операционные системы и сетевые среды имеют разные требования для настройки прокси-сервера на уровне системы.</span><span class="sxs-lookup"><span data-stu-id="33b44-149">Different operating systems and network environment have different requirements for configuring a system-wide proxy.</span></span> <span data-ttu-id="33b44-150">Обратитесь к системному администратору, чтобы узнать о параметрах своего прокси-сервера и о том, как настроить их для своей среды.</span><span class="sxs-lookup"><span data-stu-id="33b44-150">Contact your system administrator for your proxy settings and how to configure them for your environment.</span></span>

<span data-ttu-id="33b44-151">Возможно, среду PowerShell нельзя настроить для автоматического использования этого прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="33b44-151">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="33b44-152">В PowerShell 5.1 и более поздних версий настройте сеанс PowerShell для использования прокси-сервера с помощью следующих команд:</span><span class="sxs-lookup"><span data-stu-id="33b44-152">With PowerShell 5.1 and later, configure the PowerShell session to use a proxy using the following commands:</span></span>

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="33b44-153">Если учетные данные операционной системы настроены правильно, конфигурация будет направлять запросы PowerShell через прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="33b44-153">If your operating system credentials are configured correctly, this configuration routes PowerShell requests through the proxy.</span></span> <span data-ttu-id="33b44-154">Чтобы такое поведение сохранялось между сеансами, добавьте команду в [профиль PowerShell](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="33b44-154">To have this setting persist between sessions, add the commands to your [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="33b44-155">Для установки пакета ваш прокси-сервер должен разрешать HTTPS-подключения по следующему адресу:</span><span class="sxs-lookup"><span data-stu-id="33b44-155">To install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="33b44-156">Вход</span><span class="sxs-lookup"><span data-stu-id="33b44-156">Sign in</span></span>

<span data-ttu-id="33b44-157">Чтобы начать работу с Azure PowerShell, выполните вход, используя данные своей учетной записи в Azure.</span><span class="sxs-lookup"><span data-stu-id="33b44-157">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="33b44-158">Если вы отключили автоматическую загрузку модулей, вручную импортируйте модуль с помощью `Import-Module -Name Az`.</span><span class="sxs-lookup"><span data-stu-id="33b44-158">If you've disabled module autoloading, manually import the module with `Import-Module -Name Az`.</span></span>
> <span data-ttu-id="33b44-159">Из-за структуры модуля эта операция может занять несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="33b44-159">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="33b44-160">Эти действия нужно повторять для каждого нового сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="33b44-160">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="33b44-161">См. сведения в статье [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="33b44-161">To learn how to persist your Azure sign in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="33b44-162">Обновление модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="33b44-162">Update the Azure PowerShell module</span></span>

<span data-ttu-id="33b44-163">Для обновления любого модуля PowerShell следует использовать тот же метод, который использовался для установки модуля.</span><span class="sxs-lookup"><span data-stu-id="33b44-163">To update any PowerShell module, you should use the same method used to install the module.</span></span> <span data-ttu-id="33b44-164">Например, если вы изначально использовали `Install-Module`, для получения последней версии следует использовать командлет [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="33b44-164">For example, if you originally used `Install-Module`, then you should use [Update-Module](/powershell/module/powershellget/update-module) to get the latest version.</span></span> <span data-ttu-id="33b44-165">Если вы изначально использовали пакет MSI, необходимо скачать и установить новый пакет MSI.</span><span class="sxs-lookup"><span data-stu-id="33b44-165">If you originally used the MSI package then you should download and install the new MSI package.</span></span>

<span data-ttu-id="33b44-166">Командлеты PowerShellGet не могут обновлять модули, установленные из пакета MSI.</span><span class="sxs-lookup"><span data-stu-id="33b44-166">The PowerShellGet cmdlets cannot update modules that were installed from an MSI package.</span></span> <span data-ttu-id="33b44-167">Пакеты MSI не обновляют модули, установленные с помощью PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="33b44-167">MSI packages do not update modules that were installed using PowerShellGet.</span></span> <span data-ttu-id="33b44-168">Если у вас возникли проблемы с обновлением с помощью модуля PowerShellGet, необходимо выполнить **повторную установку**, а не просто **обновление**.</span><span class="sxs-lookup"><span data-stu-id="33b44-168">If you have any issues updating using PowershellGet, then you should **reinstall**, rather than **update**.</span></span> <span data-ttu-id="33b44-169">Повторная установка выполняется так же, как и первоначальная, но необходимо добавить параметр `-Force`:</span><span class="sxs-lookup"><span data-stu-id="33b44-169">Reinstalling is done the same way as installing, but you need to add the `-Force` parameter:</span></span>

```powershell
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Force
}
```

<span data-ttu-id="33b44-170">В отличие от установки с помощью MSI, при установке или обновлении с помощью PowerShellGet не удаляются более старые версии, которые могут существовать в вашей системе.</span><span class="sxs-lookup"><span data-stu-id="33b44-170">Unlike MSI-based installations, installing or updating using PowerShellGet does not remove older versions that may exist on your system.</span></span> <span data-ttu-id="33b44-171">См. сведения об [удалении из системы предыдущих версий модуля Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="33b44-171">To remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span> <span data-ttu-id="33b44-172">См. сведения об [установке Azure PowerShell с помощью MSI](install-az-ps-msi.md).</span><span class="sxs-lookup"><span data-stu-id="33b44-172">For more information about MSI-based installations, see [Install Azure PowerShell with an MSI](install-az-ps-msi.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="33b44-173">Использование нескольких версий Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="33b44-173">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="33b44-174">Вы можете установить несколько версий Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="33b44-174">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="33b44-175">Чтобы проверить наличие нескольких установленных версий Azure PowerShell, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="33b44-175">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | Select-Object -Property Name, Version
```

<span data-ttu-id="33b44-176">Сведения о том, как удалить версию Azure PowerShell, см. в статье [Удаление модуля Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="33b44-176">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="33b44-177">Если у вас установлено несколько версий модуля, модуль автозагрузки и `Import-Module` загрузит последнюю версию по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="33b44-177">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

<span data-ttu-id="33b44-178">Определенную версию модуля `Az` можно установить или загрузить с помощью параметра `-RequiredVersion`.</span><span class="sxs-lookup"><span data-stu-id="33b44-178">You can install or load a specific version of the `Az` module using the `-RequiredVersion` parameter:</span></span>

```powershell-interactive
# Install Az version 3.6.1
Install-Module -Name Az -RequiredVersion 3.6.1
# Load Az version 3.6.1
Import-Module -Name Az -RequiredVersion 3.6.1
```

## <a name="use-multiple-repositories-with-powershellget"></a><span data-ttu-id="33b44-179">Использование нескольких репозиториев с PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="33b44-179">Use multiple repositories with PowerShellGet</span></span>

<span data-ttu-id="33b44-180">Параметр **Repository** является обязательным, если вы добавили дополнительные репозитории в PowerShellGet в системе и модуль Az можно найти более чем в одном из них.</span><span class="sxs-lookup"><span data-stu-id="33b44-180">The **Repository** parameter is required if you have added additional repositories to PowerShellGet on your system and the Az module can be found in more than one of them.</span></span>

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message 'Az module not installed. Having both the AzureRM and Az modules installed at the same time is not supported.'
} else {
    Install-Module -Name Az -Repository PSGallery -AllowClobber -Force
}
```

## <a name="provide-feedback"></a><span data-ttu-id="33b44-181">Отзывы</span><span class="sxs-lookup"><span data-stu-id="33b44-181">Provide feedback</span></span>

<span data-ttu-id="33b44-182">Если вы нашли ошибку при работе с Azure PowerShell, [сообщите о проблеме на GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="33b44-182">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="33b44-183">Чтобы отправить отзыв из командной строки, используйте командлет [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="33b44-183">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="33b44-184">Next Steps</span><span class="sxs-lookup"><span data-stu-id="33b44-184">Next Steps</span></span>

<span data-ttu-id="33b44-185">Дополнительные сведения о модулях Azure PowerShell и их функциях см. в статье [Get Started with Azure PowerShell](get-started-azureps.md) (Начало работы с Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="33b44-185">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="33b44-186">Если вы знакомы с Azure PowerShell и вам необходимо мигрировать из AzureRM, см. статью [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) (Миграция с AzureRM на Az).</span><span class="sxs-lookup"><span data-stu-id="33b44-186">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
