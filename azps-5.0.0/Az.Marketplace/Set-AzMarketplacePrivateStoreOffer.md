---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/set-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: e39e3e09c99955ee90c285853988713f9a3972c4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248897"
---
# <span data-ttu-id="82e28-101">Set-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="82e28-101">Set-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="82e28-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="82e28-102">SYNOPSIS</span></span>
<span data-ttu-id="82e28-103">Обновление или создание предложения для частного магазина.</span><span class="sxs-lookup"><span data-stu-id="82e28-103">Updates or creates offer for private store.</span></span>

## <span data-ttu-id="82e28-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="82e28-104">SYNTAX</span></span>

```
Set-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String>
 -SpecificPlanIdsLimitation <System.Collections.Generic.List`1[System.String]> [-ETag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82e28-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82e28-105">DESCRIPTION</span></span>
<span data-ttu-id="82e28-106">Обновляет или создает предложение для частного магазина, созданного в рамках области клиента.</span><span class="sxs-lookup"><span data-stu-id="82e28-106">Updates or creates offer for private store that was created under tenant scope.</span></span>

## <span data-ttu-id="82e28-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="82e28-107">EXAMPLES</span></span>

### <span data-ttu-id="82e28-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="82e28-108">Example 1</span></span>
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

<span data-ttu-id="82e28-109">Создает предложение с частными и общедоступными планами для закрытого магазина, созданного в области "клиент".</span><span class="sxs-lookup"><span data-stu-id="82e28-109">Creates offer with private + public plans for private store that was created under tenant scope.</span></span> 

### <span data-ttu-id="82e28-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="82e28-110">Example 2</span></span>
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

<span data-ttu-id="82e28-111">Создает предложение с частными планами только для частного магазина, созданного в рамках области подписок.</span><span class="sxs-lookup"><span data-stu-id="82e28-111">Creates offer with private plans only for private store that was created under subscription scope.</span></span> 

### <span data-ttu-id="82e28-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="82e28-112">Example 3</span></span>
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

<span data-ttu-id="82e28-113">Обновления предлагают закрытые и общедоступные планы для закрытого магазина, созданного в области "клиент".</span><span class="sxs-lookup"><span data-stu-id="82e28-113">Updates offer with private + public plans for private store that was created under tenant scope.</span></span> <span data-ttu-id="82e28-114">Требуется ETag.</span><span class="sxs-lookup"><span data-stu-id="82e28-114">Etag is needed.</span></span>

### <span data-ttu-id="82e28-115">Пример 4</span><span class="sxs-lookup"><span data-stu-id="82e28-115">Example 4</span></span>
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

<span data-ttu-id="82e28-116">Обновления предлагают частный магазин только с частными планами, созданными в разделе "область подписки".</span><span class="sxs-lookup"><span data-stu-id="82e28-116">Updates offer for private store with private plans only that was created under subscription scope.</span></span> <span data-ttu-id="82e28-117">Требуется ETag.</span><span class="sxs-lookup"><span data-stu-id="82e28-117">Etag is needed.</span></span>


## <span data-ttu-id="82e28-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="82e28-118">PARAMETERS</span></span>

### <span data-ttu-id="82e28-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82e28-119">-DefaultProfile</span></span>
<span data-ttu-id="82e28-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="82e28-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82e28-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="82e28-121">-ETag</span></span>
<span data-ttu-id="82e28-122">ETag privateStore предложения Azure Marketplace для обновления</span><span class="sxs-lookup"><span data-stu-id="82e28-122">Azure Marketplace privateStore offer's eTag for update</span></span>

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

### <span data-ttu-id="82e28-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="82e28-123">-OfferId</span></span>
<span data-ttu-id="82e28-124">Обязательное предложение Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="82e28-124">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="82e28-125">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="82e28-125">-PrivateStoreId</span></span>
<span data-ttu-id="82e28-126">Обязательные возможности Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="82e28-126">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="82e28-127">-SpecificPlanIdsLimitation</span><span class="sxs-lookup"><span data-stu-id="82e28-127">-SpecificPlanIdsLimitation</span></span>
<span data-ttu-id="82e28-128">Обязательные ограничения для идентификаторов планов для Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="82e28-128">Required Azure Marketplace privateStore offer's specific plan ids limitation</span></span>

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

### <span data-ttu-id="82e28-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82e28-129">-Confirm</span></span>
<span data-ttu-id="82e28-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="82e28-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82e28-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82e28-131">-WhatIf</span></span>
<span data-ttu-id="82e28-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="82e28-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82e28-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="82e28-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82e28-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82e28-134">CommonParameters</span></span>
<span data-ttu-id="82e28-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="82e28-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82e28-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82e28-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82e28-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="82e28-137">INPUTS</span></span>

### <span data-ttu-id="82e28-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="82e28-138">None</span></span>

## <span data-ttu-id="82e28-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="82e28-139">OUTPUTS</span></span>

### <span data-ttu-id="82e28-140">Microsoft. Azure. Commands. Marketplace. Models. PrivateStore. PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="82e28-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="82e28-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="82e28-141">NOTES</span></span>

## <span data-ttu-id="82e28-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82e28-142">RELATED LINKS</span></span>
