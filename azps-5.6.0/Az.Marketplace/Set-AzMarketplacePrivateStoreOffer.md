---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/powershell/module/az.marketplace/set-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 9a2f5744f5595b7be4a0a59c3181435e4f1d0eb6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009619"
---
# <span data-ttu-id="57f35-101">Set-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="57f35-101">Set-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="57f35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57f35-102">SYNOPSIS</span></span>
<span data-ttu-id="57f35-103">Обновляет или создает предложение для частного магазина.</span><span class="sxs-lookup"><span data-stu-id="57f35-103">Updates or creates offer for private store.</span></span>

## <span data-ttu-id="57f35-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="57f35-104">SYNTAX</span></span>

```
Set-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String>
 -SpecificPlanIdsLimitation <System.Collections.Generic.List`1[System.String]> [-ETag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57f35-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57f35-105">DESCRIPTION</span></span>
<span data-ttu-id="57f35-106">Обновляет или создает предложение для частного магазина, созданного в рамках клиента.</span><span class="sxs-lookup"><span data-stu-id="57f35-106">Updates or creates offer for private store that was created under tenant scope.</span></span>

## <span data-ttu-id="57f35-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="57f35-107">EXAMPLES</span></span>

### <span data-ttu-id="57f35-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="57f35-108">Example 1</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73", "PublisherEnterpriseLinux73-ARM ", "PublisherEnterpriseLinux73-ARM-pr")

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009562-0000-0600-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux72, PublisherEnterpriseLinux72-ARM, PublisherEnterpriseLinux73, PublisherEnterpriseLinux73-ARM, PublisherEnterpriseLinux73-ARM-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="57f35-109">Создает предложение с закрытыми и общедоступными планами для частного магазина, созданного в области клиента.</span><span class="sxs-lookup"><span data-stu-id="57f35-109">Creates offer with private + public plans for private store that was created under tenant scope.</span></span> 

### <span data-ttu-id="57f35-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="57f35-110">Example 2</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281 -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73", "PublisherEnterpriseLinux73-ARM ", "PublisherEnterpriseLinux73-ARM-pr")

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009562-0000-0600-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux73-ARM-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="57f35-111">Создает предложение с закрытыми планами только для частного магазина, созданного в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="57f35-111">Creates offer with private plans only for private store that was created under subscription scope.</span></span> 

### <span data-ttu-id="57f35-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="57f35-112">Example 3</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73") -ETag 04009562-0000-0600-0000-5ecd2fb00000

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "02009562-0000-0600-0120-3ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux72, PublisherEnterpriseLinux72-ARM, PublisherEnterpriseLinux73}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="57f35-113">Предлагаются обновления с закрытыми и общедоступными планами для частного магазина, созданного в области клиента.</span><span class="sxs-lookup"><span data-stu-id="57f35-113">Updates offer with private + public plans for private store that was created under tenant scope.</span></span> <span data-ttu-id="57f35-114">Требуется Etag.</span><span class="sxs-lookup"><span data-stu-id="57f35-114">Etag is needed.</span></span>

### <span data-ttu-id="57f35-115">Пример 4</span><span class="sxs-lookup"><span data-stu-id="57f35-115">Example 4</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281 -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux73-pr") -ETag 04009562-0000-0600-0000-5ecd2fb00000

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "02009562-0000-0600-0120-3ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux73-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="57f35-116">Обновления предлагаются для частного магазина с закрытыми планами, созданными в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="57f35-116">Updates offer for private store with private plans only that was created under subscription scope.</span></span> <span data-ttu-id="57f35-117">Требуется Etag.</span><span class="sxs-lookup"><span data-stu-id="57f35-117">Etag is needed.</span></span>


## <span data-ttu-id="57f35-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57f35-118">PARAMETERS</span></span>

### <span data-ttu-id="57f35-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57f35-119">-DefaultProfile</span></span>
<span data-ttu-id="57f35-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57f35-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57f35-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="57f35-121">-ETag</span></span>
<span data-ttu-id="57f35-122">ETag предложения privateStore Azure Marketplace для обновления</span><span class="sxs-lookup"><span data-stu-id="57f35-122">Azure Marketplace privateStore offer's eTag for update</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f35-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="57f35-123">-OfferId</span></span>
<span data-ttu-id="57f35-124">Обязательное предложение privateStore для Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="57f35-124">Required Azure Marketplace privateStore offer</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f35-125">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="57f35-125">-PrivateStoreId</span></span>
<span data-ttu-id="57f35-126">Требуемая возможность предложений privateStore в Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="57f35-126">Required Azure Marketplace privateStore offers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f35-127">-SpecificPlanIdsLimitation</span><span class="sxs-lookup"><span data-stu-id="57f35-127">-SpecificPlanIdsLimitation</span></span>
<span data-ttu-id="57f35-128">Обязательное ограничение на набор предложений privateStore для Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="57f35-128">Required Azure Marketplace privateStore offer's specific plan ids limitation</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f35-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57f35-129">-Confirm</span></span>
<span data-ttu-id="57f35-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57f35-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f35-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57f35-131">-WhatIf</span></span>
<span data-ttu-id="57f35-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57f35-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57f35-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="57f35-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f35-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57f35-134">CommonParameters</span></span>
<span data-ttu-id="57f35-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57f35-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57f35-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57f35-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57f35-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57f35-137">INPUTS</span></span>

### <span data-ttu-id="57f35-138">Нет</span><span class="sxs-lookup"><span data-stu-id="57f35-138">None</span></span>

## <span data-ttu-id="57f35-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="57f35-139">OUTPUTS</span></span>

### <span data-ttu-id="57f35-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="57f35-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="57f35-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="57f35-141">NOTES</span></span>

## <span data-ttu-id="57f35-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57f35-142">RELATED LINKS</span></span>
