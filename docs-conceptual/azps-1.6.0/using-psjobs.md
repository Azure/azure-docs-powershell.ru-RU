---
title: Выполняйте командлеты в параллельном режиме с помощью заданий PowerShell
description: Как выполнять командлеты в параллельном режиме с помощью параметра -AsJob.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 58aa777ca599c2a6181f0ecc5c20f6db7a89b75f
ms.sourcegitcommit: 8f59e11e5c991543964154d63648aa1e6ae22512
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/26/2019
ms.locfileid: "58475622"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a><span data-ttu-id="18fd4-103">Выполнение командлетов в параллельном режиме с помощью заданий PowerShell</span><span class="sxs-lookup"><span data-stu-id="18fd4-103">Running cmdlets in parallel using PowerShell jobs</span></span>

<span data-ttu-id="18fd4-104">PowerShell поддерживает выполнение асинхронных действий с помощью [заданий PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="18fd4-104">PowerShell supports asynchronous action with [PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>
<span data-ttu-id="18fd4-105">Azure PowerShell в значительной степени зависит от выполнения и ожидания сетевых вызовов в Azure.</span><span class="sxs-lookup"><span data-stu-id="18fd4-105">Azure PowerShell is heavily dependent on making, and waiting for, network calls to Azure.</span></span> <span data-ttu-id="18fd4-106">Возможно, вам часто требуется выполнять неблокирующие вызовы.</span><span class="sxs-lookup"><span data-stu-id="18fd4-106">You may often find yourself needing to make non-blocking calls.</span></span> <span data-ttu-id="18fd4-107">Для решения такой задачи Azure PowerShell предоставляет первоклассную поддержку [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="18fd4-107">To address this need, Azure PowerShell provides first-class [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) support.</span></span>

## <a name="context-persistence-and-psjobs"></a><span data-ttu-id="18fd4-108">Сохранение контекста и PSJobs</span><span class="sxs-lookup"><span data-stu-id="18fd4-108">Context Persistence and PSJobs</span></span>

<span data-ttu-id="18fd4-109">Так как задания PSJob выполняются как отдельные процессы, необходимо обеспечить передачу сведений о подключении к Azure в эти задания.</span><span class="sxs-lookup"><span data-stu-id="18fd4-109">Since PSJobs are run as separate processes, your Azure connection must be shared with them.</span></span> <span data-ttu-id="18fd4-110">После входа в учетную запись Azure с помощью `Connect-AzAccount` передайте контекст в задание.</span><span class="sxs-lookup"><span data-stu-id="18fd4-110">After signing in to your Azure account with `Connect-AzAccount`, pass the context to a job.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -Arguments (Get-AzContext),$creds
```

<span data-ttu-id="18fd4-111">Но если вы настроили для контекста автоматическое сохранение с помощью `Enable-AzContextAutosave`, то контекст автоматически будет доступными для создаваемых заданий.</span><span class="sxs-lookup"><span data-stu-id="18fd4-111">However, if you have chosen to have your context automatically saved with `Enable-AzContextAutosave`, the context is automatically shared with any jobs you create.</span></span>

```azurepowershell-interactive
Enable-AzContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin} -Arguments $creds
```

## <a name="automatic-jobs-with--asjob"></a><span data-ttu-id="18fd4-112">Выполнение автоматических заданий с помощью `-AsJob`</span><span class="sxs-lookup"><span data-stu-id="18fd4-112">Automatic Jobs with `-AsJob`</span></span>

<span data-ttu-id="18fd4-113">Для удобства Azure PowerShell также предоставляет параметр `-AsJob` для некоторых длительно выполняющихся командлетов.</span><span class="sxs-lookup"><span data-stu-id="18fd4-113">As a convenience, Azure PowerShell also provides an `-AsJob` switch on some long-running cmdlets.</span></span>
<span data-ttu-id="18fd4-114">Параметр `-AsJob` еще больше упрощает создание PSJobs.</span><span class="sxs-lookup"><span data-stu-id="18fd4-114">The `-AsJob` switch makes creating PSJobs even easier.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzVM -Name MyVm -Credential $creds -AsJob
```

<span data-ttu-id="18fd4-115">Задание и ход выполнения можно проверить в любое время с помощью `Get-Job` и `Get-AzVM`.</span><span class="sxs-lookup"><span data-stu-id="18fd4-115">You can inspect the job and progress at any time with `Get-Job` and `Get-AzVM`.</span></span>

```azurepowershell-interactive
Get-Job $job
Get-AzVM MyVm
```

```output
Id Name                                       PSJobTypeName         State   HasMoreData Location  Command
-- ----                                       -------------         -----   ----------- --------  -------
1  Long Running Operation for 'New-AzVM' AzureLongRunningJob`1 Running True        localhost New-AzVM

ResourceGroupName    Name Location          VmSize  OsType     NIC ProvisioningState Zone
-----------------    ---- --------          ------  ------     --- ----------------- ----
MyVm                 MyVm   eastus Standard_DS1_v2 Windows    MyVm          Creating
```

<span data-ttu-id="18fd4-116">Когда задание завершится, получите его результат с помощью `Receive-Job`.</span><span class="sxs-lookup"><span data-stu-id="18fd4-116">When the job completes, get the result of the job with `Receive-Job`.</span></span>

> [!NOTE]
> <span data-ttu-id="18fd4-117">`Receive-Job` возвращает результат от командлета так, как если бы флаг `-AsJob` отсутствовал.</span><span class="sxs-lookup"><span data-stu-id="18fd4-117">`Receive-Job` returns the result from the cmdlet as if the `-AsJob` flag were not present.</span></span>
> <span data-ttu-id="18fd4-118">Например, результат `Receive-Job` для `Do-Action -AsJob` будет того же типа, что и результат для `Do-Action`.</span><span class="sxs-lookup"><span data-stu-id="18fd4-118">For example, the `Receive-Job` result of `Do-Action -AsJob` is of the same type as the result of `Do-Action`.</span></span>

```azurepowershell-interactive
$vm = Receive-Job $job
$vm
```

```output
ResourceGroupName        : MyVm
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyVm/providers/Microsoft.Compute/virtualMachines/MyVm
VmId                     : dff1f79e-a8f7-4664-ab72-0ec28b9fbb5b
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvmmyvm.eastus.cloudapp.azure.com
```

## <a name="example-scenarios"></a><span data-ttu-id="18fd4-119">Примеры сценариев</span><span class="sxs-lookup"><span data-stu-id="18fd4-119">Example Scenarios</span></span>

<span data-ttu-id="18fd4-120">Создайте несколько виртуальных машин за раз:</span><span class="sxs-lookup"><span data-stu-id="18fd4-120">Create several VMs at once:</span></span>

```azurepowershell-interactive
$creds = Get-Credential
# Create 10 jobs.
for($k = 0; $k -lt 10; $k++) {
    New-AzVm -Name MyVm$k  -Credential $creds -AsJob
}

# Get all jobs and wait on them.
Get-Job | Wait-Job
"All jobs completed"
Get-AzVM
```

<span data-ttu-id="18fd4-121">В этом примере командлет `Wait-Job` приостанавливает работу скрипта во время выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="18fd4-121">In this example, the `Wait-Job` cmdlet causes the script to pause while jobs run.</span></span> <span data-ttu-id="18fd4-122">Скрипт продолжит работу после выполнения всех заданий.</span><span class="sxs-lookup"><span data-stu-id="18fd4-122">The script continues executing once all of the jobs have completed.</span></span> <span data-ttu-id="18fd4-123">Прежде чем продолжить, скрипт ожидает завершения нескольких заданий, которые выполняются одновременно.</span><span class="sxs-lookup"><span data-stu-id="18fd4-123">Several jobs run in parallel then the script waits for completion before continuing.</span></span>

```output
Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
3      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
4      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
5      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
6      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
7      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
8      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
9      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
10     Long Running... AzureLongRun... Running       True            localhost            New-AzVM
11     Long Running... AzureLongRun... Running       True            localhost            New-AzVM
2      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
3      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
4      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
5      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
6      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
7      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
8      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
9      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
10     Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
11     Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
All Jobs completed.

ResourceGroupName        Name   Location          VmSize  OsType           NIC ProvisioningState Zone
-----------------        ----   --------          ------  ------           --- ----------------- ----
MYVM                     MyVm     eastus Standard_DS1_v2 Windows          MyVm         Succeeded
MYVM0                   MyVm0     eastus Standard_DS1_v2 Windows         MyVm0         Succeeded
MYVM1                   MyVm1     eastus Standard_DS1_v2 Windows         MyVm1         Succeeded
MYVM2                   MyVm2     eastus Standard_DS1_v2 Windows         MyVm2         Succeeded
MYVM3                   MyVm3     eastus Standard_DS1_v2 Windows         MyVm3         Succeeded
MYVM4                   MyVm4     eastus Standard_DS1_v2 Windows         MyVm4         Succeeded
MYVM5                   MyVm5     eastus Standard_DS1_v2 Windows         MyVm5         Succeeded
MYVM6                   MyVm6     eastus Standard_DS1_v2 Windows         MyVm6         Succeeded
MYVM7                   MyVm7     eastus Standard_DS1_v2 Windows         MyVm7         Succeeded
MYVM8                   MyVm8     eastus Standard_DS1_v2 Windows         MyVm8         Succeeded
MYVM9                   MyVm9     eastus Standard_DS1_v2 Windows         MyVm9         Succeeded
```