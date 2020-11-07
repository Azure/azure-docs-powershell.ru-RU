---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 99142e3dd33d84e11f326258450d92a58fe70e20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730582"
---
# <span data-ttu-id="a3acb-101">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="a3acb-101">Get-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="a3acb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a3acb-102">SYNOPSIS</span></span>
<span data-ttu-id="a3acb-103">Возвращает конфигурацию пиринга для перекрестного подключения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a3acb-103">Gets an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="a3acb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a3acb-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnectionPeering [-Name <String>]
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3acb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3acb-105">DESCRIPTION</span></span>
<span data-ttu-id="a3acb-106">Командлет **Get-AzExpressRouteCrossConnectionPeering** извлекает конфигурацию однорангового отношения для перекрестного соединения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a3acb-106">The **Get-AzExpressRouteCrossConnectionPeering** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="a3acb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a3acb-107">EXAMPLES</span></span>

### <span data-ttu-id="a3acb-108">Пример 1: отображение конфигурации пиринга для перекрестного соединения ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="a3acb-108">Example 1: Display the peering configuration for an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $RG
Get-AzExpressRouteCrossConnectionPeering -Name "AzurePrivatePeering" -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="a3acb-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a3acb-109">PARAMETERS</span></span>

### <span data-ttu-id="a3acb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3acb-110">-DefaultProfile</span></span>
<span data-ttu-id="a3acb-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a3acb-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3acb-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="a3acb-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="a3acb-113">Объект перекрестного соединения ExpressRoute, содержащий конфигурацию пиринга.</span><span class="sxs-lookup"><span data-stu-id="a3acb-113">The ExpressRoute cross connection object containing the peering configuration.</span></span>

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

### <span data-ttu-id="a3acb-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a3acb-114">-Name</span></span>
<span data-ttu-id="a3acb-115">Имя конфигурации пиринга, которую нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="a3acb-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="a3acb-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3acb-116">CommonParameters</span></span>
<span data-ttu-id="a3acb-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a3acb-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3acb-118">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3acb-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3acb-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a3acb-119">INPUTS</span></span>

### <span data-ttu-id="a3acb-120">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="a3acb-120">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="a3acb-121">Параметр "ExpressRouteCrossConnection" принимает значение типа "PSExpressRouteCrossConnection" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a3acb-121">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="a3acb-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3acb-122">OUTPUTS</span></span>

### <span data-ttu-id="a3acb-123">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="a3acb-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="a3acb-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="a3acb-124">NOTES</span></span>

## <span data-ttu-id="a3acb-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3acb-125">RELATED LINKS</span></span>

[<span data-ttu-id="a3acb-126">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="a3acb-126">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="a3acb-127">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="a3acb-127">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="a3acb-128">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="a3acb-128">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="a3acb-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="a3acb-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
