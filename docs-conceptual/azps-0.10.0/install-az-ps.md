---
title: Установка Azure PowerShell с помощью PowerShellGet
description: Инструкции по установке Azure PowerShell с помощью PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/26/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 00cb5542e8d805f6e5e79e2177270fcbb93af808
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89241914"
---
# <a name="install-azure-powershell"></a><span data-ttu-id="26002-103">Установите Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="26002-103">Install Azure PowerShell</span></span>

<span data-ttu-id="26002-104">В этой статье показано, как установить модули Azure PowerShell с помощью [PowerShellGet](/powershell/scripting/gallery/installing-psget).</span><span class="sxs-lookup"><span data-stu-id="26002-104">This article explains how to install the Azure PowerShell modules using [PowerShellGet](/powershell/scripting/gallery/installing-psget).</span></span> <span data-ttu-id="26002-105">Эти инструкции применимы для платформ Windows, macOS и Linux.</span><span class="sxs-lookup"><span data-stu-id="26002-105">These instructions work on Windows, macOS, and Linux platforms.</span></span>

<span data-ttu-id="26002-106">Среда Azure PowerShell также доступна в Azure [Cloud Shell](/azure/cloud-shell/overview).</span><span class="sxs-lookup"><span data-stu-id="26002-106">Azure PowerShell is also available in Azure [Cloud Shell](/azure/cloud-shell/overview).</span></span>

## <a name="requirements"></a><span data-ttu-id="26002-107">Требования</span><span class="sxs-lookup"><span data-stu-id="26002-107">Requirements</span></span>

<span data-ttu-id="26002-108">Azure PowerShell работает с PowerShell 5.1 или более поздней версии на платформе Windows или с PowerShell Core 6.x или более поздней версии на любых платформах.</span><span class="sxs-lookup"><span data-stu-id="26002-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="26002-109">Необходимо установить [последнюю версию PowerShell](/powershell/scripting/install/installing-powershell) для вашей операционной системы.</span><span class="sxs-lookup"><span data-stu-id="26002-109">You should install the [latest version of PowerShell](/powershell/scripting/install/installing-powershell) available for your operating system.</span></span> <span data-ttu-id="26002-110">Дополнительных требований для использования Azure PowerShell в PowerShell версии 6.2.4 и выше нет.</span><span class="sxs-lookup"><span data-stu-id="26002-110">Azure PowerShell has no additional requirements when run on PowerShell 6.2.4 and later.</span></span>

<span data-ttu-id="26002-111">Чтобы узнать вашу версию PowerShell, выполните приведенную ниже команду:</span><span class="sxs-lookup"><span data-stu-id="26002-111">To check your PowerShell version, run the command:</span></span>

```azurepowershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="26002-112">Чтобы использовать Azure PowerShell в PowerShell 5.1 в Windows, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="26002-112">To use Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="26002-113">Выполните обновление до [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="26002-113">Update to [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span></span>
   <span data-ttu-id="26002-114">Если вы используете Windows 10 версии 1607 и выше, у вас уже есть PowerShell версии 5.1.</span><span class="sxs-lookup"><span data-stu-id="26002-114">If you're on Windows 10 version 1607 or higher, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="26002-115">[Установите платформу .NET Framework версии 4.7.2 или более поздней](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="26002-115">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>
3. <span data-ttu-id="26002-116">Убедитесь, что у вас установлена последняя версия PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="26002-116">Make sure you have the latest version of PowerShellGet.</span></span> <span data-ttu-id="26002-117">Выполните `Install-Module -Name PowerShellGet -Force`.</span><span class="sxs-lookup"><span data-stu-id="26002-117">Run `Install-Module -Name PowerShellGet -Force`.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="26002-118">Установка модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="26002-118">Install the Azure PowerShell module</span></span>

> [!WARNING]
> <span data-ttu-id="26002-119">В Windows нельзя одновременно установить модули AzureRM и Az для PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="26002-119">We do not support having both the AzureRM and Az modules installed for PowerShell 5.1 on Windows at the same time.</span></span> <span data-ttu-id="26002-120">Если в системе нужно оставить модуль AzureRM, установите модуль Az для PowerShell версии 6.2.4 и выше.</span><span class="sxs-lookup"><span data-stu-id="26002-120">If you need to keep AzureRM available on your system, install the Az module for PowerShell 6.2.4 or later.</span></span>

<span data-ttu-id="26002-121">Использование командлетов PowerShellGet — предпочтительный метод установки.</span><span class="sxs-lookup"><span data-stu-id="26002-121">Using the PowerShellGet cmdlets is the preferred installation method.</span></span> <span data-ttu-id="26002-122">Установите модуль Az только для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="26002-122">Install the Az module for the current user only.</span></span> <span data-ttu-id="26002-123">Это рекомендуемая область установки.</span><span class="sxs-lookup"><span data-stu-id="26002-123">This is the recommended installation scope.</span></span> <span data-ttu-id="26002-124">Этот метод работает одинаково на платформах Windows, macOS и Linux.</span><span class="sxs-lookup"><span data-stu-id="26002-124">This method works the same on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="26002-125">Выполните следующую команду из сеанса PowerShell:</span><span class="sxs-lookup"><span data-stu-id="26002-125">Run the following command from a PowerShell session:</span></span>

```powershell-interactive
if (Get-Module -Name AzureRM -ListAvailable) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope CurrentUser
}
```

<span data-ttu-id="26002-126">По умолчанию коллекция PowerShell не используется как доверенный репозиторий для PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="26002-126">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="26002-127">При первом использовании PSGallery отображается следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="26002-127">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="26002-128">Ответьте `Yes` или `Yes to All`, чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="26002-128">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="26002-129">Для установки модуля для всех пользователей системы требуются повышенные права.</span><span class="sxs-lookup"><span data-stu-id="26002-129">Installing the module for all users on a system requires elevated privileges.</span></span> <span data-ttu-id="26002-130">Запустите сеанс PowerShell **от имени администратора** в Windows либо выполните команду `sudo` в macOS или Linux:</span><span class="sxs-lookup"><span data-stu-id="26002-130">Start the PowerShell session using **Run as administrator** in Windows or use the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
if (Get-Module -Name AzureRM -ListAvailable) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope AllUsers
}
```

<span data-ttu-id="26002-131">Модуль Az — это общий модуль для командлетов Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="26002-131">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="26002-132">Во время его установки скачиваются все общедоступные модули Az PowerShell, а после этого становятся доступными все соответствующие командлеты.</span><span class="sxs-lookup"><span data-stu-id="26002-132">Installing it downloads all of the generally available Az PowerShell modules, and makes their cmdlets available for use.</span></span>

## <a name="install-offline"></a><span data-ttu-id="26002-133">Установка в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="26002-133">Install offline</span></span>

<span data-ttu-id="26002-134">В некоторых средах невозможно подключиться к коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="26002-134">In some environments, it's not possible to connect to the PowerShell Gallery.</span></span> <span data-ttu-id="26002-135">В таких случаях все же можно выполнить установку в автономном режиме, используя один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="26002-135">In those situations, you can still install offline using one of these methods:</span></span>

