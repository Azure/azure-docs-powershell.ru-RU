---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitstats
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
ms.openlocfilehash: 4577eb4f105bca235e7b5e9feb0b0ef308298881
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732259"
---
# <span data-ttu-id="a9a5f-101">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="a9a5f-101">Get-AzureRmExpressRouteCircuitStats</span></span>

## <span data-ttu-id="a9a5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a9a5f-102">SYNOPSIS</span></span>
<span data-ttu-id="a9a5f-103">Возвращает статистику использования канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a9a5f-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9a5f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a9a5f-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9a5f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9a5f-105">DESCRIPTION</span></span>
<span data-ttu-id="a9a5f-106">Командлет **Get-AzureRmExpressRouteCircuitStats** извлекает статистику трафика для канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a9a5f-106">The **Get-AzureRmExpressRouteCircuitStats** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="a9a5f-107">Статистика включает количество байтов, отправленных и полученных по основным и дополнительным маршрутам.</span><span class="sxs-lookup"><span data-stu-id="a9a5f-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="a9a5f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a9a5f-108">EXAMPLES</span></span>

### <span data-ttu-id="a9a5f-109">Пример 1: отображение статистики трафика для однорангового узла ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="a9a5f-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="a9a5f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a9a5f-110">PARAMETERS</span></span>

### <span data-ttu-id="a9a5f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9a5f-111">-DefaultProfile</span></span>
<span data-ttu-id="a9a5f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a9a5f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9a5f-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="a9a5f-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="a9a5f-114">Имя проверяемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a9a5f-114">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9a5f-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="a9a5f-115">-PeeringType</span></span>
<span data-ttu-id="a9a5f-116">Допустимые значения этого параметра: `AzurePrivatePeering` , `AzurePublicPeering` и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="a9a5f-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a5f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9a5f-117">-ResourceGroupName</span></span>
<span data-ttu-id="a9a5f-118">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a9a5f-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="a9a5f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9a5f-119">CommonParameters</span></span>
<span data-ttu-id="a9a5f-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a9a5f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9a5f-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9a5f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9a5f-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a9a5f-122">INPUTS</span></span>

### <span data-ttu-id="a9a5f-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="a9a5f-123">None</span></span>
<span data-ttu-id="a9a5f-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a9a5f-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a9a5f-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9a5f-125">OUTPUTS</span></span>

### <span data-ttu-id="a9a5f-126">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="a9a5f-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="a9a5f-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="a9a5f-127">NOTES</span></span>

## <span data-ttu-id="a9a5f-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9a5f-128">RELATED LINKS</span></span>

[<span data-ttu-id="a9a5f-129">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a9a5f-129">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="a9a5f-130">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a9a5f-130">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="a9a5f-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a9a5f-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)
