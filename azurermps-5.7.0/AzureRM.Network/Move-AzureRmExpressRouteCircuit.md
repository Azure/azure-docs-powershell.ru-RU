---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/move-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: d0fb9fb0c6fb27ff683fcbb2b3ae537d736189cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564763"
---
# <span data-ttu-id="0f959-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0f959-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="0f959-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f959-102">SYNOPSIS</span></span>
<span data-ttu-id="0f959-103">Перемещает цепь ExpressRoute из классической модели развертывания в модель развертывания диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f959-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f959-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f959-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f959-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f959-105">DESCRIPTION</span></span>
<span data-ttu-id="0f959-106">Командлет **Move-AzureRmExpressRouteCircuit** перемещает канал ExpressRoute из классической модели развертывания в модель развертывания диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f959-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="0f959-107">После перемещения канал ExpressRoute работает так же, как и любой другой канал ExpressRoute, созданный в модели развертывания диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f959-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="0f959-108">Ссылки на каналы, виртуальные сети и шлюзы VPN не перемещаются по этой операции.</span><span class="sxs-lookup"><span data-stu-id="0f959-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="0f959-109">Эти ресурсы необходимо перенастроить после перемещения.</span><span class="sxs-lookup"><span data-stu-id="0f959-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="0f959-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f959-110">EXAMPLES</span></span>

### <span data-ttu-id="0f959-111">Пример 1: Перемещение канала ExpressRoute в модель развертывания диспетчера ресурсов</span><span class="sxs-lookup"><span data-stu-id="0f959-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="0f959-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f959-112">PARAMETERS</span></span>

### <span data-ttu-id="0f959-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f959-113">-AsJob</span></span>
<span data-ttu-id="0f959-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0f959-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f959-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f959-115">-DefaultProfile</span></span>
<span data-ttu-id="0f959-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0f959-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f959-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0f959-117">-Force</span></span>
<span data-ttu-id="0f959-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="0f959-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0f959-119">-Location</span><span class="sxs-lookup"><span data-stu-id="0f959-119">-Location</span></span>
<span data-ttu-id="0f959-120">Имя расположения Azure, в котором находится цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0f959-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="0f959-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0f959-121">-Name</span></span>
<span data-ttu-id="0f959-122">Имя канала ExpressRoute для перемещения.</span><span class="sxs-lookup"><span data-stu-id="0f959-122">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="0f959-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f959-123">-ResourceGroupName</span></span>
<span data-ttu-id="0f959-124">Имя группы ресурсов, в которой будет содержаться перемещаемая цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0f959-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="0f959-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="0f959-125">-ServiceKey</span></span>
<span data-ttu-id="0f959-126">Ключ службы, используемый цепью ExpressRoute в классической модели развертывания.</span><span class="sxs-lookup"><span data-stu-id="0f959-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="0f959-127">-Тег</span><span class="sxs-lookup"><span data-stu-id="0f959-127">-Tag</span></span>
<span data-ttu-id="0f959-128">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="0f959-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0f959-129">Например:</span><span class="sxs-lookup"><span data-stu-id="0f959-129">For example:</span></span>

<span data-ttu-id="0f959-130">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="0f959-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0f959-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f959-131">-Confirm</span></span>
<span data-ttu-id="0f959-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0f959-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f959-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f959-133">-WhatIf</span></span>
<span data-ttu-id="0f959-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0f959-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f959-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0f959-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f959-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f959-136">CommonParameters</span></span>
<span data-ttu-id="0f959-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f959-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f959-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f959-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f959-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f959-139">INPUTS</span></span>

### <span data-ttu-id="0f959-140">Ничего</span><span class="sxs-lookup"><span data-stu-id="0f959-140">None</span></span>
<span data-ttu-id="0f959-141">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="0f959-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0f959-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f959-142">OUTPUTS</span></span>

### <span data-ttu-id="0f959-143">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0f959-143">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="0f959-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f959-144">NOTES</span></span>

## <span data-ttu-id="0f959-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f959-145">RELATED LINKS</span></span>

[<span data-ttu-id="0f959-146">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0f959-146">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="0f959-147">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0f959-147">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="0f959-148">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0f959-148">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="0f959-149">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0f959-149">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
