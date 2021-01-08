---
title: Автоматическая миграция скриптов PowerShell из AzureRM в модуль Az PowerShell
description: Узнайте, как выполнить автоматическую миграцию скриптов PowerShell из AzureRM в модуль Az PowerShell
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 12/18/2020
ms.openlocfilehash: 57218c130f172bc359334b83db16e5790fa5562c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "97893334"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a><span data-ttu-id="597e2-103">Краткое руководство. Автоматическая миграция скриптов PowerShell из AzureRM в модуль Az PowerShell</span><span class="sxs-lookup"><span data-stu-id="597e2-103">Quickstart: Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module</span></span>

<span data-ttu-id="597e2-104">В этой статье показано, как использовать модуль Az.Tools.Migration PowerShell для автоматической миграции скриптов PowerShell и модулей скриптов из AzureRM в модуль Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="597e2-104">In this article, you'll learn how to use the Az.Tools.Migration PowerShell module to automatically upgrade your PowerShell scripts and script modules from AzureRM to the Az PowerShell module.</span></span> <span data-ttu-id="597e2-105">Дополнительные варианты миграции см. в статье [Перенос Azure PowerShell с AzureRM на Az](/powershell/azure/migrate-from-azurerm-to-az).</span><span class="sxs-lookup"><span data-stu-id="597e2-105">For additional migration options, see [Migrate Azure PowerShell from AzureRM to Az](/powershell/azure/migrate-from-azurerm-to-az).</span></span>

## <a name="requirements"></a><span data-ttu-id="597e2-106">Требования</span><span class="sxs-lookup"><span data-stu-id="597e2-106">Requirements</span></span>

