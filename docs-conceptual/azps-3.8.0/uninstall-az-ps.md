---
title: Удаление Azure PowerShell
description: Сведения о том, как полностью удалить Azure PowerShell.
ms.date: 10/22/2019
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 1bf94f4c7a27328b60b7f9369888f688541ba4a7
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386873"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="48cce-103">Удаление модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="48cce-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="48cce-104">Из этой статьи вы узнаете, как удалить предыдущую версию Azure PowerShell или полностью удалить этот модуль из системы.</span><span class="sxs-lookup"><span data-stu-id="48cce-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="48cce-105">Если вы решили полностью удалить Azure PowerShell, отправьте нам отзыв с помощью командлета [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="48cce-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>
<span data-ttu-id="48cce-106">Если возникнет ошибка, мы будем признательны, если вы [сообщите о ней на GitHub](https://github.com/azure/azure-powershell/issues), чтобы мы исправили ее.</span><span class="sxs-lookup"><span data-stu-id="48cce-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-azure-powershell-from-msi"></a><span data-ttu-id="48cce-107">Удаление Azure PowerShell из MSI</span><span class="sxs-lookup"><span data-stu-id="48cce-107">Uninstall Azure PowerShell from MSI</span></span>

<span data-ttu-id="48cce-108">Если вы установили Azure PowerShell с помощью пакета MSI, удалять модуль нужно через систему Windows, а не PowerShell.</span><span class="sxs-lookup"><span data-stu-id="48cce-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="48cce-109">Платформа</span><span class="sxs-lookup"><span data-stu-id="48cce-109">Platform</span></span> | <span data-ttu-id="48cce-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="48cce-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="48cce-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="48cce-111">Windows 10</span></span> | <span data-ttu-id="48cce-112">Пуск > Параметры > Приложения</span><span class="sxs-lookup"><span data-stu-id="48cce-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="48cce-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="48cce-113">Windows 7</span></span> </br><span data-ttu-id="48cce-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="48cce-114">Windows 8</span></span> | <span data-ttu-id="48cce-115">Пуск > Панель управления > Программы > Удалить программу</span><span class="sxs-lookup"><span data-stu-id="48cce-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="48cce-116">В этом окне в списке программ вы должны увидеть модуль __Azure PowerShell__.</span><span class="sxs-lookup"><span data-stu-id="48cce-116">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="48cce-117">Это программа, которую можно удалить.</span><span class="sxs-lookup"><span data-stu-id="48cce-117">This is the app to uninstall.</span></span> <span data-ttu-id="48cce-118">Если этой программы нет в списке, значит, она установлена с помощью PowerShellGet. Следуйте приведенным ниже инструкциям.</span><span class="sxs-lookup"><span data-stu-id="48cce-118">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

## <a name="uninstall-azure-powershell-from-powershell-get"></a><span data-ttu-id="48cce-119">Удаление Azure PowerShell из PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="48cce-119">Uninstall Azure PowerShell from PowerShell Get</span></span>

<span data-ttu-id="48cce-120">Чтобы удалить модули Az, используйте командлет [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="48cce-120">To uninstall the Az modules, use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="48cce-121">Учтите, что `Uninstall-Module` удаляет только один модуль.</span><span class="sxs-lookup"><span data-stu-id="48cce-121">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="48cce-122">Чтобы полностью удалить Azure PowerShell, каждый модуль нужно удалять отдельно.</span><span class="sxs-lookup"><span data-stu-id="48cce-122">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="48cce-123">Удаление может усложниться, если у вас установлено несколько версий Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="48cce-123">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="48cce-124">Чтобы проверить, какие версии Azure PowerShell у вас установлены, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="48cce-124">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

<a name="uninstall-script"/>

<span data-ttu-id="48cce-125">Следующий скрипт запрашивает из коллекции PowerShell список зависимых подмодулей,</span><span class="sxs-lookup"><span data-stu-id="48cce-125">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="48cce-126">а затем удаляет правильную версию каждого подмодуля.</span><span class="sxs-lookup"><span data-stu-id="48cce-126">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="48cce-127">Необходимы права доступа администратора для запуска этого скрипта в области, отличающейся от `Process` или `CurrentUser`.</span><span class="sxs-lookup"><span data-stu-id="48cce-127">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

```powershell-interactive
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force,

    [switch]$WhatIf
  )
  
  $AllModules = @()
  
  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    if ($_.PSObject.Properties.Name -contains 'requiredVersion') {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version -ErrorAction Ignore
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        $availableModules = Get-InstalledModule $_.name -AllVersions
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall. Available versions are: {2}" -f $_.name,$version,($availableModules.Version -join ', '))
      }
    }
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}...' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop -WhatIf:$WhatIf
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

<span data-ttu-id="48cce-128">Чтобы воспользоваться этой функцией, скопируйте и вставьте этот код в окно сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="48cce-128">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="48cce-129">В примере ниже показано, как запустить функцию, чтобы удалить предыдущую версию Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="48cce-129">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

<span data-ttu-id="48cce-130">Во время выполнения скрипта в окне будут отображаться имя и версия каждого удаляемого подмодуля.</span><span class="sxs-lookup"><span data-stu-id="48cce-130">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="48cce-131">Чтобы запустить скрипт для просмотра только удаляемых компонентов без удаления, используйте параметр `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="48cce-131">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

> [!NOTE]
> <span data-ttu-id="48cce-132">Если скрипт не может сопоставить определенную зависимость с версией для удаления, _ни одна_ из версий этой зависимости не будет удалена.</span><span class="sxs-lookup"><span data-stu-id="48cce-132">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="48cce-133">Это обусловлено тем, что на компьютере могут быть установлены другие версии целевого модуля, связанные с этими зависимостями.</span><span class="sxs-lookup"><span data-stu-id="48cce-133">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="48cce-134">В этом случае перечисляются доступные версии зависимости.</span><span class="sxs-lookup"><span data-stu-id="48cce-134">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="48cce-135">После этого вы можете вручную удалить любые предыдущие версии с помощью `Uninstall-Module`.</span><span class="sxs-lookup"><span data-stu-id="48cce-135">You can then remove any old versions manually with `Uninstall-Module`.</span></span>

<span data-ttu-id="48cce-136">Выполните эту команду для каждой версии Azure PowerShell, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="48cce-136">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="48cce-137">Для удобства следующий скрипт удалит все версии Az, __за исключением__ последней.</span><span class="sxs-lookup"><span data-stu-id="48cce-137">For convenience, the following script will uninstall all versions of Az __except__ for the latest.</span></span>

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="48cce-138">Удаление модуля AzureRM</span><span class="sxs-lookup"><span data-stu-id="48cce-138">Uninstall the AzureRM module</span></span>

<span data-ttu-id="48cce-139">Если в вашей системе установлен модуль Az и вы хотите удалить AzureRM, существуют два метода, которые не требуют выполнения сценария `Uninstall-AllModules`, описанного выше.</span><span class="sxs-lookup"><span data-stu-id="48cce-139">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options that don't require running the `Uninstall-AllModules` script above.</span></span> <span data-ttu-id="48cce-140">Выбор метода зависит от того, как был установлен модуль AzureRM.</span><span class="sxs-lookup"><span data-stu-id="48cce-140">Which method you follow depends on how you installed the AzureRM module.</span></span>
<span data-ttu-id="48cce-141">Если вы этого не знаете, тогда сначала удалите MSI.</span><span class="sxs-lookup"><span data-stu-id="48cce-141">If you're not sure of your original install method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="48cce-142">Удаление Azure PowerShell MSI</span><span class="sxs-lookup"><span data-stu-id="48cce-142">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="48cce-143">Если вы установили модули AzureRM Azure PowerShell с помощью пакета MSI, удалять модуль нужно через систему Windows, а не PowerShell.</span><span class="sxs-lookup"><span data-stu-id="48cce-143">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="48cce-144">Платформа</span><span class="sxs-lookup"><span data-stu-id="48cce-144">Platform</span></span> | <span data-ttu-id="48cce-145">Instructions</span><span class="sxs-lookup"><span data-stu-id="48cce-145">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="48cce-146">Windows 10</span><span class="sxs-lookup"><span data-stu-id="48cce-146">Windows 10</span></span> | <span data-ttu-id="48cce-147">Пуск > Параметры > Приложения</span><span class="sxs-lookup"><span data-stu-id="48cce-147">Start > Settings > Apps</span></span> |
| <span data-ttu-id="48cce-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="48cce-148">Windows 7</span></span> </br><span data-ttu-id="48cce-149">Windows 8</span><span class="sxs-lookup"><span data-stu-id="48cce-149">Windows 8</span></span> | <span data-ttu-id="48cce-150">Пуск > Панель управления > Программы > Удалить программу</span><span class="sxs-lookup"><span data-stu-id="48cce-150">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="48cce-151">В этом окне в списке программ вы должны увидеть __Azure PowerShell__ или __Microsoft Azure PowerShell — месяц год__.</span><span class="sxs-lookup"><span data-stu-id="48cce-151">Once on this screen you should see __Azure PowerShell__ or __Microsoft Azure PowerShell - Month Year__ in the program listing.</span></span> <span data-ttu-id="48cce-152">Это программа, которую можно удалить.</span><span class="sxs-lookup"><span data-stu-id="48cce-152">This is the app to uninstall.</span></span> <span data-ttu-id="48cce-153">Если этой программы нет в списке, значит, она установлена с помощью PowerShellGet. Следуйте приведенным ниже инструкциям.</span><span class="sxs-lookup"><span data-stu-id="48cce-153">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="48cce-154">Удаление с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="48cce-154">Uninstall from PowerShell</span></span>

<span data-ttu-id="48cce-155">Если вы установили AzureRM с помощью PowerShellGet, то модули можно удалить с помощью команды [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), доступной в модуле `Az.Accounts`.</span><span class="sxs-lookup"><span data-stu-id="48cce-155">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) command, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="48cce-156">С вашего компьютера удалятся _все_ модули AzureRM, но для этого требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="48cce-156">This removes _all_ AzureRM modules from your machine, but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```
<span data-ttu-id="48cce-157">или диспетчер конфигурации служб</span><span class="sxs-lookup"><span data-stu-id="48cce-157">or</span></span>
```powershell-interactive
Uninstall-Module AzureRm
```

<span data-ttu-id="48cce-158">Если вам не удается запустить команду `Uninstall-AzureRM`, используйте [скрипт `Uninstall-AllModules`](#uninstall-script), приведенный в этой статье, путем следующего вызова:</span><span class="sxs-lookup"><span data-stu-id="48cce-158">If you can't successfully run the `Uninstall-AzureRM` command, use the [`Uninstall-AllModules` script](#uninstall-script) provided in this article with the following invocation:</span></span>

```powershell-interactive
$versions = (Get-InstalledModule AzureRM -AllVersions | Select-Object Version)
$versions | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
<span data-ttu-id="48cce-159">или диспетчер конфигурации служб</span><span class="sxs-lookup"><span data-stu-id="48cce-159">or</span></span>
```powershell-interactive
foreach ($module in (Get-Module -ListAvailable AzureRM*).Name |Get-Unique) {
   write-host "Removing Module $module"
   Uninstall-module $module
}
```
