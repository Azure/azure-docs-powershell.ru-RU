---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 15aed0e5a4cca1b67c85cbe651453d64cecc13ee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248131"
---
# <span data-ttu-id="396cb-101">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="396cb-101">Get-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="396cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="396cb-102">SYNOPSIS</span></span>
<span data-ttu-id="396cb-103">Возвращает конфигурацию пиринга для перекрестного подключения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="396cb-103">Gets an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="396cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="396cb-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnectionPeering [-Name <String>]
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="396cb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="396cb-105">DESCRIPTION</span></span>
<span data-ttu-id="396cb-106">Командлет **Get-AzExpressRouteCrossConnectionPeering** извлекает конфигурацию однорангового отношения для перекрестного соединения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="396cb-106">The **Get-AzExpressRouteCrossConnectionPeering** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="396cb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="396cb-107">EXAMPLES</span></span>

### <span data-ttu-id="396cb-108">Пример 1: отображение конфигурации пиринга для перекрестного соединения ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="396cb-108">Example 1: Display the peering configuration for an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $RG
Get-AzExpressRouteCrossConnectionPeering -Name "AzurePrivatePeering" -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="396cb-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="396cb-109">PARAMETERS</span></span>

### <span data-ttu-id="396cb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="396cb-110">-DefaultProfile</span></span>
<span data-ttu-id="396cb-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="396cb-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="396cb-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="396cb-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="396cb-113">Объект перекрестного соединения ExpressRoute, содержащий конфигурацию пиринга.</span><span class="sxs-lookup"><span data-stu-id="396cb-113">The ExpressRoute cross connection object containing the peering configuration.</span></span>

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

### <span data-ttu-id="396cb-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="396cb-114">-Name</span></span>
<span data-ttu-id="396cb-115">Имя конфигурации пиринга, которую нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="396cb-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="396cb-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="396cb-116">CommonParameters</span></span>
<span data-ttu-id="396cb-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="396cb-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="396cb-118">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="396cb-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="396cb-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="396cb-119">INPUTS</span></span>

### <span data-ttu-id="396cb-120">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="396cb-120">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="396cb-121">Параметр "ExpressRouteCrossConnection" принимает значение типа "PSExpressRouteCrossConnection" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="396cb-121">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="396cb-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="396cb-122">OUTPUTS</span></span>

### <span data-ttu-id="396cb-123">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="396cb-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="396cb-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="396cb-124">NOTES</span></span>

## <span data-ttu-id="396cb-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="396cb-125">RELATED LINKS</span></span>

[<span data-ttu-id="396cb-126">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="396cb-126">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="396cb-127">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="396cb-127">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="396cb-128">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="396cb-128">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="396cb-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="396cb-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)