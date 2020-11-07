---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionmarketplace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionMarketplace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionMarketplace.md
ms.openlocfilehash: 4533ed3c522cbd1633184b86de68288a3c8dd1ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901493"
---
# <span data-ttu-id="1d254-101">Get-AzConsumptionMarketplace</span><span class="sxs-lookup"><span data-stu-id="1d254-101">Get-AzConsumptionMarketplace</span></span>

## <span data-ttu-id="1d254-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1d254-102">SYNOPSIS</span></span>
<span data-ttu-id="1d254-103">Получение рынка для подписки.</span><span class="sxs-lookup"><span data-stu-id="1d254-103">Get marketplaces of the subscription.</span></span>

## <span data-ttu-id="1d254-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1d254-104">SYNTAX</span></span>

```
Get-AzConsumptionMarketplace [-BillingPeriodName <String>] [-EndDate <DateTime>] [-InstanceId <String>]
 [-InstanceName <String>] [-ResourceGroup <String>] [-StartDate <DateTime>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d254-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d254-105">DESCRIPTION</span></span>
<span data-ttu-id="1d254-106">Командлет **Get-AzConsumptionMarketplace** возвращает Marketplaces для подписки.</span><span class="sxs-lookup"><span data-stu-id="1d254-106">The **Get-AzConsumptionMarketplace** cmdlet gets marketplaces of the subscription.</span></span>

## <span data-ttu-id="1d254-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1d254-107">EXAMPLES</span></span>

### <span data-ttu-id="1d254-108">Пример 1: получение сведений об рынках</span><span class="sxs-lookup"><span data-stu-id="1d254-108">Example 1: Get marketplaces usage</span></span>
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

### <span data-ttu-id="1d254-109">Пример 2: получение сведений об использовании Marketplace с диапазоном дат</span><span class="sxs-lookup"><span data-stu-id="1d254-109">Example 2: Get marketplace usage with date range</span></span>
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

### <span data-ttu-id="1d254-110">Пример 3: получение сведений об использовании BillingPeriodName на рынке</span><span class="sxs-lookup"><span data-stu-id="1d254-110">Example 3: Get marketplace usage of BillingPeriodName</span></span>
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

### <span data-ttu-id="1d254-111">Пример 4: получение сведений об использовании Marketplace с фильтром InstanceName</span><span class="sxs-lookup"><span data-stu-id="1d254-111">Example 4: Get marketplace usage with InstanceName filter</span></span>
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

## <span data-ttu-id="1d254-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1d254-112">PARAMETERS</span></span>

### <span data-ttu-id="1d254-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="1d254-113">-BillingPeriodName</span></span>
<span data-ttu-id="1d254-114">Название определенного расчетного периода, который нужно связать с магазином рынка.</span><span class="sxs-lookup"><span data-stu-id="1d254-114">Name of a specific billing period to get the marketplace that associate with.</span></span>

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

### <span data-ttu-id="1d254-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d254-115">-DefaultProfile</span></span>
<span data-ttu-id="1d254-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1d254-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d254-117">-EndDate</span><span class="sxs-lookup"><span data-stu-id="1d254-117">-EndDate</span></span>
<span data-ttu-id="1d254-118">Конечная дата (в формате UTC) Marketplaces для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="1d254-118">The end date (in UTC) of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="1d254-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="1d254-119">-InstanceId</span></span>
<span data-ttu-id="1d254-120">Идентификатор экземпляра Marketplaces для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="1d254-120">The instance id of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="1d254-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="1d254-121">-InstanceName</span></span>
<span data-ttu-id="1d254-122">Имя экземпляра Marketplaces для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="1d254-122">The instance name of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="1d254-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1d254-123">-ResourceGroup</span></span>
<span data-ttu-id="1d254-124">Группа ресурсов для "рынки", которые нужно отфильтровать.</span><span class="sxs-lookup"><span data-stu-id="1d254-124">The resource group of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="1d254-125">-StartDate</span><span class="sxs-lookup"><span data-stu-id="1d254-125">-StartDate</span></span>
<span data-ttu-id="1d254-126">Начальная дата (в формате UTC) партнеров, которые нужно отфильтровать.</span><span class="sxs-lookup"><span data-stu-id="1d254-126">The start date (in UTC) of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="1d254-127">-Top</span><span class="sxs-lookup"><span data-stu-id="1d254-127">-Top</span></span>
<span data-ttu-id="1d254-128">Определение максимального числа возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="1d254-128">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="1d254-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d254-129">CommonParameters</span></span>
<span data-ttu-id="1d254-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1d254-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d254-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d254-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d254-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1d254-132">INPUTS</span></span>

### <span data-ttu-id="1d254-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="1d254-133">None</span></span>

## <span data-ttu-id="1d254-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d254-134">OUTPUTS</span></span>

### <span data-ttu-id="1d254-135">Microsoft. Azure. Commands. потребление. Models. PSMarketplace</span><span class="sxs-lookup"><span data-stu-id="1d254-135">Microsoft.Azure.Commands.Consumption.Models.PSMarketplace</span></span>

## <span data-ttu-id="1d254-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="1d254-136">NOTES</span></span>

## <span data-ttu-id="1d254-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d254-137">RELATED LINKS</span></span>
