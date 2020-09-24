---
title: Удаление Azure PowerShell
description: Сведения о том, как полностью удалить Azure PowerShell.
ms.date: 09/15/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 20859d6135676a3a4fb1e9f5d66909d157b38ac6
ms.sourcegitcommit: 15f21c40dcb7610e2fbaaabf264ad925e4224500
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/22/2020
ms.locfileid: "90928600"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="2c2fa-103">Удаление модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="2c2fa-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="2c2fa-104">Из этой статьи вы узнаете, как удалить предыдущую версию Azure PowerShell или полностью удалить этот модуль из системы.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="2c2fa-105">Если вы решили полностью удалить Azure PowerShell, отправьте нам отзыв с помощью командлета [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="2c2fa-105">If you've decided to completely uninstall Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span> <span data-ttu-id="2c2fa-106">Если возникнет ошибка, мы будем признательны, если вы [сообщите о ней на GitHub](https://github.com/azure/azure-powershell/issues), чтобы мы исправили ее.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-the-az-powershell-module-from-msi"></a><span data-ttu-id="2c2fa-107">Удаление модуля Az PowerShell из MSI</span><span class="sxs-lookup"><span data-stu-id="2c2fa-107">Uninstall the Az PowerShell module from MSI</span></span>

<span data-ttu-id="2c2fa-108">Если вы установили модуль Az PowerShell с помощью пакета MSI, удалять модуль нужно через систему Windows, а не PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-108">If you installed Az PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="2c2fa-109">Платформа</span><span class="sxs-lookup"><span data-stu-id="2c2fa-109">Platform</span></span>         |                      <span data-ttu-id="2c2fa-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="2c2fa-110">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="2c2fa-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="2c2fa-111">Windows 10</span></span>               | <span data-ttu-id="2c2fa-112">Пуск > Параметры > Приложения</span><span class="sxs-lookup"><span data-stu-id="2c2fa-112">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="2c2fa-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2c2fa-113">Windows 7</span></span> </br><span data-ttu-id="2c2fa-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2c2fa-114">Windows 8</span></span> | <span data-ttu-id="2c2fa-115">Пуск > Панель управления > Программы > Удалить программу</span><span class="sxs-lookup"><span data-stu-id="2c2fa-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="2c2fa-116">В этом окне в списке программ вы должны увидеть модуль **Azure PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-116">Once on this screen, you should see **Azure PowerShell** in the program listing.</span></span> <span data-ttu-id="2c2fa-117">Это программа, которую можно удалить.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-117">This is the app to uninstall.</span></span> <span data-ttu-id="2c2fa-118">Если этой программы нет в списке, значит, она установлена с помощью PowerShellGet. Следуйте приведенным ниже инструкциям.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-118">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

## <a name="uninstall-the-az-powershell-module-from-powershellget"></a><span data-ttu-id="2c2fa-119">Удаление модуля Az PowerShell из PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="2c2fa-119">Uninstall the Az PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="2c2fa-120">Чтобы удалить модули Az, используйте командлет [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="2c2fa-120">To uninstall the Az modules, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="2c2fa-121">Учтите, что `Uninstall-Module` удаляет только один модуль.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-121">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="2c2fa-122">Чтобы полностью удалить модуль Az PowerShell, каждый модуль нужно удалять отдельно.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-122">To remove the Az PowerShell module completely, you must uninstall each module individually.</span></span> <span data-ttu-id="2c2fa-123">Удаление может усложниться, если у вас установлено несколько версий Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-123">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="2c2fa-124">Чтобы проверить, какие версии модуля Az PowerShell у вас установлены, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="2c2fa-124">To check which versions of the Az PowerShell module you've installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

<span data-ttu-id="2c2fa-125">Следующий скрипт запрашивает из коллекции PowerShell список зависимых подмодулей,</span><span class="sxs-lookup"><span data-stu-id="2c2fa-125">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="2c2fa-126">а затем удаляет правильную версию каждого подмодуля.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-126">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="2c2fa-127">Для запуска этого скрипта в области, отличающейся от **Процесс** или **Текущий пользователь**, требуются права доступа администратора.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-127">You need to have administrator access to run this script in a scope other than **Process** or **Current User**.</span></span>

