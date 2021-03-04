---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/powershell/module/az.network/move-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
ms.openlocfilehash: 6964767438fac6a1afd8da4333560f49cfe1bb44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952200"
---
# <span data-ttu-id="b071e-101">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b071e-101">Move-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="b071e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b071e-102">SYNOPSIS</span></span>
<span data-ttu-id="b071e-103">Перемещение схемы ExpressRoute из классической модели развертывания в модель развертывания Диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b071e-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

## <span data-ttu-id="b071e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b071e-104">SYNTAX</span></span>

```
Move-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> -ServiceKey <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b071e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b071e-105">DESCRIPTION</span></span>
<span data-ttu-id="b071e-106">Для **перемещения-AzExpressRouteCircuit** канал ExpressRoute из классической модели развертывания в модель развертывания Диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b071e-106">The **Move-AzExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="b071e-107">После перемещения канал ExpressRoute работает и работает так же, как любой другой канал ExpressRoute, созданный в модели развертывания Диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b071e-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="b071e-108">В ходе этой операции не перемещаются сетевые, виртуальные сети и VPN-шлюзы.</span><span class="sxs-lookup"><span data-stu-id="b071e-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="b071e-109">После перемещения эти ресурсы необходимо перенастроить.</span><span class="sxs-lookup"><span data-stu-id="b071e-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="b071e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b071e-110">EXAMPLES</span></span>

### <span data-ttu-id="b071e-111">Пример 1. Перемещение схемы ExpressRoute в модель развертывания Диспетчера ресурсов</span><span class="sxs-lookup"><span data-stu-id="b071e-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="b071e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b071e-112">PARAMETERS</span></span>

### <span data-ttu-id="b071e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b071e-113">-AsJob</span></span>
<span data-ttu-id="b071e-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b071e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b071e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b071e-115">-DefaultProfile</span></span>
<span data-ttu-id="b071e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b071e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b071e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b071e-117">-Force</span></span>
<span data-ttu-id="b071e-118">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="b071e-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b071e-119">-Location</span><span class="sxs-lookup"><span data-stu-id="b071e-119">-Location</span></span>
<span data-ttu-id="b071e-120">Имя расположения Azure, в котором находится канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b071e-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b071e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b071e-121">-Name</span></span>
<span data-ttu-id="b071e-122">Имя перемещаемого контура ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b071e-122">The name of the ExpressRoute circuit to be moved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b071e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b071e-123">-ResourceGroupName</span></span>
<span data-ttu-id="b071e-124">Имя группы ресурсов, которая будет содержать канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b071e-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b071e-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="b071e-125">-ServiceKey</span></span>
<span data-ttu-id="b071e-126">Ключ службы, используемый каналом ExpressRoute в классической модели развертывания.</span><span class="sxs-lookup"><span data-stu-id="b071e-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b071e-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="b071e-127">-Tag</span></span>
<span data-ttu-id="b071e-128">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="b071e-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b071e-129">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="b071e-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b071e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b071e-130">-Confirm</span></span>
<span data-ttu-id="b071e-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b071e-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b071e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b071e-132">-WhatIf</span></span>
<span data-ttu-id="b071e-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b071e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b071e-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b071e-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b071e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b071e-135">CommonParameters</span></span>
<span data-ttu-id="b071e-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b071e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b071e-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b071e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b071e-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b071e-138">INPUTS</span></span>

### <span data-ttu-id="b071e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b071e-139">System.String</span></span>

### <span data-ttu-id="b071e-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b071e-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b071e-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b071e-141">OUTPUTS</span></span>

### <span data-ttu-id="b071e-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b071e-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b071e-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b071e-143">NOTES</span></span>

## <span data-ttu-id="b071e-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b071e-144">RELATED LINKS</span></span>

[<span data-ttu-id="b071e-145">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b071e-145">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="b071e-146">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b071e-146">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="b071e-147">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b071e-147">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="b071e-148">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b071e-148">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
