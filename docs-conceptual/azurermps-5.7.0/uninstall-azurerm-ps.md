---
title: Удаление Azure PowerShell
description: Сведения о том, как полностью удалить Azure PowerShell.
ms.date: 06/10/2019
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 17a9b604da84f131c434e3001732a34f7d620fbd
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243588"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="719c8-103">Удаление модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="719c8-103">Uninstall the Azure PowerShell module</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="719c8-104">Из этой статьи вы узнаете, как удалить предыдущую версию Azure PowerShell или полностью удалить этот модуль из системы.</span><span class="sxs-lookup"><span data-stu-id="719c8-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="719c8-105">Если вы решили полностью удалить Azure PowerShell, отправьте нам отзыв с помощью командлета [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="719c8-105">If you've decided to completely uninstall the Azure PowerShell, please give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="719c8-106">Если возникнет ошибка, мы будем признательны, если вы [сообщите о ней на GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="719c8-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-msi-or-web-platform-installer"></a><span data-ttu-id="719c8-107">Удаление пакета MSI или установщика веб-платформы</span><span class="sxs-lookup"><span data-stu-id="719c8-107">Uninstall MSI or Web Platform Installer</span></span>

<span data-ttu-id="719c8-108">Если вы установили Azure PowerShell с помощью пакета MSI или установщика веб-платформы, удалять модуль нужно из системы Windows, а не с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="719c8-108">If you installed Azure PowerShell using the MSI package or the Web Platform Installer, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="719c8-109">Платформа</span><span class="sxs-lookup"><span data-stu-id="719c8-109">Platform</span></span> | <span data-ttu-id="719c8-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="719c8-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="719c8-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="719c8-111">Windows 10</span></span> | <span data-ttu-id="719c8-112">Пуск > Параметры > Приложения</span><span class="sxs-lookup"><span data-stu-id="719c8-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="719c8-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="719c8-113">Windows 7</span></span> </br><span data-ttu-id="719c8-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="719c8-114">Windows 8</span></span> | <span data-ttu-id="719c8-115">Пуск > Панель управления > Программы > Удалить программу</span><span class="sxs-lookup"><span data-stu-id="719c8-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="719c8-116">В этом окне в списке программ вы должны увидеть модуль Azure PowerShell, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="719c8-116">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="719c8-117">Удаление с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="719c8-117">Uninstall from PowerShell</span></span>

<span data-ttu-id="719c8-118">Если вы установили Azure PowerShell с помощью PowerShellGet, для удаления можно использовать командлет [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="719c8-118">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="719c8-119">Учтите, что `Uninstall-Module` удаляет только один модуль.</span><span class="sxs-lookup"><span data-stu-id="719c8-119">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="719c8-120">Чтобы полностью удалить Azure PowerShell, каждый модуль нужно удалять отдельно.</span><span class="sxs-lookup"><span data-stu-id="719c8-120">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="719c8-121">Удаление может усложниться, если у вас установлено несколько версий Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="719c8-121">Uninstallation can be complicated if you have multiple versions of Azure PowerShell installed.</span></span>

<span data-ttu-id="719c8-122">Ниже приведен скрипт, с помощью которого можно полностью удалить одну версию Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="719c8-122">You use the following script can be used to completely remove a single version of Azure PowerShell.</span></span> <span data-ttu-id="719c8-123">Скрипт запрашивает из коллекции PowerShell список зависимых подмодулей,</span><span class="sxs-lookup"><span data-stu-id="719c8-123">The script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="719c8-124">а затем удаляет правильную версию каждого подмодуля.</span><span class="sxs-lookup"><span data-stu-id="719c8-124">Then, the script uninstalls the correct version of each submodule.</span></span>

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

<span data-ttu-id="719c8-125">Чтобы воспользоваться этой функцией, скопируйте и вставьте этот код в окно сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="719c8-125">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="719c8-126">В примере ниже показано, как запустить функцию, чтобы удалить предыдущую версию Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="719c8-126">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="719c8-127">Во время выполнения скрипта в окне будут отображаться имя и версия каждого удаляемого подмодуля.</span><span class="sxs-lookup"><span data-stu-id="719c8-127">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="719c8-128">Чтобы запустить скрипт для просмотра только удаляемых компонентов без удаления, используйте параметр `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="719c8-128">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

> [!NOTE]
> <span data-ttu-id="719c8-129">Если скрипт не может сопоставить определенную зависимость с версией для удаления, _ни одна_ из версий этой зависимости не будет удалена.</span><span class="sxs-lookup"><span data-stu-id="719c8-129">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="719c8-130">Это обусловлено тем, что на компьютере могут быть установлены другие версии целевого модуля, связанные с этими зависимостями.</span><span class="sxs-lookup"><span data-stu-id="719c8-130">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="719c8-131">В этом случае перечисляются доступные версии зависимости.</span><span class="sxs-lookup"><span data-stu-id="719c8-131">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="719c8-132">После этого вы можете вручную удалить любые предыдущие версии с помощью `Uninstall-Module`.</span><span class="sxs-lookup"><span data-stu-id="719c8-132">You can then remove any old versions manually with `Uninstall-Module`.</span></span>


<span data-ttu-id="719c8-133">Выполните эту команду для каждой версии Azure PowerShell, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="719c8-133">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="719c8-134">Для удобства следующий скрипт удалит все версии AzureRM __за исключением__ последней.</span><span class="sxs-lookup"><span data-stu-id="719c8-134">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
