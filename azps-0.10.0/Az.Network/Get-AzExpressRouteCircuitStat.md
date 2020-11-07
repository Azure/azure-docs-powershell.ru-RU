---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-AzExpressRouteCircuitStat
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
ms.openlocfilehash: 48136f033a75cfb49d05f5af76b1688ac6f68463
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909993"
---
# <span data-ttu-id="f00a3-101">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="f00a3-101">Get-AzExpressRouteCircuitStat</span></span>

## <span data-ttu-id="f00a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f00a3-102">SYNOPSIS</span></span>
<span data-ttu-id="f00a3-103">Возвращает статистику использования канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f00a3-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="f00a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f00a3-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitStat -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f00a3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f00a3-105">DESCRIPTION</span></span>
<span data-ttu-id="f00a3-106">Командлет **Get-AzExpressRouteCircuitStat** извлекает статистику трафика для канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f00a3-106">The **Get-AzExpressRouteCircuitStat** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="f00a3-107">Статистика включает количество байтов, отправленных и полученных по основным и дополнительным маршрутам.</span><span class="sxs-lookup"><span data-stu-id="f00a3-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="f00a3-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f00a3-108">EXAMPLES</span></span>

### <span data-ttu-id="f00a3-109">Пример 1: отображение статистики трафика для однорангового узла ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="f00a3-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitStat -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="f00a3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f00a3-110">PARAMETERS</span></span>

### <span data-ttu-id="f00a3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f00a3-111">-DefaultProfile</span></span>
<span data-ttu-id="f00a3-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f00a3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f00a3-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="f00a3-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="f00a3-114">Имя проверяемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f00a3-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="f00a3-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="f00a3-115">-PeeringType</span></span>
<span data-ttu-id="f00a3-116">Допустимые значения этого параметра: `AzurePrivatePeering` , `AzurePublicPeering` и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="f00a3-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="f00a3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f00a3-117">-ResourceGroupName</span></span>
<span data-ttu-id="f00a3-118">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f00a3-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="f00a3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f00a3-119">CommonParameters</span></span>
<span data-ttu-id="f00a3-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f00a3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f00a3-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f00a3-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f00a3-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f00a3-122">INPUTS</span></span>

## <span data-ttu-id="f00a3-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f00a3-123">OUTPUTS</span></span>

### <span data-ttu-id="f00a3-124">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="f00a3-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="f00a3-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="f00a3-125">NOTES</span></span>

## <span data-ttu-id="f00a3-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f00a3-126">RELATED LINKS</span></span>

[<span data-ttu-id="f00a3-127">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f00a3-127">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="f00a3-128">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f00a3-128">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="f00a3-129">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f00a3-129">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)
