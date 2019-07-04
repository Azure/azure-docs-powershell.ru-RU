---
title: Удаление Azure PowerShell
description: Сведения о том, как полностью удалить Azure PowerShell.
ms.date: 05/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: b32547e9c3df0df7495d1631a43be6934e1f62dc
ms.sourcegitcommit: febbbd3f75c8dd1a296281d265289f015b6cb537
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/12/2019
ms.locfileid: "67037767"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="95ab3-103">Удаление модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="95ab3-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="95ab3-104">Из этой статьи вы узнаете, как удалить предыдущую версию Azure PowerShell или полностью удалить этот модуль из системы.</span><span class="sxs-lookup"><span data-stu-id="95ab3-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="95ab3-105">Если вы решили полностью удалить Azure PowerShell, отправьте нам отзыв с помощью командлета [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="95ab3-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>
<span data-ttu-id="95ab3-106">Если возникнет ошибка, мы будем признательны, если вы [сообщите о ней на GitHub](https://github.com/azure/azure-powershell/issues), чтобы мы исправили ее.</span><span class="sxs-lookup"><span data-stu-id="95ab3-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-the-az-module"></a><span data-ttu-id="95ab3-107">Удаление модуля Az</span><span class="sxs-lookup"><span data-stu-id="95ab3-107">Uninstall the Az module</span></span>

<span data-ttu-id="95ab3-108">Чтобы удалить модули Az, используйте командлет [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="95ab3-108">To uninstall the Az modules, use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="95ab3-109">Учтите, что `Uninstall-Module` удаляет только один модуль.</span><span class="sxs-lookup"><span data-stu-id="95ab3-109">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="95ab3-110">Чтобы полностью удалить Azure PowerShell, каждый модуль нужно удалять отдельно.</span><span class="sxs-lookup"><span data-stu-id="95ab3-110">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="95ab3-111">Удаление может усложниться, если у вас установлено несколько версий Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="95ab3-111">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="95ab3-112">Чтобы проверить, какие версии Azure PowerShell у вас установлены, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="95ab3-112">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

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

<span data-ttu-id="95ab3-113">Следующий скрипт запрашивает из коллекции PowerShell список зависимых подмодулей,</span><span class="sxs-lookup"><span data-stu-id="95ab3-113">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="95ab3-114">а затем удаляет правильную версию каждого подмодуля.</span><span class="sxs-lookup"><span data-stu-id="95ab3-114">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="95ab3-115">Необходимы права доступа администратора для запуска этого скрипта в области, отличающейся от `Process` или `CurrentUser`.</span><span class="sxs-lookup"><span data-stu-id="95ab3-115">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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

<span data-ttu-id="95ab3-116">Чтобы воспользоваться этой функцией, скопируйте и вставьте этот код в окно сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="95ab3-116">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="95ab3-117">В примере ниже показано, как запустить функцию, чтобы удалить предыдущую версию Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="95ab3-117">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

<span data-ttu-id="95ab3-118">Во время выполнения скрипта в окне будут отображаться имя и версия каждого удаляемого подмодуля.</span><span class="sxs-lookup"><span data-stu-id="95ab3-118">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="95ab3-119">Чтобы запустить скрипт для просмотра только удаляемых компонентов без удаления, используйте параметр `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="95ab3-119">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

> [!NOTE]
> <span data-ttu-id="95ab3-120">Если скрипт не может сопоставить определенную версию зависимого модуля для удаления, _ни одна_ из версий этого модуля не будет удалена.</span><span class="sxs-lookup"><span data-stu-id="95ab3-120">If this script can't match an exact dependent module version to uninstall, it won't uninstall _any_ version of that module.</span></span> <span data-ttu-id="95ab3-121">Это обусловлено тем, что на компьютере могут быть установлены другие версии `Az`, связанные с этими модулями.</span><span class="sxs-lookup"><span data-stu-id="95ab3-121">This is because there may be other versions of `Az` on your system which rely on these modules.</span></span> <span data-ttu-id="95ab3-122">В этом случае выводится список версий модуля, которые не удалось найти, если эти версии были установлены.</span><span class="sxs-lookup"><span data-stu-id="95ab3-122">In this case, the versions of the module that couldn't be found will be listed, if any were installed.</span></span> <span data-ttu-id="95ab3-123">После этого вы можете вручную удалить любые предыдущие версии с помощью `Uninstall-Module`.</span><span class="sxs-lookup"><span data-stu-id="95ab3-123">You can then remove any old versions manually with `Uninstall-Module`.</span></span>

<span data-ttu-id="95ab3-124">Выполните эту команду для каждой версии Azure PowerShell, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="95ab3-124">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="95ab3-125">Для удобства следующий скрипт удалит все версии Az, __за исключением__ последней.</span><span class="sxs-lookup"><span data-stu-id="95ab3-125">For convenience, the following script will uninstall all versions of Az __except__ for the latest.</span></span>

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="95ab3-126">Удаление модуля AzureRM</span><span class="sxs-lookup"><span data-stu-id="95ab3-126">Uninstall the AzureRM module</span></span>

<span data-ttu-id="95ab3-127">Если в вашей системе установлен модуль Az и вы хотите удалить AzureRM, существуют два метода, которые не требуют выполнения сценария `Uninstall-AllModules`, описанного выше.</span><span class="sxs-lookup"><span data-stu-id="95ab3-127">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options that don't require running the `Uninstall-AllModules` script above.</span></span> <span data-ttu-id="95ab3-128">Выбор метода зависит от того, как был установлен модуль AzureRM.</span><span class="sxs-lookup"><span data-stu-id="95ab3-128">Which method you follow depends on how you installed the AzureRM module.</span></span>
<span data-ttu-id="95ab3-129">Если вы этого не знаете, тогда сначала удалите MSI.</span><span class="sxs-lookup"><span data-stu-id="95ab3-129">If you're not sure of your original install method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="95ab3-130">Удаление Azure PowerShell MSI</span><span class="sxs-lookup"><span data-stu-id="95ab3-130">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="95ab3-131">Если вы установили модули AzureRM Azure PowerShell с помощью пакета MSI, удалять модуль нужно через систему Windows, а не PowerShell.</span><span class="sxs-lookup"><span data-stu-id="95ab3-131">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="95ab3-132">платформа</span><span class="sxs-lookup"><span data-stu-id="95ab3-132">Platform</span></span> | <span data-ttu-id="95ab3-133">Указания</span><span class="sxs-lookup"><span data-stu-id="95ab3-133">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="95ab3-134">Windows 10</span><span class="sxs-lookup"><span data-stu-id="95ab3-134">Windows 10</span></span> | <span data-ttu-id="95ab3-135">"Пуск" > "Параметры" > "Приложения"</span><span class="sxs-lookup"><span data-stu-id="95ab3-135">Start > Settings > Apps</span></span> |
| <span data-ttu-id="95ab3-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="95ab3-136">Windows 7</span></span> </br><span data-ttu-id="95ab3-137">Windows 8</span><span class="sxs-lookup"><span data-stu-id="95ab3-137">Windows 8</span></span> | <span data-ttu-id="95ab3-138">"Пуск" > "Панель управления" > "Программы" > "Удаление программы"</span><span class="sxs-lookup"><span data-stu-id="95ab3-138">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="95ab3-139">В этом окне в списке программ вы должны увидеть модуль __Azure PowerShell__.</span><span class="sxs-lookup"><span data-stu-id="95ab3-139">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="95ab3-140">Это программа, которую можно удалить.</span><span class="sxs-lookup"><span data-stu-id="95ab3-140">This is the app to uninstall.</span></span> <span data-ttu-id="95ab3-141">Если этой программы нет в списке, значит, она установлена с помощью PowerShellGet. Следуйте приведенным ниже инструкциям.</span><span class="sxs-lookup"><span data-stu-id="95ab3-141">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="95ab3-142">Удаление с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="95ab3-142">Uninstall from PowerShell</span></span>

<span data-ttu-id="95ab3-143">Если вы установили AzureRM с помощью PowerShellGet, то модули можно удалить с помощью команды [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), доступной в модуле `Az.Accounts`.</span><span class="sxs-lookup"><span data-stu-id="95ab3-143">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) command, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="95ab3-144">С вашего компьютера удалятся _все_ модули AzureRM, но для этого требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="95ab3-144">This removes _all_ AzureRM modules from your machine, but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```

<span data-ttu-id="95ab3-145">Если вам не удается запустить команду `Uninstall-AzureRM`, используйте [скрипт `Uninstall-AllModules`](#uninstall-script), приведенный в этой статье, путем следующего вызова:</span><span class="sxs-lookup"><span data-stu-id="95ab3-145">If you can't successfully run the `Uninstall-AzureRM` command, use the [`Uninstall-AllModules` script](#uninstall-script) provided in this article with the following invocation:</span></span>

```powershell-interactive
$versions = (Get-InstalledModule AzureRM -AllVersions | Select-Object Version)
$versions | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```