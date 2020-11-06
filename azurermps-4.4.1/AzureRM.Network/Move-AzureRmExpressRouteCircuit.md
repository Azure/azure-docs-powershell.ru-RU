---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: e4d167f98f837434018e04da91a31973acb45c8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566684"
---
# <span data-ttu-id="afca9-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="afca9-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="afca9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="afca9-102">SYNOPSIS</span></span>
<span data-ttu-id="afca9-103">Перемещает цепь ExpressRoute из классической модели развертывания в модель развертывания диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="afca9-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afca9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="afca9-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afca9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="afca9-105">DESCRIPTION</span></span>
<span data-ttu-id="afca9-106">Командлет **Move-AzureRmExpressRouteCircuit** перемещает канал ExpressRoute из классической модели развертывания в модель развертывания диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="afca9-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="afca9-107">После перемещения канал ExpressRoute работает так же, как и любой другой канал ExpressRoute, созданный в модели развертывания диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="afca9-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="afca9-108">Ссылки на каналы, виртуальные сети и шлюзы VPN не перемещаются по этой операции.</span><span class="sxs-lookup"><span data-stu-id="afca9-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="afca9-109">Эти ресурсы необходимо перенастроить после перемещения.</span><span class="sxs-lookup"><span data-stu-id="afca9-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="afca9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="afca9-110">EXAMPLES</span></span>

### <span data-ttu-id="afca9-111">Пример 1: Перемещение канала ExpressRoute в модель развертывания диспетчера ресурсов</span><span class="sxs-lookup"><span data-stu-id="afca9-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="afca9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="afca9-112">PARAMETERS</span></span>

### <span data-ttu-id="afca9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="afca9-113">-Force</span></span>
<span data-ttu-id="afca9-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="afca9-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="afca9-115">-Location</span><span class="sxs-lookup"><span data-stu-id="afca9-115">-Location</span></span>
<span data-ttu-id="afca9-116">Имя расположения Azure, в котором находится цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="afca9-116">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="afca9-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="afca9-117">-Name</span></span>
<span data-ttu-id="afca9-118">Имя канала ExpressRoute для перемещения.</span><span class="sxs-lookup"><span data-stu-id="afca9-118">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="afca9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afca9-119">-ResourceGroupName</span></span>
<span data-ttu-id="afca9-120">Имя группы ресурсов, в которой будет содержаться перемещаемая цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="afca9-120">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="afca9-121">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="afca9-121">-ServiceKey</span></span>
<span data-ttu-id="afca9-122">Ключ службы, используемый цепью ExpressRoute в классической модели развертывания.</span><span class="sxs-lookup"><span data-stu-id="afca9-122">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="afca9-123">-Тег</span><span class="sxs-lookup"><span data-stu-id="afca9-123">-Tag</span></span>
<span data-ttu-id="afca9-124">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="afca9-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="afca9-125">Например:</span><span class="sxs-lookup"><span data-stu-id="afca9-125">For example:</span></span>

<span data-ttu-id="afca9-126">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="afca9-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="afca9-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afca9-127">-Confirm</span></span>
<span data-ttu-id="afca9-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="afca9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afca9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afca9-129">-WhatIf</span></span>
<span data-ttu-id="afca9-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="afca9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afca9-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="afca9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afca9-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afca9-132">-DefaultProfile</span></span>
<span data-ttu-id="afca9-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="afca9-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afca9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afca9-134">CommonParameters</span></span>
<span data-ttu-id="afca9-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="afca9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afca9-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afca9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afca9-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="afca9-137">INPUTS</span></span>

## <span data-ttu-id="afca9-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="afca9-138">OUTPUTS</span></span>

### <span data-ttu-id="afca9-139">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="afca9-139">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="afca9-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="afca9-140">NOTES</span></span>

## <span data-ttu-id="afca9-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="afca9-141">RELATED LINKS</span></span>

[<span data-ttu-id="afca9-142">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="afca9-142">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="afca9-143">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="afca9-143">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="afca9-144">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="afca9-144">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="afca9-145">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="afca9-145">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
