---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionmarketplace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionMarketplace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionMarketplace.md
ms.openlocfilehash: 0dfdec27fe53aaf40ebd46a2c623047381faa554
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509517"
---
# <span data-ttu-id="602de-101">Get-AzConsumptionMarketplace</span><span class="sxs-lookup"><span data-stu-id="602de-101">Get-AzConsumptionMarketplace</span></span>

## <span data-ttu-id="602de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="602de-102">SYNOPSIS</span></span>
<span data-ttu-id="602de-103">Получите marketplaces of the subscription.</span><span class="sxs-lookup"><span data-stu-id="602de-103">Get marketplaces of the subscription.</span></span>

## <span data-ttu-id="602de-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="602de-104">SYNTAX</span></span>

```
Get-AzConsumptionMarketplace [-BillingPeriodName <String>] [-EndDate <DateTime>] [-InstanceId <String>]
 [-InstanceName <String>] [-ResourceGroup <String>] [-StartDate <DateTime>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="602de-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="602de-105">DESCRIPTION</span></span>
<span data-ttu-id="602de-106">Для получения сбыта подписки вы получаете проектлет **Get-AzConsumptionMarketplace.**</span><span class="sxs-lookup"><span data-stu-id="602de-106">The **Get-AzConsumptionMarketplace** cmdlet gets marketplaces of the subscription.</span></span>

## <span data-ttu-id="602de-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="602de-107">EXAMPLES</span></span>

### <span data-ttu-id="602de-108">Пример 1. Использование Marketplace</span><span class="sxs-lookup"><span data-stu-id="602de-108">Example 1: Get marketplaces usage</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1/providers/Microsoft.Consumption/marketplaces/018b7291-57a5-e194-65ea-28c3f1db76aa
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  018b7291-57a5-e194-65ea-28c3f1db76aa
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2018-04-29T00:00:00Z
UsageStart:  2018-04-28T00:00:00Z
```

### <span data-ttu-id="602de-109">Пример 2. Использование marketplace с диапазоном дат</span><span class="sxs-lookup"><span data-stu-id="602de-109">Example 2: Get marketplace usage with date range</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -StartDate 2018-01-03 -EndDate 2018-01-20 -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201803-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201803-1/providers/Microsoft.Consumption/marketplaces/0ec2bd1e-1cd6-0c75-3661-eaf3f635df33
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  0ec2bd1e-1cd6-0c75-3661-eaf3f635df33
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2018-01-04T00:00:00Z
UsageStart:  2018-01-03T00:00:00Z
```

### <span data-ttu-id="602de-110">Пример 3. Использование BillingPeriodName в Marketplace</span><span class="sxs-lookup"><span data-stu-id="602de-110">Example 3: Get marketplace usage of BillingPeriodName</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -BillingPeriodName 201801-1 -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201801-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201801-1/providers/Microsoft.Consumption/marketplaces/ea82233a-9f76-7eaa-4478-42bd61cf6287
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  ea82233a-9f76-7eaa-4478-42bd61cf6287
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2017-10-29T00:00:00Z
UsageStart:  2017-10-28T00:00:00Z
```

### <span data-ttu-id="602de-111">Пример 4. Использование Marketplace с помощью фильтра InstanceName</span><span class="sxs-lookup"><span data-stu-id="602de-111">Example 4: Get marketplace usage with InstanceName filter</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -InstanceName TestVM -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1/providers/Microsoft.Consumption/marketplaces/018b7291-57a5-e194-65ea-28c3f1db76aa
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  018b7291-57a5-e194-65ea-28c3f1db76aa
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2018-04-29T00:00:00Z
UsageStart:  2018-04-28T00:00:00Z
```

## <span data-ttu-id="602de-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="602de-112">PARAMETERS</span></span>

### <span data-ttu-id="602de-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="602de-113">-BillingPeriodName</span></span>
<span data-ttu-id="602de-114">Название определенного периода вы выставления счета, чтобы получить магазин, который связывает с ним.</span><span class="sxs-lookup"><span data-stu-id="602de-114">Name of a specific billing period to get the marketplace that associate with.</span></span>

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

### <span data-ttu-id="602de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="602de-115">-DefaultProfile</span></span>
<span data-ttu-id="602de-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="602de-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="602de-117">-EndDate</span><span class="sxs-lookup"><span data-stu-id="602de-117">-EndDate</span></span>
<span data-ttu-id="602de-118">Даты окончания (в UTC) магазинов, которые нужно отфильтровать.</span><span class="sxs-lookup"><span data-stu-id="602de-118">The end date (in UTC) of the marketplaces to filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="602de-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="602de-119">-InstanceId</span></span>
<span data-ttu-id="602de-120">ИД экземпляра магазинов, которые нужно отфильтровать.</span><span class="sxs-lookup"><span data-stu-id="602de-120">The instance id of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="602de-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="602de-121">-InstanceName</span></span>
<span data-ttu-id="602de-122">Имя фильтруемого экземпляра marketplaces.</span><span class="sxs-lookup"><span data-stu-id="602de-122">The instance name of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="602de-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="602de-123">-ResourceGroup</span></span>
<span data-ttu-id="602de-124">Группа ресурсов магазинов, которые нужно отфильтровать.</span><span class="sxs-lookup"><span data-stu-id="602de-124">The resource group of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="602de-125">-StartDate</span><span class="sxs-lookup"><span data-stu-id="602de-125">-StartDate</span></span>
<span data-ttu-id="602de-126">Начальную дату (в UTC) магазинов, которые нужно отфильтровать.</span><span class="sxs-lookup"><span data-stu-id="602de-126">The start date (in UTC) of the marketplaces to filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="602de-127">-Top</span><span class="sxs-lookup"><span data-stu-id="602de-127">-Top</span></span>
<span data-ttu-id="602de-128">Определите максимальное количество возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="602de-128">Determine the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="602de-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="602de-129">CommonParameters</span></span>
<span data-ttu-id="602de-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="602de-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="602de-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="602de-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="602de-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="602de-132">INPUTS</span></span>

### <span data-ttu-id="602de-133">Нет</span><span class="sxs-lookup"><span data-stu-id="602de-133">None</span></span>

## <span data-ttu-id="602de-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="602de-134">OUTPUTS</span></span>

### <span data-ttu-id="602de-135">Microsoft.Azure.Commands.Consumption.Models.PSMarketplace</span><span class="sxs-lookup"><span data-stu-id="602de-135">Microsoft.Azure.Commands.Consumption.Models.PSMarketplace</span></span>

## <span data-ttu-id="602de-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="602de-136">NOTES</span></span>

## <span data-ttu-id="602de-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="602de-137">RELATED LINKS</span></span>
