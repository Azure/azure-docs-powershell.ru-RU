---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
ms.openlocfilehash: d01919008adf8c15fa9b4a0c8144e279a3997a92
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074644"
---
# <span data-ttu-id="d5e40-101">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d5e40-101">Get-AzAvailabilitySet</span></span>

## <span data-ttu-id="d5e40-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d5e40-102">SYNOPSIS</span></span>
<span data-ttu-id="d5e40-103">Получает наборы доступности Azure в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d5e40-103">Gets Azure availability sets in a resource group.</span></span>

## <span data-ttu-id="d5e40-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d5e40-104">SYNTAX</span></span>

```
Get-AzAvailabilitySet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5e40-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5e40-105">DESCRIPTION</span></span>
<span data-ttu-id="d5e40-106">Командлет **Get-AzAvailabilitySet** получает наборы доступности Azure в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d5e40-106">The **Get-AzAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="d5e40-107">Вы можете указать имя определенного набора доступности, которое нужно получить.</span><span class="sxs-lookup"><span data-stu-id="d5e40-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="d5e40-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d5e40-108">EXAMPLES</span></span>

### <span data-ttu-id="d5e40-109">Пример 1: получение определенной группы доступности</span><span class="sxs-lookup"><span data-stu-id="d5e40-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="d5e40-110">Эта команда получает группу доступности с именем AvailabilitySet03 в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d5e40-110">This command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="d5e40-111">Пример 2: получение всех наборов доступности</span><span class="sxs-lookup"><span data-stu-id="d5e40-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet10
Name                      : AvailabilitySet10
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="d5e40-112">Эта команда получает все наборы доступности в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d5e40-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="d5e40-113">Пример 3: получение всех наборов доступности с фильтрацией</span><span class="sxs-lookup"><span data-stu-id="d5e40-113">Example 3: Get all availability sets with filtering</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup1*" -Name "AvailabilitySet0*"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="d5e40-114">Эта команда получает все наборы доступности в группе ресурсов с именем ResourceGroup11, которая начинается с "AvailabilitySet0".</span><span class="sxs-lookup"><span data-stu-id="d5e40-114">This command gets all the availability sets in the resource group named ResourceGroup11 that start with "AvailabilitySet0".</span></span>

### <span data-ttu-id="d5e40-115">Пример 4: получение всех наборов доступности с именем, начинающимся с AvailabilitySet0</span><span class="sxs-lookup"><span data-stu-id="d5e40-115">Example 4: Get all availability sets with name starting with AvailabilitySet0</span></span>
```
PS C:\> Get-AzAvailabilitySet -Name AvailabilitySet0*

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup12
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup12/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="d5e40-116">Эта команда получает все наборы доступности, которые начинаются с "AvailabilitySet0".</span><span class="sxs-lookup"><span data-stu-id="d5e40-116">This command gets all the availability sets that start with "AvailabilitySet0".</span></span>

## <span data-ttu-id="d5e40-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d5e40-117">PARAMETERS</span></span>

### <span data-ttu-id="d5e40-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5e40-118">-DefaultProfile</span></span>
<span data-ttu-id="d5e40-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d5e40-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e40-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d5e40-120">-Name</span></span>
<span data-ttu-id="d5e40-121">Указывает имя набора доступности, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d5e40-121">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d5e40-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5e40-122">-ResourceGroupName</span></span>
<span data-ttu-id="d5e40-123">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d5e40-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d5e40-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5e40-124">CommonParameters</span></span>
<span data-ttu-id="d5e40-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d5e40-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5e40-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5e40-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5e40-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d5e40-127">INPUTS</span></span>

### <span data-ttu-id="d5e40-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d5e40-128">System.String</span></span>

## <span data-ttu-id="d5e40-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5e40-129">OUTPUTS</span></span>

### <span data-ttu-id="d5e40-130">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d5e40-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="d5e40-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="d5e40-131">NOTES</span></span>

## <span data-ttu-id="d5e40-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5e40-132">RELATED LINKS</span></span>

[<span data-ttu-id="d5e40-133">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d5e40-133">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)

[<span data-ttu-id="d5e40-134">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d5e40-134">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