* <span data-ttu-id="26002-136">Скачайте модули в другое сетевое расположение и используйте его в качестве источника установки.</span><span class="sxs-lookup"><span data-stu-id="26002-136">Download the modules to another location in your network and use that as an installation source.</span></span>
  <span data-ttu-id="26002-137">Так вы сможете кэшировать модули PowerShell на отдельном сервере или в общей папке, чтобы развернуть их с помощью PowerShellGet в любой системе в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="26002-137">This method allows you to cache PowerShell modules on a single server or file share to be deployed with PowerShellGet to any disconnected systems.</span></span> <span data-ttu-id="26002-138">Сведения о том, как настроить локальный репозиторий и установить его в системах без подключения к сети, см. в статье [Работа с локальными хранилищами PowerShellGet](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span><span class="sxs-lookup"><span data-stu-id="26002-138">Learn how to set up a local repository and install on disconnected systems with [Working with local PowerShellGet repositories](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span></span>
* <span data-ttu-id="26002-139">[Скачайте MSI для Azure PowerShell](install-az-ps-msi.md) на компьютер, подключенный к сети, а затем скопируйте установщик в системы без доступа к коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="26002-139">[Download the Azure PowerShell MSI](install-az-ps-msi.md) to a machine connected to the network, and then copy the installer to systems without access to PowerShell Gallery.</span></span> <span data-ttu-id="26002-140">Помните, что установщик MSI работает только с PowerShell 5.1 в Windows.</span><span class="sxs-lookup"><span data-stu-id="26002-140">Keep in mind that the MSI installer only works for PowerShell 5.1 on Windows.</span></span>
* <span data-ttu-id="26002-141">С помощью команды [Save-Module](/powershell/module/PowershellGet/Save-Module) сохраните модуль в общую папку или в другом источнике и вручную скопируйте на другие компьютеры.</span><span class="sxs-lookup"><span data-stu-id="26002-141">Save the module with [Save-Module](/powershell/module/PowershellGet/Save-Module) to a file share, or save it to another source and manually copy it to other machines:</span></span>

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a><span data-ttu-id="26002-142">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="26002-142">Troubleshooting</span></span>

<span data-ttu-id="26002-143">Ниже описаны некоторые распространенные проблемы с установкой модуля Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="26002-143">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="26002-144">Если у вас возникла проблема, не описанная здесь, [сообщите о ней на сайте GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="26002-144">If you experience a problem not listed here, [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="26002-145">Прокси-сервер блокирует подключения</span><span class="sxs-lookup"><span data-stu-id="26002-145">Proxy blocks connection</span></span>

<span data-ttu-id="26002-146">Если командлет `Install-Module` возвращает ошибки о том, что коллекция PowerShell недоступна, возможно, ваша система находится за прокси-сервером.</span><span class="sxs-lookup"><span data-stu-id="26002-146">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="26002-147">Разные операционные системы и сетевые среды имеют разные требования для настройки прокси-сервера на уровне системы.</span><span class="sxs-lookup"><span data-stu-id="26002-147">Different operating systems and network environment have different requirements for configuring a system-wide proxy.</span></span> <span data-ttu-id="26002-148">Обратитесь к системному администратору, чтобы узнать о параметрах своего прокси-сервера и о том, как настроить их для своей среды.</span><span class="sxs-lookup"><span data-stu-id="26002-148">Contact your system administrator for your proxy settings and how to configure them for your environment.</span></span>

<span data-ttu-id="26002-149">Возможно, среду PowerShell нельзя настроить для автоматического использования этого прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="26002-149">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="26002-150">В PowerShell 5.1 и более поздних версий настройте сеанс PowerShell для использования прокси-сервера с помощью следующих команд:</span><span class="sxs-lookup"><span data-stu-id="26002-150">With PowerShell 5.1 and later, configure the PowerShell session to use a proxy using the following commands:</span></span>

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="26002-151">Если учетные данные операционной системы настроены правильно, конфигурация будет направлять запросы PowerShell через прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="26002-151">If your operating system credentials are configured correctly, this configuration routes PowerShell requests through the proxy.</span></span> <span data-ttu-id="26002-152">Чтобы такое поведение сохранялось между сеансами, добавьте команду в [профиль PowerShell](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="26002-152">To have this setting persist between sessions, add the commands to your [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="26002-153">Для установки пакета ваш прокси-сервер должен разрешать HTTPS-подключения по следующему адресу:</span><span class="sxs-lookup"><span data-stu-id="26002-153">To install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="26002-154">Вход</span><span class="sxs-lookup"><span data-stu-id="26002-154">Sign in</span></span>

<span data-ttu-id="26002-155">Чтобы начать работу с Azure PowerShell, выполните вход, используя данные своей учетной записи в Azure.</span><span class="sxs-lookup"><span data-stu-id="26002-155">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="26002-156">Если вы отключили автоматическую загрузку модулей, вручную импортируйте модуль с помощью `Import-Module -Name Az`.</span><span class="sxs-lookup"><span data-stu-id="26002-156">If you've disabled module autoloading, manually import the module with `Import-Module -Name Az`.</span></span>
> <span data-ttu-id="26002-157">Из-за структуры модуля эта операция может занять несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="26002-157">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="26002-158">Эти действия нужно повторять для каждого нового сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="26002-158">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="26002-159">См. сведения в статье [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="26002-159">To learn how to persist your Azure sign in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="26002-160">Обновление модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="26002-160">Update the Azure PowerShell module</span></span>

<span data-ttu-id="26002-161">Для обновления любого модуля PowerShell следует использовать тот же метод, который использовался для установки модуля.</span><span class="sxs-lookup"><span data-stu-id="26002-161">To update any PowerShell module, you should use the same method used to install the module.</span></span> <span data-ttu-id="26002-162">Например, если вы изначально использовали `Install-Module`, для получения последней версии следует использовать командлет [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="26002-162">For example, if you originally used `Install-Module`, then you should use [Update-Module](/powershell/module/powershellget/update-module) to get the latest version.</span></span> <span data-ttu-id="26002-163">Если вы изначально использовали пакет MSI, необходимо скачать и установить новый пакет MSI.</span><span class="sxs-lookup"><span data-stu-id="26002-163">If you originally used the MSI package then you should download and install the new MSI package.</span></span>

<span data-ttu-id="26002-164">Командлеты PowerShellGet не могут обновлять модули, установленные из пакета MSI.</span><span class="sxs-lookup"><span data-stu-id="26002-164">The PowerShellGet cmdlets cannot update modules that were installed from an MSI package.</span></span> <span data-ttu-id="26002-165">Пакеты MSI не обновляют модули, установленные с помощью PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="26002-165">MSI packages do not update modules that were installed using PowerShellGet.</span></span> <span data-ttu-id="26002-166">Если у вас возникли проблемы с обновлением с помощью модуля PowerShellGet, необходимо выполнить **повторную установку**, а не просто **обновление**.</span><span class="sxs-lookup"><span data-stu-id="26002-166">If you have any issues updating using PowershellGet, then you should **reinstall**, rather than **update**.</span></span> <span data-ttu-id="26002-167">Повторная установка выполняется так же, как и первоначальная, но необходимо добавить параметр `-Force`:</span><span class="sxs-lookup"><span data-stu-id="26002-167">Reinstalling is done the same way as installing, but you need to add the `-Force` parameter:</span></span>

```powershell
if (Get-Module -Name AzureRM -ListAvailable) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Force
}
```

<span data-ttu-id="26002-168">В отличие от установки с помощью MSI, при установке или обновлении с помощью PowerShellGet не удаляются более старые версии, которые могут существовать в вашей системе.</span><span class="sxs-lookup"><span data-stu-id="26002-168">Unlike MSI-based installations, installing or updating using PowerShellGet does not remove older versions that may exist on your system.</span></span> <span data-ttu-id="26002-169">См. сведения об [удалении из системы предыдущих версий модуля Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="26002-169">To remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span> <span data-ttu-id="26002-170">См. сведения об [установке Azure PowerShell с помощью MSI](install-az-ps-msi.md).</span><span class="sxs-lookup"><span data-stu-id="26002-170">For more information about MSI-based installations, see [Install Azure PowerShell with an MSI](install-az-ps-msi.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="26002-171">Использование нескольких версий Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="26002-171">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="26002-172">Вы можете установить несколько версий Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="26002-172">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="26002-173">Чтобы проверить наличие нескольких установленных версий Azure PowerShell, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="26002-173">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | Select-Object -Property Name, Version
```

<span data-ttu-id="26002-174">Сведения о том, как удалить версию Azure PowerShell, см. в статье [Удаление модуля Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="26002-174">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="26002-175">Если у вас установлено несколько версий модуля, модуль автозагрузки и `Import-Module` загрузит последнюю версию по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="26002-175">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

<span data-ttu-id="26002-176">Определенную версию модуля `Az` можно установить или загрузить с помощью параметра `-RequiredVersion`:</span><span class="sxs-lookup"><span data-stu-id="26002-176">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` parameter:</span></span>

```powershell-interactive
# Install Az version 3.6.1
Install-Module -Name Az -RequiredVersion 3.6.1
# Load Az version 3.6.1
Import-Module -Name Az -RequiredVersion 3.6.1
```

## <a name="provide-feedback"></a><span data-ttu-id="26002-177">Отзывы</span><span class="sxs-lookup"><span data-stu-id="26002-177">Provide feedback</span></span>

<span data-ttu-id="26002-178">Если вы нашли ошибку при работе с Azure PowerShell, [сообщите о проблеме на GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="26002-178">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="26002-179">Чтобы отправить отзыв из командной строки, используйте командлет [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="26002-179">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="26002-180">Next Steps</span><span class="sxs-lookup"><span data-stu-id="26002-180">Next Steps</span></span>

<span data-ttu-id="26002-181">Дополнительные сведения о модулях Azure PowerShell и их функциях см. в статье [Get Started with Azure PowerShell](get-started-azureps.md) (Начало работы с Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="26002-181">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="26002-182">Если вы знакомы с Azure PowerShell и вам необходимо мигрировать из AzureRM, см. статью [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) (Миграция с AzureRM на Az).</span><span class="sxs-lookup"><span data-stu-id="26002-182">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