* <span data-ttu-id="597e2-107">Обновите существующие скрипты PowerShell до последней версии [модуля AzureRM PowerShell (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span><span class="sxs-lookup"><span data-stu-id="597e2-107">Update your existing PowerShell scripts to the latest version of the [AzureRM PowerShell module (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span>
* <span data-ttu-id="597e2-108">Установите модуль Az.Tools.Migration PowerShell.</span><span class="sxs-lookup"><span data-stu-id="597e2-108">Install the Az.Tools.Migration PowerShell module.</span></span>

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a><span data-ttu-id="597e2-109">Шаг 1. Создание плана обновления</span><span class="sxs-lookup"><span data-stu-id="597e2-109">Step 1: Generate an upgrade plan</span></span>

<span data-ttu-id="597e2-110">Используйте командлет **`New-AzUpgradeModulePlan`** , чтобы создать план обновления для переноса скриптов и модулей в модуль Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="597e2-110">You use the **`New-AzUpgradeModulePlan`** cmdlet to generate an upgrade plan for migrating your scripts and modules to the Az PowerShell module.</span></span> <span data-ttu-id="597e2-111">Этот командлет не вносит никаких изменений в существующие скрипты.</span><span class="sxs-lookup"><span data-stu-id="597e2-111">This cmdlet doesn’t make any changes to your existing scripts.</span></span> <span data-ttu-id="597e2-112">Используйте параметр **`FilePath`** для определенного скрипта или параметр **`DirectoryPath`** для выбора всех скриптов в определенной папке.</span><span class="sxs-lookup"><span data-stu-id="597e2-112">Use the **`FilePath`** parameter for targeting a specific script or the **`DirectoryPath`** parameter for targeting all scripts in a specific folder.</span></span>

> [!NOTE]
> <span data-ttu-id="597e2-113">Командлет **`New-AzUpgradeModulePlan`** не выполняет план, а только создает только шаги по обновлению.</span><span class="sxs-lookup"><span data-stu-id="597e2-113">The **`New-AzUpgradeModulePlan`** cmdlet doesn't execute the plan, it only generates the upgrade steps.</span></span>

<span data-ttu-id="597e2-114">В следующем примере создается план для всех скриптов в папке _`C:\Scripts`_ .</span><span class="sxs-lookup"><span data-stu-id="597e2-114">The following example generates a plan for all the scripts in the _`C:\Scripts`_ folder.</span></span> <span data-ttu-id="597e2-115">Параметр **`OutVariable`** указан, поэтому результаты возвращаются и сохраняются в переменной с именем **`Plan`** .</span><span class="sxs-lookup"><span data-stu-id="597e2-115">The **`OutVariable`** parameter is specified so the results are returned and simultaneously stored in a variable named **`Plan`**.</span></span>

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 5.2.0 -DirectoryPath 'C:\Scripts' -OutVariable Plan
```

<span data-ttu-id="597e2-116">Как показано в следующих выходных данных, в этом плане обновления указан определенный файл и точки смещения, которые нужно изменить при переходе от AzureRM к командлетам Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="597e2-116">As shown in the following output, the upgrade plan details the specific file and offset points that require changes when moving from AzureRM to the Az PowerShell cmdlets.</span></span>

```Output
Order Location                                                   UpgradeType     PlanResult             Original
----- --------                                                   -----------     ----------             --------
1     compute-create-dockerhost.ps1:59:24                        CmdletParameter ReadyToUpgrade         ExtensionName
2     compute-create-dockerhost.ps1:59:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
3     compute-create-dockerhost.ps1:54:1                         Cmdlet          ReadyToUpgrade         New-AzureRmVM
4     compute-create-dockerhost.ps1:51:1                         Cmdlet          ReadyToUpgrade         Add-AzureRmVM...
5     compute-create-dockerhost.ps1:47:1                         Cmdlet          ReadyToUpgrade         Add-AzureRmVM...
6     compute-create-dockerhost.ps1:46:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
7     compute-create-dockerhost.ps1:45:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
8     compute-create-dockerhost.ps1:44:13                        Cmdlet          ReadyToUpgrade         New-AzureRmVM...
9     compute-create-dockerhost.ps1:40:8                         Cmdlet          ReadyToUpgrade         New-AzureRmNe...
10    compute-create-dockerhost.ps1:36:8                         Cmdlet          ReadyToUpgrade         New-AzureRmNe...
11    compute-create-dockerhost.ps1:31:16                        Cmdlet          ReadyToUpgrade         New-AzureRmNe...
12    compute-create-dockerhost.ps1:26:15                        Cmdlet          ReadyToUpgrade         New-AzureRmNe...
13    compute-create-dockerhost.ps1:22:8                         Cmdlet          ReadyToUpgrade         New-AzureRmPu...
14    compute-create-dockerhost.ps1:18:9                         Cmdlet          ReadyToUpgrade         New-AzureRmVi...
15    compute-create-dockerhost.ps1:15:17                        Cmdlet          ReadyToUpgrade         New-AzureRmVi...
16    compute-create-dockerhost.ps1:12:1                         Cmdlet          ReadyToUpgrade         New-AzureRmRe...
17    compute-create-windowsvm-quick.ps1:18:3                    CmdletParameter ReadyToUpgrade         ImageName
18    compute-create-windowsvm-quick.ps1:14:1                    Cmdlet          ReadyToUpgrade         New-AzureRmVM
19    compute-create-windowsvm-quick.ps1:11:1                    Cmdlet          ReadyToUpgrade         New-AzureRmRe...
20    compute-create-wordpress-mysql.ps1:59:24                   CmdletParameter ReadyToUpgrade         ExtensionName
...
```

<span data-ttu-id="597e2-117">Перед выполнением обновления необходимо просмотреть результаты плана для проблем.</span><span class="sxs-lookup"><span data-stu-id="597e2-117">Before performing the upgrade, you need to view the results of the plan for problems.</span></span> <span data-ttu-id="597e2-118">В следующем примере возвращается список скриптов и элементов в этих скриптах, которые не позволяют автоматически обновлять их.</span><span class="sxs-lookup"><span data-stu-id="597e2-118">The following example returns a list of scripts and the items in those scripts that will prevent them from being upgraded automatically.</span></span>

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

<span data-ttu-id="597e2-119">Элементы, показанные в следующих выходных данных, не будут обновляться автоматически без предварительного устранения проблем.</span><span class="sxs-lookup"><span data-stu-id="597e2-119">The items shown in the following output will not be upgraded automatically without manually correcting the issues first.</span></span>

```Output
Order                  : 42
UpgradeType            : CmdletParameter
PlanResult             : ErrorParameterNotFound
PlanSeverity           : Error
PlanResultReason       : Parameter was not found in Get-AzResource or it's aliases.
SourceCommand          : CommandReference
SourceCommandParameter : CommandReferenceParameter
Location               : devtestlab-add-marketplace-image-to-lab.ps1:14:74
FullPath               : C:\Scripts\devtestlab-add-marketplace-image-to-lab.ps1
StartOffset            : 556
Original               : ResourceNameEquals
Replacement            :
```

## <a name="step-2-perform-the-upgrade"></a><span data-ttu-id="597e2-120">Шаг 2. Выполнение обновления</span><span class="sxs-lookup"><span data-stu-id="597e2-120">Step 2: Perform the upgrade</span></span>

> [!CAUTION]
> <span data-ttu-id="597e2-121">Операция отмены не предусмотрена.</span><span class="sxs-lookup"><span data-stu-id="597e2-121">There is no undo operation.</span></span> <span data-ttu-id="597e2-122">Обязательно убедитесь, что существует резервная копия скриптов и модулей PowerShell, которые вы пытаетесь обновить.</span><span class="sxs-lookup"><span data-stu-id="597e2-122">Always ensure that you have a backup copy of your PowerShell scripts and modules that you're attempting to upgrade.</span></span>

<span data-ttu-id="597e2-123">Когда вас будет устраивать план, обновление будет выполнено с помощью командлета **`Invoke-AzUpgradeModulePlan`** .</span><span class="sxs-lookup"><span data-stu-id="597e2-123">After you’re satisfied with the plan, the upgrade is performed with the **`Invoke-AzUpgradeModulePlan`** cmdlet.</span></span> <span data-ttu-id="597e2-124">Укажите **`SaveChangesToNewFiles`** для значения параметра **`FileEditMode`** , чтобы предотвратить внесение изменений в исходные скрипты.</span><span class="sxs-lookup"><span data-stu-id="597e2-124">Specify **`SaveChangesToNewFiles`** for the **`FileEditMode`** parameter value to prevent changes from being made to your original scripts.</span></span> <span data-ttu-id="597e2-125">При использовании этого режима обновление выполняется путем создания копии каждого скрипта, используемого с _`_az_upgraded`_ при добавлении к именам файлов.</span><span class="sxs-lookup"><span data-stu-id="597e2-125">When using this mode, the upgrade is performed by creating a copy of each script targeted with _`_az_upgraded`_ appended to the filenames.</span></span>

> [!WARNING]
> <span data-ttu-id="597e2-126">Действие командлета **`Invoke-AzUpgradeModulePlan`** может оказаться разрушительным, если указан параметр **`-FileEditMode ModifyExistingFiles`** !</span><span class="sxs-lookup"><span data-stu-id="597e2-126">The **`Invoke-AzUpgradeModulePlan`** cmdlet is destructive when the **`-FileEditMode ModifyExistingFiles`** option is specified!</span></span> <span data-ttu-id="597e2-127">Это приведет к непосредственному изменению скриптов и функций в соответствии с планом обновления модуля, созданным командлетом **`New-AzUpgradeModulePlan`** .</span><span class="sxs-lookup"><span data-stu-id="597e2-127">It modifies your scripts and functions in place according to the module upgrade plan generated by the **`New-AzUpgradeModulePlan`** cmdlet.</span></span> <span data-ttu-id="597e2-128">Чтобы сохранить возможность восстановить прежнее состояние, укажите параметр **`-FileEditMode SaveChangesToNewFiles`** .</span><span class="sxs-lookup"><span data-stu-id="597e2-128">For the non-destructive option specify **`-FileEditMode SaveChangesToNewFiles`** instead.</span></span>

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles -OutVariable Results
```

```Output
Order Location                                                   UpgradeType     UpgradeResult    Original
----- --------                                                   -----------     -------------    --------
1     compute-create-dockerhost.ps1:59:24                        CmdletParameter UpgradeCompleted ExtensionName
2     compute-create-dockerhost.ps1:59:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMExtens...
3     compute-create-dockerhost.ps1:54:1                         Cmdlet          UpgradeCompleted New-AzureRmVM
4     compute-create-dockerhost.ps1:51:1                         Cmdlet          UpgradeCompleted Add-AzureRmVMSshPub...
5     compute-create-dockerhost.ps1:47:1                         Cmdlet          UpgradeCompleted Add-AzureRmVMNetwor...
6     compute-create-dockerhost.ps1:46:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMSource...
7     compute-create-dockerhost.ps1:45:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMOperat...
8     compute-create-dockerhost.ps1:44:13                        Cmdlet          UpgradeCompleted New-AzureRmVMConfig
9     compute-create-dockerhost.ps1:40:8                         Cmdlet          UpgradeCompleted New-AzureRmNetworkI...
10    compute-create-dockerhost.ps1:36:8                         Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
11    compute-create-dockerhost.ps1:31:16                        Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
12    compute-create-dockerhost.ps1:26:15                        Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
13    compute-create-dockerhost.ps1:22:8                         Cmdlet          UpgradeCompleted New-AzureRmPublicIp...
14    compute-create-dockerhost.ps1:18:9                         Cmdlet          UpgradeCompleted New-AzureRmVirtualN...
15    compute-create-dockerhost.ps1:15:17                        Cmdlet          UpgradeCompleted New-AzureRmVirtualN...
16    compute-create-dockerhost.ps1:12:1                         Cmdlet          UpgradeCompleted New-AzureRmResource...
17    compute-create-windowsvm-quick.ps1:18:3                    CmdletParameter UpgradeCompleted ImageName
18    compute-create-windowsvm-quick.ps1:14:1                    Cmdlet          UpgradeCompleted New-AzureRmVM
19    compute-create-windowsvm-quick.ps1:11:1                    Cmdlet          UpgradeCompleted New-AzureRmResource...
20    compute-create-wordpress-mysql.ps1:59:24                   CmdletParameter UpgradeCompleted ExtensionName
...
```

<span data-ttu-id="597e2-129">Если в результатах будут ошибки, их можно изучить с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="597e2-129">If any errors are returned, you can take a closer look at the error results with the following command:</span></span>

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

```Output
Order                  : 42
UpgradeType            : CmdletParameter
UpgradeResult          : UnableToUpgrade
UpgradeSeverity        : Error
UpgradeResultReason    : Parameter was not found in Get-AzResource or it's aliases.
SourceCommand          : CommandReference
SourceCommandParameter : CommandReferenceParameter
Location               : devtestlab-add-marketplace-image-to-lab.ps1:14:74
FullPath               : C:\Scripts\devtestlab-add-marketplace-image-to-lab.ps1
StartOffset            : 556
Original               : ResourceNameEquals
Replacement            :
```

## <a name="limitations"></a><span data-ttu-id="597e2-130">Ограничения</span><span class="sxs-lookup"><span data-stu-id="597e2-130">Limitations</span></span>

* <span data-ttu-id="597e2-131">Операции файлового ввода-вывода используют кодировку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="597e2-131">File I/O operations use default encoding.</span></span> <span data-ttu-id="597e2-132">Нетипичные сценарии использования кодировки файлов могут вызвать проблемы.</span><span class="sxs-lookup"><span data-stu-id="597e2-132">Unusual file encoding situations may cause problems.</span></span>
* <span data-ttu-id="597e2-133">Командлеты AzureRM, переданные в качестве аргументов в инструкции макетирования модульного тестирования Pester, не обнаруживаются.</span><span class="sxs-lookup"><span data-stu-id="597e2-133">AzureRM cmdlets passed as arguments to Pester unit test mock statements aren't detected.</span></span>
* <span data-ttu-id="597e2-134">Сейчас в качестве целевого объекта поддерживается только модуль Az PowerShell версии 5.2.0.</span><span class="sxs-lookup"><span data-stu-id="597e2-134">Currently, only Az PowerShell module version 5.2.0 is supported as a target.</span></span>

## <a name="how-to-report-issues"></a><span data-ttu-id="597e2-135">Отправка сообщений о проблемах</span><span class="sxs-lookup"><span data-stu-id="597e2-135">How to report issues</span></span>

<span data-ttu-id="597e2-136">Вы можете оставить свой отзыв и сообщить о проблемах, связанных с модулем Az.Tools.Migration PowerShell, в разделе [проблем GitHub](https://github.com/Azure/azure-powershell-migration/issues) в репозитории `azure-powershell-migration`.</span><span class="sxs-lookup"><span data-stu-id="597e2-136">Report feedback and issues about the Az.Tools.Migration PowerShell module via [a GitHub issue](https://github.com/Azure/azure-powershell-migration/issues) in the `azure-powershell-migration` repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="597e2-137">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="597e2-137">Next steps</span></span>

<span data-ttu-id="597e2-138">Дополнительные сведения о модуле Az PowerShell см. в [документации по Azure PowerShell](/powershell/azure/).</span><span class="sxs-lookup"><span data-stu-id="597e2-138">To learn more about the Az PowerShell module, see the [Azure PowerShell documentation](/powershell/azure/)</span></span>
