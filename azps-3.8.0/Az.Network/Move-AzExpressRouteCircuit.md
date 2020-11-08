---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/move-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
ms.openlocfilehash: 2c5219e4a829ac9786b69a41afaa7362783f26b0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074853"
---
# <span data-ttu-id="bca4e-101">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bca4e-101">Move-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="bca4e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bca4e-102">SYNOPSIS</span></span>
<span data-ttu-id="bca4e-103">Перемещает цепь ExpressRoute из классической модели развертывания в модель развертывания диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bca4e-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

## <span data-ttu-id="bca4e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bca4e-104">SYNTAX</span></span>

```
Move-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> -ServiceKey <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bca4e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bca4e-105">DESCRIPTION</span></span>
<span data-ttu-id="bca4e-106">Командлет **Move-AzExpressRouteCircuit** перемещает канал ExpressRoute из классической модели развертывания в модель развертывания диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bca4e-106">The **Move-AzExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="bca4e-107">После перемещения канал ExpressRoute работает так же, как и любой другой канал ExpressRoute, созданный в модели развертывания диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bca4e-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="bca4e-108">Ссылки на каналы, виртуальные сети и шлюзы VPN не перемещаются по этой операции.</span><span class="sxs-lookup"><span data-stu-id="bca4e-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="bca4e-109">Эти ресурсы необходимо перенастроить после перемещения.</span><span class="sxs-lookup"><span data-stu-id="bca4e-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="bca4e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bca4e-110">EXAMPLES</span></span>

### <span data-ttu-id="bca4e-111">Пример 1: Перемещение канала ExpressRoute в модель развертывания диспетчера ресурсов</span><span class="sxs-lookup"><span data-stu-id="bca4e-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="bca4e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bca4e-112">PARAMETERS</span></span>

### <span data-ttu-id="bca4e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bca4e-113">-AsJob</span></span>
<span data-ttu-id="bca4e-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bca4e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bca4e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bca4e-115">-DefaultProfile</span></span>
<span data-ttu-id="bca4e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bca4e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bca4e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="bca4e-117">-Force</span></span>
<span data-ttu-id="bca4e-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="bca4e-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bca4e-119">-Location</span><span class="sxs-lookup"><span data-stu-id="bca4e-119">-Location</span></span>
<span data-ttu-id="bca4e-120">Имя расположения Azure, в котором находится цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bca4e-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="bca4e-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bca4e-121">-Name</span></span>
<span data-ttu-id="bca4e-122">Имя канала ExpressRoute для перемещения.</span><span class="sxs-lookup"><span data-stu-id="bca4e-122">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="bca4e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bca4e-123">-ResourceGroupName</span></span>
<span data-ttu-id="bca4e-124">Имя группы ресурсов, в которой будет содержаться перемещаемая цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bca4e-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="bca4e-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="bca4e-125">-ServiceKey</span></span>
<span data-ttu-id="bca4e-126">Ключ службы, используемый цепью ExpressRoute в классической модели развертывания.</span><span class="sxs-lookup"><span data-stu-id="bca4e-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="bca4e-127">-Тег</span><span class="sxs-lookup"><span data-stu-id="bca4e-127">-Tag</span></span>
<span data-ttu-id="bca4e-128">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="bca4e-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bca4e-129">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="bca4e-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="bca4e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bca4e-130">-Confirm</span></span>
<span data-ttu-id="bca4e-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bca4e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bca4e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bca4e-132">-WhatIf</span></span>
<span data-ttu-id="bca4e-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bca4e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bca4e-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bca4e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bca4e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bca4e-135">CommonParameters</span></span>
<span data-ttu-id="bca4e-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bca4e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bca4e-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bca4e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bca4e-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bca4e-138">INPUTS</span></span>

### <span data-ttu-id="bca4e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bca4e-139">System.String</span></span>

### <span data-ttu-id="bca4e-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bca4e-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bca4e-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bca4e-141">OUTPUTS</span></span>

### <span data-ttu-id="bca4e-142">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bca4e-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="bca4e-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="bca4e-143">NOTES</span></span>

## <span data-ttu-id="bca4e-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bca4e-144">RELATED LINKS</span></span>

[<span data-ttu-id="bca4e-145">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bca4e-145">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="bca4e-146">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bca4e-146">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="bca4e-147">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bca4e-147">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="bca4e-148">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bca4e-148">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
