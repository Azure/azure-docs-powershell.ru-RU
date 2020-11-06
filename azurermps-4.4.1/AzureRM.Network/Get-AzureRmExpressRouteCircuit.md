---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 90814e90b4d4951a9e899fd8cf50f365b646f497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562480"
---
# <span data-ttu-id="e875e-101">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e875e-101">Get-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="e875e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e875e-102">SYNOPSIS</span></span>
<span data-ttu-id="e875e-103">Возвращает цепь Azure ExpressRoute из Azure.</span><span class="sxs-lookup"><span data-stu-id="e875e-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e875e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e875e-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e875e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e875e-105">DESCRIPTION</span></span>
<span data-ttu-id="e875e-106">Командлет **Get-AzureRmExpressRouteCircuit** используется для получения объекта цепи ExpressRoute из подписки.</span><span class="sxs-lookup"><span data-stu-id="e875e-106">The **Get-AzureRmExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="e875e-107">Возвращаемый объект цепью можно использовать в качестве входных данных для других командлетов, которые работают с каналами ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e875e-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="e875e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e875e-108">EXAMPLES</span></span>

### <span data-ttu-id="e875e-109">Пример 1: получение канала ExpressRoute для удаления</span><span class="sxs-lookup"><span data-stu-id="e875e-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="e875e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e875e-110">PARAMETERS</span></span>

### <span data-ttu-id="e875e-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e875e-111">-Name</span></span>
<span data-ttu-id="e875e-112">Имя канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e875e-112">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e875e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e875e-113">-ResourceGroupName</span></span>
<span data-ttu-id="e875e-114">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e875e-114">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e875e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e875e-115">-DefaultProfile</span></span>
<span data-ttu-id="e875e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e875e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e875e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e875e-117">CommonParameters</span></span>
<span data-ttu-id="e875e-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e875e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e875e-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e875e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e875e-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e875e-120">INPUTS</span></span>

## <span data-ttu-id="e875e-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e875e-121">OUTPUTS</span></span>

### <span data-ttu-id="e875e-122">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e875e-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e875e-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="e875e-123">NOTES</span></span>

## <span data-ttu-id="e875e-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e875e-124">RELATED LINKS</span></span>

[<span data-ttu-id="e875e-125">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e875e-125">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e875e-126">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e875e-126">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e875e-127">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e875e-127">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e875e-128">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e875e-128">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
