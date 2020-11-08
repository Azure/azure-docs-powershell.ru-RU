---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitstat
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
ms.openlocfilehash: 15b02ce4693e452bda370c9fb1ae9c69012e9574
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248346"
---
# <span data-ttu-id="a2fd9-101">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="a2fd9-101">Get-AzExpressRouteCircuitStat</span></span>

## <span data-ttu-id="a2fd9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2fd9-102">SYNOPSIS</span></span>
<span data-ttu-id="a2fd9-103">Возвращает статистику использования канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a2fd9-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="a2fd9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2fd9-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitStat -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2fd9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2fd9-105">DESCRIPTION</span></span>
<span data-ttu-id="a2fd9-106">Командлет **Get-AzExpressRouteCircuitStat** извлекает статистику трафика для канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a2fd9-106">The **Get-AzExpressRouteCircuitStat** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="a2fd9-107">Статистика включает количество байтов, отправленных и полученных по основным и дополнительным маршрутам.</span><span class="sxs-lookup"><span data-stu-id="a2fd9-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="a2fd9-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2fd9-108">EXAMPLES</span></span>

### <span data-ttu-id="a2fd9-109">Пример 1: отображение статистики трафика для однорангового узла ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="a2fd9-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitStat -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="a2fd9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2fd9-110">PARAMETERS</span></span>

### <span data-ttu-id="a2fd9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2fd9-111">-DefaultProfile</span></span>
<span data-ttu-id="a2fd9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2fd9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2fd9-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="a2fd9-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="a2fd9-114">Имя проверяемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a2fd9-114">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2fd9-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="a2fd9-115">-PeeringType</span></span>
<span data-ttu-id="a2fd9-116">Допустимые значения этого параметра: `AzurePrivatePeering` , `AzurePublicPeering` и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="a2fd9-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2fd9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2fd9-117">-ResourceGroupName</span></span>
<span data-ttu-id="a2fd9-118">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a2fd9-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="a2fd9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2fd9-119">CommonParameters</span></span>
<span data-ttu-id="a2fd9-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2fd9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2fd9-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2fd9-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2fd9-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2fd9-122">INPUTS</span></span>

### <span data-ttu-id="a2fd9-123">System. String</span><span class="sxs-lookup"><span data-stu-id="a2fd9-123">System.String</span></span>

## <span data-ttu-id="a2fd9-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2fd9-124">OUTPUTS</span></span>

### <span data-ttu-id="a2fd9-125">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="a2fd9-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="a2fd9-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2fd9-126">NOTES</span></span>

## <span data-ttu-id="a2fd9-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2fd9-127">RELATED LINKS</span></span>

[<span data-ttu-id="a2fd9-128">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a2fd9-128">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="a2fd9-129">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a2fd9-129">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="a2fd9-130">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a2fd9-130">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)
