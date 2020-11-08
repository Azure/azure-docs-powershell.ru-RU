---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: fd775b45504ec10855b54e9fd3a31d2abf8934e6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247320"
---
# <span data-ttu-id="dfc2f-101">Get-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="dfc2f-101">Get-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="dfc2f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dfc2f-102">SYNOPSIS</span></span>
<span data-ttu-id="dfc2f-103">Получение одного или нескольких предложений частного магазина.</span><span class="sxs-lookup"><span data-stu-id="dfc2f-103">Get one or more private store's offer.</span></span>

## <span data-ttu-id="dfc2f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dfc2f-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> [-OfferId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfc2f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfc2f-105">DESCRIPTION</span></span>
<span data-ttu-id="dfc2f-106">Получите одно или несколько предложений частного магазина с общедоступными и частными планами, которые были добавлены в область "клиент".</span><span class="sxs-lookup"><span data-stu-id="dfc2f-106">Get one or more private store's offer with public + private plans  that were added under tenant scope.</span></span> <span data-ttu-id="dfc2f-107">Если вы предоставляете идентификатор подписки, получите одно или несколько предложений частного магазина с частными планами только в соответствии с областью подписки.</span><span class="sxs-lookup"><span data-stu-id="dfc2f-107">If subscription id is presents, get one or more private store's offer with private plans only under subscription scope</span></span>
## <span data-ttu-id="dfc2f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dfc2f-108">EXAMPLES</span></span>

### <span data-ttu-id="dfc2f-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dfc2f-109">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {small, medium-with-upgraded-bandwidth, medium-with-upgraded-apps, large, large-pr, small-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers

UniqueOfferId             : publisherid1.offerid1
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "00009568-0000-0100-0000-5ec4f9590000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {azure_managedservices_professional ,azure_managedservices_professional-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid1.offerid1
Name                      : publisherid1.offerid1
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="dfc2f-110">Получите предложение частного магазина с частными и общедоступными планами, которые были добавлены в область "клиент".</span><span class="sxs-lookup"><span data-stu-id="dfc2f-110">Get private store's offers with private + public plans  that were added under tenant scope.</span></span>

### <span data-ttu-id="dfc2f-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="dfc2f-111">Example 2</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {large-pr, small-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers

UniqueOfferId             : publisherid1.offerid1
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "00009568-0000-0100-0000-5ec4f9590000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {azure_managedservices_professional-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid1.offerid1
Name                      : publisherid1.offerid1
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="dfc2f-112">Получить предложение частного магазина с частными планами, которые были добавлены в раздел область подписки.</span><span class="sxs-lookup"><span data-stu-id="dfc2f-112">Get private store's offers with private plans only that were added under subscription scope.</span></span>

### <span data-ttu-id="dfc2f-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="dfc2f-113">Example 3</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -OfferId publisherid.offerid


UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {small, medium-with-upgraded-bandwidth, medium-with-upgraded-apps, large, large-pr, small-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="dfc2f-114">Получение предложения частного магазина с частными и общедоступными планами, которые были добавлены в область "клиент".</span><span class="sxs-lookup"><span data-stu-id="dfc2f-114">Get  private store's offer with private + public plans that was been added under tenant scope.</span></span>

### <span data-ttu-id="dfc2f-115">Пример 4</span><span class="sxs-lookup"><span data-stu-id="dfc2f-115">Example 4</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -OfferId publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281


UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {large-pr, small-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="dfc2f-116">Получить предложение частного магазина с частными планами, которые были добавлены в раздел "область клиента".</span><span class="sxs-lookup"><span data-stu-id="dfc2f-116">Get private store's offer with private plans only that was been added under tenant scope.</span></span>


## <span data-ttu-id="dfc2f-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dfc2f-117">PARAMETERS</span></span>

### <span data-ttu-id="dfc2f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfc2f-118">-DefaultProfile</span></span>
<span data-ttu-id="dfc2f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dfc2f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfc2f-120">-OfferId</span><span class="sxs-lookup"><span data-stu-id="dfc2f-120">-OfferId</span></span>
<span data-ttu-id="dfc2f-121">Обязательное предложение Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="dfc2f-121">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="dfc2f-122">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="dfc2f-122">-PrivateStoreId</span></span>
<span data-ttu-id="dfc2f-123">Обязательные возможности Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="dfc2f-123">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="dfc2f-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dfc2f-124">-SubscriptionId</span></span>
<span data-ttu-id="dfc2f-125">Идентификатор подписки на Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="dfc2f-125">Azure Marketplace subscription id</span></span>

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

### <span data-ttu-id="dfc2f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfc2f-126">CommonParameters</span></span>
<span data-ttu-id="dfc2f-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dfc2f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfc2f-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfc2f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfc2f-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dfc2f-129">INPUTS</span></span>

### <span data-ttu-id="dfc2f-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="dfc2f-130">None</span></span>

## <span data-ttu-id="dfc2f-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfc2f-131">OUTPUTS</span></span>

### <span data-ttu-id="dfc2f-132">Microsoft. Azure. Commands. Marketplace. Models. PrivateStore. PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="dfc2f-132">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="dfc2f-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="dfc2f-133">NOTES</span></span>

## <span data-ttu-id="dfc2f-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dfc2f-134">RELATED LINKS</span></span>