```powershell-interactive
function Uninstall-AzModule {
  [CmdletBinding(SupportsShouldProcess)]
  param(
    [ValidateNotNullOrEmpty()]
    [ValidateSet('Az','AzureRM','Azure')]
    [string]$Name = 'Az',

    [Parameter(Mandatory)]
    [string]$Version,

    [switch]$AllowPrerelease
  )

  $Params = @{}

  if ($PSBoundParameters.AllowPrerelease) {
    $Params.AllowPrerelease = $true
  }

  $IsAdmin = ([Security.Principal.WindowsPrincipal] [Security.Principal.WindowsIdentity]::GetCurrent()).IsInRole([Security.Principal.WindowsBuiltInRole] 'Administrator')

  if (-not(Get-InstalledModule -Name $Name -RequiredVersion $Version -ErrorAction SilentlyContinue -OutVariable RootModule @Params)) {

    Write-Warning -Message "Uninstall aborted. $Name version $Version not found."

  } elseif (($RootModule.InstalledLocation -notlike "*$env:USERPROFILE*") -and ($IsAdmin -eq $false)) {

    Write-Warning -Message "Uninstall aborted. $Name version $Version exists in a system path. PowerShell must be run elevated as an admin to remove it."

  } elseif ((Get-Process -Name powershell, pwsh -OutVariable Sessions -ErrorAction SilentlyContinue).Count -gt 1) {

    Write-Warning -Message "Uninstall aborted. Please close all other PowerShell sessions before continuing. There are currently $($Sessions.Count) PowerShell sessions running."

  } else {
    Write-Verbose -Message 'Creating list of dependencies...'
    $target = Find-Module -Name $Name -RequiredVersion $Version @Params

    $AllModules = @([pscustomobject]@{
      Name = $Name
      Version = $Version
    })

    $AllModules += foreach ($dependency in $target.Dependencies) {
      switch ($dependency.keys) {
        {$_ -contains 'RequiredVersion'} {$UninstallVersion = $dependency.RequiredVersion; break}
        {$_ -contains 'MinimumVersion'} {$UninstallVersion = $dependency.MinimumVersion; break}
      }

      [pscustomobject]@{
        Name = $dependency.Name
        Version = $UninstallVersion
      }
    }

    [int]$i = 100 / $AllModules.Count

    foreach ($module in $AllModules) {
      Write-Progress -Activity 'Uninstallation in Progress' -Status "$i% Complete:" -PercentComplete $i
      $i++

      if (Get-InstalledModule -Name $module.Name -RequiredVersion $module.Version -ErrorAction SilentlyContinue @Params) {
        Write-Verbose -Message "Uninstalling $($module.Name) version $($module.Version)"

        Remove-Module -FullyQualifiedName @{ModuleName=$module.Name;ModuleVersion=$module.Version} -ErrorAction SilentlyContinue

        try {
          if ($PSCmdlet.ShouldProcess("$($module.Name) version $($module.Version)")) {
            Uninstall-Module -Name $module.Name -RequiredVersion $module.Version -Force -ErrorAction Stop @Params
          }
          $State = 'Uninstalled'
        } Catch {
          $State = 'Manual uninstall required'
          Write-Verbose -Message "$($module.Name) version: $($module.Version) may require manual uninstallation."
        }

      } else {
        $State = 'Not found'
        Write-Verbose -Message "$($module.Name) version: $($module.Version) not found."
      }

      if (-not $PSBoundParameters.WhatIf) {
        [pscustomobject]@{
          ModuleName = $module.Name
          Version = $module.Version
          State = $State
        }
      }

    }
  }
}
```

<span data-ttu-id="2c2fa-128">Чтобы воспользоваться этой функцией, скопируйте и вставьте этот код в окно сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-128">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="2c2fa-129">В примере ниже показано, как выполнить функцию для удаления предыдущей версии модуля Az PowerShell и его подмодулей.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-129">The following example shows how to run the function to remove an older version of the Az PowerShell module and its submodules.</span></span>

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

<span data-ttu-id="2c2fa-130">Во время выполнения скрипта в окне будут отображаться **имя**, **версия** и **состояние** каждого удаляемого подмодуля.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-130">As the script runs, it displays the **Name**, **Version**, and **State** of each submodule that is being uninstalled.</span></span> <span data-ttu-id="2c2fa-131">Чтобы запустить скрипт только для просмотра удаляемых компонентов без их удаления, используйте параметр `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-131">To run the script to only see what would be deleted, without removing it, specify the `-WhatIf` parameter.</span></span>

```output
ModuleName              Version  State
----------              -------  -----
Az.Accounts             1.5.1    Not found
Az.Aks                  1.0.1    Uninstalled
Az.AnalysisServices     1.1.0    Uninstalled
Az.ApiManagement        1.0.0    Uninstalled
Az.ApplicationInsights  1.0.0    Uninstalled
...
```

