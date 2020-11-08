---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 691a45899480485f35164d4f18aea1595f70fbc9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246077"
---
# <span data-ttu-id="0195c-101">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0195c-101">Remove-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="0195c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0195c-102">SYNOPSIS</span></span>
<span data-ttu-id="0195c-103">Удаление пула баз данных из подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="0195c-103">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="0195c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0195c-104">SYNTAX</span></span>

### <span data-ttu-id="0195c-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0195c-105">DeleteByNameParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -Name <String> [-LoadBalancerName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0195c-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0195c-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -Name <String> [-LoadBalancerName <String>]
 -LoadBalancer <PSLoadBalancer> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0195c-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0195c-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] [-InputObject <PSBackendAddressPool>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0195c-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0195c-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0195c-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0195c-109">DESCRIPTION</span></span>
<span data-ttu-id="0195c-110">Удаление пула баз данных из подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="0195c-110">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="0195c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0195c-111">EXAMPLES</span></span>

### <span data-ttu-id="0195c-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0195c-112">Example 1</span></span>
```powershell
##removing by passing lb object via pipeline
PS C:\> $lb | Remove-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="0195c-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0195c-113">Example 2</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -InputObject $backendPoolObject
```

### <span data-ttu-id="0195c-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="0195c-114">Example 3</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -ResourceId $backendPoolObject.Id
```

## <span data-ttu-id="0195c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0195c-115">PARAMETERS</span></span>

### <span data-ttu-id="0195c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0195c-116">-DefaultProfile</span></span>
<span data-ttu-id="0195c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0195c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0195c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0195c-118">-InputObject</span></span>
<span data-ttu-id="0195c-119">Пул серверных адресов, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="0195c-119">The backend address pool to remove</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0195c-120">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="0195c-120">-LoadBalancer</span></span>
<span data-ttu-id="0195c-121">Ресурс подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0195c-121">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0195c-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="0195c-122">-LoadBalancerName</span></span>
<span data-ttu-id="0195c-123">Имя подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0195c-123">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0195c-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0195c-124">-Name</span></span>
<span data-ttu-id="0195c-125">Имя подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0195c-125">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0195c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0195c-126">-PassThru</span></span>
<span data-ttu-id="0195c-127">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="0195c-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="0195c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0195c-128">-ResourceGroupName</span></span>
<span data-ttu-id="0195c-129">Имя группы ресурсов для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0195c-129">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0195c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0195c-130">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0195c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0195c-131">-Confirm</span></span>
<span data-ttu-id="0195c-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0195c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0195c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0195c-133">-WhatIf</span></span>
<span data-ttu-id="0195c-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0195c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0195c-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0195c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0195c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0195c-136">CommonParameters</span></span>
<span data-ttu-id="0195c-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0195c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0195c-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0195c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0195c-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0195c-139">INPUTS</span></span>

### <span data-ttu-id="0195c-140">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0195c-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="0195c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0195c-141">System.String</span></span>

## <span data-ttu-id="0195c-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0195c-142">OUTPUTS</span></span>

### <span data-ttu-id="0195c-143">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0195c-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="0195c-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="0195c-144">NOTES</span></span>

## <span data-ttu-id="0195c-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0195c-145">RELATED LINKS</span></span>
