---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHost.md
ms.openlocfilehash: cc9b536517a70fd7c004be6fcac300afa0a4760b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727473"
---
# <span data-ttu-id="498f8-101">Get-AzHost</span><span class="sxs-lookup"><span data-stu-id="498f8-101">Get-AzHost</span></span>

## <span data-ttu-id="498f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="498f8-102">SYNOPSIS</span></span>
<span data-ttu-id="498f8-103">Получение или перечисление узлов.</span><span class="sxs-lookup"><span data-stu-id="498f8-103">Get or list hosts.</span></span>

## <span data-ttu-id="498f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="498f8-104">SYNTAX</span></span>

### <span data-ttu-id="498f8-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="498f8-105">DefaultParameter (Default)</span></span>
```
Get-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="498f8-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="498f8-106">ResourceIdParameter</span></span>
```
Get-AzHost [-ResourceId] <String> [-InstanceView] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="498f8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="498f8-107">DESCRIPTION</span></span>
<span data-ttu-id="498f8-108">Этот командлет получит узел в группе узлов.</span><span class="sxs-lookup"><span data-stu-id="498f8-108">This cmdlet will get a host in a host group.</span></span>
<span data-ttu-id="498f8-109">Этот командлет также перечисляет все узлы в группе узлов, если не задано имя узла.</span><span class="sxs-lookup"><span data-stu-id="498f8-109">This cmdlet also lists all hosts in a host group if a host name is not given.</span></span>

## <span data-ttu-id="498f8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="498f8-110">EXAMPLES</span></span>

### <span data-ttu-id="498f8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="498f8-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName

ResourceGroupName    : myrg01
PlatformFaultDomain  : 1
AutoReplaceOnFailure : True
HostId               : 00000000-0000-0000-0000-000000000000
VirtualMachines[0]   : 
  Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/virtualMachines/myvm01
VirtualMachines[1]   : 
  Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/virtualMachines/myvm02
ProvisioningTime     : 7/27/2019 3:22:59 AM
ProvisioningState    : Succeeded
Sku                  : 
  Name               : ESv3-Type1
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                 : myhost01
Location             : eastus
Tags                 : {"key1":"val2"}
```

<span data-ttu-id="498f8-112">Эта команда возвращает узел.</span><span class="sxs-lookup"><span data-stu-id="498f8-112">This command returns a host.</span></span>

### <span data-ttu-id="498f8-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="498f8-113">Example 2</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName -InstanceView

ResourceGroupName      : myrg01
PlatformFaultDomain    : 0
AutoReplaceOnFailure   : True
HostId                 : 00000000-0000-0000-0000-000000000000
ProvisioningTime       : 8/19/2019 9:13:19 PM
ProvisioningState      : Succeeded
InstanceView           : 
  AssetId              : 00000000-0000-0000-0000-000000000000
  AvailableCapacity    : 
    AllocatableVMs[0]  : 
      VmSize           : Standard_E2s_v3
      Count            : 28
    AllocatableVMs[1]  : 
      VmSize           : Standard_E4-2s_v3
      Count            : 14
    AllocatableVMs[2]  : 
      VmSize           : Standard_E4s_v3
      Count            : 14
  Statuses[0]          : 
    Code               : ProvisioningState/succeeded
    Level              : Info
    DisplayStatus      : Provisioning succeeded
    Time               : 8/19/2019 9:13:19 PM
  Statuses[1]          : 
    Code               : HealthState/available
    Level              : Info
    DisplayStatus      : Host available
Sku                    : 
  Name                 : ESv3-Type1
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                   : crptestps2264host
Location               : eastus
Tags                   : {"key1":"val2"}
```

<span data-ttu-id="498f8-114">Эта команда возвращает представление экземпляра узла.</span><span class="sxs-lookup"><span data-stu-id="498f8-114">This command returns the instance view of a host.</span></span>

### <span data-ttu-id="498f8-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="498f8-115">Example 3</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName

ResourceGroupName       Name Location           Tags        Sku FD
-----------------       ---- --------           ----        --- --
myrg01              myhost01   eastus {[key1, val2]} ESv3-Type1  0
myrg01              myhost02   eastus {[key1, val2]} ESv3-Type1  1
```

<span data-ttu-id="498f8-116">Эта команда возвращает все узлы в заданной группе узлов.</span><span class="sxs-lookup"><span data-stu-id="498f8-116">This command returns all hosts in the given host group.</span></span>

## <span data-ttu-id="498f8-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="498f8-117">PARAMETERS</span></span>

### <span data-ttu-id="498f8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="498f8-118">-DefaultProfile</span></span>
<span data-ttu-id="498f8-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="498f8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="498f8-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="498f8-120">-HostGroupName</span></span>
<span data-ttu-id="498f8-121">Имя группы узлов.</span><span class="sxs-lookup"><span data-stu-id="498f8-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="498f8-122">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="498f8-122">-InstanceView</span></span>
<span data-ttu-id="498f8-123">Указывает на то, что этот командлет получает только представление экземпляра узла.</span><span class="sxs-lookup"><span data-stu-id="498f8-123">Indicates that this cmdlet gets only the instance view of the host.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="498f8-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="498f8-124">-Name</span></span>
<span data-ttu-id="498f8-125">Имя узла.</span><span class="sxs-lookup"><span data-stu-id="498f8-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="498f8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="498f8-126">-ResourceGroupName</span></span>
<span data-ttu-id="498f8-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="498f8-127">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="498f8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="498f8-128">-ResourceId</span></span>
<span data-ttu-id="498f8-129">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="498f8-129">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="498f8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="498f8-130">CommonParameters</span></span>
<span data-ttu-id="498f8-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="498f8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="498f8-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="498f8-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="498f8-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="498f8-133">INPUTS</span></span>

### <span data-ttu-id="498f8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="498f8-134">System.String</span></span>

## <span data-ttu-id="498f8-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="498f8-135">OUTPUTS</span></span>

### <span data-ttu-id="498f8-136">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSHost</span><span class="sxs-lookup"><span data-stu-id="498f8-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="498f8-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="498f8-137">NOTES</span></span>

## <span data-ttu-id="498f8-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="498f8-138">RELATED LINKS</span></span>