> [!IMPORTANT]
> <span data-ttu-id="2c2fa-132">Если скрипт не может сопоставить определенную зависимость с версией для удаления, _ни одна_ из версий этой зависимости не будет удалена.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-132">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependency.</span></span> <span data-ttu-id="2c2fa-133">Это обусловлено тем, что на компьютере могут быть установлены другие версии целевого модуля, связанные с этими зависимостями.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-133">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span>

<span data-ttu-id="2c2fa-134">Выполните следующий пример для каждой версии модуля Az PowerShell, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-134">Run the following example for every version of the Az PowerShell module that you want to uninstall.</span></span>
<span data-ttu-id="2c2fa-135">Для удобства следующий скрипт удалит все версии Az, **кроме** последней.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-135">For convenience, the following script uninstalls all versions of Az **except** for the latest.</span></span>

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions |
    Sort-Object -Property Version -Descending |
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="2c2fa-136">Удаление модуля AzureRM</span><span class="sxs-lookup"><span data-stu-id="2c2fa-136">Uninstall the AzureRM module</span></span>

<span data-ttu-id="2c2fa-137">Если в вашей системе установлен модуль Az и вы хотите удалить AzureRM, это можно сделать одним из двух методов.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-137">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options.</span></span> <span data-ttu-id="2c2fa-138">Выбор метода зависит от того, как был установлен модуль AzureRM.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-138">Which method you follow depends on how you installed the AzureRM module.</span></span> <span data-ttu-id="2c2fa-139">Если вы этого не знаете, тогда сначала удалите MSI.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-139">If you're not sure of your original installation method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-the-azurerm-powershell-module-from-msi"></a><span data-ttu-id="2c2fa-140">Удаление модуля AzureRM PowerShell из MSI</span><span class="sxs-lookup"><span data-stu-id="2c2fa-140">Uninstall the AzureRM PowerShell module from MSI</span></span>

<span data-ttu-id="2c2fa-141">Если вы установили модуль AzureRM PowerShell с помощью пакета MSI, удалять модуль нужно через систему Windows, а не PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-141">If you installed the AzureRM PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="2c2fa-142">Платформа</span><span class="sxs-lookup"><span data-stu-id="2c2fa-142">Platform</span></span>         |                      <span data-ttu-id="2c2fa-143">Instructions</span><span class="sxs-lookup"><span data-stu-id="2c2fa-143">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="2c2fa-144">Windows 10</span><span class="sxs-lookup"><span data-stu-id="2c2fa-144">Windows 10</span></span>               | <span data-ttu-id="2c2fa-145">Пуск > Параметры > Приложения</span><span class="sxs-lookup"><span data-stu-id="2c2fa-145">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="2c2fa-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2c2fa-146">Windows 7</span></span> </br><span data-ttu-id="2c2fa-147">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2c2fa-147">Windows 8</span></span> | <span data-ttu-id="2c2fa-148">Пуск > Панель управления > Программы > Удалить программу</span><span class="sxs-lookup"><span data-stu-id="2c2fa-148">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="2c2fa-149">В этом окне в списке программ вы должны увидеть **Azure PowerShell** или **Microsoft Azure PowerShell — месяц год**.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-149">Once on this screen, you should see **Azure PowerShell** or **Microsoft Azure PowerShell - Month Year** in the program listing.</span></span> <span data-ttu-id="2c2fa-150">Это программа, которую можно удалить.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-150">This is the app to uninstall.</span></span> <span data-ttu-id="2c2fa-151">Если этой программы нет в списке, значит, она установлена с помощью PowerShellGet. Следуйте приведенным ниже инструкциям.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-151">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-the-azurerm-powershell-module-from-powershellget"></a><span data-ttu-id="2c2fa-152">Удаление модуля AzureRM PowerShell из PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="2c2fa-152">Uninstall the AzureRM PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="2c2fa-153">Если вы установили AzureRM с помощью PowerShellGet, вы можете удалить модули с помощью командлета [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), доступного в модуле `Az.Accounts`.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-153">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="2c2fa-154">Приведенный ниже пример команды удалит с вашего компьютера _все_ модули AzureRM.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-154">The following example removes _all_ AzureRM modules from your machine.</span></span> <span data-ttu-id="2c2fa-155">Для ее выполнения требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-155">It requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```
