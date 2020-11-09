---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 034e33b1c465f106c1edfa8647fe34233575b801
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247594"
---
# <span data-ttu-id="148a2-101">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="148a2-101">Set-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="148a2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="148a2-102">SYNOPSIS</span></span>
<span data-ttu-id="148a2-103">Обновляет пул серверной базы данных в подсистеме балансировки</span><span class="sxs-lookup"><span data-stu-id="148a2-103">Updates the backend pool on a loadbalancer</span></span>

## <span data-ttu-id="148a2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="148a2-104">SYNTAX</span></span>

### <span data-ttu-id="148a2-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="148a2-105">SetByNameParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="148a2-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="148a2-106">SetByParentObjectParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -Name <String> -LoadBalancer <PSLoadBalancer>
 -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="148a2-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="148a2-107">SetByInputObjectParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -InputObject <PSBackendAddressPool> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="148a2-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="148a2-108">SetByResourceIdParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>
 -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="148a2-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="148a2-109">DESCRIPTION</span></span>
<span data-ttu-id="148a2-110">Обновляет пул серверной базы данных в подсистеме балансировки</span><span class="sxs-lookup"><span data-stu-id="148a2-110">Updates the backend pool on a loadbalancer</span></span>

## <span data-ttu-id="148a2-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="148a2-111">EXAMPLES</span></span>

### <span data-ttu-id="148a2-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="148a2-112">Example 1</span></span>
```powershell
###Set by name and modified input object
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip3 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.7" -Name "TestVNetRef3" -VirtualNetworkId $virtualNetwork.id
PS C:\> $ips = @($ip1, $ip2)
PS C:\> $b2 = Get-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool1
PS C:\> $b2.LoadBalancerBackendAddresses.Add($ip3)

PS C:\> Set-AzLoadBalancerBackendAddressPool -InputObject $b2
```
### <span data-ttu-id="148a2-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="148a2-113">Example 2</span></span>
```powershell
###Set by specific backend from piped loadbalancer and set two IP's
PS C:\> $lb | Set-AzLoadBalancerBackendAddressPool -LoadBalancerBackendAddress $ips -Name $backendPool1
```

### <span data-ttu-id="148a2-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="148a2-114">Example 3</span></span>
```powershell
### #set by ResourceId
PS C:\> Set-AzLoadBalancerBackendAddressPool -ResourceId b2.Id -LoadBalancerBackendAddress $b2.LoadBalancerBackendAddresses
```

## <span data-ttu-id="148a2-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="148a2-115">PARAMETERS</span></span>

### <span data-ttu-id="148a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="148a2-116">-DefaultProfile</span></span>
<span data-ttu-id="148a2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="148a2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="148a2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="148a2-118">-Force</span></span>
<span data-ttu-id="148a2-119">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="148a2-119">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="148a2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="148a2-120">-InputObject</span></span>
<span data-ttu-id="148a2-121">Устанавливаемый пул адресов серверной базы данных</span><span class="sxs-lookup"><span data-stu-id="148a2-121">The backend address pool to set</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="148a2-122">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="148a2-122">-LoadBalancer</span></span>
<span data-ttu-id="148a2-123">Ресурс подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="148a2-123">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="148a2-124">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="148a2-124">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="148a2-125">Внутренние адреса.</span><span class="sxs-lookup"><span data-stu-id="148a2-125">The backend addresses.</span></span>

```yaml
Type: PSLoadBalancerBackendAddress[]
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="148a2-126">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="148a2-126">-LoadBalancerName</span></span>
<span data-ttu-id="148a2-127">Имя подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="148a2-127">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="148a2-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="148a2-128">-Name</span></span>
<span data-ttu-id="148a2-129">Имя пула баз данных.</span><span class="sxs-lookup"><span data-stu-id="148a2-129">The name of the backend pool.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="148a2-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="148a2-130">-PassThru</span></span>
<span data-ttu-id="148a2-131">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="148a2-131">{{ Fill PassThru Description }}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="148a2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="148a2-132">-ResourceGroupName</span></span>
<span data-ttu-id="148a2-133">Имя группы ресурсов для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="148a2-133">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="148a2-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="148a2-134">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="148a2-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="148a2-135">-Confirm</span></span>
<span data-ttu-id="148a2-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="148a2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="148a2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="148a2-137">-WhatIf</span></span>
<span data-ttu-id="148a2-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="148a2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="148a2-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="148a2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="148a2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="148a2-140">CommonParameters</span></span>
<span data-ttu-id="148a2-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="148a2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="148a2-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="148a2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="148a2-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="148a2-143">INPUTS</span></span>

### <span data-ttu-id="148a2-144">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="148a2-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="148a2-145">System. String</span><span class="sxs-lookup"><span data-stu-id="148a2-145">System.String</span></span>

## <span data-ttu-id="148a2-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="148a2-146">OUTPUTS</span></span>

### <span data-ttu-id="148a2-147">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="148a2-147">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="148a2-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="148a2-148">NOTES</span></span>

## <span data-ttu-id="148a2-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="148a2-149">RELATED LINKS</span></span>