---
title: Автоматическая миграция скриптов PowerShell из AzureRM в модуль Az PowerShell
description: Узнайте, как выполнить автоматическую миграцию скриптов PowerShell из AzureRM в модуль Az PowerShell.
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 09/11/2020
ms.openlocfilehash: d342ca65baf7664f430de3b7d294c0fc9815c0a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "92002340"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a><span data-ttu-id="369f4-103">Краткое руководство. Автоматическая миграция скриптов PowerShell из AzureRM в модуль Az PowerShell</span><span class="sxs-lookup"><span data-stu-id="369f4-103">Quickstart: Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module</span></span>

<span data-ttu-id="369f4-104">В этой статье показано, как использовать модуль Az.Tools.Migration PowerShell для автоматической миграции скриптов PowerShell и модулей скриптов из AzureRM в модуль Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="369f4-104">In this article, you'll learn how to use the Az.Tools.Migration PowerShell module to automatically upgrade your PowerShell scripts and script modules from AzureRM to the Az PowerShell module.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="369f4-105">Модуль PowerShell Az.Tools.Migration сейчас предоставляется в общедоступной предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="369f4-105">The Az.Tools.Migration PowerShell module is currently in public preview.</span></span> <span data-ttu-id="369f4-106">Эта предварительная версия предоставляется без соглашения об уровне обслуживания.</span><span class="sxs-lookup"><span data-stu-id="369f4-106">This preview version is provided without a service level agreement.</span></span> <span data-ttu-id="369f4-107">Эта версия не рекомендуется для использования с рабочими нагрузками в производственной среде.</span><span class="sxs-lookup"><span data-stu-id="369f4-107">It's not recommended for production workloads.</span></span> <span data-ttu-id="369f4-108">Некоторые функции могут не поддерживаться или их возможности могут быть ограничены.</span><span class="sxs-lookup"><span data-stu-id="369f4-108">Certain features might not be supported or might have constrained capabilities.</span></span> <span data-ttu-id="369f4-109">Дополнительные сведения см. в статье [Дополнительные условия использования предварительных выпусков Microsoft Azure](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span><span class="sxs-lookup"><span data-stu-id="369f4-109">For more information, see [Supplemental Terms of Use for Microsoft Azure Previews](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span></span>

<span data-ttu-id="369f4-110">Вы можете оставить свой отзыв и сообщить о проблемах, связанных с модулем Az.Tools.Migration PowerShell, в разделе [проблем GitHub](https://github.com/Azure/azure-powershell-migration/issues) в репозитории `azure-powershell-migration`.</span><span class="sxs-lookup"><span data-stu-id="369f4-110">Report feedback and issues about the Az.Tools.Migration PowerShell module via [a GitHub issue](https://github.com/Azure/azure-powershell-migration/issues) in the `azure-powershell-migration` repository.</span></span>

## <a name="requirements"></a><span data-ttu-id="369f4-111">Требования</span><span class="sxs-lookup"><span data-stu-id="369f4-111">Requirements</span></span>

* <span data-ttu-id="369f4-112">Обновите существующие скрипты PowerShell до последней версии [модуля AzureRM PowerShell (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span><span class="sxs-lookup"><span data-stu-id="369f4-112">Update your existing PowerShell scripts to the latest version of the [AzureRM PowerShell module (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span>
* <span data-ttu-id="369f4-113">Установите модуль Az.Tools.Migration PowerShell.</span><span class="sxs-lookup"><span data-stu-id="369f4-113">Install the Az.Tools.Migration PowerShell module.</span></span>

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a><span data-ttu-id="369f4-114">Шаг 1. Создание плана обновления</span><span class="sxs-lookup"><span data-stu-id="369f4-114">Step 1: Generate an upgrade plan</span></span>

<span data-ttu-id="369f4-115">Используйте командлет `New-AzUpgradeModulePlan`, чтобы создать план обновления для переноса скриптов и модулей в модуль Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="369f4-115">You use the `New-AzUpgradeModulePlan` cmdlet to generate an upgrade plan for migrating your scripts and modules to the Az PowerShell module.</span></span> <span data-ttu-id="369f4-116">В этом плане обновления указан конкретный файл и точки смещения, которые нужно изменить при переходе от AzureRM к командлетам Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="369f4-116">The upgrade plan details the specific file and offset points that require changes when moving from AzureRM to the Az PowerShell cmdlets.</span></span>

> [!NOTE]
> <span data-ttu-id="369f4-117">Командлет `New-AzUpgradeModulePlan` не выполняет план, а только создает только шаги по обновлению.</span><span class="sxs-lookup"><span data-stu-id="369f4-117">The `New-AzUpgradeModulePlan` cmdlet doesn't execute the plan, it only generates the upgrade steps.</span></span>

```powershell
#  Generate an upgrade plan for the specified PowerShell script and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -FilePath 'C:\Scripts\my-azure-script.ps1'
```

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts'
```

<span data-ttu-id="369f4-118">Проверьте результаты плана обновления.</span><span class="sxs-lookup"><span data-stu-id="369f4-118">Review the results of the upgrade plan.</span></span>

```powershell
# Show the entire upgrade plan
$Plan
```

<span data-ttu-id="369f4-119">Выполните следующую команду, чтобы отфильтровать результаты по командам с предупреждениями или ошибками.</span><span class="sxs-lookup"><span data-stu-id="369f4-119">Run the following command to filter the results to commands that have warnings or errors.</span></span> <span data-ttu-id="369f4-120">Это может быть удобным в больших результирующих наборах для быстрого поиска ошибок перед выполнением обновления.</span><span class="sxs-lookup"><span data-stu-id="369f4-120">This may be helpful on large result sets to quickly identify errors before performing the upgrade.</span></span>

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

## <a name="step-2-perform-the-upgrade"></a><span data-ttu-id="369f4-121">Шаг 2. выполнение обновления.</span><span class="sxs-lookup"><span data-stu-id="369f4-121">Step 2: Perform the upgrade</span></span>

<span data-ttu-id="369f4-122">План обновления выполняется при запуске командлета `Invoke-AzUpgradeModulePlan`.</span><span class="sxs-lookup"><span data-stu-id="369f4-122">The upgrade plan is executed when you run the `Invoke-AzUpgradeModulePlan` cmdlet.</span></span> <span data-ttu-id="369f4-123">Эта команда выполняет обновление указанных файлов или папок, кроме всех файлов и папок с ошибками, обнаруженными командлетом `New-AzUpgradeModulePlan`.</span><span class="sxs-lookup"><span data-stu-id="369f4-123">This command performs an upgrade of the specified file or folders except for any errors that were identified by the `New-AzUpgradeModulePlan` cmdlet.</span></span>

<span data-ttu-id="369f4-124">Для этой команды нужно указать, следует ли изменять файлы на месте или сохранять новые файлы вместе с исходными файлами (сохраняя исходные файлы без изменений).</span><span class="sxs-lookup"><span data-stu-id="369f4-124">This command requires you to specify if the files should be modified in place or if new files should be saved alongside your original files (leaving originals unmodified).</span></span>

> [!CAUTION]
> <span data-ttu-id="369f4-125">Операция отмены не предусмотрена.</span><span class="sxs-lookup"><span data-stu-id="369f4-125">There is no undo operation.</span></span> <span data-ttu-id="369f4-126">Обязательно убедитесь, что существует резервная копия скриптов и модулей PowerShell, которые вы пытаетесь обновить.</span><span class="sxs-lookup"><span data-stu-id="369f4-126">Always ensure that you have a backup copy of your PowerShell scripts and modules that you're attempting to upgrade.</span></span>

> [!WARNING]
> <span data-ttu-id="369f4-127">Действие командлета `Invoke-AzUpgradeModulePlan` может оказаться разрушительным, если указан параметр `-FileEditMode ModifyExistingFiles`!</span><span class="sxs-lookup"><span data-stu-id="369f4-127">The `Invoke-AzUpgradeModulePlan` cmdlet is destructive when the `-FileEditMode ModifyExistingFiles` option is specified!</span></span> <span data-ttu-id="369f4-128">Это приведет к изменению скриптов и функций "на месте" в соответствии с планом обновления модуля, созданным командлетом `New-AzUpgradeModulePlan`.</span><span class="sxs-lookup"><span data-stu-id="369f4-128">It modifies your scripts and functions in place according to the module upgrade plan generated by the `New-AzUpgradeModulePlan` cmdlet.</span></span> <span data-ttu-id="369f4-129">Чтобы сохранить возможность восстановить прежнее состояние, укажите параметр `-FileEditMode SaveChangesToNewFiles`.</span><span class="sxs-lookup"><span data-stu-id="369f4-129">For the non-destructive option specify `-FileEditMode SaveChangesToNewFiles` instead.</span></span>

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
$Results = Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles
```

<span data-ttu-id="369f4-130">Проверьте результаты операции обновления.</span><span class="sxs-lookup"><span data-stu-id="369f4-130">Review the results of the upgrade operation.</span></span>

```powershell
# Show the results for the entire upgrade operation
$Results
```

<span data-ttu-id="369f4-131">Если в результатах будут ошибки, их можно изучить с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="369f4-131">If any errors are returned, you can take a closer look at the error results with the following command:</span></span>

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

## <a name="limitations"></a><span data-ttu-id="369f4-132">Ограничения</span><span class="sxs-lookup"><span data-stu-id="369f4-132">Limitations</span></span>

* <span data-ttu-id="369f4-133">Автоматическое обновление имени параметра в формат параметров с символом @ не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="369f4-133">Automated parameter name updates to splatted parameter sets aren't supported.</span></span> <span data-ttu-id="369f4-134">Если такие параметры будут обнаружены во время создания плана обновления, отобразится предупреждение.</span><span class="sxs-lookup"><span data-stu-id="369f4-134">If any are found during upgrade plan generation, a warning is returned.</span></span>
* <span data-ttu-id="369f4-135">Операции файлового ввода-вывода используют кодировку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="369f4-135">File I/O operations use default encoding.</span></span> <span data-ttu-id="369f4-136">Нетипичные сценарии использования кодировки файлов могут вызвать проблемы.</span><span class="sxs-lookup"><span data-stu-id="369f4-136">Unusual file encoding situations may cause problems.</span></span>
* <span data-ttu-id="369f4-137">Командлеты AzureRM, переданные в качестве аргументов в инструкции макетирования модульного тестирования Pester, не обнаруживаются.</span><span class="sxs-lookup"><span data-stu-id="369f4-137">AzureRM cmdlets passed as arguments to Pester unit test mock statements aren't detected.</span></span>
* <span data-ttu-id="369f4-138">Сейчас в качестве целевого объекта поддерживается только модуль Az PowerShell версии 4.6.1.</span><span class="sxs-lookup"><span data-stu-id="369f4-138">Currently, only Az PowerShell module version 4.6.1 is supported as a target.</span></span>

## <a name="next-steps"></a><span data-ttu-id="369f4-139">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="369f4-139">Next steps</span></span>

<span data-ttu-id="369f4-140">Дополнительные сведения о модуле Az PowerShell см. в [документации по Azure PowerShell](https://docs.microsoft.com/powershell/azure/).</span><span class="sxs-lookup"><span data-stu-id="369f4-140">To learn more about the Az PowerShell module, see the [Azure PowerShell documentation](https://docs.microsoft.com/powershell/azure/)</span></span>