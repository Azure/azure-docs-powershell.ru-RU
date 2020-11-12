---
title: Выходные данные запроса командлетов Azure PowerShell
description: Как обратиться к ресурсам в Azure и форматировать результаты запроса.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/10/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 71de99fec7de36cf8cc0fe3e8840fb55cedc5db7
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2020
ms.locfileid: "93408893"
---
# <a name="query-output-of-azure-powershell"></a><span data-ttu-id="63e99-103">Выходные данные запроса к Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="63e99-103">Query output of Azure PowerShell</span></span> 

<span data-ttu-id="63e99-104">Результаты каждого командлета Azure PowerShell представлены в виде объекта Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="63e99-104">The results of each Azure PowerShell cmdlet are an Azure PowerShell object.</span></span> <span data-ttu-id="63e99-105">Даже командлеты, не являющиеся явными операциями `Get-`, могут возвращать значение, которое можно проверить, чтобы получить информацию о созданном или измененном ресурсе.</span><span class="sxs-lookup"><span data-stu-id="63e99-105">Even cmdlets that aren't explicitly `Get-` operations might return a value that can be inspected, to give information about a resource that was created or modified.</span></span> <span data-ttu-id="63e99-106">Хотя большинство командлетов возвращают один объект, некоторые возвращают массив, для которого необходимо выполнять итерацию.</span><span class="sxs-lookup"><span data-stu-id="63e99-106">While most cmdlets return a single object, some return an array that should be iterated through.</span></span>

<span data-ttu-id="63e99-107">Практически во всех случаях запрос возвращает выходные данные Azure PowerShell с помощью командлета [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object), который часто сокращается до `select`.</span><span class="sxs-lookup"><span data-stu-id="63e99-107">In almost all cases, you query output from Azure PowerShell with the [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object) cmdlet, often abbreviated to `select`.</span></span> <span data-ttu-id="63e99-108">Выходные данные можно отфильтровать с помощью [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object) или его псевдонима `where`.</span><span class="sxs-lookup"><span data-stu-id="63e99-108">Output can be filtered with [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object), or its alias `where`.</span></span>

## <a name="select-simple-properties"></a><span data-ttu-id="63e99-109">Выбор простых свойств</span><span class="sxs-lookup"><span data-stu-id="63e99-109">Select simple properties</span></span>

<span data-ttu-id="63e99-110">В формате таблицы по умолчанию для командлетов Azure PowerShell не отображаются все доступные свойства.</span><span class="sxs-lookup"><span data-stu-id="63e99-110">In the default table format, Azure PowerShell cmdlets don't display all of their available properties.</span></span> <span data-ttu-id="63e99-111">Полный список свойств можно получить, воспользовавшись командлетом [Format-List](/powershell/module/microsoft.powershell.utility/format-list) или передав выходные данные в `Select-Object *`:</span><span class="sxs-lookup"><span data-stu-id="63e99-111">You can get the full properties by using the [Format-List](/powershell/module/microsoft.powershell.utility/format-list) cmdlet, or by piping output to `Select-Object *`:</span></span>

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object *
```

```output
ResourceGroupName        : TESTGROUP
Id                       : /subscriptions/711d8ed1-b888-4c52-8ab9-66f07b87eb6b/resourceGroups/TESTGROUP/providers/Micro
                           soft.Compute/virtualMachines/TestVM
VmId                     : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
Name                     : TestVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
LicenseType              :
Tags                     : {}
AvailabilitySetReference :
DiagnosticsProfile       :
Extensions               : {}
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
Plan                     :
ProvisioningState        : Succeeded
StorageProfile           : Microsoft.Azure.Management.Compute.Models.StorageProfile
DisplayHint              : Compact
Identity                 :
Zones                    : {}
FullyQualifiedDomainName :
AdditionalCapabilities   :
RequestId                : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
StatusCode               : OK
```

<span data-ttu-id="63e99-112">Как только вы узнаете имена интересующих вас свойств, такие имена можно будет использовать с `Select-Object`, чтобы получить свойства напрямую:</span><span class="sxs-lookup"><span data-stu-id="63e99-112">Once you know the names of the properties that you're interested in, you can use those property names with `Select-Object` to get them directly:</span></span>

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object Name,VmId,ProvisioningState
```

```output
Name   VmId                                 ProvisioningState
----   ----                                 -----------------
TestVM 711d8ed1-b888-4c52-8ab9-66f07b87eb6b Succeeded
```

