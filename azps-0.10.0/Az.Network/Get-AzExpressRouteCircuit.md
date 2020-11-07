---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: f72d398eaea1d127ba600130fae3bbc690052332
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910025"
---
# <span data-ttu-id="0d5c7-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0d5c7-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="0d5c7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d5c7-102">SYNOPSIS</span></span>
<span data-ttu-id="0d5c7-103">Возвращает цепь Azure ExpressRoute из Azure.</span><span class="sxs-lookup"><span data-stu-id="0d5c7-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="0d5c7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d5c7-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d5c7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d5c7-105">DESCRIPTION</span></span>
<span data-ttu-id="0d5c7-106">Командлет **Get-AzExpressRouteCircuit** используется для получения объекта цепи ExpressRoute из подписки.</span><span class="sxs-lookup"><span data-stu-id="0d5c7-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="0d5c7-107">Возвращаемый объект цепью можно использовать в качестве входных данных для других командлетов, которые работают с каналами ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0d5c7-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="0d5c7-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d5c7-108">EXAMPLES</span></span>

### <span data-ttu-id="0d5c7-109">Пример 1: получение канала ExpressRoute для удаления</span><span class="sxs-lookup"><span data-stu-id="0d5c7-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="0d5c7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d5c7-110">PARAMETERS</span></span>

### <span data-ttu-id="0d5c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d5c7-111">-DefaultProfile</span></span>
<span data-ttu-id="0d5c7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d5c7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d5c7-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0d5c7-113">-Name</span></span>
<span data-ttu-id="0d5c7-114">Имя канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0d5c7-114">The name of the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="0d5c7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d5c7-115">-ResourceGroupName</span></span>
<span data-ttu-id="0d5c7-116">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0d5c7-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="0d5c7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d5c7-117">CommonParameters</span></span>
<span data-ttu-id="0d5c7-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d5c7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d5c7-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d5c7-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d5c7-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d5c7-120">INPUTS</span></span>

## <span data-ttu-id="0d5c7-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d5c7-121">OUTPUTS</span></span>

### <span data-ttu-id="0d5c7-122">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0d5c7-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="0d5c7-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d5c7-123">NOTES</span></span>

## <span data-ttu-id="0d5c7-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d5c7-124">RELATED LINKS</span></span>

[<span data-ttu-id="0d5c7-125">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0d5c7-125">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="0d5c7-126">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0d5c7-126">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="0d5c7-127">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0d5c7-127">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="0d5c7-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0d5c7-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
