---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 691a45899480485f35164d4f18aea1595f70fbc9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506885"
---
# <span data-ttu-id="a2ab2-101">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a2ab2-101">Remove-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="a2ab2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2ab2-102">SYNOPSIS</span></span>
<span data-ttu-id="a2ab2-103">Удаление пула резервов из балансиров нагрузки</span><span class="sxs-lookup"><span data-stu-id="a2ab2-103">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="a2ab2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a2ab2-104">SYNTAX</span></span>

### <span data-ttu-id="a2ab2-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2ab2-105">DeleteByNameParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -Name <String> [-LoadBalancerName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2ab2-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2ab2-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -Name <String> [-LoadBalancerName <String>]
 -LoadBalancer <PSLoadBalancer> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2ab2-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2ab2-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] [-InputObject <PSBackendAddressPool>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2ab2-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2ab2-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2ab2-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2ab2-109">DESCRIPTION</span></span>
<span data-ttu-id="a2ab2-110">Удаление пула резервов из балансиров нагрузки</span><span class="sxs-lookup"><span data-stu-id="a2ab2-110">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="a2ab2-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a2ab2-111">EXAMPLES</span></span>

### <span data-ttu-id="a2ab2-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a2ab2-112">Example 1</span></span>
```powershell
##removing by passing lb object via pipeline
PS C:\> $lb | Remove-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="a2ab2-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a2ab2-113">Example 2</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -InputObject $backendPoolObject
```

### <span data-ttu-id="a2ab2-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a2ab2-114">Example 3</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -ResourceId $backendPoolObject.Id
```

## <span data-ttu-id="a2ab2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2ab2-115">PARAMETERS</span></span>

### <span data-ttu-id="a2ab2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2ab2-116">-DefaultProfile</span></span>
<span data-ttu-id="a2ab2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2ab2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2ab2-118">-InputObject</span></span>
<span data-ttu-id="a2ab2-119">Пул адресов для backend, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="a2ab2-119">The backend address pool to remove</span></span>

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

### <span data-ttu-id="a2ab2-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a2ab2-120">-LoadBalancer</span></span>
<span data-ttu-id="a2ab2-121">Ресурс балансировы нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-121">The load balancer resource.</span></span>

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

### <span data-ttu-id="a2ab2-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="a2ab2-122">-LoadBalancerName</span></span>
<span data-ttu-id="a2ab2-123">Имя балансира нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-123">The name of the load balancer.</span></span>

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

### <span data-ttu-id="a2ab2-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a2ab2-124">-Name</span></span>
<span data-ttu-id="a2ab2-125">Имя балансира нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-125">The name of the load balancer.</span></span>

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

### <span data-ttu-id="a2ab2-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2ab2-126">-PassThru</span></span>
<span data-ttu-id="a2ab2-127">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="a2ab2-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="a2ab2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2ab2-128">-ResourceGroupName</span></span>
<span data-ttu-id="a2ab2-129">Имя группы ресурсов балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-129">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="a2ab2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2ab2-130">-ResourceId</span></span>

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

### <span data-ttu-id="a2ab2-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2ab2-131">-Confirm</span></span>
<span data-ttu-id="a2ab2-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2ab2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2ab2-133">-WhatIf</span></span>
<span data-ttu-id="a2ab2-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2ab2-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2ab2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2ab2-136">CommonParameters</span></span>
<span data-ttu-id="a2ab2-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2ab2-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2ab2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2ab2-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2ab2-139">INPUTS</span></span>

### <span data-ttu-id="a2ab2-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a2ab2-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="a2ab2-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a2ab2-141">System.String</span></span>

## <span data-ttu-id="a2ab2-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a2ab2-142">OUTPUTS</span></span>

### <span data-ttu-id="a2ab2-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a2ab2-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="a2ab2-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a2ab2-144">NOTES</span></span>

## <span data-ttu-id="a2ab2-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2ab2-145">RELATED LINKS</span></span>