<span data-ttu-id="63e99-113">Результат выполнения `Select-Object` всегда форматируется для отображения запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="63e99-113">Output from using `Select-Object` is always formatted to display the requested information.</span></span> <span data-ttu-id="63e99-114">Чтобы узнать об использовании форматирования в качестве части результатов запроса командлета, см. статью [Форматирование выходных данных командлетов Azure PowerShell](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="63e99-114">To learn about using formatting as part of querying cmdlet results, see [Format Azure PowerShell cmdlet output](formatting-output.md).</span></span>

## <a name="select-nested-properties"></a><span data-ttu-id="63e99-115">Выбор вложенных свойств</span><span class="sxs-lookup"><span data-stu-id="63e99-115">Select nested properties</span></span>

<span data-ttu-id="63e99-116">В некоторых свойствах выходных данных командлета Azure PowerShell используются вложенные объекты, например свойство `StorageProfile` в выходных данных `Get-AzVM`.</span><span class="sxs-lookup"><span data-stu-id="63e99-116">Some properties in Azure PowerShell cmdlet output use nested objects, like the `StorageProfile` property of `Get-AzVM` output.</span></span> <span data-ttu-id="63e99-117">Чтобы получить значение из вложенного свойства, укажите отображаемое имя и полный путь к значению, которое необходимо проверить, как часть аргумента словаря в `Select-Object`:</span><span class="sxs-lookup"><span data-stu-id="63e99-117">To get a value from a nested property, provide a display name and the full path to the value you want to inspect as part of a dictionary argument to `Select-Object`:</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Select-Object Name,@{Name="OSType"; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name     OSType
----     ------
TestVM    Linux
TestVM2   Linux
WinVM   Windows
```

<span data-ttu-id="63e99-118">Каждый аргумент словаря выбирает одно свойство из объекта.</span><span class="sxs-lookup"><span data-stu-id="63e99-118">Each dictionary argument selects one property from the object.</span></span> <span data-ttu-id="63e99-119">Извлекаемое свойство должно быть частью выражения.</span><span class="sxs-lookup"><span data-stu-id="63e99-119">The property to extract must be part of an expression.</span></span>

## <a name="filter-results"></a><span data-ttu-id="63e99-120">Фильтрация результатов</span><span class="sxs-lookup"><span data-stu-id="63e99-120">Filter results</span></span> 

<span data-ttu-id="63e99-121">Командлет `Where-Object` позволяет фильтровать результаты в зависимости от любого значения свойства, включая вложенные свойства.</span><span class="sxs-lookup"><span data-stu-id="63e99-121">The `Where-Object` cmdlet allows you to filter the result based on any property value, including nested properties.</span></span> <span data-ttu-id="63e99-122">В следующем примере показано, как использовать `Where-Object` для поиска виртуальных машин Linux в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63e99-122">The next example shows how to use `Where-Object` to find the Linux VMs in a resource group.</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OSDisk.OSType -eq "Linux"}
```

```output
ResourceGroupName    Name Location          VmSize OsType        NIC ProvisioningState Zone
-----------------    ---- --------          ------ ------        --- ----------------- ----
TestGroup          TestVM  westus2 Standard_D2s_v3  Linux  testvm299         Succeeded
TestGroup         TestVM2  westus2 Standard_D2s_v3  Linux testvm2669         Succeeded
```

<span data-ttu-id="63e99-123">Вы можете передать результаты `Select-Object` и `Where-Object` из одного командлета в другой.</span><span class="sxs-lookup"><span data-stu-id="63e99-123">You can pipe the results of `Select-Object` and `Where-Object` to each other.</span></span> <span data-ttu-id="63e99-124">Чтобы повысить производительность, рекомендуем поместить операцию `Where-Object` перед `Select-Object`:</span><span class="sxs-lookup"><span data-stu-id="63e99-124">For performance purposes, it's always recommended to put the `Where-Object` operation before `Select-Object`:</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OsDisk.OsType -eq "Linux"} | `
    Select-Object Name,VmID,ProvisioningState
```

```output
Name    VmId                                 ProvisioningState
----    ----                                 -----------------
TestVM  711d8ed1-b888-4c52-8ab9-66f07b87eb6  Succeeded
TestVM2 cbcee769-dd78-45e3-a14d-2ad11c647d0  Succeeded
```
