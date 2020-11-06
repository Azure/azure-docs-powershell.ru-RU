---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/move-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: f565adcf308e9615374753a28992f572feda61ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562900"
---
# <span data-ttu-id="3a0f7-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3a0f7-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="3a0f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3a0f7-102">SYNOPSIS</span></span>
<span data-ttu-id="3a0f7-103">Перемещает цепь ExpressRoute из классической модели развертывания в модель развертывания диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3a0f7-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a0f7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3a0f7-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a0f7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a0f7-105">DESCRIPTION</span></span>
<span data-ttu-id="3a0f7-106">Командлет **Move-AzureRmExpressRouteCircuit** перемещает канал ExpressRoute из классической модели развертывания в модель развертывания диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3a0f7-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="3a0f7-107">После перемещения канал ExpressRoute работает так же, как и любой другой канал ExpressRoute, созданный в модели развертывания диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3a0f7-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="3a0f7-108">Ссылки на каналы, виртуальные сети и шлюзы VPN не перемещаются по этой операции.</span><span class="sxs-lookup"><span data-stu-id="3a0f7-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="3a0f7-109">Эти ресурсы необходимо перенастроить после перемещения.</span><span class="sxs-lookup"><span data-stu-id="3a0f7-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="3a0f7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3a0f7-110">EXAMPLES</span></span>

### <span data-ttu-id="3a0f7-111">Пример 1: Перемещение канала ExpressRoute в модель развертывания диспетчера ресурсов</span><span class="sxs-lookup"><span data-stu-id="3a0f7-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="3a0f7-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3a0f7-112">PARAMETERS</span></span>

### <span data-ttu-id="3a0f7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a0f7-113">-AsJob</span></span>
<span data-ttu-id="3a0f7-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3a0f7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a0f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a0f7-115">-DefaultProfile</span></span>
<span data-ttu-id="3a0f7-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3a0f7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a0f7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3a0f7-117">-Force</span></span>
<span data-ttu-id="3a0f7-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="3a0f7-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3a0f7-119">-Location</span><span class="sxs-lookup"><span data-stu-id="3a0f7-119">-Location</span></span>
<span data-ttu-id="3a0f7-120">Имя расположения Azure, в котором находится цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3a0f7-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="3a0f7-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3a0f7-121">-Name</span></span>
<span data-ttu-id="3a0f7-122">Имя канала ExpressRoute для перемещения.</span><span class="sxs-lookup"><span data-stu-id="3a0f7-122">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="3a0f7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a0f7-123">-ResourceGroupName</span></span>
<span data-ttu-id="3a0f7-124">Имя группы ресурсов, в которой будет содержаться перемещаемая цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3a0f7-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="3a0f7-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="3a0f7-125">-ServiceKey</span></span>
<span data-ttu-id="3a0f7-126">Ключ службы, используемый цепью ExpressRoute в классической модели развертывания.</span><span class="sxs-lookup"><span data-stu-id="3a0f7-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="3a0f7-127">-Тег</span><span class="sxs-lookup"><span data-stu-id="3a0f7-127">-Tag</span></span>
<span data-ttu-id="3a0f7-128">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="3a0f7-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3a0f7-129">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="3a0f7-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3a0f7-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a0f7-130">-Confirm</span></span>
<span data-ttu-id="3a0f7-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3a0f7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a0f7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a0f7-132">-WhatIf</span></span>
<span data-ttu-id="3a0f7-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3a0f7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a0f7-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3a0f7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a0f7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a0f7-135">CommonParameters</span></span>
<span data-ttu-id="3a0f7-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3a0f7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a0f7-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a0f7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a0f7-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3a0f7-138">INPUTS</span></span>

### <span data-ttu-id="3a0f7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3a0f7-139">System.String</span></span>

### <span data-ttu-id="3a0f7-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3a0f7-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3a0f7-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a0f7-141">OUTPUTS</span></span>

### <span data-ttu-id="3a0f7-142">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3a0f7-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="3a0f7-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="3a0f7-143">NOTES</span></span>

## <span data-ttu-id="3a0f7-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a0f7-144">RELATED LINKS</span></span>

[<span data-ttu-id="3a0f7-145">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3a0f7-145">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="3a0f7-146">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3a0f7-146">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="3a0f7-147">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3a0f7-147">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="3a0f7-148">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3a0f7-148">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
