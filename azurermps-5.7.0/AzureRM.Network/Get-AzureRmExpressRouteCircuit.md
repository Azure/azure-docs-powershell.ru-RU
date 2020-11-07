---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 380a5f52a520f487e625663f7d84cbbc55564db5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733015"
---
# <span data-ttu-id="815a8-101">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="815a8-101">Get-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="815a8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="815a8-102">SYNOPSIS</span></span>
<span data-ttu-id="815a8-103">Возвращает цепь Azure ExpressRoute из Azure.</span><span class="sxs-lookup"><span data-stu-id="815a8-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="815a8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="815a8-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="815a8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="815a8-105">DESCRIPTION</span></span>
<span data-ttu-id="815a8-106">Командлет **Get-AzureRmExpressRouteCircuit** используется для получения объекта цепи ExpressRoute из подписки.</span><span class="sxs-lookup"><span data-stu-id="815a8-106">The **Get-AzureRmExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="815a8-107">Возвращаемый объект цепью можно использовать в качестве входных данных для других командлетов, которые работают с каналами ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="815a8-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="815a8-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="815a8-108">EXAMPLES</span></span>

### <span data-ttu-id="815a8-109">Пример 1: получение канала ExpressRoute для удаления</span><span class="sxs-lookup"><span data-stu-id="815a8-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="815a8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="815a8-110">PARAMETERS</span></span>

### <span data-ttu-id="815a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="815a8-111">-DefaultProfile</span></span>
<span data-ttu-id="815a8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="815a8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="815a8-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="815a8-113">-Name</span></span>
<span data-ttu-id="815a8-114">Имя канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="815a8-114">The name of the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="815a8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="815a8-115">-ResourceGroupName</span></span>
<span data-ttu-id="815a8-116">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="815a8-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="815a8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="815a8-117">CommonParameters</span></span>
<span data-ttu-id="815a8-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="815a8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="815a8-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="815a8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="815a8-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="815a8-120">INPUTS</span></span>

### <span data-ttu-id="815a8-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="815a8-121">None</span></span>
<span data-ttu-id="815a8-122">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="815a8-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="815a8-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="815a8-123">OUTPUTS</span></span>

### <span data-ttu-id="815a8-124">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="815a8-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="815a8-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="815a8-125">NOTES</span></span>

## <span data-ttu-id="815a8-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="815a8-126">RELATED LINKS</span></span>

[<span data-ttu-id="815a8-127">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="815a8-127">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="815a8-128">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="815a8-128">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="815a8-129">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="815a8-129">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="815a8-130">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="815a8-130">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
