---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionpricesheet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionPriceSheet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionPriceSheet.md
ms.openlocfilehash: 46e38df713483b60735247c7fafe984fc5fb6d52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560987"
---
# <span data-ttu-id="8d754-101">Get-AzureRmConsumptionPriceSheet</span><span class="sxs-lookup"><span data-stu-id="8d754-101">Get-AzureRmConsumptionPriceSheet</span></span>

## <span data-ttu-id="8d754-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8d754-102">SYNOPSIS</span></span>
<span data-ttu-id="8d754-103">Получение прайс – листов для подписки.</span><span class="sxs-lookup"><span data-stu-id="8d754-103">Get price sheets of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d754-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8d754-104">SYNTAX</span></span>

```
Get-AzureRmConsumptionPriceSheet [-BillingPeriodName <String>] [-ExpandMeterDetail] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d754-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d754-105">DESCRIPTION</span></span>
<span data-ttu-id="8d754-106">Командлет **Get-AzureRmConsumptionPriceSheet** получает листы цен для подписки.</span><span class="sxs-lookup"><span data-stu-id="8d754-106">The **Get-AzureRmConsumptionPriceSheet** cmdlet gets price sheets of the subscription.</span></span>

## <span data-ttu-id="8d754-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8d754-107">EXAMPLES</span></span>

### <span data-ttu-id="8d754-108">Пример 1: получение прайс – листов</span><span class="sxs-lookup"><span data-stu-id="8d754-108">Example 1: Get price sheets</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionPriceSheet
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

### <span data-ttu-id="8d754-109">Пример 2: получение прайс – листов с развернутым MeterDetails</span><span class="sxs-lookup"><span data-stu-id="8d754-109">Example 2: Get price sheets with expand of MeterDetails</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionPriceSheet -ExpandMeterDetail
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterDetails:  MeterCategory:  Virtual Machines
                             MeterLocation:  US North Central
                             MeterName:  Compute Hours
                             MeterSubCategory:  Standard_D11_v2 VM_Promo (Windows)
                             Unit:  Hours
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

### <span data-ttu-id="8d754-110">Пример 3: получение прайс – листов для BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="8d754-110">Example 3: Get price sheets of BillingPeriodName</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionPriceSheet -BillingPeriodName 201712
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  46367D67-1E4C-4ED4-8267-4477083F581C
              PartNumber:  AAA-53590
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.37
```

### <span data-ttu-id="8d754-111">Пример 4: получение первых 5 записей прайс – листов</span><span class="sxs-lookup"><span data-stu-id="8d754-111">Example 4: Get top 5 records of price sheets</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionPriceSheet -Top 5
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

## <span data-ttu-id="8d754-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8d754-112">PARAMETERS</span></span>

### <span data-ttu-id="8d754-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="8d754-113">-BillingPeriodName</span></span>
<span data-ttu-id="8d754-114">Название определенного расчетного периода, чтобы получить прайс-листы, связанные с.</span><span class="sxs-lookup"><span data-stu-id="8d754-114">Name of a specific billing period to get the price sheets that associate with.</span></span>

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

### <span data-ttu-id="8d754-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d754-115">-DefaultProfile</span></span>
<span data-ttu-id="8d754-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d754-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d754-117">-ExpandMeterDetail</span><span class="sxs-lookup"><span data-stu-id="8d754-117">-ExpandMeterDetail</span></span>
<span data-ttu-id="8d754-118">Разворачивать прайсные листы, основываясь на MeterDetails.</span><span class="sxs-lookup"><span data-stu-id="8d754-118">Expand the price sheets based on MeterDetails.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d754-119">-Top</span><span class="sxs-lookup"><span data-stu-id="8d754-119">-Top</span></span>
<span data-ttu-id="8d754-120">Определение максимального числа возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="8d754-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="8d754-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d754-121">CommonParameters</span></span>
<span data-ttu-id="8d754-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8d754-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d754-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d754-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d754-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8d754-124">INPUTS</span></span>

### <span data-ttu-id="8d754-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="8d754-125">None</span></span>

## <span data-ttu-id="8d754-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d754-126">OUTPUTS</span></span>

### <span data-ttu-id="8d754-127">Microsoft. Azure. Commands. потребление. Models. PSPriceSheet</span><span class="sxs-lookup"><span data-stu-id="8d754-127">Microsoft.Azure.Commands.Consumption.Models.PSPriceSheet</span></span>

## <span data-ttu-id="8d754-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="8d754-128">NOTES</span></span>

## <span data-ttu-id="8d754-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d754-129">RELATED LINKS</span></span>
