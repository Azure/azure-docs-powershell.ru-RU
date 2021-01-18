---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 58df8e57a225d1ee003da317ca24c71b1db34f5f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517998"
---
# <span data-ttu-id="7ca20-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7ca20-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="7ca20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ca20-102">SYNOPSIS</span></span>
<span data-ttu-id="7ca20-103">Изменяет канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7ca20-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="7ca20-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7ca20-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ca20-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ca20-105">DESCRIPTION</span></span>
<span data-ttu-id="7ca20-106">**Cmdlet Set-AzExpressRouteCircuit** сохраняет измененный канал ExpressRoute в Azure.</span><span class="sxs-lookup"><span data-stu-id="7ca20-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="7ca20-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7ca20-107">EXAMPLES</span></span>

### <span data-ttu-id="7ca20-108">Пример 1. Изменение ServiceKey в канале ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="7ca20-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="7ca20-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ca20-109">PARAMETERS</span></span>

### <span data-ttu-id="7ca20-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ca20-110">-AsJob</span></span>
<span data-ttu-id="7ca20-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7ca20-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ca20-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ca20-112">-DefaultProfile</span></span>
<span data-ttu-id="7ca20-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7ca20-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ca20-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7ca20-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="7ca20-115">Определяет объект **ExpressRouteCircuit,** который изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ca20-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7ca20-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ca20-116">CommonParameters</span></span>
<span data-ttu-id="7ca20-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ca20-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ca20-118">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ca20-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ca20-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ca20-119">INPUTS</span></span>

### <span data-ttu-id="7ca20-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7ca20-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="7ca20-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7ca20-121">OUTPUTS</span></span>

### <span data-ttu-id="7ca20-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7ca20-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="7ca20-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7ca20-123">NOTES</span></span>

## <span data-ttu-id="7ca20-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7ca20-124">RELATED LINKS</span></span>

[<span data-ttu-id="7ca20-125">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7ca20-125">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="7ca20-126">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7ca20-126">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="7ca20-127">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7ca20-127">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="7ca20-128">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7ca20-128">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
