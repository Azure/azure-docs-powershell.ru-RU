---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: dd887874540a216cc826f807059e6534b99e28f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413951"
---
# <span data-ttu-id="27bb6-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27bb6-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="27bb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27bb6-102">SYNOPSIS</span></span>
<span data-ttu-id="27bb6-103">Возвращает баланс нагрузки.</span><span class="sxs-lookup"><span data-stu-id="27bb6-103">Gets a load balancer.</span></span>

## <span data-ttu-id="27bb6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="27bb6-104">SYNTAX</span></span>

### <span data-ttu-id="27bb6-105">NoExpand (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="27bb6-105">NoExpand (Default)</span></span>
```
Get-AzLoadBalancer [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="27bb6-106">Развернуть</span><span class="sxs-lookup"><span data-stu-id="27bb6-106">Expand</span></span>
```
Get-AzLoadBalancer -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27bb6-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27bb6-107">DESCRIPTION</span></span>
<span data-ttu-id="27bb6-108">Для **этого можно** получить один или несколько балансовых балансов нагрузки Azure, которые содержатся в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="27bb6-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="27bb6-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="27bb6-109">EXAMPLES</span></span>

### <span data-ttu-id="27bb6-110">Пример 1. Остаток на балансе нагрузки</span><span class="sxs-lookup"><span data-stu-id="27bb6-110">Example 1: Get a load balancer</span></span>
```
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer1" -ResourceGroupName "MyResourceGroup"

Name                     : MyLoadBalancer1
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }
```

<span data-ttu-id="27bb6-111">Эта команда возвращает балансировку нагрузки MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="27bb6-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="27bb6-112">Перед запуском этого cmdlet необходимо иметь баланс нагрузки.</span><span class="sxs-lookup"><span data-stu-id="27bb6-112">A load balancer must exist before you can run this cmdlet.</span></span>

### <span data-ttu-id="27bb6-113">Пример 2. Балансиры нагрузки списков с использованием фильтрации</span><span class="sxs-lookup"><span data-stu-id="27bb6-113">Example 2: List load balancers using filtering</span></span>
```
PS C:\> Get-AzLoadBalancer -Name MyLoadBalancer*

Name                     : MyLoadBalancer1
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }

Name                     : MyLoadBalancer2
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer2
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }
```

<span data-ttu-id="27bb6-114">Эта команда получает все балансиры нагрузки с именем, которое начинается с "MyLoadBalancer"</span><span class="sxs-lookup"><span data-stu-id="27bb6-114">This command gets all load balancers with a name that starts with "MyLoadBalancer"</span></span>

## <span data-ttu-id="27bb6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27bb6-115">PARAMETERS</span></span>

### <span data-ttu-id="27bb6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27bb6-116">-DefaultProfile</span></span>
<span data-ttu-id="27bb6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="27bb6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27bb6-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="27bb6-118">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27bb6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="27bb6-119">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="27bb6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27bb6-120">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="27bb6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27bb6-121">CommonParameters</span></span>
<span data-ttu-id="27bb6-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27bb6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27bb6-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27bb6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27bb6-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="27bb6-124">INPUTS</span></span>

### <span data-ttu-id="27bb6-125">System.String</span><span class="sxs-lookup"><span data-stu-id="27bb6-125">System.String</span></span>

## <span data-ttu-id="27bb6-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="27bb6-126">OUTPUTS</span></span>

### <span data-ttu-id="27bb6-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27bb6-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="27bb6-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="27bb6-128">NOTES</span></span>

## <span data-ttu-id="27bb6-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27bb6-129">RELATED LINKS</span></span>

[<span data-ttu-id="27bb6-130">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27bb6-130">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="27bb6-131">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27bb6-131">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="27bb6-132">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27bb6-132">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


