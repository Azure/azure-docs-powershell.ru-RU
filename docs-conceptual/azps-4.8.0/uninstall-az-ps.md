---
title: Удаление Azure PowerShell
description: Сведения о том, как полностью удалить Azure PowerShell.
ms.date: 09/15/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 7f831bdf6d6144640e036d72900958847283acf1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "92002395"
---
# <a name="how-to-uninstall-azure-powershell-modules"></a><span data-ttu-id="8a961-103">Как удалить модули Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8a961-103">How to uninstall Azure PowerShell modules</span></span>

<span data-ttu-id="8a961-104">Из этой статьи вы узнаете, как удалить предыдущую версию Azure PowerShell или полностью удалить этот модуль из системы.</span><span class="sxs-lookup"><span data-stu-id="8a961-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="8a961-105">Если вы решили полностью удалить Azure PowerShell, отправьте нам отзыв с помощью командлета [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="8a961-105">If you've decided to completely uninstall Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span> <span data-ttu-id="8a961-106">Если возникнет ошибка, мы будем признательны, если вы [сообщите о ней на GitHub](https://github.com/azure/azure-powershell/issues), чтобы мы исправили ее.</span><span class="sxs-lookup"><span data-stu-id="8a961-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-the-az-module"></a><span data-ttu-id="8a961-107">Удаление модуля Az</span><span class="sxs-lookup"><span data-stu-id="8a961-107">Uninstall the Az module</span></span>

<span data-ttu-id="8a961-108">Если в вашей системе установлен модуль Az и вы хотите удалить его, это можно сделать одним из двух методов.</span><span class="sxs-lookup"><span data-stu-id="8a961-108">If you have the Az module installed on your system and would like to uninstall it, there are two options.</span></span> <span data-ttu-id="8a961-109">Выбор метода зависит от того, как был установлен модуль Az.</span><span class="sxs-lookup"><span data-stu-id="8a961-109">Which method you follow depends on how you installed the Az module.</span></span> <span data-ttu-id="8a961-110">Если вы этого не знаете, сначала выполните инструкции по удалению для MSI.</span><span class="sxs-lookup"><span data-stu-id="8a961-110">If you're not sure of your original installation method, follow the MSI steps for uninstalling first.</span></span>

### <a name="option-1-uninstall-the-az-powershell-module-from-msi"></a><span data-ttu-id="8a961-111">Вариант 1. Удаление модуля Az PowerShell из MSI</span><span class="sxs-lookup"><span data-stu-id="8a961-111">Option 1: Uninstall the Az PowerShell module from MSI</span></span>

<span data-ttu-id="8a961-112">Если вы установили модуль Az PowerShell с помощью пакета MSI, удалять модуль нужно через систему Windows, а не PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8a961-112">If you installed Az PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="8a961-113">Платформа</span><span class="sxs-lookup"><span data-stu-id="8a961-113">Platform</span></span>         |                      <span data-ttu-id="8a961-114">Instructions</span><span class="sxs-lookup"><span data-stu-id="8a961-114">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="8a961-115">Windows 10</span><span class="sxs-lookup"><span data-stu-id="8a961-115">Windows 10</span></span>               | <span data-ttu-id="8a961-116">Пуск > Параметры > Приложения</span><span class="sxs-lookup"><span data-stu-id="8a961-116">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="8a961-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8a961-117">Windows 7</span></span> </br><span data-ttu-id="8a961-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8a961-118">Windows 8</span></span> | <span data-ttu-id="8a961-119">Пуск > Панель управления > Программы > Удалить программу</span><span class="sxs-lookup"><span data-stu-id="8a961-119">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="8a961-120">В этом окне в списке программ вы должны увидеть модуль **Azure PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="8a961-120">Once on this screen, you should see **Azure PowerShell** in the program listing.</span></span> <span data-ttu-id="8a961-121">Это программа, которую можно удалить.</span><span class="sxs-lookup"><span data-stu-id="8a961-121">This is the app to uninstall.</span></span> <span data-ttu-id="8a961-122">Если этой программы нет в списке, значит, она установлена с помощью PowerShellGet. Следуйте приведенным ниже инструкциям.</span><span class="sxs-lookup"><span data-stu-id="8a961-122">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="option-2-uninstall-the-az-powershell-module-from-powershellget"></a><span data-ttu-id="8a961-123">Вариант 2. Удаление модуля Az PowerShell из PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="8a961-123">Option 2: Uninstall the Az PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="8a961-124">Чтобы удалить модули Az, используйте командлет [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="8a961-124">To uninstall the Az modules, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="8a961-125">Учтите, что `Uninstall-Module` удаляет только один модуль.</span><span class="sxs-lookup"><span data-stu-id="8a961-125">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="8a961-126">Чтобы полностью удалить модуль Az PowerShell, каждый модуль нужно удалять отдельно.</span><span class="sxs-lookup"><span data-stu-id="8a961-126">To remove the Az PowerShell module completely, you must uninstall each module individually.</span></span> <span data-ttu-id="8a961-127">Удаление может усложниться, если у вас установлено несколько версий Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8a961-127">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="8a961-128">Чтобы проверить, какие версии модуля Az PowerShell у вас установлены, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="8a961-128">To check which versions of the Az PowerShell module you've installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

