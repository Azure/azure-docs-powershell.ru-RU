---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: e106656124aea48dff6c7fd7183027e183dce93b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213721"
---
# <span data-ttu-id="0eb96-101">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0eb96-101">New-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="0eb96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0eb96-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb96-103">Создает пул адресов для резервирования загрузки.</span><span class="sxs-lookup"><span data-stu-id="0eb96-103">Creates a backend address pool on a loadbalancer.</span></span> 

## <span data-ttu-id="0eb96-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0eb96-104">SYNTAX</span></span>

### <span data-ttu-id="0eb96-105">CreateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0eb96-105">CreateByNameParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eb96-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0eb96-106">CreateByParentObjectParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -LoadBalancer <PSLoadBalancer> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eb96-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0eb96-107">DESCRIPTION</span></span>
<span data-ttu-id="0eb96-108">Создает пул адресов для резервирования загрузки.</span><span class="sxs-lookup"><span data-stu-id="0eb96-108">Creates a backend address pool on a loadbalancer.</span></span> <span data-ttu-id="0eb96-109">Разрешает выбор массива PSLoadBalancerBackendAddress.</span><span class="sxs-lookup"><span data-stu-id="0eb96-109">Allows for specifiying a array of PSLoadBalancerBackendAddress.</span></span> 
## <span data-ttu-id="0eb96-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0eb96-110">EXAMPLES</span></span>

### <span data-ttu-id="0eb96-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0eb96-111">Example 1</span></span>
```powershell
## create by passing loadbalancer without Ips
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ips = @($ip1, $ip2)

PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="0eb96-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0eb96-112">Example 2</span></span>
```powershell
## create by passing loadbalancer with ips
PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool7 -LoadBalancerBackendAddress $ips
```

### <span data-ttu-id="0eb96-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="0eb96-113">Example 3</span></span>
```powershell
## create by name without ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3
```

### <span data-ttu-id="0eb96-114">Пример 4</span><span class="sxs-lookup"><span data-stu-id="0eb96-114">Example 4</span></span>
```powershell
## create by name with ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3 -LoadBalancerBackendAddress $ips
```

## <span data-ttu-id="0eb96-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0eb96-115">PARAMETERS</span></span>

### <span data-ttu-id="0eb96-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eb96-116">-DefaultProfile</span></span>
<span data-ttu-id="0eb96-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0eb96-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb96-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0eb96-118">-LoadBalancer</span></span>
<span data-ttu-id="0eb96-119">Ресурс балансировы нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0eb96-119">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0eb96-120">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="0eb96-120">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="0eb96-121">Backend addresses (Адреса на заднем и обратном адресах).</span><span class="sxs-lookup"><span data-stu-id="0eb96-121">The backend addresses.</span></span>

```yaml
Type: PSLoadBalancerBackendAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb96-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="0eb96-122">-LoadBalancerName</span></span>
<span data-ttu-id="0eb96-123">Имя балансира нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0eb96-123">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb96-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0eb96-124">-Name</span></span>
<span data-ttu-id="0eb96-125">Имя пула backend.</span><span class="sxs-lookup"><span data-stu-id="0eb96-125">The name of the backend pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb96-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eb96-126">-ResourceGroupName</span></span>
<span data-ttu-id="0eb96-127">Имя группы ресурсов балансира нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0eb96-127">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb96-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0eb96-128">-Confirm</span></span>
<span data-ttu-id="0eb96-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0eb96-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb96-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eb96-130">-WhatIf</span></span>
<span data-ttu-id="0eb96-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eb96-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0eb96-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0eb96-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb96-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb96-133">CommonParameters</span></span>
<span data-ttu-id="0eb96-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eb96-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb96-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0eb96-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb96-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0eb96-136">INPUTS</span></span>

### <span data-ttu-id="0eb96-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0eb96-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0eb96-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0eb96-138">OUTPUTS</span></span>

### <span data-ttu-id="0eb96-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0eb96-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="0eb96-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0eb96-140">NOTES</span></span>

## <span data-ttu-id="0eb96-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0eb96-141">RELATED LINKS</span></span>
