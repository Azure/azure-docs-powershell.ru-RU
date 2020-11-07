---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/move-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: bd4d51c03d26a1fb99b04c8b5245850512c2c940
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913809"
---
# <span data-ttu-id="aba3c-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="aba3c-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="aba3c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aba3c-102">SYNOPSIS</span></span>
<span data-ttu-id="aba3c-103">Перемещает цепь ExpressRoute из классической модели развертывания в модель развертывания диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aba3c-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aba3c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aba3c-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aba3c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aba3c-105">DESCRIPTION</span></span>
<span data-ttu-id="aba3c-106">Командлет **Move-AzureRmExpressRouteCircuit** перемещает канал ExpressRoute из классической модели развертывания в модель развертывания диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aba3c-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="aba3c-107">После перемещения канал ExpressRoute работает так же, как и любой другой канал ExpressRoute, созданный в модели развертывания диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aba3c-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="aba3c-108">Ссылки на каналы, виртуальные сети и шлюзы VPN не перемещаются по этой операции.</span><span class="sxs-lookup"><span data-stu-id="aba3c-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="aba3c-109">Эти ресурсы необходимо перенастроить после перемещения.</span><span class="sxs-lookup"><span data-stu-id="aba3c-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="aba3c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aba3c-110">EXAMPLES</span></span>

### <span data-ttu-id="aba3c-111">Пример 1: Перемещение канала ExpressRoute в модель развертывания диспетчера ресурсов</span><span class="sxs-lookup"><span data-stu-id="aba3c-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="aba3c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aba3c-112">PARAMETERS</span></span>

### <span data-ttu-id="aba3c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aba3c-113">-AsJob</span></span>
<span data-ttu-id="aba3c-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="aba3c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aba3c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aba3c-115">-DefaultProfile</span></span>
<span data-ttu-id="aba3c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aba3c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aba3c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="aba3c-117">-Force</span></span>
<span data-ttu-id="aba3c-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="aba3c-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aba3c-119">-Location</span><span class="sxs-lookup"><span data-stu-id="aba3c-119">-Location</span></span>
<span data-ttu-id="aba3c-120">Имя расположения Azure, в котором находится цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="aba3c-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aba3c-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aba3c-121">-Name</span></span>
<span data-ttu-id="aba3c-122">Имя канала ExpressRoute для перемещения.</span><span class="sxs-lookup"><span data-stu-id="aba3c-122">The name of the ExpressRoute circuit to be moved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aba3c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aba3c-123">-ResourceGroupName</span></span>
<span data-ttu-id="aba3c-124">Имя группы ресурсов, в которой будет содержаться перемещаемая цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="aba3c-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aba3c-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="aba3c-125">-ServiceKey</span></span>
<span data-ttu-id="aba3c-126">Ключ службы, используемый цепью ExpressRoute в классической модели развертывания.</span><span class="sxs-lookup"><span data-stu-id="aba3c-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aba3c-127">-Тег</span><span class="sxs-lookup"><span data-stu-id="aba3c-127">-Tag</span></span>
<span data-ttu-id="aba3c-128">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="aba3c-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="aba3c-129">Например:</span><span class="sxs-lookup"><span data-stu-id="aba3c-129">For example:</span></span>

<span data-ttu-id="aba3c-130">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="aba3c-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aba3c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aba3c-131">-Confirm</span></span>
<span data-ttu-id="aba3c-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aba3c-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aba3c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aba3c-133">-WhatIf</span></span>
<span data-ttu-id="aba3c-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aba3c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aba3c-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aba3c-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aba3c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aba3c-136">CommonParameters</span></span>
<span data-ttu-id="aba3c-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aba3c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aba3c-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aba3c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aba3c-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aba3c-139">INPUTS</span></span>

## <span data-ttu-id="aba3c-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aba3c-140">OUTPUTS</span></span>

### <span data-ttu-id="aba3c-141">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="aba3c-141">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="aba3c-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="aba3c-142">NOTES</span></span>

## <span data-ttu-id="aba3c-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aba3c-143">RELATED LINKS</span></span>

[<span data-ttu-id="aba3c-144">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="aba3c-144">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="aba3c-145">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="aba3c-145">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="aba3c-146">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="aba3c-146">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="aba3c-147">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="aba3c-147">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
