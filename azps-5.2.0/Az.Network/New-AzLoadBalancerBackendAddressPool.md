---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: e106656124aea48dff6c7fd7183027e183dce93b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398676"
---
# <span data-ttu-id="3d7a8-101">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3d7a8-101">New-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="3d7a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d7a8-102">SYNOPSIS</span></span>
<span data-ttu-id="3d7a8-103">Создает пул адресов для резервирования загрузки.</span><span class="sxs-lookup"><span data-stu-id="3d7a8-103">Creates a backend address pool on a loadbalancer.</span></span> 

## <span data-ttu-id="3d7a8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3d7a8-104">SYNTAX</span></span>

### <span data-ttu-id="3d7a8-105">CreateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d7a8-105">CreateByNameParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d7a8-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d7a8-106">CreateByParentObjectParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -LoadBalancer <PSLoadBalancer> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d7a8-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d7a8-107">DESCRIPTION</span></span>
<span data-ttu-id="3d7a8-108">Создает пул адресов для резервирования загрузки.</span><span class="sxs-lookup"><span data-stu-id="3d7a8-108">Creates a backend address pool on a loadbalancer.</span></span> <span data-ttu-id="3d7a8-109">Разрешает выбор массива PSLoadBalancerBackendAddress.</span><span class="sxs-lookup"><span data-stu-id="3d7a8-109">Allows for specifiying a array of PSLoadBalancerBackendAddress.</span></span> 
## <span data-ttu-id="3d7a8-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3d7a8-110">EXAMPLES</span></span>

### <span data-ttu-id="3d7a8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3d7a8-111">Example 1</span></span>
```powershell
## create by passing loadbalancer without Ips
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ips = @($ip1, $ip2)

PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="3d7a8-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3d7a8-112">Example 2</span></span>
```powershell
## create by passing loadbalancer with ips
PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool7 -LoadBalancerBackendAddress $ips
```

### <span data-ttu-id="3d7a8-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3d7a8-113">Example 3</span></span>
```powershell
## create by name without ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3
```

### <span data-ttu-id="3d7a8-114">Пример 4</span><span class="sxs-lookup"><span data-stu-id="3d7a8-114">Example 4</span></span>
```powershell
## create by name with ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3 -LoadBalancerBackendAddress $ips
```

## <span data-ttu-id="3d7a8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d7a8-115">PARAMETERS</span></span>

### <span data-ttu-id="3d7a8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d7a8-116">-DefaultProfile</span></span>
<span data-ttu-id="3d7a8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3d7a8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d7a8-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3d7a8-118">-LoadBalancer</span></span>
<span data-ttu-id="3d7a8-119">Ресурс балансировы нагрузки.</span><span class="sxs-lookup"><span data-stu-id="3d7a8-119">The load balancer resource.</span></span>

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

### <span data-ttu-id="3d7a8-120">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="3d7a8-120">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="3d7a8-121">Backend addresses (Адреса для backend- и backend-адресов).</span><span class="sxs-lookup"><span data-stu-id="3d7a8-121">The backend addresses.</span></span>

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

### <span data-ttu-id="3d7a8-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="3d7a8-122">-LoadBalancerName</span></span>
<span data-ttu-id="3d7a8-123">Имя балансира нагрузки.</span><span class="sxs-lookup"><span data-stu-id="3d7a8-123">The name of the load balancer.</span></span>

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

### <span data-ttu-id="3d7a8-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3d7a8-124">-Name</span></span>
<span data-ttu-id="3d7a8-125">Имя пула backend.</span><span class="sxs-lookup"><span data-stu-id="3d7a8-125">The name of the backend pool.</span></span>

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

### <span data-ttu-id="3d7a8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d7a8-126">-ResourceGroupName</span></span>
<span data-ttu-id="3d7a8-127">Имя группы ресурсов балансира нагрузки.</span><span class="sxs-lookup"><span data-stu-id="3d7a8-127">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="3d7a8-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d7a8-128">-Confirm</span></span>
<span data-ttu-id="3d7a8-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d7a8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d7a8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d7a8-130">-WhatIf</span></span>
<span data-ttu-id="3d7a8-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d7a8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d7a8-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3d7a8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d7a8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d7a8-133">CommonParameters</span></span>
<span data-ttu-id="3d7a8-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d7a8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d7a8-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d7a8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d7a8-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3d7a8-136">INPUTS</span></span>

### <span data-ttu-id="3d7a8-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3d7a8-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3d7a8-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3d7a8-138">OUTPUTS</span></span>

### <span data-ttu-id="3d7a8-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3d7a8-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="3d7a8-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3d7a8-140">NOTES</span></span>

## <span data-ttu-id="3d7a8-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d7a8-141">RELATED LINKS</span></span>
