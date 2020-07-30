---
title: Установка и настройка Azure PowerShell | Документация Майкрософт
description: Как установить и настроить Azure PowerShell для первого использования.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: 653284edc093943972516dfd4253af6297754a6a
ms.sourcegitcommit: c19bf5a96a82a56e2b1fa9ab5e106690f850cedf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/27/2020
ms.locfileid: "87177515"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="fe14b-103">Установка Azure PowerShell в ОС Windows с помощью PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="fe14b-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="fe14b-104">В этой статье содержатся инструкции по установке модулей Azure PowerShell для PowerShell 5.x для Windows с помощью PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="fe14b-104">This article explains the steps to install the Azure PowerShell modules for PowerShell 5.x for Windows using PowerShellGet.</span></span> <span data-ttu-id="fe14b-105">PowerShellGet и управление модулями — это предпочтительный способ установки Azure PowerShell, но если вы хотите использовать для установки пакет MSI или установщик веб-платформы, см. статью о [других способах установки](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="fe14b-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="fe14b-106">Эта версия Azure PowerShell не поддерживает классическую модель развертывания Azure.</span><span class="sxs-lookup"><span data-stu-id="fe14b-106">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="fe14b-107">Если вам нужна поддержка классического развертывания, см. статью [Установка модуля управления службами Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="fe14b-107">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fe14b-108">Модуль AzureRM не поддерживается в macOS и Linux.</span><span class="sxs-lookup"><span data-stu-id="fe14b-108">The AzureRM module is not supported for macOS or Linux.</span></span> <span data-ttu-id="fe14b-109">Чтобы использовать командлеты Azure PowerShell на этих платформах, [установите модуль Az](/powershell/azure/install-az-ps).</span><span class="sxs-lookup"><span data-stu-id="fe14b-109">To use Azure PowerShell cmdlets on these platforms, [Install the Az module](/powershell/azure/install-az-ps).</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="fe14b-110">Шаг 1. Установка PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="fe14b-110">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="fe14b-111">Чтобы установить элементы из коллекции PowerShell, требуется модуль PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="fe14b-111">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="fe14b-112">Убедитесь, что в системе установлена необходимая версия PowerShellGet и что выполнены другие требования к системе.</span><span class="sxs-lookup"><span data-stu-id="fe14b-112">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="fe14b-113">Выполните следующую команду, чтобы определить наличие PowerShellGet в вашей системе:</span><span class="sxs-lookup"><span data-stu-id="fe14b-113">Run the following command to see if you have PowerShellGet installed on your system.</span></span>


```powershell-interactive
Get-InstalledModule -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="fe14b-114">Должен отобразиться результат, аналогичный следующему:</span><span class="sxs-lookup"><span data-stu-id="fe14b-114">You should see something similar to the following output:</span></span>

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="fe14b-115">Необходимо установить версию PowerShellGet 1.1.2.0 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="fe14b-115">You need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="fe14b-116">Для обновления PowerShellGet используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="fe14b-116">To update PowerShellGet, use the following command:</span></span>

```powershell-interactive
Install-Module PowerShellGet -Force
```

<span data-ttu-id="fe14b-117">Если у вас не установлен PowerShellGet, перейдите к разделу [Как установить PowerShellGet](#how-to-get-powershellget) этой статьи.</span><span class="sxs-lookup"><span data-stu-id="fe14b-117">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="fe14b-118">Чтобы использовать PowerShellGet, необходимо иметь политику выполнения, которая позволяет запускать сценарии.</span><span class="sxs-lookup"><span data-stu-id="fe14b-118">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="fe14b-119">Дополнительные сведения о политике выполнения PowerShell см. в [этой статье](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span><span class="sxs-lookup"><span data-stu-id="fe14b-119">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>
>
> [!IMPORTANT]
> <span data-ttu-id="fe14b-120">Для модуля AzureRM, описанном в этом документе, используется .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="fe14b-120">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="fe14b-121">Из-за этого модуль несовместимым с PowerShell версии 6.0, для которой используется .NET Core.</span><span class="sxs-lookup"><span data-stu-id="fe14b-121">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="fe14b-122">Если вы используете PowerShell 6.0, изучите [инструкции по установке для macOS и Linux](/powershell/azure/install-az-ps).</span><span class="sxs-lookup"><span data-stu-id="fe14b-122">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](/powershell/azure/install-az-ps).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="fe14b-123">Шаг 2. Установите Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="fe14b-123">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="fe14b-124">Для установки Azure PowerShell из коллекции PowerShell требуются повышенные права.</span><span class="sxs-lookup"><span data-stu-id="fe14b-124">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="fe14b-125">Выполните следующую команду PowerShell с повышенными правами:</span><span class="sxs-lookup"><span data-stu-id="fe14b-125">Run the following command from an elevated PowerShell session:</span></span>

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="fe14b-126">По умолчанию коллекция PowerShell не настроена как доверенное хранилище для PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="fe14b-126">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="fe14b-127">При первом использовании PSGallery отображается следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="fe14b-127">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="fe14b-128">Ответьте Yes (Да) или Yes to All (Да для всех), чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="fe14b-128">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="fe14b-129">Если установленная версия NuGet предшествует версии 2.8.5.201, вам будет предложено скачать и установить последнюю версию NuGet.</span><span class="sxs-lookup"><span data-stu-id="fe14b-129">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="fe14b-130">Модуль AzureRM — это набор командлетов для работы с Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="fe14b-130">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="fe14b-131">При установке модуля AzureRM любой модуль Azure PowerShell, который ранее не был установлен, скачивается из коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fe14b-131">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="fe14b-132">Если у вас установлена предыдущая версия Azure PowerShell, то может появиться сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="fe14b-132">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="fe14b-133">Для устранения этой проблемы см. раздел [Обновление Azure PowerShell до новой версии](#update-azps) далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="fe14b-133">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="fe14b-134">Шаг 3. Загрузка модуля AzureRM</span><span class="sxs-lookup"><span data-stu-id="fe14b-134">Step 3: Load the AzureRM module</span></span>

<span data-ttu-id="fe14b-135">После установки модуля его необходимо загрузить в сеанс PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fe14b-135">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="fe14b-136">Это необходимо сделать в обычном (без повышенных привилегий) сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fe14b-136">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="fe14b-137">Модули можно загрузить с помощью командлета `Import-Module` следующим образом:</span><span class="sxs-lookup"><span data-stu-id="fe14b-137">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell-interactive
Import-Module -Name AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="fe14b-138">Next Steps</span><span class="sxs-lookup"><span data-stu-id="fe14b-138">Next Steps</span></span>

<span data-ttu-id="fe14b-139">Дополнительные сведения об использовании Azure PowerShell см. в следующей статье:</span><span class="sxs-lookup"><span data-stu-id="fe14b-139">For more information about using Azure PowerShell, see the following articles:</span></span>

* <span data-ttu-id="fe14b-140">[Getting started with Azure PowerShell](get-started-azureps.md) (Приступая к работе с Azure PowerShell)</span><span class="sxs-lookup"><span data-stu-id="fe14b-140">[Get started with Azure PowerShell](get-started-azureps.md)</span></span>

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="fe14b-141">Создание отчетов о проблемах и обратная связь</span><span class="sxs-lookup"><span data-stu-id="fe14b-141">Reporting issues and feedback</span></span>

<span data-ttu-id="fe14b-142">При появлении ошибок в средстве сообщите о проблеме в разделе [Проблемы](https://github.com/Azure/azure-powershell/issues) репозитория GitHub.</span><span class="sxs-lookup"><span data-stu-id="fe14b-142">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-powershell/issues) section of our GitHub repo.</span></span> <span data-ttu-id="fe14b-143">Чтобы отправить отзыв из командной строки, используйте командлет `Send-Feedback`.</span><span class="sxs-lookup"><span data-stu-id="fe14b-143">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="fe14b-144">Часто задаваемые вопросы</span><span class="sxs-lookup"><span data-stu-id="fe14b-144">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="fe14b-145">Как установить PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="fe14b-145">How to get PowerShellGet</span></span>

|<span data-ttu-id="fe14b-146">Сценарий</span><span class="sxs-lookup"><span data-stu-id="fe14b-146">OS Version</span></span>|<span data-ttu-id="fe14b-147">Инструкции по установке</span><span class="sxs-lookup"><span data-stu-id="fe14b-147">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="fe14b-148">Используется Windows 10 или Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fe14b-148">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="fe14b-149">Встроен в пакет Windows Management Framework (WMF) 5.0, который входит в состав ОС</span><span class="sxs-lookup"><span data-stu-id="fe14b-149">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="fe14b-150">Обновление до PowerShell 5.0</span><span class="sxs-lookup"><span data-stu-id="fe14b-150">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="fe14b-151">Установите последнюю версию WMF</span><span class="sxs-lookup"><span data-stu-id="fe14b-151">Install the latest version of WMF</span></span>](https://www.microsoft.com/download/details.aspx?id=54616)|
|<span data-ttu-id="fe14b-152">Используется версия Windows с PowerShell 3 или PowerShell 4</span><span class="sxs-lookup"><span data-stu-id="fe14b-152">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="fe14b-153">Скачайте модули PackageManagement</span><span class="sxs-lookup"><span data-stu-id="fe14b-153">Get the PackageManagement modules</span></span>](https://go.microsoft.com/fwlink/?LinkID=746217)|

### <a name="div-idhelpmechoosechecking-the-version-of-azure-powershell"></a><div id="helpmechoose"/><span data-ttu-id="fe14b-154">Проверка версии Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="fe14b-154">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="fe14b-155">Хотя мы советуем выполнить обновление до последней версии как можно скорее, поддерживается несколько версий Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fe14b-155">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="fe14b-156">Чтобы определить, какая версия Azure PowerShell установлена, выполните в командной строке команду `Get-InstalledModule AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="fe14b-156">To determine the version of Azure PowerShell you have installed, run `Get-InstalledModule AzureRM` from your command line.</span></span>

```powershell-interactive
Get-InstalledModule AzureRM -AllVersions | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="fe14b-157">Поддержка классических методов развертывания</span><span class="sxs-lookup"><span data-stu-id="fe14b-157">Support for classic deployment methods</span></span>

<span data-ttu-id="fe14b-158">При наличии экземпляров, развернутых с помощью классической модели, вы можете установить Azure PowerShell для управления службами.</span><span class="sxs-lookup"><span data-stu-id="fe14b-158">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="fe14b-159">Дополнительные сведения см. в статье об [установке модуля управления службами Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="fe14b-159">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="fe14b-160">Модули Azure и AzureRM имеют общие зависимости.</span><span class="sxs-lookup"><span data-stu-id="fe14b-160">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="fe14b-161">При использовании обоих модулей (Azure и AzureRM) необходимо установить одинаковую версию каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="fe14b-161">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a name="div-idupdate-azpsupdating-to-a-new-version-of-azure-powershell"></a><div id="update-azps"/><span data-ttu-id="fe14b-162">Обновление Azure PowerShell до новой версии</span><span class="sxs-lookup"><span data-stu-id="fe14b-162">Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="fe14b-163">Если у вас установлена предыдущая версия Azure PowerShell, включающая модуль управления службами, то может появиться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="fe14b-163">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

<span data-ttu-id="fe14b-164">Как указано в сообщении об ошибке, для установки модуля предлагается использовать параметр -AllowClobber</span><span class="sxs-lookup"><span data-stu-id="fe14b-164">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="fe14b-165">Используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="fe14b-165">Use the following command:</span></span>

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="fe14b-166">Дополнительные сведения см. в статье, посвященной командлету [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span><span class="sxs-lookup"><span data-stu-id="fe14b-166">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="fe14b-167">Установка версий модуля без замены</span><span class="sxs-lookup"><span data-stu-id="fe14b-167">Installing module versions side by side</span></span>

<span data-ttu-id="fe14b-168">Метод установки PowerShellGet — это единственный метод, поддерживающий установку нескольких версий.</span><span class="sxs-lookup"><span data-stu-id="fe14b-168">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="fe14b-169">Например, вы можете использовать скрипты, написанные с помощью предыдущих версий Azure PowerShell, которые вы не можете обновить из-за отсутствия времени или ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fe14b-169">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="fe14b-170">Чтобы установить несколько версий Azure PowerShell, выполните следующие команды:</span><span class="sxs-lookup"><span data-stu-id="fe14b-170">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell-interactive
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="fe14b-171">В сеанс PowerShell можно загрузить только одну версию модуля.</span><span class="sxs-lookup"><span data-stu-id="fe14b-171">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="fe14b-172">Необходимо открыть новое окно PowerShell и с помощью команды `Import-Module` импортировать определенную версию командлетов AzureRM:</span><span class="sxs-lookup"><span data-stu-id="fe14b-172">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell-interactive
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

> [!NOTE]
> <span data-ttu-id="fe14b-173">Версии 2.1.0 и 1.2.6 — это первые версии модуля, предназначенные для установки и использования без удаления предыдущей версии.</span><span class="sxs-lookup"><span data-stu-id="fe14b-173">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="fe14b-174">Если загрузить более раннюю версию модуля Azure PowerShell, то загрузится несовместимая версия модуля **AzureRM.Profile**.</span><span class="sxs-lookup"><span data-stu-id="fe14b-174">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="fe14b-175">Это приведет к тому, что при каждом выполнении командлета будет отображаться запрос на вход.</span><span class="sxs-lookup"><span data-stu-id="fe14b-175">This results in the cmdlets prompting you to sign in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="fe14b-176">Другие методы установки</span><span class="sxs-lookup"><span data-stu-id="fe14b-176">Other installation methods</span></span>

<span data-ttu-id="fe14b-177">Сведения об установке с помощью установщика веб-платформы или пакета MSI см. статье [Other installation methods](other-install.md) (Другие методы установки).</span><span class="sxs-lookup"><span data-stu-id="fe14b-177">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
