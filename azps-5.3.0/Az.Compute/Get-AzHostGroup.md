---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
ms.openlocfilehash: e0d15be05bf5678eb645a2a26dc2459e6790210a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509202"
---
# <span data-ttu-id="4d332-101">Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="4d332-101">Get-AzHostGroup</span></span>

## <span data-ttu-id="4d332-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d332-102">SYNOPSIS</span></span>
<span data-ttu-id="4d332-103">Получить или перечислить hosts.</span><span class="sxs-lookup"><span data-stu-id="4d332-103">Get or list hosts.</span></span>

## <span data-ttu-id="4d332-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4d332-104">SYNTAX</span></span>

### <span data-ttu-id="4d332-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4d332-105">DefaultParameter (Default)</span></span>
```
Get-AzHostGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d332-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="4d332-106">ResourceIdParameter</span></span>
```
Get-AzHostGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d332-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d332-107">DESCRIPTION</span></span>
<span data-ttu-id="4d332-108">Этот cmdlet получит группу хостов.</span><span class="sxs-lookup"><span data-stu-id="4d332-108">This cmdlet will get a host group.</span></span>
<span data-ttu-id="4d332-109">Этот cmdlet также содержит список всех групп хостов в группе ресурсов, если имя группы не задано.</span><span class="sxs-lookup"><span data-stu-id="4d332-109">This cmdlet also lists all host groups in a resource group if a host group name is not given.</span></span>
<span data-ttu-id="4d332-110">Этот cmdlet также содержит список всех групп хостов в подписке, если ни имя группы хоста, ни названия группы ресурсов не задано.</span><span class="sxs-lookup"><span data-stu-id="4d332-110">This cmdlet also lists all host groups in a subscription if neither host group name nor resource group name is given.</span></span>

## <span data-ttu-id="4d332-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4d332-111">EXAMPLES</span></span>

### <span data-ttu-id="4d332-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4d332-112">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="4d332-113">Эта команда возвращает группу хостов.</span><span class="sxs-lookup"><span data-stu-id="4d332-113">This command returns a host group.</span></span>

### <span data-ttu-id="4d332-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4d332-114">Example 2</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
```

<span data-ttu-id="4d332-115">Эта команда возвращает все группы хостов в заданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4d332-115">This command returns all host groups in the given resource group.</span></span>

### <span data-ttu-id="4d332-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="4d332-116">Example 3</span></span>
```
PS C:\> Get-AzHostGroup

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
myrg02                     myhostgroup03   eastus {[key1, val1]}       2
```

<span data-ttu-id="4d332-117">Эта команда возвращает все группы хостов в подписке.</span><span class="sxs-lookup"><span data-stu-id="4d332-117">This command returns all host groups in the subscription.</span></span>

## <span data-ttu-id="4d332-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d332-118">PARAMETERS</span></span>

### <span data-ttu-id="4d332-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d332-119">-DefaultProfile</span></span>
<span data-ttu-id="4d332-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4d332-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d332-121">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="4d332-121">-InstanceView</span></span>
<span data-ttu-id="4d332-122">Развернете возвращаемый объект, чтобы также получить список представлений экземпляров хоста.</span><span class="sxs-lookup"><span data-stu-id="4d332-122">Expand the returned object to also list the host's instance views.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d332-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4d332-123">-Name</span></span>
<span data-ttu-id="4d332-124">Имя группы хостов.</span><span class="sxs-lookup"><span data-stu-id="4d332-124">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d332-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d332-125">-ResourceGroupName</span></span>
<span data-ttu-id="4d332-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4d332-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d332-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d332-127">-ResourceId</span></span>
<span data-ttu-id="4d332-128">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="4d332-128">The ID of the resource.</span></span>

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

### <span data-ttu-id="4d332-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d332-129">CommonParameters</span></span>
<span data-ttu-id="4d332-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d332-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d332-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d332-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d332-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d332-132">INPUTS</span></span>

### <span data-ttu-id="4d332-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4d332-133">System.String</span></span>

## <span data-ttu-id="4d332-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4d332-134">OUTPUTS</span></span>

### <span data-ttu-id="4d332-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="4d332-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="4d332-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4d332-136">NOTES</span></span>

## <span data-ttu-id="4d332-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d332-137">RELATED LINKS</span></span>