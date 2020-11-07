---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: cf15d39a8c1ec320b45e488ccaac7903c82e30f0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913633"
---
# <span data-ttu-id="484f5-101">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="484f5-101">Get-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="484f5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="484f5-102">SYNOPSIS</span></span>
<span data-ttu-id="484f5-103">Возвращает цепь Azure ExpressRoute из Azure.</span><span class="sxs-lookup"><span data-stu-id="484f5-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="484f5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="484f5-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="484f5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="484f5-105">DESCRIPTION</span></span>
<span data-ttu-id="484f5-106">Командлет **Get-AzureRmExpressRouteCircuit** используется для получения объекта цепи ExpressRoute из подписки.</span><span class="sxs-lookup"><span data-stu-id="484f5-106">The **Get-AzureRmExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="484f5-107">Возвращаемый объект цепью можно использовать в качестве входных данных для других командлетов, которые работают с каналами ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="484f5-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="484f5-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="484f5-108">EXAMPLES</span></span>

### <span data-ttu-id="484f5-109">Пример 1: получение канала ExpressRoute для удаления</span><span class="sxs-lookup"><span data-stu-id="484f5-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="484f5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="484f5-110">PARAMETERS</span></span>

### <span data-ttu-id="484f5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="484f5-111">-DefaultProfile</span></span>
<span data-ttu-id="484f5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="484f5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="484f5-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="484f5-113">-Name</span></span>
<span data-ttu-id="484f5-114">Имя канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="484f5-114">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="484f5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="484f5-115">-ResourceGroupName</span></span>
<span data-ttu-id="484f5-116">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="484f5-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="484f5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="484f5-117">CommonParameters</span></span>
<span data-ttu-id="484f5-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="484f5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="484f5-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="484f5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="484f5-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="484f5-120">INPUTS</span></span>

## <span data-ttu-id="484f5-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="484f5-121">OUTPUTS</span></span>

### <span data-ttu-id="484f5-122">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="484f5-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="484f5-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="484f5-123">NOTES</span></span>

## <span data-ttu-id="484f5-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="484f5-124">RELATED LINKS</span></span>

[<span data-ttu-id="484f5-125">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="484f5-125">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="484f5-126">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="484f5-126">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="484f5-127">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="484f5-127">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="484f5-128">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="484f5-128">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