<span data-ttu-id="8a961-129">Следующий скрипт запрашивает из коллекции PowerShell список зависимых подмодулей,</span><span class="sxs-lookup"><span data-stu-id="8a961-129">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="8a961-130">а затем удаляет правильную версию каждого подмодуля.</span><span class="sxs-lookup"><span data-stu-id="8a961-130">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="8a961-131">Для запуска этого скрипта в области, отличающейся от **Процесс** или **Текущий пользователь**, требуются права доступа администратора.</span><span class="sxs-lookup"><span data-stu-id="8a961-131">You need to have administrator access to run this script in a scope other than **Process** or **Current User**.</span></span>

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

<span data-ttu-id="8a961-132">Чтобы воспользоваться этой функцией, скопируйте и вставьте этот код в окно сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8a961-132">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="8a961-133">В примере ниже показано, как выполнить функцию для удаления предыдущей версии модуля Az PowerShell и его подмодулей.</span><span class="sxs-lookup"><span data-stu-id="8a961-133">The following example shows how to run the function to remove an older version of the Az PowerShell module and its submodules.</span></span>

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

<span data-ttu-id="8a961-134">Во время выполнения скрипта в окне будут отображаться **имя**, **версия** и **состояние** каждого удаляемого подмодуля.</span><span class="sxs-lookup"><span data-stu-id="8a961-134">As the script runs, it displays the **Name**, **Version**, and **State** of each submodule that is being uninstalled.</span></span> <span data-ttu-id="8a961-135">Чтобы запустить скрипт только для просмотра удаляемых компонентов без их удаления, используйте параметр `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="8a961-135">To run the script to only see what would be deleted, without removing it, specify the `-WhatIf` parameter.</span></span>

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
> <span data-ttu-id="8a961-136">Если скрипт не может сопоставить определенную зависимость с версией для удаления, _ни одна_ из версий этой зависимости не будет удалена.</span><span class="sxs-lookup"><span data-stu-id="8a961-136">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependency.</span></span> <span data-ttu-id="8a961-137">Это обусловлено тем, что на компьютере могут быть установлены другие версии целевого модуля, связанные с этими зависимостями.</span><span class="sxs-lookup"><span data-stu-id="8a961-137">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span>

<span data-ttu-id="8a961-138">Выполните следующий пример для каждой версии модуля Az PowerShell, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="8a961-138">Run the following example for every version of the Az PowerShell module that you want to uninstall.</span></span>
<span data-ttu-id="8a961-139">Для удобства следующий скрипт удалит все версии Az, **кроме** последней.</span><span class="sxs-lookup"><span data-stu-id="8a961-139">For convenience, the following script uninstalls all versions of Az **except** for the latest.</span></span>

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions |
    Sort-Object -Property Version -Descending |
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="8a961-140">Удаление модуля AzureRM</span><span class="sxs-lookup"><span data-stu-id="8a961-140">Uninstall the AzureRM module</span></span>

<span data-ttu-id="8a961-141">Если в вашей системе установлен модуль Az и вы хотите удалить AzureRM, это можно сделать одним из двух методов.</span><span class="sxs-lookup"><span data-stu-id="8a961-141">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options.</span></span> <span data-ttu-id="8a961-142">Выбор метода зависит от того, как был установлен модуль AzureRM.</span><span class="sxs-lookup"><span data-stu-id="8a961-142">Which method you follow depends on how you installed the AzureRM module.</span></span> <span data-ttu-id="8a961-143">Если вы этого не знаете, сначала выполните инструкции по удалению для MSI.</span><span class="sxs-lookup"><span data-stu-id="8a961-143">If you're not sure of your original installation method, follow the MSI steps for uninstalling first.</span></span>

### <a name="option-1-uninstall-the-azurerm-powershell-module-from-msi"></a><span data-ttu-id="8a961-144">Вариант 1. Удаление модуля AzureRM PowerShell из MSI</span><span class="sxs-lookup"><span data-stu-id="8a961-144">Option 1: Uninstall the AzureRM PowerShell module from MSI</span></span>

<span data-ttu-id="8a961-145">Если вы установили модуль AzureRM PowerShell с помощью пакета MSI, удалять модуль нужно через систему Windows, а не PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8a961-145">If you installed the AzureRM PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="8a961-146">Платформа</span><span class="sxs-lookup"><span data-stu-id="8a961-146">Platform</span></span>         |                      <span data-ttu-id="8a961-147">Instructions</span><span class="sxs-lookup"><span data-stu-id="8a961-147">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="8a961-148">Windows 10</span><span class="sxs-lookup"><span data-stu-id="8a961-148">Windows 10</span></span>               | <span data-ttu-id="8a961-149">Пуск > Параметры > Приложения</span><span class="sxs-lookup"><span data-stu-id="8a961-149">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="8a961-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8a961-150">Windows 7</span></span> </br><span data-ttu-id="8a961-151">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8a961-151">Windows 8</span></span> | <span data-ttu-id="8a961-152">Пуск > Панель управления > Программы > Удалить программу</span><span class="sxs-lookup"><span data-stu-id="8a961-152">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="8a961-153">В этом окне в списке программ вы должны увидеть **Azure PowerShell** или **Microsoft Azure PowerShell — месяц год**.</span><span class="sxs-lookup"><span data-stu-id="8a961-153">Once on this screen, you should see **Azure PowerShell** or **Microsoft Azure PowerShell - Month Year** in the program listing.</span></span> <span data-ttu-id="8a961-154">Это программа, которую можно удалить.</span><span class="sxs-lookup"><span data-stu-id="8a961-154">This is the app to uninstall.</span></span> <span data-ttu-id="8a961-155">Если этой программы нет в списке, значит, она установлена с помощью PowerShellGet. Следуйте приведенным ниже инструкциям.</span><span class="sxs-lookup"><span data-stu-id="8a961-155">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="option-2-uninstall-the-azurerm-powershell-module-from-powershellget"></a><span data-ttu-id="8a961-156">Вариант 2. Удаление модуля AzureRM PowerShell из PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="8a961-156">Option 2: Uninstall the AzureRM PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="8a961-157">Если вы установили AzureRM с помощью PowerShellGet, вы можете удалить модули с помощью командлета [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), доступного в модуле `Az.Accounts`.</span><span class="sxs-lookup"><span data-stu-id="8a961-157">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet, available as part of the `Az.Accounts` module.</span></span>

<span data-ttu-id="8a961-158">Чтобы использовать модуль `Az.Accounts`, необходимо установить модуль Az.</span><span class="sxs-lookup"><span data-stu-id="8a961-158">In order to use the `Az.Accounts` module, you will need to have the Az module installed.</span></span>  <span data-ttu-id="8a961-159">Одновременное использование модуля AzureRM и модуля Az не поддерживается. Но с помощью модуля Az можно немедленно удалить модуль AzureRM.</span><span class="sxs-lookup"><span data-stu-id="8a961-159">Having both the AzureRM and the Az modules installed at the same time is not supported however the Az module can be used to immediately uninstall the AzureRM module.</span></span>  <span data-ttu-id="8a961-160">Вы можете установить модуль Az и пропустить предупреждение модуля AzureRM с помощью следующей команды (если модуль Az еще не установлен):</span><span class="sxs-lookup"><span data-stu-id="8a961-160">You can install the Az module and bypass the AzureRM module warning with the following command if you do not have the Az module installed already:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="8a961-161">После установки модуля Az можно удалить _все_ модули AzureRM с компьютера с помощью приведенной ниже команды.</span><span class="sxs-lookup"><span data-stu-id="8a961-161">Once the Az module is installed, the following command removes _all_ AzureRM modules from your machine.</span></span> <span data-ttu-id="8a961-162">Для ее выполнения требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="8a961-162">It requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```
