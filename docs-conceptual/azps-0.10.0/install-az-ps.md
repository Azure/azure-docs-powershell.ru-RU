---
title: Установка Azure PowerShell с помощью PowerShellGet
description: Инструкции по установке Azure PowerShell с помощью PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/26/2020
ms.openlocfilehash: 7a25270566f5e856ee44c4c191a47a3e7334508b
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/05/2020
ms.locfileid: "81445702"
---
# <a name="install-azure-powershell"></a><span data-ttu-id="40fd0-103">Установите Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="40fd0-103">Install Azure PowerShell</span></span>

<span data-ttu-id="40fd0-104">В этой статье показано, как установить модули Azure PowerShell с помощью PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="40fd0-104">This article explains how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="40fd0-105">Эти инструкции применимы для платформ Windows, macOS и Linux.</span><span class="sxs-lookup"><span data-stu-id="40fd0-105">These instructions work on Windows, macOS, and Linux platforms.</span></span>

<span data-ttu-id="40fd0-106">Azure PowerShell также предоставляется в Azure [Cloud Shell](/azure/cloud-shell/overview) и предустанавливается в [образах Docker](azureps-in-docker.md).</span><span class="sxs-lookup"><span data-stu-id="40fd0-106">Azure PowerShell is also available in Azure [Cloud Shell](/azure/cloud-shell/overview) and is now preinstalled in [Docker images](azureps-in-docker.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="40fd0-107">Требования</span><span class="sxs-lookup"><span data-stu-id="40fd0-107">Requirements</span></span>

<span data-ttu-id="40fd0-108">Azure PowerShell работает с PowerShell 5.1 или более поздней версии на платформе Windows или с PowerShell Core 6.x или более поздней версии на любых платформах.</span><span class="sxs-lookup"><span data-stu-id="40fd0-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="40fd0-109">Необходимо установить [последнюю версию PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core) для вашей операционной системы.</span><span class="sxs-lookup"><span data-stu-id="40fd0-109">You should install the [latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core) available for your operating system.</span></span> <span data-ttu-id="40fd0-110">Дополнительных требований для использования Azure PowerShell в PowerShell Core нет.</span><span class="sxs-lookup"><span data-stu-id="40fd0-110">Azure PowerShell has no additional requirements when run on PowerShell Core.</span></span>

<span data-ttu-id="40fd0-111">Чтобы узнать вашу версию PowerShell, выполните приведенную ниже команду:</span><span class="sxs-lookup"><span data-stu-id="40fd0-111">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="40fd0-112">Чтобы использовать Azure PowerShell в PowerShell 5.1 в Windows, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="40fd0-112">To use Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="40fd0-113">При необходимости выполните обновление до [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="40fd0-113">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="40fd0-114">Если вы используете Windows 10, среда PowerShell 5.1 уже установлена.</span><span class="sxs-lookup"><span data-stu-id="40fd0-114">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="40fd0-115">[Установите платформу .NET Framework версии 4.7.2 или более поздней](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="40fd0-115">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>
3. <span data-ttu-id="40fd0-116">Убедитесь, что у вас установлена последняя версия PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="40fd0-116">Make sure you have the latest version of PowerShellGet.</span></span> <span data-ttu-id="40fd0-117">Выполните `Update-Module PowerShellGet -Force`.</span><span class="sxs-lookup"><span data-stu-id="40fd0-117">Run `Update-Module PowerShellGet -Force`.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="40fd0-118">Установка модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="40fd0-118">Install the Azure PowerShell module</span></span>

<span data-ttu-id="40fd0-119">Использование командлетов PowerShellGet является предпочтительным методом установки.</span><span class="sxs-lookup"><span data-stu-id="40fd0-119">Using the PowerShellGet cmdlets is the preferred installation method.</span></span> <span data-ttu-id="40fd0-120">Этот метод работает одинаково на платформах Windows, macOS и Linux.</span><span class="sxs-lookup"><span data-stu-id="40fd0-120">This method works the same on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="40fd0-121">Выполните следующую команду из сеанса PowerShell:</span><span class="sxs-lookup"><span data-stu-id="40fd0-121">Run the following command from a PowerShell session:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="40fd0-122">По умолчанию коллекция PowerShell не используется как доверенный репозиторий для PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="40fd0-122">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="40fd0-123">При первом использовании PSGallery отображается следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="40fd0-123">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="40fd0-124">Ответьте `Yes` или `Yes to All`, чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="40fd0-124">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="40fd0-125">Модуль Az — это общий модуль для командлетов Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="40fd0-125">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="40fd0-126">Во время его установки скачиваются все доступные модули Azure Resource Manager и устанавливаются все соответствующие командлеты.</span><span class="sxs-lookup"><span data-stu-id="40fd0-126">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

> [!WARNING]
> <span data-ttu-id="40fd0-127">Для PowerShell 5.1 в Windows нельзя одновременно установить модули AzureRM и Az.</span><span class="sxs-lookup"><span data-stu-id="40fd0-127">We do not support having both the AzureRM and Az modules installed for PowerShell 5.1 for Windows at the same time.</span></span> <span data-ttu-id="40fd0-128">Если в системе нужно оставить модуль AzureRM, установите модуль Az для PowerShell Core версии 6.x или более поздней.</span><span class="sxs-lookup"><span data-stu-id="40fd0-128">If you need to keep AzureRM available on your system, install the Az module for PowerShell Core 6.x or later.</span></span>

<span data-ttu-id="40fd0-129">Во-первых, [скачайте и установите PowerShell Core 6.x или более поздней версии](/powershell/scripting/install/installing-powershell-core-on-windows).</span><span class="sxs-lookup"><span data-stu-id="40fd0-129">First, [install PowerShell Core 6.x or later](/powershell/scripting/install/installing-powershell-core-on-windows)</span></span>

<span data-ttu-id="40fd0-130">Затем из сеанса PowerShell Core установите модуль Az только для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="40fd0-130">Then, from a PowerShell Core session, install the Az module for the current user only.</span></span> <span data-ttu-id="40fd0-131">Это рекомендуемая область установки.</span><span class="sxs-lookup"><span data-stu-id="40fd0-131">This is the recommended installation scope.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="40fd0-132">Для установки модуля для всех пользователей системы требуются повышенные права.</span><span class="sxs-lookup"><span data-stu-id="40fd0-132">Installing the module for all users on a system requires elevated privileges.</span></span> <span data-ttu-id="40fd0-133">Запустите сеанс PowerShell **от имени администратора** в Windows или используйте команду `sudo` в macOS или Linux:</span><span class="sxs-lookup"><span data-stu-id="40fd0-133">Start the PowerShell session using **Run as administrator** in Windows or use the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

## <a name="install-offline"></a><span data-ttu-id="40fd0-134">Установка в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="40fd0-134">Install offline</span></span>

<span data-ttu-id="40fd0-135">В некоторых средах невозможно подключиться к коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="40fd0-135">In some environments it's not possible to connect to the PowerShell Gallery.</span></span> <span data-ttu-id="40fd0-136">В таких случаях все же можно выполнить установку в автономном режиме, используя один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="40fd0-136">In those situations, you can still install offline using one of these methods:</span></span>

* <span data-ttu-id="40fd0-137">Скачайте модули в другое сетевое расположение и используйте его в качестве источника установки.</span><span class="sxs-lookup"><span data-stu-id="40fd0-137">Download the modules to another location in your network and use that as an installation source.</span></span>
  <span data-ttu-id="40fd0-138">Так вы сможете кэшировать модули PowerShell на отдельном сервере или в общей папке, чтобы развернуть их с помощью PowerShellGet в любой системе без подключения к сети.</span><span class="sxs-lookup"><span data-stu-id="40fd0-138">This allows you to cache PowerShell modules on a single server or file share to be deployed with PowerShellGet to any disconnected systems.</span></span> <span data-ttu-id="40fd0-139">Сведения о том, как настроить локальный репозиторий и установить его в системах без подключения к сети, см. в статье [Работа с локальными хранилищами PowerShellGet](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span><span class="sxs-lookup"><span data-stu-id="40fd0-139">Learn how to set up a local repository and install on disconnected systems with [Working with local PowerShellGet repositories](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span></span>
* <span data-ttu-id="40fd0-140">[Скачайте MSI для Azure PowerShell](install-az-ps-msi.md) на компьютер, подключенный к сети, а затем скопируйте установщик в системы без доступа к коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="40fd0-140">[Download the Azure PowerShell MSI](install-az-ps-msi.md) to a machine connected to the network, and then copy the installer to systems without access to PowerShell Gallery.</span></span> <span data-ttu-id="40fd0-141">Помните, что установщик MSI работает только с PowerShell 5.1 в Windows.</span><span class="sxs-lookup"><span data-stu-id="40fd0-141">Keep in mind that the MSI installer only works for PowerShell 5.1 on Windows.</span></span>
* <span data-ttu-id="40fd0-142">С помощью команды [Save-Module](/powershell/module/PowershellGet/Save-Module) сохраните модуль в общую папку или в другом источнике и вручную скопируйте на другие компьютеры.</span><span class="sxs-lookup"><span data-stu-id="40fd0-142">Save the module with [Save-Module](/powershell/module/PowershellGet/Save-Module) to a file share, or save it to another source and manually copy it to other machines:</span></span>

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a><span data-ttu-id="40fd0-143">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="40fd0-143">Troubleshooting</span></span>

<span data-ttu-id="40fd0-144">Ниже описаны некоторые распространенные проблемы с установкой модуля Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="40fd0-144">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="40fd0-145">Если у вас возникла проблема, не описанная здесь, [сообщите о ней на сайте GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="40fd0-145">If you experience a problem not listed here, please [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="40fd0-146">Прокси-сервер блокирует подключения</span><span class="sxs-lookup"><span data-stu-id="40fd0-146">Proxy blocks connection</span></span>

<span data-ttu-id="40fd0-147">Если командлет `Install-Module` возвращает ошибки о том, что коллекция PowerShell недоступна, возможно, ваша система находится за прокси-сервером.</span><span class="sxs-lookup"><span data-stu-id="40fd0-147">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="40fd0-148">Разные операционные системы и сетевые среды имеют разные требования для настройки прокси-сервера на уровне системы.</span><span class="sxs-lookup"><span data-stu-id="40fd0-148">Different operating systems and network environment have different requirements for configuring a system-wide proxy.</span></span> <span data-ttu-id="40fd0-149">Обратитесь к системному администратору, чтобы узнать о параметрах своего прокси-сервера и о том, как настроить их для своей среды.</span><span class="sxs-lookup"><span data-stu-id="40fd0-149">Contact your system administrator for your proxy settings and how to configure them for your environment.</span></span>

<span data-ttu-id="40fd0-150">Возможно, среду PowerShell нельзя настроить для автоматического использования этого прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="40fd0-150">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="40fd0-151">В PowerShell 5.1 и более поздних версий настройте сеанс PowerShell для использования прокси-сервера с помощью следующих команд:</span><span class="sxs-lookup"><span data-stu-id="40fd0-151">With PowerShell 5.1 and later, configure the PowerShell session to use a proxy using the following commands:</span></span>

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="40fd0-152">Если учетные данные операционной системы настроены правильно, конфигурация будет направлять запросы PowerShell через прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="40fd0-152">If your operating system credentials are configured correctly, this configuration routes PowerShell requests through the proxy.</span></span> <span data-ttu-id="40fd0-153">Чтобы такое поведение сохранялось между сеансами, добавьте команду в [профиль PowerShell](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="40fd0-153">To have this setting persist between sessions, add the commands to your [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="40fd0-154">Для установки пакета ваш прокси-сервер должен разрешать HTTPS-подключения по следующему адресу:</span><span class="sxs-lookup"><span data-stu-id="40fd0-154">To install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="40fd0-155">Вход</span><span class="sxs-lookup"><span data-stu-id="40fd0-155">Sign in</span></span>

<span data-ttu-id="40fd0-156">Чтобы начать работу с Azure PowerShell, выполните вход, используя данные своей учетной записи в Azure.</span><span class="sxs-lookup"><span data-stu-id="40fd0-156">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="40fd0-157">Если вы отключили автоматическую загрузку модулей, вручную импортируйте модуль с помощью `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="40fd0-157">If you've disabled module autoloading, manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="40fd0-158">Из-за структуры модуля эта операция может занять несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="40fd0-158">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="40fd0-159">Эти действия нужно повторять для каждого нового сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="40fd0-159">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="40fd0-160">Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах PowerShell, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="40fd0-160">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="40fd0-161">Обновление модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="40fd0-161">Update the Azure PowerShell module</span></span>

<span data-ttu-id="40fd0-162">Для обновления любого модуля PowerShell следует использовать тот же метод, который использовался для установки модуля.</span><span class="sxs-lookup"><span data-stu-id="40fd0-162">To update any PowerShell module, you should use the same method used to install the module.</span></span> <span data-ttu-id="40fd0-163">Например, если вы изначально использовали `Install-Module`, для получения последней версии следует использовать командлет [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="40fd0-163">For example, if you originally used `Install-Module`, then you should use [Update-Module](/powershell/module/powershellget/update-module) to get the latest version.</span></span> <span data-ttu-id="40fd0-164">Если вы изначально использовали пакет MSI, необходимо скачать и установить новый пакет MSI.</span><span class="sxs-lookup"><span data-stu-id="40fd0-164">If you originally used the MSI package then you should download and install the new MSI package.</span></span>

<span data-ttu-id="40fd0-165">Командлеты PowerShellGet не могут обновлять модули, установленные из пакета MSI.</span><span class="sxs-lookup"><span data-stu-id="40fd0-165">The PowerShellGet cmdlets cannot update modules that were installed from an MSI package.</span></span> <span data-ttu-id="40fd0-166">Пакеты MSI не обновляют модули, установленные с помощью PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="40fd0-166">MSI packages do not update modules that were installed using PowerShellGet.</span></span> <span data-ttu-id="40fd0-167">Если у вас возникли проблемы с обновлением с помощью модуля PowerShellGet, необходимо выполнить **повторную установку**, а не просто **обновление**.</span><span class="sxs-lookup"><span data-stu-id="40fd0-167">If you have any issues updating using PowershellGet then you should **reinstall**, rather than **update**.</span></span> <span data-ttu-id="40fd0-168">Повторная установка выполняется так же, как и первоначальная, но необходимо добавить параметр `-Force`:</span><span class="sxs-lookup"><span data-stu-id="40fd0-168">Reinstalling is done the same way as installing, but you need to add the `-Force` parameter:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="40fd0-169">В отличие от установки с помощью MSI, при установке или обновлении с помощью PowerShellGet не удаляются более старые версии, которые могут существовать в вашей системе.</span><span class="sxs-lookup"><span data-stu-id="40fd0-169">Unlike MSI-based installations, installing or updating using PowerShellGet does not remove older versions that may exist on your system.</span></span> <span data-ttu-id="40fd0-170">См. сведения об [удалении из системы предыдущих версий модуля Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="40fd0-170">To remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span> <span data-ttu-id="40fd0-171">См. сведения об [установке Azure PowerShell с помощью MSI](install-az-ps-msi.md).</span><span class="sxs-lookup"><span data-stu-id="40fd0-171">For more information about MSI-based installations, see [Install Azure PowerShell with an MSI](install-az-ps-msi.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="40fd0-172">Использование нескольких версий Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="40fd0-172">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="40fd0-173">Вы можете установить несколько версий Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="40fd0-173">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="40fd0-174">Чтобы проверить наличие нескольких установленных версий Azure PowerShell, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="40fd0-174">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="40fd0-175">Сведения о том, как удалить версию Azure PowerShell, см. в статье [Удаление модуля Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="40fd0-175">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="40fd0-176">Если у вас установлено несколько версий модуля, модуль автозагрузки и `Import-Module` загрузит последнюю версию по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="40fd0-176">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

<span data-ttu-id="40fd0-177">Определенную версию модуля `Az` можно установить или загрузить с помощью параметра `-RequiredVersion`:</span><span class="sxs-lookup"><span data-stu-id="40fd0-177">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` parameter:</span></span>

```powershell-interactive
# Install Az version 3.6.1
Install-Module -Name Az -RequiredVersion 3.6.1
# Load Az version 3.6.1
Import-Module -Name Az -RequiredVersion 3.6.1
```

## <a name="provide-feedback"></a><span data-ttu-id="40fd0-178">Отзывы</span><span class="sxs-lookup"><span data-stu-id="40fd0-178">Provide feedback</span></span>

<span data-ttu-id="40fd0-179">Если вы нашли ошибку при работе с Azure PowerShell, [сообщите о проблеме на GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="40fd0-179">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="40fd0-180">Чтобы отправить отзыв из командной строки, используйте командлет [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="40fd0-180">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="40fd0-181">Next Steps</span><span class="sxs-lookup"><span data-stu-id="40fd0-181">Next Steps</span></span>

<span data-ttu-id="40fd0-182">Дополнительные сведения о модулях Azure PowerShell и их функциях см. в статье [Get Started with Azure PowerShell](get-started-azureps.md) (Начало работы с Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="40fd0-182">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="40fd0-183">Если вы знакомы с Azure PowerShell и вам необходимо мигрировать из AzureRM, см. статью [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) (Миграция с AzureRM на Az).</span><span class="sxs-lookup"><span data-stu-id="40fd0-183">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
