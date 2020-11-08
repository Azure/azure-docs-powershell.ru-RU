---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azlegacypeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
ms.openlocfilehash: e7b5ef8ef41c66cc3c19fd5ebdcfd53ddcc6f3a9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234835"
---
# <span data-ttu-id="eafef-101">Get-AzLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="eafef-101">Get-AzLegacyPeering</span></span>

## <span data-ttu-id="eafef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eafef-102">SYNOPSIS</span></span>
<span data-ttu-id="eafef-103">Используется для преобразования устаревших ресурсов однорангового соединения в ресурсы управления ресурсами Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="eafef-103">Used to Convert Legacy Peering resources to Azure Resource Management (ARM) Resources.</span></span> 

## <span data-ttu-id="eafef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eafef-104">SYNTAX</span></span>

```
Get-AzLegacyPeering [-PeeringLocation] <String> [-Kind] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eafef-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eafef-105">DESCRIPTION</span></span>
<span data-ttu-id="eafef-106">Эта команда используется для просмотра устаревших ресурсов пиринга, которые нужно преобразовать в ресурсы управления ресурсами Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="eafef-106">The command is used to view legacy Peering resources which all you to convert them to Azure Resource Management (ARM) Resources.</span></span>

## <span data-ttu-id="eafef-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eafef-107">EXAMPLES</span></span>

### <span data-ttu-id="eafef-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eafef-108">Example 1</span></span>
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

<span data-ttu-id="eafef-109">Получает старый одноранговый элемент для Сиэтле.</span><span class="sxs-lookup"><span data-stu-id="eafef-109">Gets the legacy peering for Seattle</span></span>

## <span data-ttu-id="eafef-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eafef-110">PARAMETERS</span></span>

### <span data-ttu-id="eafef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eafef-111">-DefaultProfile</span></span>
<span data-ttu-id="eafef-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eafef-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eafef-113">-Видах</span><span class="sxs-lookup"><span data-stu-id="eafef-113">-Kind</span></span>
<span data-ttu-id="eafef-114">Показывает все ресурсы пиринга по типу.</span><span class="sxs-lookup"><span data-stu-id="eafef-114">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="eafef-115">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="eafef-115">-PeeringLocation</span></span>
<span data-ttu-id="eafef-116">Показывает все ресурсы пиринга по типу.</span><span class="sxs-lookup"><span data-stu-id="eafef-116">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="eafef-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eafef-117">CommonParameters</span></span>
<span data-ttu-id="eafef-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eafef-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eafef-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eafef-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eafef-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eafef-120">INPUTS</span></span>

### <span data-ttu-id="eafef-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="eafef-121">None</span></span>

## <span data-ttu-id="eafef-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eafef-122">OUTPUTS</span></span>

### <span data-ttu-id="eafef-123">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeering)</span><span class="sxs-lookup"><span data-stu-id="eafef-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="eafef-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="eafef-124">NOTES</span></span>

## <span data-ttu-id="eafef-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eafef-125">RELATED LINKS</span></span>
