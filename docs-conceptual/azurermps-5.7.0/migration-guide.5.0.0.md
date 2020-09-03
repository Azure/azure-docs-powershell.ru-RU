---
title: Критические изменения для Microsoft Azure PowerShell 5.0.0
description: Это руководство по миграции содержит список критических изменений, внесенных в выпуск Azure PowerShell версии 5.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 81f52ee8b84f60d59a7f2d53b6675129ac054fd6
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243741"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a><span data-ttu-id="ce661-103">Критические изменения для Microsoft Azure PowerShell 5.0.0</span><span class="sxs-lookup"><span data-stu-id="ce661-103">Breaking changes for Microsoft Azure PowerShell 5.0.0</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="ce661-104">Этот документ предназначен для уведомления о критических изменениях и является руководством по миграции для пользователей командлетов Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ce661-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="ce661-105">В каждом разделе описана причина критического изменения и самый простой путь миграции.</span><span class="sxs-lookup"><span data-stu-id="ce661-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="ce661-106">Подробное описание см. в запросах на вытягивание для каждого изменения.</span><span class="sxs-lookup"><span data-stu-id="ce661-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="ce661-107">Оглавление</span><span class="sxs-lookup"><span data-stu-id="ce661-107">Table of Contents</span></span>

- [<span data-ttu-id="ce661-108">Критические изменения в командлетах ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ce661-108">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
- [<span data-ttu-id="ce661-109">Критические изменения в командлетах Batch</span><span class="sxs-lookup"><span data-stu-id="ce661-109">Breaking changes to Batch cmdlets</span></span>](#breaking-changes-to-batch-cmdlets)
- [<span data-ttu-id="ce661-110">Критические изменения в командлетах Compute</span><span class="sxs-lookup"><span data-stu-id="ce661-110">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="ce661-111">Критические изменения в командлетах EventHub</span><span class="sxs-lookup"><span data-stu-id="ce661-111">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="ce661-112">Критические изменения в командлетах Insights</span><span class="sxs-lookup"><span data-stu-id="ce661-112">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="ce661-113">Критические изменения в командлетах Network</span><span class="sxs-lookup"><span data-stu-id="ce661-113">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="ce661-114">Критические изменения в командлетах Resources</span><span class="sxs-lookup"><span data-stu-id="ce661-114">Breaking changes to Resources cmdlets</span></span>](#breaking-changes-to-resources-cmdlets)
- [<span data-ttu-id="ce661-115">Критические изменения в командлетах ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ce661-115">Breaking Changes to ServiceBus Cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="ce661-116">Критические изменения в командлетах ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ce661-116">Breaking changes to ApiManagement cmdlets</span></span>

### <a name="new-azurermapimanagementbackendproxy"></a><span data-ttu-id="ce661-117">**New-AzureRmApiManagementBackendProxy**</span><span class="sxs-lookup"><span data-stu-id="ce661-117">**New-AzureRmApiManagementBackendProxy**</span></span>
- <span data-ttu-id="ce661-118">Параметры UserName и Password заменены на PSCredential.</span><span class="sxs-lookup"><span data-stu-id="ce661-118">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell-interactive
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a><span data-ttu-id="ce661-119">**New-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="ce661-119">**New-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="ce661-120">Параметр Password заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="ce661-120">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a><span data-ttu-id="ce661-121">**Set-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="ce661-121">**Set-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="ce661-122">Параметр Password заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="ce661-122">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a><span data-ttu-id="ce661-123">Критические изменения в командлетах Batch</span><span class="sxs-lookup"><span data-stu-id="ce661-123">Breaking changes to Batch cmdlets</span></span>

### <a name="new-azurebatchcertificate"></a><span data-ttu-id="ce661-124">**New-AzureBatchCertificate**</span><span class="sxs-lookup"><span data-stu-id="ce661-124">**New-AzureBatchCertificate**</span></span>
- <span data-ttu-id="ce661-125">Параметр `Password` заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="ce661-125">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a><span data-ttu-id="ce661-126">**New-AzureBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="ce661-126">**New-AzureBatchComputeNodeUser**</span></span>
- <span data-ttu-id="ce661-127">Параметр `Password` заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="ce661-127">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a><span data-ttu-id="ce661-128">**Set-AzureRmBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="ce661-128">**Set-AzureRmBatchComputeNodeUser**</span></span>
- <span data-ttu-id="ce661-129">Параметр `Password` заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="ce661-129">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a><span data-ttu-id="ce661-130">**New-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="ce661-130">**New-AzureBatchTask**</span></span>
 - <span data-ttu-id="ce661-131">Переключатель `RunElevated` удален и заменен на `UserIdentity`.</span><span class="sxs-lookup"><span data-stu-id="ce661-131">Removed the `RunElevated` switch and replaced it with `UserIdentity`.</span></span>

```powershell-interactive
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

<span data-ttu-id="ce661-132">Это также касается свойства `RunElevated` в `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` и `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="ce661-132">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="psmultiinstancesettings"></a><span data-ttu-id="ce661-133">**PSMultiInstanceSettings**</span><span class="sxs-lookup"><span data-stu-id="ce661-133">**PSMultiInstanceSettings**</span></span>

- <span data-ttu-id="ce661-134">Конструктор `PSMultiInstanceSettings` больше не принимает обязательный параметр `numberOfInstances`. Вместо него он принимает обязательный параметр `coordinationCommandLine`.</span><span class="sxs-lookup"><span data-stu-id="ce661-134">`PSMultiInstanceSettings` constructor no longer takes a required `numberOfInstances` parameter, instead it takes a required `coordinationCommandLine` parameter.</span></span>

```powershell-interactive
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a><span data-ttu-id="ce661-135">**Get-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="ce661-135">**Get-AzureBatchTask**</span></span>
 - <span data-ttu-id="ce661-136">Удалено свойство `RunElevated` в `PSCloudTask`.</span><span class="sxs-lookup"><span data-stu-id="ce661-136">Removed the `RunElevated` property on `PSCloudTask`.</span></span> <span data-ttu-id="ce661-137">Добавлено свойство `UserIdentity` для замены `RunElevated`.</span><span class="sxs-lookup"><span data-stu-id="ce661-137">The `UserIdentity` property has been added to replace `RunElevated`.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

<span data-ttu-id="ce661-138">Это также касается свойства `RunElevated` в `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` и `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="ce661-138">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="multiple-types"></a><span data-ttu-id="ce661-139">**Несколько типов**</span><span class="sxs-lookup"><span data-stu-id="ce661-139">**Multiple types**</span></span>

- <span data-ttu-id="ce661-140">Свойство `SchedulingError` в `PSExitConditions` переименовано в `PreProcessingError`.</span><span class="sxs-lookup"><span data-stu-id="ce661-140">Renamed the `SchedulingError` property on `PSExitConditions` to `PreProcessingError`.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a><span data-ttu-id="ce661-141">**Несколько типов**</span><span class="sxs-lookup"><span data-stu-id="ce661-141">**Multiple types**</span></span>

- <span data-ttu-id="ce661-142">Свойство `SchedulingError` в `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` и `PSTaskExecutionInformation` переименовано в `FailureInformation`.</span><span class="sxs-lookup"><span data-stu-id="ce661-142">Renamed the `SchedulingError` property on `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation`, and `PSTaskExecutionInformation` to `FailureInformation`.</span></span>
  - <span data-ttu-id="ce661-143">`FailureInformation` возвращается при каждом сбое задачи.</span><span class="sxs-lookup"><span data-stu-id="ce661-143">`FailureInformation` is returned any time there is a task failure.</span></span> <span data-ttu-id="ce661-144">Сюда входят все предыдущие случаи ошибок планирования, а также коды завершения задач со значением, отличным от нуля, и ошибки передачи файлов из новой функции выходных файлов.</span><span class="sxs-lookup"><span data-stu-id="ce661-144">This includes all previous scheduling error cases, as well as nonzero task exit codes, and file upload failures from the new output files feature.</span></span>
  - <span data-ttu-id="ce661-145">Структура не изменилась, поэтому при использовании этого типа не нужно преобразовывать код.</span><span class="sxs-lookup"><span data-stu-id="ce661-145">This is structured the same as before, so no code change is needed when using this type.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

<span data-ttu-id="ce661-146">Это также касается Get-AzureBatchPool, Get-AzureBatchSubtask и Get-AzureBatchJobPreparationAndReleaseTaskStatus.</span><span class="sxs-lookup"><span data-stu-id="ce661-146">This additionally impacts: Get-AzureBatchPool, Get-AzureBatchSubtask, and Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

### <a name="new-azurebatchpool"></a><span data-ttu-id="ce661-147">**New-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="ce661-147">**New-AzureBatchPool**</span></span>
 - <span data-ttu-id="ce661-148">Параметр `TargetDedicated` удален и заменен на `TargetDedicatedComputeNodes` и `TargetLowPriorityComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="ce661-148">Removed `TargetDedicated` and replaced it with `TargetDedicatedComputeNodes` and `TargetLowPriorityComputeNodes`.</span></span>
 - <span data-ttu-id="ce661-149">Псевдоним `TargetDedicatedComputeNodes` — `TargetDedicated`.</span><span class="sxs-lookup"><span data-stu-id="ce661-149">`TargetDedicatedComputeNodes` has an alias `TargetDedicated`.</span></span>

```powershell-interactive
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

<span data-ttu-id="ce661-150">Это также касается Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="ce661-150">This also impacts: Start-AzureBatchPoolResize</span></span>

### <a name="get-azurebatchpool"></a><span data-ttu-id="ce661-151">**Get-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="ce661-151">**Get-AzureBatchPool**</span></span>
 - <span data-ttu-id="ce661-152">Свойства `TargetDedicated` и `CurrentDedicated` в `PSCloudPool` переименованы в `TargetDedicatedComputeNodes` и `CurrentDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="ce661-152">Renamed the `TargetDedicated` and `CurrentDedicated` properties on `PSCloudPool` to `TargetDedicatedComputeNodes` and `CurrentDedicatedComputeNodes`.</span></span>

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

### <a name="type-pscloudpool"></a><span data-ttu-id="ce661-153">**Тип PSCloudPool**</span><span class="sxs-lookup"><span data-stu-id="ce661-153">**Type PSCloudPool**</span></span>

- <span data-ttu-id="ce661-154">Параметр `ResizeError` в `PSCloudPool` переименован в `ResizeErrors` и теперь является коллекцией.</span><span class="sxs-lookup"><span data-stu-id="ce661-154">Renamed `ResizeError` to `ResizeErrors` on `PSCloudPool`, and it is now a collection.</span></span>

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a><span data-ttu-id="ce661-155">**New-AzureBatchJob**</span><span class="sxs-lookup"><span data-stu-id="ce661-155">**New-AzureBatchJob**</span></span>
- <span data-ttu-id="ce661-156">Свойство `TargetDedicated` в `PSPoolSpecification` переименовано в `TargetDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="ce661-156">Renamed the `TargetDedicated` property on `PSPoolSpecification` to `TargetDedicatedComputeNodes`.</span></span>

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

### <a name="get-azurebatchnodefile"></a><span data-ttu-id="ce661-157">**Get-AzureBatchNodeFile**</span><span class="sxs-lookup"><span data-stu-id="ce661-157">**Get-AzureBatchNodeFile**</span></span>
 - <span data-ttu-id="ce661-158">Параметр `Name` удален и заменен на `Path`.</span><span class="sxs-lookup"><span data-stu-id="ce661-158">Removed `Name` and replaced it with `Path`.</span></span>
 - <span data-ttu-id="ce661-159">Псевдоним `Path` — `Name`.</span><span class="sxs-lookup"><span data-stu-id="ce661-159">`Path` has an alias `Name`.</span></span>

```powershell-interactive
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

<span data-ttu-id="ce661-160">Это также касается Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="ce661-160">This also impacts: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span></span>

### <a name="type-psnodefile"></a><span data-ttu-id="ce661-161">Тип **PSNodeFile**</span><span class="sxs-lookup"><span data-stu-id="ce661-161">Type **PSNodeFile**</span></span>

 - <span data-ttu-id="ce661-162">Свойство `Name` в `PSNodeFile` переименовано в `Path`.</span><span class="sxs-lookup"><span data-stu-id="ce661-162">Renamed the `Name` property on `PSNodeFile` to `Path`.</span></span>

```powershell-interactive
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a><span data-ttu-id="ce661-163">**Get-AzureBatchSubtask**</span><span class="sxs-lookup"><span data-stu-id="ce661-163">**Get-AzureBatchSubtask**</span></span>
- <span data-ttu-id="ce661-164">Свойства `PreviousState` и `State` для `PSSubtaskInformation` больше не относятся к типу `TaskState`. Теперь они относятся к типу `SubtaskState`.</span><span class="sxs-lookup"><span data-stu-id="ce661-164">The `PreviousState` and `State` properties of `PSSubtaskInformation` are no longer of type `TaskState`, instead they are of type `SubtaskState`.</span></span>
  - <span data-ttu-id="ce661-165">В отличие от `TaskState`, для `SubtaskState` не устанавливается значение `Active`, так как состояние подзадачи не может иметь значение `Active`.</span><span class="sxs-lookup"><span data-stu-id="ce661-165">Unlike `TaskState`, `SubtaskState` has no `Active` value, since it is not possible for subtasks to be in an `Active` state.</span></span>

```powershell-interactive
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="ce661-166">Критические изменения в командлетах Compute</span><span class="sxs-lookup"><span data-stu-id="ce661-166">Breaking changes to Compute cmdlets</span></span>

### <a name="set-azurermvmaccessextension"></a><span data-ttu-id="ce661-167">**Set-AzureRmVMAccessExtension**</span><span class="sxs-lookup"><span data-stu-id="ce661-167">**Set-AzureRmVMAccessExtension**</span></span>
- <span data-ttu-id="ce661-168">Параметры UserName и Password заменены на PSCredential.</span><span class="sxs-lookup"><span data-stu-id="ce661-168">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell-interactive
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="ce661-169">Критические изменения в командлетах EventHub</span><span class="sxs-lookup"><span data-stu-id="ce661-169">Breaking changes to EventHub cmdlets</span></span>

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="ce661-170">**New-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ce661-170">**New-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="ce661-171">Командлет New-AzureRmEventHubNamespaceAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="ce661-171">The 'New-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ce661-172">Используйте командлет New-AzureRmEventHubAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="ce661-172">Please use the 'New-AzureRmEventHubAuthorizationRule' cmdlet</span></span>

### <a name="get-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="ce661-173">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ce661-173">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="ce661-174">Командлет Get-AzureRmEventHubNamespaceAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="ce661-174">The 'Get-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ce661-175">Используйте командлет Get-AzureRmEventHubAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="ce661-175">Please use the 'Get-AzureRmEventHubAuthorizationRule' cmdlet</span></span>

### <a name="set-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="ce661-176">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ce661-176">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="ce661-177">Командлет Set-AzureRmEventHubNamespaceAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="ce661-177">The 'Set-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ce661-178">Используйте командлет Set-AzureRmEventHubAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="ce661-178">Please use the 'Set-AzureRmEventHubAuthorizationRule' cmdlet</span></span>

### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="ce661-179">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ce661-179">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="ce661-180">Командлет Remove-AzureRmEventHubNamespaceAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="ce661-180">The 'Remove-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ce661-181">Используйте командлет Remove-AzureRmEventHubAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="ce661-181">Please use the 'Remove-AzureRmEventHubAuthorizationRule' cmdlet</span></span>

### <a name="new-azurermeventhubnamespacekey"></a><span data-ttu-id="ce661-182">**New-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="ce661-182">**New-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="ce661-183">Командлет New-AzureRmEventHubNamespaceKey удален.</span><span class="sxs-lookup"><span data-stu-id="ce661-183">The 'New-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="ce661-184">Используйте командлет New-AzureRmEventHubKey.</span><span class="sxs-lookup"><span data-stu-id="ce661-184">Please use the 'New-AzureRmEventHubKey' cmdlet</span></span>

### <a name="get-azurermeventhubnamespacekey"></a><span data-ttu-id="ce661-185">**Get-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="ce661-185">**Get-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="ce661-186">Командлет Get-AzureRmEventHubNamespaceKey удален.</span><span class="sxs-lookup"><span data-stu-id="ce661-186">The 'Get-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="ce661-187">Используйте командлет Get-AzureRmEventHubKey.</span><span class="sxs-lookup"><span data-stu-id="ce661-187">Please use the 'Get-AzureRmEventHubKey' cmdlet</span></span>

### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="ce661-188">**New-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="ce661-188">**New-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="ce661-189">Свойства Status и Enabled из NamespceAttributes будут удалены.</span><span class="sxs-lookup"><span data-stu-id="ce661-189">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span>

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

### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="ce661-190">**Get-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="ce661-190">**Get-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="ce661-191">Свойства Status и Enabled из NamespceAttributes будут удалены.</span><span class="sxs-lookup"><span data-stu-id="ce661-191">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span>

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

### <a name="set-azurermeventhubnamespace"></a><span data-ttu-id="ce661-192">**Set-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="ce661-192">**Set-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="ce661-193">Свойства Status и Enabled из NamespceAttributes будут удалены.</span><span class="sxs-lookup"><span data-stu-id="ce661-193">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span>

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

### <a name="new-azurermeventhubconsumergroup"></a><span data-ttu-id="ce661-194">**New-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="ce661-194">**New-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="ce661-195">Свойство EventHubPath из ConsumerGroupAttributes будет удалено.</span><span class="sxs-lookup"><span data-stu-id="ce661-195">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```

### <a name="set-azurermeventhubconsumergroup"></a><span data-ttu-id="ce661-196">**Set-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="ce661-196">**Set-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="ce661-197">Свойство EventHubPath из ConsumerGroupAttributes будет удалено.</span><span class="sxs-lookup"><span data-stu-id="ce661-197">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```

### <a name="get-azurermeventhubconsumergroup"></a><span data-ttu-id="ce661-198">**Get-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="ce661-198">**Get-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="ce661-199">Свойство EventHubPath из ConsumerGroupAttributes будет удалено.</span><span class="sxs-lookup"><span data-stu-id="ce661-199">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="ce661-200">Критические изменения в командлетах Insights</span><span class="sxs-lookup"><span data-stu-id="ce661-200">Breaking changes to Insights cmdlets</span></span>

### <a name="add-azurermlogalertrule"></a><span data-ttu-id="ce661-201">**Add-AzureRMLogAlertRule**</span><span class="sxs-lookup"><span data-stu-id="ce661-201">**Add-AzureRMLogAlertRule**</span></span>
- <span data-ttu-id="ce661-202">Командлет **Add-AzureRMLogAlertRule** отмечен как нерекомендуемый.</span><span class="sxs-lookup"><span data-stu-id="ce661-202">The **Add-AzureRMLogAlertRule** cmdlet has been deprecated</span></span>
- <span data-ttu-id="ce661-203">Начиная с 1 октября этот командлет не будет действовать, так как эта функция заменена на оповещения журнала действий.</span><span class="sxs-lookup"><span data-stu-id="ce661-203">After October 1st using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="ce661-204">Дополнительные сведения см. по адресу https://aka.ms/migratemealerts.</span><span class="sxs-lookup"><span data-stu-id="ce661-204">Please see https://aka.ms/migratemealerts for more information.</span></span>

### <a name="get-azurermusage"></a><span data-ttu-id="ce661-205">**Get-AzureRMUsage**</span><span class="sxs-lookup"><span data-stu-id="ce661-205">**Get-AzureRMUsage**</span></span>
- <span data-ttu-id="ce661-206">Командлет **Get AzureRMUsage** отмечен как нерекомендуемый.</span><span class="sxs-lookup"><span data-stu-id="ce661-206">The **Get-AzureRMUsage** cmdlet has been deprecated</span></span>

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a><span data-ttu-id="ce661-207">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span><span class="sxs-lookup"><span data-stu-id="ce661-207">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span></span>
- <span data-ttu-id="ce661-208">Изменение выходных данных: поле EventChannels из объекта EventData (возвращаемое этими командлетами) отмечено как нерекомендуемое, так как теперь оно возвращает значение константы (Admin, Operation).</span><span class="sxs-lookup"><span data-stu-id="ce661-208">Output change: The field EventChannels from the EventData object (returned by these cmdlets) is being deprecated since it now returns a constant value (Admin,Operation.)</span></span>

### <a name="get-azurermalertrule"></a><span data-ttu-id="ce661-209">**Get-AzureRmAlertRule**</span><span class="sxs-lookup"><span data-stu-id="ce661-209">**Get-AzureRmAlertRule**</span></span>
- <span data-ttu-id="ce661-210">Изменение выходных данных: выходные данные этого командлета будут преобразованы в плоскую структуру, т. е. будет исключено поле свойств, чтобы повысить удобство работы для пользователей.</span><span class="sxs-lookup"><span data-stu-id="ce661-210">Output change: The output of this cmdlet will be flattened, i.e. elimination of the properties field, to improve the user experience.</span></span>

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

### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="ce661-211">**Get-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="ce661-211">**Get-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="ce661-212">Изменение выходных данных: поле AutoscaleSettingResourceName будет отмечено как нерекомендуемое, так как оно всегда будет иметь значение, аналогичное установленному в поле Name.</span><span class="sxs-lookup"><span data-stu-id="ce661-212">Output change: The AutoscaleSettingResourceName field will be deprecated since it always equals the Name field.</span></span>

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

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a><span data-ttu-id="ce661-213">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="ce661-213">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span></span>
- <span data-ttu-id="ce661-214">Изменение выходных данных: тип выходных данных будет изменен для возврата одного объекта с идентификатором запроса и кодом состояния.</span><span class="sxs-lookup"><span data-stu-id="ce661-214">Output change: The type of the output will change to return a single object containing the request Id and the status code.</span></span>

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

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="ce661-215">Критические изменения в командлетах Network</span><span class="sxs-lookup"><span data-stu-id="ce661-215">Breaking changes to Network cmdlets</span></span>

### <a name="add-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="ce661-216">**Add-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="ce661-216">**Add-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="ce661-217">Параметр Password заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="ce661-217">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="ce661-218">**New-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="ce661-218">**New-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="ce661-219">Параметр Password заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="ce661-219">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="ce661-220">**Set-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="ce661-220">**Set-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="ce661-221">Параметр Password заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="ce661-221">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a><span data-ttu-id="ce661-222">Критические изменения в командлетах Resources</span><span class="sxs-lookup"><span data-stu-id="ce661-222">Breaking changes to Resources cmdlets</span></span>

### <a name="new-azurermadappcredential"></a><span data-ttu-id="ce661-223">**New-AzureRmADAppCredential**</span><span class="sxs-lookup"><span data-stu-id="ce661-223">**New-AzureRmADAppCredential**</span></span>
- <span data-ttu-id="ce661-224">Параметр Password заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="ce661-224">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a><span data-ttu-id="ce661-225">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="ce661-225">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="ce661-226">Параметр Password заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="ce661-226">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a><span data-ttu-id="ce661-227">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="ce661-227">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="ce661-228">Параметр Password заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="ce661-228">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a><span data-ttu-id="ce661-229">**New-AzureRmADSpCredential**</span><span class="sxs-lookup"><span data-stu-id="ce661-229">**New-AzureRmADSpCredential**</span></span>
- <span data-ttu-id="ce661-230">Параметр Password заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="ce661-230">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a><span data-ttu-id="ce661-231">**New-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="ce661-231">**New-AzureRmADUser**</span></span>
- <span data-ttu-id="ce661-232">Параметр Password заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="ce661-232">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a><span data-ttu-id="ce661-233">**Set-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="ce661-233">**Set-AzureRmADUser**</span></span>
- <span data-ttu-id="ce661-234">Параметр Password заменен на SecureString.</span><span class="sxs-lookup"><span data-stu-id="ce661-234">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="ce661-235">Критические изменения в командлетах ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ce661-235">Breaking changes to ServiceBus cmdlets</span></span>

### <a name="get-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="ce661-236">**Get-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ce661-236">**Get-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="ce661-237">Командлет Get-AzureRmServiceBusTopicAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="ce661-237">The 'Get-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ce661-238">Используйте командлет Get-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="ce661-238">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebustopickey"></a><span data-ttu-id="ce661-239">**Get-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="ce661-239">**Get-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="ce661-240">Командлет Get-AzureRmServiceBusTopicKey удален.</span><span class="sxs-lookup"><span data-stu-id="ce661-240">The 'Get-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="ce661-241">Используйте командлет Get-AzureRmServiceBusKey.</span><span class="sxs-lookup"><span data-stu-id="ce661-241">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="ce661-242">**New-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ce661-242">**New-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="ce661-243">Командлет New-AzureRmServiceBusTopicAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="ce661-243">The 'New-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ce661-244">Используйте командлет New-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="ce661-244">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebustopickey"></a><span data-ttu-id="ce661-245">**New-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="ce661-245">**New-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="ce661-246">Командлет New-AzureRmServiceBusTopicKey удален.</span><span class="sxs-lookup"><span data-stu-id="ce661-246">The 'New-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="ce661-247">Используйте командлет New-AzureRmServiceBusKey.</span><span class="sxs-lookup"><span data-stu-id="ce661-247">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="ce661-248">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ce661-248">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="ce661-249">Командлет Remove-AzureRmServiceBusTopicAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="ce661-249">The 'Remove-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ce661-250">Используйте командлет Remove-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="ce661-250">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="ce661-251">**Set-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ce661-251">**Set-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="ce661-252">Командлет Set-AzureRmServiceBusTopicAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="ce661-252">The 'Set-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ce661-253">Используйте командлет Set-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="ce661-253">Please use the 'Set-AzureRmServiceBusAuthorizationRule'cmdlet.</span></span>

### <a name="new-azurermservicebusnamespacekey"></a><span data-ttu-id="ce661-254">**New-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="ce661-254">**New-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="ce661-255">Командлет New-AzureRmServiceBusNamespaceKey удален.</span><span class="sxs-lookup"><span data-stu-id="ce661-255">The 'New-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="ce661-256">Используйте командлет New-AzureRmServiceBusKey.</span><span class="sxs-lookup"><span data-stu-id="ce661-256">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="get-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="ce661-257">**Get-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ce661-257">**Get-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="ce661-258">Командлет Get-AzureRmServiceBusQueueAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="ce661-258">The 'Get-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ce661-259">Используйте командлет Get-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="ce661-259">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusqueuekey"></a><span data-ttu-id="ce661-260">**Get-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="ce661-260">**Get-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="ce661-261">Командлет Get-AzureRmServiceBusQueueKey удален.</span><span class="sxs-lookup"><span data-stu-id="ce661-261">The 'Get-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="ce661-262">Используйте командлет Get-AzureRmServiceBusKey.</span><span class="sxs-lookup"><span data-stu-id="ce661-262">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="ce661-263">**New-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ce661-263">**New-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="ce661-264">Командлет New-AzureRmServiceBusQueueAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="ce661-264">The 'New-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ce661-265">Используйте командлет New-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="ce661-265">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebusqueuekey"></a><span data-ttu-id="ce661-266">**New-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="ce661-266">**New-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="ce661-267">Командлет New-AzureRmServiceBusQueueKey удален.</span><span class="sxs-lookup"><span data-stu-id="ce661-267">The 'New-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="ce661-268">Используйте командлет New-AzureRmServiceBusKey.</span><span class="sxs-lookup"><span data-stu-id="ce661-268">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="ce661-269">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ce661-269">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="ce661-270">Командлет Remove-AzureRmServiceBusQueueAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="ce661-270">The 'Remove-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ce661-271">Используйте командлет GRemove-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="ce661-271">Please use the 'GRemove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="ce661-272">**Set-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ce661-272">**Set-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="ce661-273">Командлет Set-AzureRmServiceBusQueueAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="ce661-273">The 'Set-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ce661-274">Используйте командлет Set-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="ce661-274">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="ce661-275">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ce661-275">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="ce661-276">Командлет Get-AzureRmServiceBusNamespaceAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="ce661-276">The 'Get-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ce661-277">Используйте командлет Get-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="ce661-277">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespacekey"></a><span data-ttu-id="ce661-278">**Get-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="ce661-278">**Get-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="ce661-279">Командлет Get-AzureRmServiceBusNamespaceKey удален.</span><span class="sxs-lookup"><span data-stu-id="ce661-279">The 'Get-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="ce661-280">Используйте командлет Get-AzureRmServiceBusKey.</span><span class="sxs-lookup"><span data-stu-id="ce661-280">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="ce661-281">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ce661-281">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="ce661-282">Командлет New-AzureRmServiceBusNamespaceAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="ce661-282">The 'New-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ce661-283">Используйте командлет New-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="ce661-283">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="ce661-284">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ce661-284">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="ce661-285">Командлет Remove-AzureRmServiceBusNamespaceAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="ce661-285">The 'Remove-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ce661-286">Используйте командлет Remove-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="ce661-286">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="ce661-287">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ce661-287">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="ce661-288">Командлет Set-AzureRmServiceBusNamespaceAuthorizationRule удален.</span><span class="sxs-lookup"><span data-stu-id="ce661-288">The 'Set-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ce661-289">Используйте командлет Set-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="ce661-289">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="type-namespaceattributes"></a><span data-ttu-id="ce661-290">**Тип NamespaceAttributes**</span><span class="sxs-lookup"><span data-stu-id="ce661-290">**Type NamespaceAttributes**</span></span>
- <span data-ttu-id="ce661-291">Следующие свойства удалены:</span><span class="sxs-lookup"><span data-stu-id="ce661-291">The following properties have been removed</span></span>
    - <span data-ttu-id="ce661-292">Активировано</span><span class="sxs-lookup"><span data-stu-id="ce661-292">Enabled</span></span>
    - <span data-ttu-id="ce661-293">Состояние</span><span class="sxs-lookup"><span data-stu-id="ce661-293">Status</span></span>

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

### <a name="type-queueattribute"></a><span data-ttu-id="ce661-294">**Тип QueueAttribute**</span><span class="sxs-lookup"><span data-stu-id="ce661-294">**Type QueueAttribute**</span></span>
- <span data-ttu-id="ce661-295">Следующие свойства отмечены как устаревшие:</span><span class="sxs-lookup"><span data-stu-id="ce661-295">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="ce661-296">EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="ce661-296">EnableBatchedOperations</span></span>
    - <span data-ttu-id="ce661-297">EntityAvailabilityStatus.</span><span class="sxs-lookup"><span data-stu-id="ce661-297">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="ce661-298">IsAnonymousAccessible;</span><span class="sxs-lookup"><span data-stu-id="ce661-298">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="ce661-299">SupportOrdering.</span><span class="sxs-lookup"><span data-stu-id="ce661-299">SupportOrdering</span></span>

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

### <a name="type-topicattribute"></a><span data-ttu-id="ce661-300">**Тип TopicAttribute**</span><span class="sxs-lookup"><span data-stu-id="ce661-300">**Type TopicAttribute**</span></span>
- <span data-ttu-id="ce661-301">Следующие свойства отмечены как устаревшие:</span><span class="sxs-lookup"><span data-stu-id="ce661-301">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="ce661-302">Расположение</span><span class="sxs-lookup"><span data-stu-id="ce661-302">Location</span></span>
    - <span data-ttu-id="ce661-303">IsExpress;</span><span class="sxs-lookup"><span data-stu-id="ce661-303">IsExpress</span></span>
    - <span data-ttu-id="ce661-304">IsAnonymousAccessible;</span><span class="sxs-lookup"><span data-stu-id="ce661-304">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="ce661-305">FilteringMessagesBeforePublishing;</span><span class="sxs-lookup"><span data-stu-id="ce661-305">FilteringMessagesBeforePublishing</span></span>
    - <span data-ttu-id="ce661-306">EnableSubscriptionPartitioning;</span><span class="sxs-lookup"><span data-stu-id="ce661-306">EnableSubscriptionPartitioning</span></span>
    - <span data-ttu-id="ce661-307">EntityAvailabilityStatus.</span><span class="sxs-lookup"><span data-stu-id="ce661-307">EntityAvailabilityStatus</span></span>

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

### <a name="type-subscriptionattribute"></a><span data-ttu-id="ce661-308">**Тип SubscriptionAttribute**</span><span class="sxs-lookup"><span data-stu-id="ce661-308">**Type SubscriptionAttribute**</span></span>
- <span data-ttu-id="ce661-309">Следующие свойства отмечены как устаревшие:</span><span class="sxs-lookup"><span data-stu-id="ce661-309">The following properties are marked as obsolete</span></span>
    - <span data-ttu-id="ce661-310">DeadLetteringOnFilterEvaluationExceptions;</span><span class="sxs-lookup"><span data-stu-id="ce661-310">DeadLetteringOnFilterEvaluationExceptions</span></span>
    - <span data-ttu-id="ce661-311">EntityAvailabilityStatus.</span><span class="sxs-lookup"><span data-stu-id="ce661-311">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="ce661-312">IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="ce661-312">IsReadOnly</span></span>
    - <span data-ttu-id="ce661-313">Расположение</span><span class="sxs-lookup"><span data-stu-id="ce661-313">Location</span></span>

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
