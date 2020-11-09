---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: 767f725633560d79cb19e1caad61c08772107b42
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249865"
---
# <span data-ttu-id="6ad6a-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6ad6a-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="6ad6a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6ad6a-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad6a-103">Получает подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="6ad6a-103">Gets a load balancer.</span></span>

## <span data-ttu-id="6ad6a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6ad6a-104">SYNTAX</span></span>

### <span data-ttu-id="6ad6a-105">NOEXPAND (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6ad6a-105">NoExpand (Default)</span></span>
```
Get-AzLoadBalancer [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ad6a-106">Кройте</span><span class="sxs-lookup"><span data-stu-id="6ad6a-106">Expand</span></span>
```
Get-AzLoadBalancer -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ad6a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ad6a-107">DESCRIPTION</span></span>
<span data-ttu-id="6ad6a-108">Командлет **Get-AzLoadBalancer** получает один или несколько подсистем балансировки нагрузки для Azure, которые содержатся в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ad6a-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="6ad6a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6ad6a-109">EXAMPLES</span></span>

### <span data-ttu-id="6ad6a-110">Пример 1: получение подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="6ad6a-110">Example 1: Get a load balancer</span></span>
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
                             "Name": "Basic"
                           }
```

<span data-ttu-id="6ad6a-111">Эта команда получает подсистему балансировки нагрузки с именем MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="6ad6a-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="6ad6a-112">Для выполнения этого командлета должна существовать подсистема балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="6ad6a-112">A load balancer must exist before you can run this cmdlet.</span></span>

### <span data-ttu-id="6ad6a-113">Пример 2: перечисление подсистем балансировки нагрузки с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="6ad6a-113">Example 2: List load balancers using filtering</span></span>
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
                             "Name": "Basic"
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
                             "Name": "Basic"
                           }
```

<span data-ttu-id="6ad6a-114">Эта команда получает все подсистемы балансировки нагрузки с именем, которое начинается с "MyLoadBalancer".</span><span class="sxs-lookup"><span data-stu-id="6ad6a-114">This command gets all load balancers with a name that starts with "MyLoadBalancer"</span></span>

## <span data-ttu-id="6ad6a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6ad6a-115">PARAMETERS</span></span>

### <span data-ttu-id="6ad6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad6a-116">-DefaultProfile</span></span>
<span data-ttu-id="6ad6a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ad6a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ad6a-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="6ad6a-118">-ExpandResource</span></span>
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

### <span data-ttu-id="6ad6a-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6ad6a-119">-Name</span></span>
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

### <span data-ttu-id="6ad6a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ad6a-120">-ResourceGroupName</span></span>
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

### <span data-ttu-id="6ad6a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad6a-121">CommonParameters</span></span>
<span data-ttu-id="6ad6a-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6ad6a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ad6a-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ad6a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad6a-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6ad6a-124">INPUTS</span></span>

### <span data-ttu-id="6ad6a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6ad6a-125">System.String</span></span>

## <span data-ttu-id="6ad6a-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ad6a-126">OUTPUTS</span></span>

### <span data-ttu-id="6ad6a-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6ad6a-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6ad6a-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="6ad6a-128">NOTES</span></span>

## <span data-ttu-id="6ad6a-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ad6a-129">RELATED LINKS</span></span>

[<span data-ttu-id="6ad6a-130">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6ad6a-130">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="6ad6a-131">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6ad6a-131">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="6ad6a-132">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6ad6a-132">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

