---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 58df8e57a225d1ee003da317ca24c71b1db34f5f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244789"
---
# <span data-ttu-id="a43a9-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a43a9-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="a43a9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a43a9-102">SYNOPSIS</span></span>
<span data-ttu-id="a43a9-103">Изменение канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a43a9-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="a43a9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a43a9-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a43a9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a43a9-105">DESCRIPTION</span></span>
<span data-ttu-id="a43a9-106">Командлет **Set-AzExpressRouteCircuit** сохраняет модифицированную цепь ExpressRoute в Azure.</span><span class="sxs-lookup"><span data-stu-id="a43a9-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="a43a9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a43a9-107">EXAMPLES</span></span>

### <span data-ttu-id="a43a9-108">Пример 1: изменение ServiceKeyа в канале ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="a43a9-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="a43a9-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a43a9-109">PARAMETERS</span></span>

### <span data-ttu-id="a43a9-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a43a9-110">-AsJob</span></span>
<span data-ttu-id="a43a9-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a43a9-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a43a9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a43a9-112">-DefaultProfile</span></span>
<span data-ttu-id="a43a9-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a43a9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a43a9-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a43a9-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="a43a9-115">Указывает объект **ExpressRouteCircuit** , который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a43a9-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a43a9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a43a9-116">CommonParameters</span></span>
<span data-ttu-id="a43a9-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a43a9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a43a9-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a43a9-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a43a9-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a43a9-119">INPUTS</span></span>

### <span data-ttu-id="a43a9-120">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a43a9-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a43a9-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a43a9-121">OUTPUTS</span></span>

### <span data-ttu-id="a43a9-122">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a43a9-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a43a9-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="a43a9-123">NOTES</span></span>

## <span data-ttu-id="a43a9-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a43a9-124">RELATED LINKS</span></span>

[<span data-ttu-id="a43a9-125">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a43a9-125">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="a43a9-126">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a43a9-126">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="a43a9-127">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a43a9-127">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="a43a9-128">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a43a9-128">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
