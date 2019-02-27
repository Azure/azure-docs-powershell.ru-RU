---
title: Критические изменения для Microsoft Azure PowerShell 5.0.0
description: Это руководство по миграции содержит список критических изменений, внесенных в выпуск Azure PowerShell версии 5.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: b4cbeb1b523664fb49c4640eaafd56e3b843ebaa
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2019
ms.locfileid: "56145052"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a><span data-ttu-id="a58ec-103">Критические изменения для Microsoft Azure PowerShell 5.0.0</span><span class="sxs-lookup"><span data-stu-id="a58ec-103">Breaking changes for Microsoft Azure PowerShell 5.0.0</span></span>

<span data-ttu-id="a58ec-104">Этот документ предназначен для уведомления о критических изменениях и является руководством по миграции для пользователей командлетов Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a58ec-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="a58ec-105">В каждом разделе описана причина критического изменения и самый простой путь миграции.</span><span class="sxs-lookup"><span data-stu-id="a58ec-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="a58ec-106">Подробное описание см. в запросах на вытягивание для каждого изменения.</span><span class="sxs-lookup"><span data-stu-id="a58ec-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="a58ec-107">Оглавление</span><span class="sxs-lookup"><span data-stu-id="a58ec-107">Table of Contents</span></span>

- [<span data-ttu-id="a58ec-108">Критические изменения в командлетах ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a58ec-108">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
- [<span data-ttu-id="a58ec-109">Критические изменения в командлетах Batch</span><span class="sxs-lookup"><span data-stu-id="a58ec-109">Breaking changes to Batch cmdlets</span></span>](#breaking-changes-to-batch-cmdlets)
- [<span data-ttu-id="a58ec-110">Критические изменения в командлетах Compute</span><span class="sxs-lookup"><span data-stu-id="a58ec-110">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="a58ec-111">Критические изменения в командлетах EventHub</span><span class="sxs-lookup"><span data-stu-id="a58ec-111">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="a58ec-112">Критические изменения в командлетах Insights</span><span class="sxs-lookup"><span data-stu-id="a58ec-112">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="a58ec-113">Критические изменения в командлетах Network</span><span class="sxs-lookup"><span data-stu-id="a58ec-113">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="a58ec-114">Критические изменения в командлетах Resources</span><span class="sxs-lookup"><span data-stu-id="a58ec-114">Breaking changes to Resources cmdlets</span></span>](#breaking-changes-to-resources-cmdlets)
- [<span data-ttu-id="a58ec-115">Критические изменения в командлетах ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a58ec-115">Breaking Changes to ServiceBus Cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="a58ec-116">Критические изменения в командлетах ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a58ec-116">Breaking changes to ApiManagement cmdlets</span></span>

### <a name="new-azurermapimanagementbackendproxy"></a><span data-ttu-id="a58ec-117">**New-AzureRmApiManagementBackendProxy**</span><span class="sxs-lookup"><span data-stu-id="a58ec-117">**New-AzureRmApiManagementBackendProxy**</span></span>
- <span data-ttu-id="a58ec-118">Параметры UserName и Password заменены на PSCredential.</span><span class="sxs-lookup"><span data-stu-id="a58ec-118">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell-interactive
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a><span data-ttu-id="a58ec-119">**New-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="a58ec-119">**New-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="a58ec-120">Параметр Password заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="a58ec-120">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a><span data-ttu-id="a58ec-121">**Set-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="a58ec-121">**Set-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="a58ec-122">Параметр Password заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="a58ec-122">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a><span data-ttu-id="a58ec-123">Критические изменения в командлетах Batch</span><span class="sxs-lookup"><span data-stu-id="a58ec-123">Breaking changes to Batch cmdlets</span></span>

### <a name="new-azurebatchcertificate"></a><span data-ttu-id="a58ec-124">**New-AzureBatchCertificate**</span><span class="sxs-lookup"><span data-stu-id="a58ec-124">**New-AzureBatchCertificate**</span></span>
- <span data-ttu-id="a58ec-125">Параметр `Password` заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="a58ec-125">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a><span data-ttu-id="a58ec-126">**New-AzureBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="a58ec-126">**New-AzureBatchComputeNodeUser**</span></span>
- <span data-ttu-id="a58ec-127">Параметр `Password` заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="a58ec-127">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a><span data-ttu-id="a58ec-128">**Set-AzureRmBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="a58ec-128">**Set-AzureRmBatchComputeNodeUser**</span></span>
- <span data-ttu-id="a58ec-129">Параметр `Password` заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="a58ec-129">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a><span data-ttu-id="a58ec-130">**New-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="a58ec-130">**New-AzureBatchTask**</span></span>
 - <span data-ttu-id="a58ec-131">Переключатель `RunElevated` удален и заменен на `UserIdentity`.</span><span class="sxs-lookup"><span data-stu-id="a58ec-131">Removed the `RunElevated` switch and replaced it with `UserIdentity`.</span></span>

```powershell-interactive
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

<span data-ttu-id="a58ec-132">Это также касается свойства `RunElevated` в `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` и `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="a58ec-132">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="psmultiinstancesettings"></a><span data-ttu-id="a58ec-133">**PSMultiInstanceSettings**</span><span class="sxs-lookup"><span data-stu-id="a58ec-133">**PSMultiInstanceSettings**</span></span>

- <span data-ttu-id="a58ec-134">Конструктор `PSMultiInstanceSettings` больше не принимает обязательный параметр `numberOfInstances`. Вместо него он принимает обязательный параметр `coordinationCommandLine`.</span><span class="sxs-lookup"><span data-stu-id="a58ec-134">`PSMultiInstanceSettings` constructor no longer takes a required `numberOfInstances` parameter, instead it takes a required `coordinationCommandLine` parameter.</span></span>

```powershell-interactive
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a><span data-ttu-id="a58ec-135">**Get-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="a58ec-135">**Get-AzureBatchTask**</span></span>
 - <span data-ttu-id="a58ec-136">Удалено свойство `RunElevated` в `PSCloudTask`.</span><span class="sxs-lookup"><span data-stu-id="a58ec-136">Removed the `RunElevated` property on `PSCloudTask`.</span></span> <span data-ttu-id="a58ec-137">Добавлено свойство `UserIdentity` для замены `RunElevated`.</span><span class="sxs-lookup"><span data-stu-id="a58ec-137">The `UserIdentity` property has been added to replace `RunElevated`.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

<span data-ttu-id="a58ec-138">Это также касается свойства `RunElevated` в `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` и `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="a58ec-138">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="multiple-types"></a><span data-ttu-id="a58ec-139">**Несколько типов**</span><span class="sxs-lookup"><span data-stu-id="a58ec-139">**Multiple types**</span></span>

- <span data-ttu-id="a58ec-140">Свойство `SchedulingError` в `PSExitConditions` переименовано в `PreProcessingError`.</span><span class="sxs-lookup"><span data-stu-id="a58ec-140">Renamed the `SchedulingError` property on `PSExitConditions` to `PreProcessingError`.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a><span data-ttu-id="a58ec-141">**Несколько типов**</span><span class="sxs-lookup"><span data-stu-id="a58ec-141">**Multiple types**</span></span>

- <span data-ttu-id="a58ec-142">Свойство `SchedulingError` в `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` и `PSTaskExecutionInformation` переименовано в `FailureInformation`.</span><span class="sxs-lookup"><span data-stu-id="a58ec-142">Renamed the `SchedulingError` property on `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation`, and `PSTaskExecutionInformation` to `FailureInformation`.</span></span>
  - <span data-ttu-id="a58ec-143">`FailureInformation` возвращается при каждом сбое задачи.</span><span class="sxs-lookup"><span data-stu-id="a58ec-143">`FailureInformation` is returned any time there is a task failure.</span></span> <span data-ttu-id="a58ec-144">Сюда входят все предыдущие случаи ошибок планирования, а также коды завершения задач со значением, отличным от нуля, и ошибки передачи файлов из новой функции выходных файлов.</span><span class="sxs-lookup"><span data-stu-id="a58ec-144">This includes all previous scheduling error cases, as well as nonzero task exit codes, and file upload failures from the new output files feature.</span></span>
  - <span data-ttu-id="a58ec-145">Структура не изменилась, поэтому при использовании этого типа не нужно преобразовывать код.</span><span class="sxs-lookup"><span data-stu-id="a58ec-145">This is structured the same as before, so no code change is needed when using this type.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

<span data-ttu-id="a58ec-146">Это также касается Get-AzureBatchPool, Get-AzureBatchSubtask и Get-AzureBatchJobPreparationAndReleaseTaskStatus.</span><span class="sxs-lookup"><span data-stu-id="a58ec-146">This additionally impacts: Get-AzureBatchPool, Get-AzureBatchSubtask, and Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

### <a name="new-azurebatchpool"></a><span data-ttu-id="a58ec-147">**New-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="a58ec-147">**New-AzureBatchPool**</span></span>
 - <span data-ttu-id="a58ec-148">Параметр `TargetDedicated` удален и заменен на `TargetDedicatedComputeNodes` и `TargetLowPriorityComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="a58ec-148">Removed `TargetDedicated` and replaced it with `TargetDedicatedComputeNodes` and `TargetLowPriorityComputeNodes`.</span></span>
 - <span data-ttu-id="a58ec-149">Псевдоним `TargetDedicatedComputeNodes` — `TargetDedicated`.</span><span class="sxs-lookup"><span data-stu-id="a58ec-149">`TargetDedicatedComputeNodes` has an alias `TargetDedicated`.</span></span>

```powershell-interactive
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

<span data-ttu-id="a58ec-150">Это также касается Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="a58ec-150">This also impacts: Start-AzureBatchPoolResize</span></span>

### <a name="get-azurebatchpool"></a><span data-ttu-id="a58ec-151">**Get-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="a58ec-151">**Get-AzureBatchPool**</span></span>
 - <span data-ttu-id="a58ec-152">Свойства `TargetDedicated` и `CurrentDedicated` в `PSCloudPool` переименованы в `TargetDedicatedComputeNodes` и `CurrentDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="a58ec-152">Renamed the `TargetDedicated` and `CurrentDedicated` properties on `PSCloudPool` to `TargetDedicatedComputeNodes` and `CurrentDedicatedComputeNodes`.</span></span>

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicated
$pool.CurrentDedicated

# New
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicatedComputeNodes
$pool.CurrentDedicatedComputeNodes
```

### <a name="type-pscloudpool"></a><span data-ttu-id="a58ec-153">**Тип PSCloudPool**</span><span class="sxs-lookup"><span data-stu-id="a58ec-153">**Type PSCloudPool**</span></span>

- <span data-ttu-id="a58ec-154">Параметр `ResizeError` в `PSCloudPool` переименован в `ResizeErrors` и теперь является коллекцией.</span><span class="sxs-lookup"><span data-stu-id="a58ec-154">Renamed `ResizeError` to `ResizeErrors` on `PSCloudPool`, and it is now a collection.</span></span>

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a><span data-ttu-id="a58ec-155">**New-AzureBatchJob**</span><span class="sxs-lookup"><span data-stu-id="a58ec-155">**New-AzureBatchJob**</span></span>
- <span data-ttu-id="a58ec-156">Свойство `TargetDedicated` в `PSPoolSpecification` переименовано в `TargetDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="a58ec-156">Renamed the `TargetDedicated` property on `PSPoolSpecification` to `TargetDedicatedComputeNodes`.</span></span>

```powershell-interactive
# Old
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicated = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo

# New
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicatedComputeNodes = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo
```

### <a name="get-azurebatchnodefile"></a><span data-ttu-id="a58ec-157">**Get-AzureBatchNodeFile**</span><span class="sxs-lookup"><span data-stu-id="a58ec-157">**Get-AzureBatchNodeFile**</span></span>
 - <span data-ttu-id="a58ec-158">Параметр `Name` удален и заменен на `Path`.</span><span class="sxs-lookup"><span data-stu-id="a58ec-158">Removed `Name` and replaced it with `Path`.</span></span>
 - <span data-ttu-id="a58ec-159">Псевдоним `Path` — `Name`.</span><span class="sxs-lookup"><span data-stu-id="a58ec-159">`Path` has an alias `Name`.</span></span>

```powershell-interactive
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

<span data-ttu-id="a58ec-160">Это также касается Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="a58ec-160">This also impacts: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span></span>

### <a name="type-psnodefile"></a><span data-ttu-id="a58ec-161">Тип **PSNodeFile**</span><span class="sxs-lookup"><span data-stu-id="a58ec-161">Type **PSNodeFile**</span></span>

 - <span data-ttu-id="a58ec-162">Свойство `Name` в `PSNodeFile` переименовано в `Path`.</span><span class="sxs-lookup"><span data-stu-id="a58ec-162">Renamed the `Name` property on `PSNodeFile` to `Path`.</span></span>

```powershell-interactive
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a><span data-ttu-id="a58ec-163">**Get-AzureBatchSubtask**</span><span class="sxs-lookup"><span data-stu-id="a58ec-163">**Get-AzureBatchSubtask**</span></span>
- <span data-ttu-id="a58ec-164">Свойства `PreviousState` и `State` для `PSSubtaskInformation` больше не относятся к типу `TaskState`. Теперь они относятся к типу `SubtaskState`.</span><span class="sxs-lookup"><span data-stu-id="a58ec-164">The `PreviousState` and `State` properties of `PSSubtaskInformation` are no longer of type `TaskState`, instead they are of type `SubtaskState`.</span></span>
  - <span data-ttu-id="a58ec-165">В отличие от `TaskState`, для `SubtaskState` не устанавливается значение `Active`, так как состояние подзадачи не может иметь значение `Active`.</span><span class="sxs-lookup"><span data-stu-id="a58ec-165">Unlike `TaskState`, `SubtaskState` has no `Active` value, since it is not possible for subtasks to be in an `Active` state.</span></span>

```powershell-interactive
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="a58ec-166">Критические изменения в командлетах Compute</span><span class="sxs-lookup"><span data-stu-id="a58ec-166">Breaking changes to Compute cmdlets</span></span>

### <a name="set-azurermvmaccessextension"></a><span data-ttu-id="a58ec-167">**Set-AzureRmVMAccessExtension**</span><span class="sxs-lookup"><span data-stu-id="a58ec-167">**Set-AzureRmVMAccessExtension**</span></span>
- <span data-ttu-id="a58ec-168">Параметры UserName и Password заменены на PSCredential.</span><span class="sxs-lookup"><span data-stu-id="a58ec-168">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell-interactive
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="a58ec-169">Критические изменения в командлетах EventHub</span><span class="sxs-lookup"><span data-stu-id="a58ec-169">Breaking changes to EventHub cmdlets</span></span>

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="a58ec-170">**New-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a58ec-170">**New-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="a58ec-171">Командлет New-AzureRmEventHubNamespaceAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="a58ec-171">The 'New-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a58ec-172">Используйте командлет New-AzureRmEventHubAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="a58ec-172">Please use the 'New-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="a58ec-173">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a58ec-173">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="a58ec-174">Командлет Get-AzureRmEventHubNamespaceAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="a58ec-174">The 'Get-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a58ec-175">Используйте командлет Get-AzureRmEventHubAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="a58ec-175">Please use the 'Get-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="set-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="a58ec-176">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a58ec-176">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="a58ec-177">Командлет Set-AzureRmEventHubNamespaceAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="a58ec-177">The 'Set-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a58ec-178">Используйте командлет Set-AzureRmEventHubAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="a58ec-178">Please use the 'Set-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="a58ec-179">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a58ec-179">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="a58ec-180">Командлет Remove-AzureRmEventHubNamespaceAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="a58ec-180">The 'Remove-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a58ec-181">Используйте командлет Remove-AzureRmEventHubAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="a58ec-181">Please use the 'Remove-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespacekey"></a><span data-ttu-id="a58ec-182">**New-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="a58ec-182">**New-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="a58ec-183">Командлет New-AzureRmEventHubNamespaceKey удален.</span><span class="sxs-lookup"><span data-stu-id="a58ec-183">The 'New-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="a58ec-184">Используйте командлет New-AzureRmEventHubKey.</span><span class="sxs-lookup"><span data-stu-id="a58ec-184">Please use the 'New-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespacekey"></a><span data-ttu-id="a58ec-185">**Get-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="a58ec-185">**Get-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="a58ec-186">Командлет Get-AzureRmEventHubNamespaceKey удален.</span><span class="sxs-lookup"><span data-stu-id="a58ec-186">The 'Get-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="a58ec-187">Используйте командлет Get-AzureRmEventHubKey.</span><span class="sxs-lookup"><span data-stu-id="a58ec-187">Please use the 'Get-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="a58ec-188">**New-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="a58ec-188">**New-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="a58ec-189">Свойство Status и Enabled из NamespceAttributes будут удалены.</span><span class="sxs-lookup"><span data-stu-id="a58ec-189">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell-interactive
# Old
# The $namespace has Status and Enabled property  
$namespace = New-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="a58ec-190">**Get-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="a58ec-190">**Get-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="a58ec-191">Свойства Status и Enabled из NamespceAttributes будут удалены.</span><span class="sxs-lookup"><span data-stu-id="a58ec-191">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell-interactive
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="set-azurermeventhubnamespace"></a><span data-ttu-id="a58ec-192">**Set-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="a58ec-192">**Set-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="a58ec-193">Свойства Status и Enabled из NamespceAttributes будут удалены.</span><span class="sxs-lookup"><span data-stu-id="a58ec-193">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell-interactive
# Old
# The $namespace has Status and Enabled property 
$namespace = Set-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Set-AzureRmEventHubNamespace <parameters>
``` 
  
### <a name="new-azurermeventhubconsumergroup"></a><span data-ttu-id="a58ec-194">**New-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="a58ec-194">**New-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="a58ec-195">Свойство EventHubPath из ConsumerGroupAttributes будет удалено.</span><span class="sxs-lookup"><span data-stu-id="a58ec-195">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="set-azurermeventhubconsumergroup"></a><span data-ttu-id="a58ec-196">**Set-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="a58ec-196">**Set-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="a58ec-197">Свойство EventHubPath из ConsumerGroupAttributes будет удалено.</span><span class="sxs-lookup"><span data-stu-id="a58ec-197">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="get-azurermeventhubconsumergroup"></a><span data-ttu-id="a58ec-198">**Get-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="a58ec-198">**Get-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="a58ec-199">Свойство EventHubPath из ConsumerGroupAttributes будет удалено.</span><span class="sxs-lookup"><span data-stu-id="a58ec-199">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="a58ec-200">Критические изменения в командлетах Insights</span><span class="sxs-lookup"><span data-stu-id="a58ec-200">Breaking changes to Insights cmdlets</span></span>

### <a name="add-azurermlogalertrule"></a><span data-ttu-id="a58ec-201">**Add-AzureRMLogAlertRule**</span><span class="sxs-lookup"><span data-stu-id="a58ec-201">**Add-AzureRMLogAlertRule**</span></span>
- <span data-ttu-id="a58ec-202">Командлет **Add-AzureRMLogAlertRule** отмечен как нерекомендуемый.</span><span class="sxs-lookup"><span data-stu-id="a58ec-202">The **Add-AzureRMLogAlertRule** cmdlet has been deprecated</span></span>
- <span data-ttu-id="a58ec-203">Начиная с 1 октября этот командлет не будет действовать, так как эта функция заменена на оповещения журнала действий.</span><span class="sxs-lookup"><span data-stu-id="a58ec-203">After October 1st using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="a58ec-204">Дополнительные сведения см. по адресу https://aka.ms/migratemealerts.</span><span class="sxs-lookup"><span data-stu-id="a58ec-204">Please see https://aka.ms/migratemealerts for more information.</span></span>

### <a name="get-azurermusage"></a><span data-ttu-id="a58ec-205">**Get-AzureRMUsage**</span><span class="sxs-lookup"><span data-stu-id="a58ec-205">**Get-AzureRMUsage**</span></span>
- <span data-ttu-id="a58ec-206">Командлет **Get AzureRMUsage** отмечен как нерекомендуемый.</span><span class="sxs-lookup"><span data-stu-id="a58ec-206">The **Get-AzureRMUsage** cmdlet has been deprecated</span></span>

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a><span data-ttu-id="a58ec-207">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span><span class="sxs-lookup"><span data-stu-id="a58ec-207">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span></span>
- <span data-ttu-id="a58ec-208">Изменение выходных данных: поле EventChannels из объекта EventData (возвращаемое этими командлетами) отмечено как нерекомендуемое, так как теперь оно возвращает значение константы (Admin, Operation).</span><span class="sxs-lookup"><span data-stu-id="a58ec-208">Output change: The field EventChannels from the EventData object (returned by these cmdlets) is being deprecated since it now returns a constant value (Admin,Operation.)</span></span>

### <a name="get-azurermalertrule"></a><span data-ttu-id="a58ec-209">**Get-AzureRmAlertRule**</span><span class="sxs-lookup"><span data-stu-id="a58ec-209">**Get-AzureRmAlertRule**</span></span>
- <span data-ttu-id="a58ec-210">Изменение выходных данных: выходные данные этого командлета будут преобразованы в плоскую структуру, т. е. будет исключено поле свойств, чтобы повысить удобство работы для пользователей.</span><span class="sxs-lookup"><span data-stu-id="a58ec-210">Output change: The output of this cmdlet will be flattened, i.e. elimination of the properties field, to improve the user experience.</span></span>

```powershell-interactive
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground Red "Error updating alert rule"
    Write-Host $rules[0].Id
    Write-Host $rules[0].Properties.IsEnabled
    Write-Host $rules[0].Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground red "Error updating alert rule"
    Write-Host $rules[0].Id

    # Properties will remain for a while
    Write-Host $rules[0].Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules[0].IsEnabled
    Write-Host $rules[0].Condition
}
```

### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="a58ec-211">**Get-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="a58ec-211">**Get-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="a58ec-212">Изменение выходных данных: поле AutoscaleSettingResourceName будет отмечено как нерекомендуемое, так как оно всегда будет иметь значение, аналогичное установленному в поле Name.</span><span class="sxs-lookup"><span data-stu-id="a58ec-212">Output change: The AutoscaleSettingResourceName field will be deprecated since it always equals the Name field.</span></span>

```powershell-interactive
# Old
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# there won't be a AutoscaleSettingResourceName
Write-Host $s1.Name    
```

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a><span data-ttu-id="a58ec-213">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="a58ec-213">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span></span>
- <span data-ttu-id="a58ec-214">Изменение выходных данных: тип выходных данных будет изменен для возврата одного объекта с идентификатором запроса и кодом состояния.</span><span class="sxs-lookup"><span data-stu-id="a58ec-214">Output change: The type of the output will change to return a single object containing the request Id and the status code.</span></span>

```powershell-interactive
# Old
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
if ($s1 -ne $null)
{
    $r = $s1[0].RequestId
    $s = $s1[0].StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
$r = $s1.RequestId
$s = $s1.StatusCode
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="a58ec-215">Критические изменения в командлетах Network</span><span class="sxs-lookup"><span data-stu-id="a58ec-215">Breaking changes to Network cmdlets</span></span>

### <a name="add-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="a58ec-216">**Add-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="a58ec-216">**Add-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="a58ec-217">Параметр Password заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="a58ec-217">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="a58ec-218">**New-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="a58ec-218">**New-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="a58ec-219">Параметр Password заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="a58ec-219">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="a58ec-220">**Set-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="a58ec-220">**Set-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="a58ec-221">Параметр Password заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="a58ec-221">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a><span data-ttu-id="a58ec-222">Критические изменения в командлетах Resources</span><span class="sxs-lookup"><span data-stu-id="a58ec-222">Breaking changes to Resources cmdlets</span></span>

### <a name="new-azurermadappcredential"></a><span data-ttu-id="a58ec-223">**New-AzureRmADAppCredential**</span><span class="sxs-lookup"><span data-stu-id="a58ec-223">**New-AzureRmADAppCredential**</span></span>
- <span data-ttu-id="a58ec-224">Параметр Password заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="a58ec-224">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a><span data-ttu-id="a58ec-225">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="a58ec-225">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="a58ec-226">Параметр Password заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="a58ec-226">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a><span data-ttu-id="a58ec-227">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="a58ec-227">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="a58ec-228">Параметр Password заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="a58ec-228">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a><span data-ttu-id="a58ec-229">**New-AzureRmADSpCredential**</span><span class="sxs-lookup"><span data-stu-id="a58ec-229">**New-AzureRmADSpCredential**</span></span>
- <span data-ttu-id="a58ec-230">Параметр Password заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="a58ec-230">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a><span data-ttu-id="a58ec-231">**New-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="a58ec-231">**New-AzureRmADUser**</span></span>
- <span data-ttu-id="a58ec-232">Параметр Password заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="a58ec-232">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a><span data-ttu-id="a58ec-233">**Set-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="a58ec-233">**Set-AzureRmADUser**</span></span>
- <span data-ttu-id="a58ec-234">Параметр Password заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="a58ec-234">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="a58ec-235">Критические изменения в командлетах ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a58ec-235">Breaking changes to ServiceBus cmdlets</span></span>

### <a name="get-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="a58ec-236">**Get-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a58ec-236">**Get-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="a58ec-237">Командлет Get-AzureRmServiceBusTopicAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="a58ec-237">The 'Get-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a58ec-238">Используйте командлет Get-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="a58ec-238">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>    

### <a name="get-azurermservicebustopickey"></a><span data-ttu-id="a58ec-239">**Get-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="a58ec-239">**Get-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="a58ec-240">Командлет Get-AzureRmServiceBusTopicKey удален.</span><span class="sxs-lookup"><span data-stu-id="a58ec-240">The 'Get-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="a58ec-241">Используйте командлет Get-AzureRmServiceBusKey.</span><span class="sxs-lookup"><span data-stu-id="a58ec-241">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="a58ec-242">**New-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a58ec-242">**New-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="a58ec-243">Командлет New-AzureRmServiceBusTopicAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="a58ec-243">The 'New-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a58ec-244">Используйте командлет New-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="a58ec-244">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebustopickey"></a><span data-ttu-id="a58ec-245">**New-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="a58ec-245">**New-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="a58ec-246">Командлет New-AzureRmServiceBusTopicKey удален.</span><span class="sxs-lookup"><span data-stu-id="a58ec-246">The 'New-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="a58ec-247">Используйте командлет New-AzureRmServiceBusKey.</span><span class="sxs-lookup"><span data-stu-id="a58ec-247">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="a58ec-248">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a58ec-248">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="a58ec-249">Командлет Remove-AzureRmServiceBusTopicAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="a58ec-249">The 'Remove-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a58ec-250">Используйте командлет Remove-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="a58ec-250">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="a58ec-251">**Set-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a58ec-251">**Set-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="a58ec-252">Командлет Set-AzureRmServiceBusTopicAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="a58ec-252">The 'Set-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a58ec-253">Используйте командлет Set-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="a58ec-253">Please use the 'Set-AzureRmServiceBusAuthorizationRule'cmdlet.</span></span>

### <a name="new-azurermservicebusnamespacekey"></a><span data-ttu-id="a58ec-254">**New-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="a58ec-254">**New-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="a58ec-255">Командлет New-AzureRmServiceBusNamespaceKey удален.</span><span class="sxs-lookup"><span data-stu-id="a58ec-255">The 'New-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="a58ec-256">Используйте командлет New-AzureRmServiceBusKey.</span><span class="sxs-lookup"><span data-stu-id="a58ec-256">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="get-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="a58ec-257">**Get-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a58ec-257">**Get-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="a58ec-258">Командлет Get-AzureRmServiceBusQueueAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="a58ec-258">The 'Get-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a58ec-259">Используйте командлет Get-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="a58ec-259">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusqueuekey"></a><span data-ttu-id="a58ec-260">**Get-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="a58ec-260">**Get-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="a58ec-261">Командлет Get-AzureRmServiceBusQueueKey удален.</span><span class="sxs-lookup"><span data-stu-id="a58ec-261">The 'Get-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="a58ec-262">Используйте командлет Get-AzureRmServiceBusKey.</span><span class="sxs-lookup"><span data-stu-id="a58ec-262">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="a58ec-263">**New-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a58ec-263">**New-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="a58ec-264">Командлет New-AzureRmServiceBusQueueAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="a58ec-264">The 'New-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a58ec-265">Используйте командлет New-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="a58ec-265">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebusqueuekey"></a><span data-ttu-id="a58ec-266">**New-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="a58ec-266">**New-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="a58ec-267">Командлет New-AzureRmServiceBusQueueKey удален.</span><span class="sxs-lookup"><span data-stu-id="a58ec-267">The 'New-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="a58ec-268">Используйте командлет New-AzureRmServiceBusKey.</span><span class="sxs-lookup"><span data-stu-id="a58ec-268">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="a58ec-269">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a58ec-269">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="a58ec-270">Командлет Remove-AzureRmServiceBusQueueAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="a58ec-270">The 'Remove-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a58ec-271">Используйте командлет GRemove-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="a58ec-271">Please use the 'GRemove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="a58ec-272">**Set-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a58ec-272">**Set-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="a58ec-273">Командлет Set-AzureRmServiceBusQueueAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="a58ec-273">The 'Set-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a58ec-274">Используйте командлет Set-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="a58ec-274">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="a58ec-275">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a58ec-275">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="a58ec-276">Командлет Get-AzureRmServiceBusNamespaceAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="a58ec-276">The 'Get-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a58ec-277">Используйте командлет Get-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="a58ec-277">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespacekey"></a><span data-ttu-id="a58ec-278">**Get-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="a58ec-278">**Get-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="a58ec-279">Командлет Get-AzureRmServiceBusNamespaceKey удален.</span><span class="sxs-lookup"><span data-stu-id="a58ec-279">The 'Get-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="a58ec-280">Используйте командлет Get-AzureRmServiceBusKey.</span><span class="sxs-lookup"><span data-stu-id="a58ec-280">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="a58ec-281">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a58ec-281">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="a58ec-282">Командлет New-AzureRmServiceBusNamespaceAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="a58ec-282">The 'New-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a58ec-283">Используйте командлет New-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="a58ec-283">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="a58ec-284">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a58ec-284">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="a58ec-285">Командлет Remove-AzureRmServiceBusNamespaceAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="a58ec-285">The 'Remove-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a58ec-286">Используйте командлет Remove-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="a58ec-286">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="a58ec-287">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a58ec-287">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="a58ec-288">Командлет Set-AzureRmServiceBusNamespaceAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="a58ec-288">The 'Set-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a58ec-289">Используйте командлет Set-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="a58ec-289">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="type-namespaceattributes"></a><span data-ttu-id="a58ec-290">**Тип NamespaceAttributes**</span><span class="sxs-lookup"><span data-stu-id="a58ec-290">**Type NamespaceAttributes**</span></span>
- <span data-ttu-id="a58ec-291">Следующие свойства удалены:</span><span class="sxs-lookup"><span data-stu-id="a58ec-291">The following properties have been removed</span></span>
    - <span data-ttu-id="a58ec-292">Включено</span><span class="sxs-lookup"><span data-stu-id="a58ec-292">Enabled</span></span>
    - <span data-ttu-id="a58ec-293">Status</span><span class="sxs-lookup"><span data-stu-id="a58ec-293">Status</span></span>
   
```powershell-interactive
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmServiceBusNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Enabled and Status properties    
$namespace = Get-AzureRmServiceBusNamespace <parameters>
```

### <a name="type-queueattribute"></a><span data-ttu-id="a58ec-294">**Тип QueueAttribute**</span><span class="sxs-lookup"><span data-stu-id="a58ec-294">**Type QueueAttribute**</span></span>
- <span data-ttu-id="a58ec-295">Следующие свойства отмечены как устаревшие:</span><span class="sxs-lookup"><span data-stu-id="a58ec-295">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="a58ec-296">EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="a58ec-296">EnableBatchedOperations</span></span>
    - <span data-ttu-id="a58ec-297">EntityAvailabilityStatus.</span><span class="sxs-lookup"><span data-stu-id="a58ec-297">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="a58ec-298">IsAnonymousAccessible;</span><span class="sxs-lookup"><span data-stu-id="a58ec-298">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="a58ec-299">SupportOrdering.</span><span class="sxs-lookup"><span data-stu-id="a58ec-299">SupportOrdering</span></span>

```powershell-interactive
# Old
# The $queue has EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$queue = Get-AzureRmServiceBusQueue <parameters>
$queue.EntityAvailabilityStatus
$queue.EnableBatchedOperations
$queue.IsAnonymousAccessible
$queue.SupportOrdering  

# New
# The call remains the same, but the returned values Queue object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$queue = Get-AzureRmServiceBusQueue <parameters>
```
   
### <a name="type-topicattribute"></a><span data-ttu-id="a58ec-300">**Тип TopicAttribute**</span><span class="sxs-lookup"><span data-stu-id="a58ec-300">**Type TopicAttribute**</span></span>
- <span data-ttu-id="a58ec-301">Следующие свойства отмечены как устаревшие:</span><span class="sxs-lookup"><span data-stu-id="a58ec-301">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="a58ec-302">Расположение</span><span class="sxs-lookup"><span data-stu-id="a58ec-302">Location</span></span>
    - <span data-ttu-id="a58ec-303">IsExpress;</span><span class="sxs-lookup"><span data-stu-id="a58ec-303">IsExpress</span></span>
    - <span data-ttu-id="a58ec-304">IsAnonymousAccessible;</span><span class="sxs-lookup"><span data-stu-id="a58ec-304">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="a58ec-305">FilteringMessagesBeforePublishing;</span><span class="sxs-lookup"><span data-stu-id="a58ec-305">FilteringMessagesBeforePublishing</span></span>
    - <span data-ttu-id="a58ec-306">EnableSubscriptionPartitioning;</span><span class="sxs-lookup"><span data-stu-id="a58ec-306">EnableSubscriptionPartitioning</span></span>
    - <span data-ttu-id="a58ec-307">EntityAvailabilityStatus.</span><span class="sxs-lookup"><span data-stu-id="a58ec-307">EntityAvailabilityStatus</span></span>

```powershell-interactive
# Old
# The $topic has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$topic = Get-AzureRmServiceBusTopic <parameters>
$topic.EntityAvailabilityStatus
$topic.EnableSubscriptionPartitioning
$topic.IsAnonymousAccessible
$topic.IsExpress
$topic.FilteringMessagesBeforePublishing
$topic.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$topic = Get-AzureRmServiceBusTopic <parameters>
```
   
### <a name="type-subscriptionattribute"></a><span data-ttu-id="a58ec-308">**Тип SubscriptionAttribute**</span><span class="sxs-lookup"><span data-stu-id="a58ec-308">**Type SubscriptionAttribute**</span></span>
- <span data-ttu-id="a58ec-309">Следующие свойства отмечены как устаревшие:</span><span class="sxs-lookup"><span data-stu-id="a58ec-309">The following properties are marked as obsolete</span></span>
    - <span data-ttu-id="a58ec-310">DeadLetteringOnFilterEvaluationExceptions;</span><span class="sxs-lookup"><span data-stu-id="a58ec-310">DeadLetteringOnFilterEvaluationExceptions</span></span>
    - <span data-ttu-id="a58ec-311">EntityAvailabilityStatus.</span><span class="sxs-lookup"><span data-stu-id="a58ec-311">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="a58ec-312">IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="a58ec-312">IsReadOnly</span></span>
    - <span data-ttu-id="a58ec-313">Расположение</span><span class="sxs-lookup"><span data-stu-id="a58ec-313">Location</span></span>
   
```powershell-interactive
# Old
# The $subscription has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$subscription = Get-AzureRmServiceBussubscription <parameters>
$subscription.EntityAvailabilityStatus
$subscription.EnableSubscriptionPartitioning
$subscription.IsAnonymousAccessible
$subscription.IsExpress
$subscription.FilteringMessagesBeforePublishing
$subscription.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$subscription = Get-AzureRmServiceBussubscription <parameters>
```