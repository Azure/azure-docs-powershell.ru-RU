---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 415c084ebf6c1c83872a16d01ce4eb556f688103
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979619"
---
# <span data-ttu-id="bd55a-101">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="bd55a-101">Get-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="bd55a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd55a-102">SYNOPSIS</span></span>
<span data-ttu-id="bd55a-103">Получает конфигурацию пиринга для перекрестного подключения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bd55a-103">Gets an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="bd55a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bd55a-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnectionPeering [-Name <String>]
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd55a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd55a-105">DESCRIPTION</span></span>
<span data-ttu-id="bd55a-106">Cmdlet **Get-AzExpressRouteCrossConnectionPeering** извлекает конфигурацию отношения пиринга для перекрестного подключения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bd55a-106">The **Get-AzExpressRouteCrossConnectionPeering** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="bd55a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bd55a-107">EXAMPLES</span></span>

### <span data-ttu-id="bd55a-108">Пример 1. Отображение конфигурации пиринга для перекрестного подключения ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="bd55a-108">Example 1: Display the peering configuration for an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $RG
Get-AzExpressRouteCrossConnectionPeering -Name "AzurePrivatePeering" -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="bd55a-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd55a-109">PARAMETERS</span></span>

### <span data-ttu-id="bd55a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd55a-110">-DefaultProfile</span></span>
<span data-ttu-id="bd55a-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd55a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd55a-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="bd55a-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="bd55a-113">Объект перекрестного подключения ExpressRoute, содержащий конфигурацию пиринга.</span><span class="sxs-lookup"><span data-stu-id="bd55a-113">The ExpressRoute cross connection object containing the peering configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd55a-114">-Name</span><span class="sxs-lookup"><span data-stu-id="bd55a-114">-Name</span></span>
<span data-ttu-id="bd55a-115">Имя извлекаемой конфигурации пиринга.</span><span class="sxs-lookup"><span data-stu-id="bd55a-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="bd55a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd55a-116">CommonParameters</span></span>
<span data-ttu-id="bd55a-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd55a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd55a-118">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd55a-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd55a-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd55a-119">INPUTS</span></span>

### <span data-ttu-id="bd55a-120">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="bd55a-120">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="bd55a-121">Параметр "ExpressRouteCrossConnection" принимает значение типа PSExpressRouteCrossConnection из конвейера.</span><span class="sxs-lookup"><span data-stu-id="bd55a-121">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="bd55a-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bd55a-122">OUTPUTS</span></span>

### <span data-ttu-id="bd55a-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="bd55a-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="bd55a-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bd55a-124">NOTES</span></span>

## <span data-ttu-id="bd55a-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd55a-125">RELATED LINKS</span></span>

[<span data-ttu-id="bd55a-126">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="bd55a-126">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="bd55a-127">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="bd55a-127">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="bd55a-128">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="bd55a-128">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="bd55a-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="bd55a-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
