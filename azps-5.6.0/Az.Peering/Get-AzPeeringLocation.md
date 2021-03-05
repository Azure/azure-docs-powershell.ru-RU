---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
ms.openlocfilehash: a4367087bd248589f3345c14f6c7681be5eae9ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989582"
---
# <span data-ttu-id="c5f26-101">Get-AzPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="c5f26-101">Get-AzPeeringLocation</span></span>

## <span data-ttu-id="c5f26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5f26-102">SYNOPSIS</span></span>
<span data-ttu-id="c5f26-103">Получает расположения пиринга, предлагаемые корпорацией Майкрософт</span><span class="sxs-lookup"><span data-stu-id="c5f26-103">Gets the Peering locations offered by Microsoft</span></span>

## <span data-ttu-id="c5f26-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c5f26-104">SYNTAX</span></span>

### <span data-ttu-id="c5f26-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c5f26-105">Default (Default)</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5f26-106">LocationByFacilityId</span><span class="sxs-lookup"><span data-stu-id="c5f26-106">LocationByFacilityId</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringDbFacilityId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5f26-107">LocationByDirectType</span><span class="sxs-lookup"><span data-stu-id="c5f26-107">LocationByDirectType</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DirectPeeringType <String>]
 [-PeeringDbFacilityId <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5f26-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5f26-108">DESCRIPTION</span></span>
<span data-ttu-id="c5f26-109">Позволяет получить средства пиринга, в которых пользователи могут подключаться к ARM.</span><span class="sxs-lookup"><span data-stu-id="c5f26-109">Gets the Peering Facilities where users can connect with ARM.</span></span>

## <span data-ttu-id="c5f26-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c5f26-110">EXAMPLES</span></span>

### <span data-ttu-id="c5f26-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c5f26-111">Example 1</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Direct

#...More above
PeeringLocation       : Dublin
Address               : Unit 2, North West Business Park
Country               : IE
PeeringDBFacilityId   : 1065
PeeringDBFacilityLink : https://www.peeringdb.com/fac/1065
BandwidthOffers       : {10Gbps, 100Gbps}

PeeringLocation       : Frankfurt
Address               : Hanauer Landstrasse 298
Country               : DE
PeeringDBFacilityId   : 58
PeeringDBFacilityLink : https://www.peeringdb.com/fac/58
BandwidthOffers       : {10Gbps, 100Gbps}
#...More below
```

<span data-ttu-id="c5f26-112">Длинный список местоположений.</span><span class="sxs-lookup"><span data-stu-id="c5f26-112">Its a long list of locations.</span></span> <span data-ttu-id="c5f26-113">Все объекты прямого пиринга.</span><span class="sxs-lookup"><span data-stu-id="c5f26-113">Gets the all the Direct Peering Facilities.</span></span>

### <span data-ttu-id="c5f26-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c5f26-114">Example 2</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Exchange -PeeringLocation "Honolulu" 

ExchangeName          : DRF IX
PeeringLocation       : Honolulu
Country               : US
PeeringDBFacilityId   : 267
PeeringDBFacilityLink : https://www.peeringdb.com/ix/267
MicrosoftIPv4Address  : 206.197.210.37
MicrosoftIPv6Address  : 2606:7c80:3375:50::37
FacilityIPv4Prefix    : 206.197.210.0/24
FacilityIPv6Prefix    : 2606:7c80:3375:50::/64
```

<span data-ttu-id="c5f26-115">Получает расположение пиринга по обмену для Гонолулу.</span><span class="sxs-lookup"><span data-stu-id="c5f26-115">Gets the exchange peering location for Honolulu.</span></span> 

### <span data-ttu-id="c5f26-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c5f26-116">Example 3</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Exchange -PeeringDbFacilityId 71 

ExchangeName          : NIX.CZ
PeeringLocation       : Prague
Country               : CZ
PeeringDBFacilityId   : 71
PeeringDBFacilityLink : https://www.peeringdb.com/ix/71
MicrosoftIPv4Address  : 91.210.16.115
MicrosoftIPv6Address  : 2001:7f8:14::6b:1
FacilityIPv4Prefix    : 91.210.16.0/22
FacilityIPv6Prefix    : 2001:7f8:14::/64
```

<span data-ttu-id="c5f26-117">Получает расположение пиринга exchange для объекта пиринга id 71.</span><span class="sxs-lookup"><span data-stu-id="c5f26-117">Gets the exchange peering location for peering facility id 71.</span></span> 

## <span data-ttu-id="c5f26-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5f26-118">PARAMETERS</span></span>

### <span data-ttu-id="c5f26-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5f26-119">-DefaultProfile</span></span>
<span data-ttu-id="c5f26-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c5f26-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5f26-121">-DirectPeeringType</span><span class="sxs-lookup"><span data-stu-id="c5f26-121">-DirectPeeringType</span></span>
<span data-ttu-id="c5f26-122">Выберите пункты "Edge", "CDN" и "Transit".</span><span class="sxs-lookup"><span data-stu-id="c5f26-122">Select 'Edge', 'CDN', and 'Transit'.</span></span>

```yaml
Type: System.String
Parameter Sets: LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5f26-123">-Kind</span><span class="sxs-lookup"><span data-stu-id="c5f26-123">-Kind</span></span>
<span data-ttu-id="c5f26-124">Показывает все ресурсы пиринга по типу.</span><span class="sxs-lookup"><span data-stu-id="c5f26-124">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="c5f26-125">-PeeringDbFacilityId</span><span class="sxs-lookup"><span data-stu-id="c5f26-125">-PeeringDbFacilityId</span></span>
<span data-ttu-id="c5f26-126">ИД PeeringDB.com объекта</span><span class="sxs-lookup"><span data-stu-id="c5f26-126">The PeeringDB.com Facility ID</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LocationByFacilityId, LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5f26-127">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="c5f26-127">-PeeringLocation</span></span>
<span data-ttu-id="c5f26-128">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="c5f26-128">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5f26-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5f26-129">CommonParameters</span></span>
<span data-ttu-id="c5f26-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5f26-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5f26-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5f26-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5f26-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5f26-132">INPUTS</span></span>

### <span data-ttu-id="c5f26-133">Нет</span><span class="sxs-lookup"><span data-stu-id="c5f26-133">None</span></span>

## <span data-ttu-id="c5f26-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c5f26-134">OUTPUTS</span></span>

### <span data-ttu-id="c5f26-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="c5f26-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringLocation</span></span>

## <span data-ttu-id="c5f26-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c5f26-136">NOTES</span></span>

## <span data-ttu-id="c5f26-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5f26-137">RELATED LINKS</span></span>
