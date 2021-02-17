---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 15aed0e5a4cca1b67c85cbe651453d64cecc13ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221260"
---
# <span data-ttu-id="54e95-101">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="54e95-101">Get-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="54e95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54e95-102">SYNOPSIS</span></span>
<span data-ttu-id="54e95-103">Получает конфигурацию пиринга для перекрестного подключения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="54e95-103">Gets an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="54e95-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="54e95-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnectionPeering [-Name <String>]
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54e95-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54e95-105">DESCRIPTION</span></span>
<span data-ttu-id="54e95-106">Cmdlet **Get-AzExpressRouteCrossConnectionPeering** извлекает конфигурацию отношения пиринга для перекрестного подключения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="54e95-106">The **Get-AzExpressRouteCrossConnectionPeering** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="54e95-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="54e95-107">EXAMPLES</span></span>

### <span data-ttu-id="54e95-108">Пример 1. Отображение конфигурации пиринга для перекрестного подключения ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="54e95-108">Example 1: Display the peering configuration for an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $RG
Get-AzExpressRouteCrossConnectionPeering -Name "AzurePrivatePeering" -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="54e95-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54e95-109">PARAMETERS</span></span>

### <span data-ttu-id="54e95-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54e95-110">-DefaultProfile</span></span>
<span data-ttu-id="54e95-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54e95-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54e95-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="54e95-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="54e95-113">Объект перекрестного подключения ExpressRoute, содержащий конфигурацию пиринга.</span><span class="sxs-lookup"><span data-stu-id="54e95-113">The ExpressRoute cross connection object containing the peering configuration.</span></span>

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

### <span data-ttu-id="54e95-114">-Name</span><span class="sxs-lookup"><span data-stu-id="54e95-114">-Name</span></span>
<span data-ttu-id="54e95-115">Имя извлекаемой конфигурации пиринга.</span><span class="sxs-lookup"><span data-stu-id="54e95-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="54e95-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54e95-116">CommonParameters</span></span>
<span data-ttu-id="54e95-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54e95-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54e95-118">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54e95-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54e95-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54e95-119">INPUTS</span></span>

### <span data-ttu-id="54e95-120">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="54e95-120">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="54e95-121">Параметр "ExpressRouteCrossConnection" принимает значение типа PSExpressRouteCrossConnection из конвейера.</span><span class="sxs-lookup"><span data-stu-id="54e95-121">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="54e95-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="54e95-122">OUTPUTS</span></span>

### <span data-ttu-id="54e95-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="54e95-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="54e95-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="54e95-124">NOTES</span></span>

## <span data-ttu-id="54e95-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54e95-125">RELATED LINKS</span></span>

[<span data-ttu-id="54e95-126">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="54e95-126">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="54e95-127">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="54e95-127">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="54e95-128">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="54e95-128">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="54e95-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="54e95-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
