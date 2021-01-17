---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 58df8e57a225d1ee003da317ca24c71b1db34f5f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399540"
---
# <span data-ttu-id="7eaba-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7eaba-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="7eaba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7eaba-102">SYNOPSIS</span></span>
<span data-ttu-id="7eaba-103">Изменяет канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7eaba-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="7eaba-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7eaba-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7eaba-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7eaba-105">DESCRIPTION</span></span>
<span data-ttu-id="7eaba-106">**Cmdlet Set-AzExpressRouteCircuit** сохраняет измененный канал ExpressRoute в Azure.</span><span class="sxs-lookup"><span data-stu-id="7eaba-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="7eaba-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7eaba-107">EXAMPLES</span></span>

### <span data-ttu-id="7eaba-108">Пример 1. Изменение ServiceKey в канале ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="7eaba-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="7eaba-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7eaba-109">PARAMETERS</span></span>

### <span data-ttu-id="7eaba-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7eaba-110">-AsJob</span></span>
<span data-ttu-id="7eaba-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7eaba-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7eaba-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eaba-112">-DefaultProfile</span></span>
<span data-ttu-id="7eaba-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7eaba-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7eaba-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7eaba-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="7eaba-115">Определяет объект **ExpressRouteCircuit,** который изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7eaba-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7eaba-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eaba-116">CommonParameters</span></span>
<span data-ttu-id="7eaba-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eaba-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eaba-118">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eaba-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eaba-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7eaba-119">INPUTS</span></span>

### <span data-ttu-id="7eaba-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7eaba-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="7eaba-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7eaba-121">OUTPUTS</span></span>

### <span data-ttu-id="7eaba-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7eaba-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="7eaba-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7eaba-123">NOTES</span></span>

## <span data-ttu-id="7eaba-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7eaba-124">RELATED LINKS</span></span>

[<span data-ttu-id="7eaba-125">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7eaba-125">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="7eaba-126">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7eaba-126">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="7eaba-127">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7eaba-127">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="7eaba-128">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7eaba-128">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
