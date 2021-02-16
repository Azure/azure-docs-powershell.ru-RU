---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azlegacypeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
ms.openlocfilehash: e7b5ef8ef41c66cc3c19fd5ebdcfd53ddcc6f3a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220761"
---
# <span data-ttu-id="7d466-101">Get-AzLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="7d466-101">Get-AzLegacyPeering</span></span>

## <span data-ttu-id="7d466-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d466-102">SYNOPSIS</span></span>
<span data-ttu-id="7d466-103">Используется для преобразования устаревших ресурсов пиринга в ресурсы управления ресурсами Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="7d466-103">Used to Convert Legacy Peering resources to Azure Resource Management (ARM) Resources.</span></span> 

## <span data-ttu-id="7d466-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7d466-104">SYNTAX</span></span>

```
Get-AzLegacyPeering [-PeeringLocation] <String> [-Kind] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d466-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d466-105">DESCRIPTION</span></span>
<span data-ttu-id="7d466-106">Команда используется для просмотра устаревших ресурсов пиринга, преобразующих их в ресурсы управления ресурсами Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="7d466-106">The command is used to view legacy Peering resources which all you to convert them to Azure Resource Management (ARM) Resources.</span></span>

## <span data-ttu-id="7d466-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7d466-107">EXAMPLES</span></span>

### <span data-ttu-id="7d466-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7d466-108">Example 1</span></span>
```powershell
PS C:> Get-AzLegacyPeering -PeeringLocation "Seattle" -Kind Direct

Name                       :
Sku                        : Basic_Direct_Free
Kind                       : Direct
PeeringLocation            : Seattle
UseForPeeringService       : False
PeerAsn.Id                 :
Connection                 : ------------------------
PeeringDBFacilityId        : 71
SessionPrefixIPv4          : 173.205.50.236/30
PeerSessionIPv4Address     : 173.205.50.237
MicrosoftIPv4Address       : 173.205.50.238
SessionStateV4             : Established
MaxPrefixesAdvertisedV4    : 20000
SessionPrefixIPv6          : 2001:668:0:3:ffff:0:adcd:32ec/126
PeerSessionIPv6Address     : 2001:668:0:3:ffff:0:adcd:32ed
MicrosoftIPv6Address       : 2001:668:0:3:ffff:0:adcd:32ee
SessionStateV6             : Established
MaxPrefixesAdvertisedV6    : 2000
ConnectionState            : Active
BandwidthInMbps            : 0
ProvisionedBandwidthInMbps : 20000
ProvisioningState          : Succeeded
```

<span data-ttu-id="7d466-109">Возвращает устаревший пиринг для Сиэтла</span><span class="sxs-lookup"><span data-stu-id="7d466-109">Gets the legacy peering for Seattle</span></span>

## <span data-ttu-id="7d466-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d466-110">PARAMETERS</span></span>

### <span data-ttu-id="7d466-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d466-111">-DefaultProfile</span></span>
<span data-ttu-id="7d466-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d466-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d466-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="7d466-113">-Kind</span></span>
<span data-ttu-id="7d466-114">Показывает все ресурсы пиринга по типу.</span><span class="sxs-lookup"><span data-stu-id="7d466-114">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d466-115">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="7d466-115">-PeeringLocation</span></span>
<span data-ttu-id="7d466-116">Показывает все ресурсы пиринга по типу.</span><span class="sxs-lookup"><span data-stu-id="7d466-116">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d466-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d466-117">CommonParameters</span></span>
<span data-ttu-id="7d466-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d466-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d466-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d466-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d466-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d466-120">INPUTS</span></span>

### <span data-ttu-id="7d466-121">Нет</span><span class="sxs-lookup"><span data-stu-id="7d466-121">None</span></span>

## <span data-ttu-id="7d466-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7d466-122">OUTPUTS</span></span>

### <span data-ttu-id="7d466-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="7d466-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="7d466-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7d466-124">NOTES</span></span>

## <span data-ttu-id="7d466-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d466-125">RELATED LINKS</span></span>
