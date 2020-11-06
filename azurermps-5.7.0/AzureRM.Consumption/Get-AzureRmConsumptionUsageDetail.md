---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionusagedetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
ms.openlocfilehash: 2694ce516b1bb3202fc194e1c1eec55610f7b92a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557460"
---
# <span data-ttu-id="e6a21-101">Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="e6a21-101">Get-AzureRmConsumptionUsageDetail</span></span>

## <span data-ttu-id="e6a21-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6a21-102">SYNOPSIS</span></span>
<span data-ttu-id="e6a21-103">Получение сведений об использовании подписки.</span><span class="sxs-lookup"><span data-stu-id="e6a21-103">Get usage details of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6a21-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6a21-104">SYNTAX</span></span>

### <span data-ttu-id="e6a21-105">Подписка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e6a21-105">Subscription (Default)</span></span>
```
Get-AzureRmConsumptionUsageDetail [-MaxCount <Int32>] [-IncludeMeterDetails] [-IncludeAdditionalProperties]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6a21-106">Фактур</span><span class="sxs-lookup"><span data-stu-id="e6a21-106">Invoice</span></span>
```
Get-AzureRmConsumptionUsageDetail -InvoiceName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6a21-107">BillingPeriod</span><span class="sxs-lookup"><span data-stu-id="e6a21-107">BillingPeriod</span></span>
```
Get-AzureRmConsumptionUsageDetail -BillingPeriodName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6a21-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6a21-108">DESCRIPTION</span></span>
<span data-ttu-id="e6a21-109">Командлет **Get-AzureRmConsumptionUsageDetail** получает сведения об использовании подписки.</span><span class="sxs-lookup"><span data-stu-id="e6a21-109">The **Get-AzureRmConsumptionUsageDetail** cmdlet gets usage details of the subscription.</span></span> 

## <span data-ttu-id="e6a21-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6a21-110">EXAMPLES</span></span>

### <span data-ttu-id="e6a21-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e6a21-111">Example 1</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeMeterDetails -InvoiceName 201704-117283130069214
```

<span data-ttu-id="e6a21-112">Получить сведения об использовании счета с указанным именем и включить в результат свойство MeterDetails.</span><span class="sxs-lookup"><span data-stu-id="e6a21-112">Get usage details of the invoice with specified name, and include MeterDetails property in the result.</span></span>

### <span data-ttu-id="e6a21-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e6a21-113">Example 2</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeAdditionalProperties -BillingPeriodName 201704-1
```

<span data-ttu-id="e6a21-114">Получить сведения об использовании расчетного периода с указанным именем и включить в результат свойство AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="e6a21-114">Get usage details of the billing period with specified name, and include AdditionalProperties property in the result.</span></span>

### <span data-ttu-id="e6a21-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e6a21-115">Example 3</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -StartDate 2017-01-17 -EndDate 2017-01-19
```

<span data-ttu-id="e6a21-116">Получение сведений об использовании подписки, которая находится между 2017-01-17 и 2017-01-19.</span><span class="sxs-lookup"><span data-stu-id="e6a21-116">Get usage details of the subscription that is between 2017-01-17 to 2017-01-19.</span></span>

## <span data-ttu-id="e6a21-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6a21-117">PARAMETERS</span></span>

### <span data-ttu-id="e6a21-118">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="e6a21-118">-BillingPeriodName</span></span>
<span data-ttu-id="e6a21-119">Название определенного расчетного периода, чтобы получить сведения об использовании, связанные с.</span><span class="sxs-lookup"><span data-stu-id="e6a21-119">Name of a specific billing period to get the usage details that associate with.</span></span>

```yaml
Type: String
Parameter Sets: BillingPeriod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6a21-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6a21-120">-DefaultProfile</span></span>
<span data-ttu-id="e6a21-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e6a21-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6a21-122">-EndDate</span><span class="sxs-lookup"><span data-stu-id="e6a21-122">-EndDate</span></span>
<span data-ttu-id="e6a21-123">Дата окончания использования (в формате UTC).</span><span class="sxs-lookup"><span data-stu-id="e6a21-123">The end date (in UTC) of the usages.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6a21-124">-IncludeAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="e6a21-124">-IncludeAdditionalProperties</span></span>
<span data-ttu-id="e6a21-125">Включите в использование дополнительные свойства.</span><span class="sxs-lookup"><span data-stu-id="e6a21-125">Include additional properties in the usages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6a21-126">-IncludeMeterDetails</span><span class="sxs-lookup"><span data-stu-id="e6a21-126">-IncludeMeterDetails</span></span>
<span data-ttu-id="e6a21-127">Включите в использование сведения о измерительных измерителях.</span><span class="sxs-lookup"><span data-stu-id="e6a21-127">Include meter details in the usages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6a21-128">-InvoiceName</span><span class="sxs-lookup"><span data-stu-id="e6a21-128">-InvoiceName</span></span>
<span data-ttu-id="e6a21-129">Название определенного счета, чтобы получить сведения об использовании, связанные с.</span><span class="sxs-lookup"><span data-stu-id="e6a21-129">Name of a specific invoice to get the usage details that associate with.</span></span>

```yaml
Type: String
Parameter Sets: Invoice
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6a21-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e6a21-130">-MaxCount</span></span>
<span data-ttu-id="e6a21-131">Определение максимального числа возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="e6a21-131">Determine the maximum number of records to return.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6a21-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="e6a21-132">-StartDate</span></span>
<span data-ttu-id="e6a21-133">Дата начала использования (в формате UTC).</span><span class="sxs-lookup"><span data-stu-id="e6a21-133">The start date (in UTC) of the usages.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6a21-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6a21-134">CommonParameters</span></span>
<span data-ttu-id="e6a21-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6a21-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6a21-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6a21-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6a21-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6a21-137">INPUTS</span></span>

### <span data-ttu-id="e6a21-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="e6a21-138">None</span></span>

## <span data-ttu-id="e6a21-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6a21-139">OUTPUTS</span></span>

### <span data-ttu-id="e6a21-140">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. потребление. Models. PSUsageDetail, Microsoft. Azure. Commands. потребление, версия = 0.1.0.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="e6a21-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail, Microsoft.Azure.Commands.Consumption, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e6a21-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6a21-141">NOTES</span></span>

## <span data-ttu-id="e6a21-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6a21-142">RELATED LINKS</span></span>

