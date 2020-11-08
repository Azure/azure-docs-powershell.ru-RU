---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
ms.openlocfilehash: 233cf87eed682919df8ca0ae38fefaec5964942c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235949"
---
# <span data-ttu-id="94f36-101">Get-AzPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="94f36-101">Get-AzPeeringLocation</span></span>

## <span data-ttu-id="94f36-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94f36-102">SYNOPSIS</span></span>
<span data-ttu-id="94f36-103">Возвращает расположения пиринга, предлагаемые корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="94f36-103">Gets the Peering locations offered by Microsoft</span></span>

## <span data-ttu-id="94f36-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94f36-104">SYNTAX</span></span>

### <span data-ttu-id="94f36-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="94f36-105">Default (Default)</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="94f36-106">LocationByFacilityId</span><span class="sxs-lookup"><span data-stu-id="94f36-106">LocationByFacilityId</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringDbFacilityId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94f36-107">LocationByDirectType</span><span class="sxs-lookup"><span data-stu-id="94f36-107">LocationByDirectType</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DirectPeeringType <String>]
 [-PeeringDbFacilityId <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94f36-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94f36-108">DESCRIPTION</span></span>
<span data-ttu-id="94f36-109">Возвращает средства пиринга, к которым пользователи могут подключаться с помощью ARM.</span><span class="sxs-lookup"><span data-stu-id="94f36-109">Gets the Peering Facilities where users can connect with ARM.</span></span>

## <span data-ttu-id="94f36-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94f36-110">EXAMPLES</span></span>

### <span data-ttu-id="94f36-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="94f36-111">Example 1</span></span>
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

<span data-ttu-id="94f36-112">Его длинный список местоположений.</span><span class="sxs-lookup"><span data-stu-id="94f36-112">Its a long list of locations.</span></span> <span data-ttu-id="94f36-113">Получает все прямые средства пиринга.</span><span class="sxs-lookup"><span data-stu-id="94f36-113">Gets the all the Direct Peering Facilities.</span></span>

### <span data-ttu-id="94f36-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="94f36-114">Example 2</span></span>
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

<span data-ttu-id="94f36-115">Возвращает расположение пиринга Exchange для Гонолулу.</span><span class="sxs-lookup"><span data-stu-id="94f36-115">Gets the exchange peering location for Honolulu.</span></span> 

### <span data-ttu-id="94f36-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="94f36-116">Example 3</span></span>
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

<span data-ttu-id="94f36-117">Возвращает расположение пиринга Exchange для ИД средства пиринга 71.</span><span class="sxs-lookup"><span data-stu-id="94f36-117">Gets the exchange peering location for peering facility id 71.</span></span> 

## <span data-ttu-id="94f36-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94f36-118">PARAMETERS</span></span>

### <span data-ttu-id="94f36-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f36-119">-DefaultProfile</span></span>
<span data-ttu-id="94f36-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94f36-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94f36-121">-DirectPeeringType</span><span class="sxs-lookup"><span data-stu-id="94f36-121">-DirectPeeringType</span></span>
<span data-ttu-id="94f36-122">Выберите "Edge", "CDN" и "транзит".</span><span class="sxs-lookup"><span data-stu-id="94f36-122">Select 'Edge', 'CDN', and 'Transit'.</span></span>

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

### <span data-ttu-id="94f36-123">-Видах</span><span class="sxs-lookup"><span data-stu-id="94f36-123">-Kind</span></span>
<span data-ttu-id="94f36-124">Показывает все ресурсы пиринга по типу.</span><span class="sxs-lookup"><span data-stu-id="94f36-124">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="94f36-125">-PeeringDbFacilityId</span><span class="sxs-lookup"><span data-stu-id="94f36-125">-PeeringDbFacilityId</span></span>
<span data-ttu-id="94f36-126">КОД средства PeeringDB.com</span><span class="sxs-lookup"><span data-stu-id="94f36-126">The PeeringDB.com Facility ID</span></span>

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

### <span data-ttu-id="94f36-127">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="94f36-127">-PeeringLocation</span></span>
<span data-ttu-id="94f36-128">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="94f36-128">The location of the resource.</span></span>

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

### <span data-ttu-id="94f36-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f36-129">CommonParameters</span></span>
<span data-ttu-id="94f36-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94f36-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f36-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94f36-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f36-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94f36-132">INPUTS</span></span>

### <span data-ttu-id="94f36-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="94f36-133">None</span></span>

## <span data-ttu-id="94f36-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94f36-134">OUTPUTS</span></span>

### <span data-ttu-id="94f36-135">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeeringLocation)</span><span class="sxs-lookup"><span data-stu-id="94f36-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringLocation</span></span>

## <span data-ttu-id="94f36-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="94f36-136">NOTES</span></span>

## <span data-ttu-id="94f36-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94f36-137">RELATED LINKS</span></span>
