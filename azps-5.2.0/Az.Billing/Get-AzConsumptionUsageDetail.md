---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionusagedetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionUsageDetail.md
ms.openlocfilehash: 8eeee753fda32f40dfabf156b352724b0bd87b92
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394951"
---
# <span data-ttu-id="79eec-101">Get-AzConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="79eec-101">Get-AzConsumptionUsageDetail</span></span>

## <span data-ttu-id="79eec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79eec-102">SYNOPSIS</span></span>
<span data-ttu-id="79eec-103">Получите сведения об использовании подписки.</span><span class="sxs-lookup"><span data-stu-id="79eec-103">Get usage details of the subscription.</span></span>

## <span data-ttu-id="79eec-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="79eec-104">SYNTAX</span></span>

```
Get-AzConsumptionUsageDetail [-BillingPeriodName <String>] [-Expand <String>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>] [-ResourceGroup <String>]
 [-InstanceName <String>] [-InstanceId <String>] [-Tag <String>] [-MaxCount <Int32>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79eec-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79eec-105">DESCRIPTION</span></span>
<span data-ttu-id="79eec-106">Подробные сведения об использовании подписки получает **cmdlet Get-AzConsumptionUsageDetail.**</span><span class="sxs-lookup"><span data-stu-id="79eec-106">The **Get-AzConsumptionUsageDetail** cmdlet gets usage details of the subscription.</span></span> 

## <span data-ttu-id="79eec-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="79eec-107">EXAMPLES</span></span>

### <span data-ttu-id="79eec-108">Пример 1. Подробные сведения об использовании с помощью расширения сведений о лимитных данных</span><span class="sxs-lookup"><span data-stu-id="79eec-108">Example 1: Get usage details with expand of MeterDetails</span></span>
```powershell
PS C:\> Get-AzConsumptionUsageDetail -Expand MeterDetails -Top 10
AccountName:  AAAA
BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
ConsumedService:  Microsoft.Compute
CostCenter:  XYZ987
Currency:  USD
DepartmentName:  Ama
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/usageDetails/24b9dff0-f022-55a1-886b-17b330000db3
InstanceId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/MAR-CCM/providers/Microsoft.Compute/disks/mar-ccm-vm01_OsDisk_1_d0beead4b6ff4b4088a687701d355d61
InstanceLocation:  usnorthcentral
InstanceName:  mar-ccm-vm01_OsDisk_1_d0beead4b6ff4b4088a687701d355d61
IsEstimated:  true
MeterDetails:  MeterCategory:  Data Management
               MeterLocation:  usnorthcentral
               MeterName:  Standard Managed Disk Operations (in 10,000s)
               MeterSubCategory:  Data Management
               Unit:  Operations
MeterId:  82cd70ab-1aee-4b30-bc04-8b71e1204dbc
Name:  24b9dff0-f022-55a1-886b-17b330000db3
PretaxCost:  0
Product:  Data Management Standard Managed Disk Operations
SubscriptionGuid:  1caaa5a3-2b66-438e-8ab4-bce37d518c5d
SubscriptionName:  CCM - Microsoft Azure Enterprise - 1
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  6/1/2018 11:59:59 PM
UsageQuantity:  3.8218
UsageStart:  6/1/2018 12:00:00 AM
```

### <span data-ttu-id="79eec-109">Пример 2. Подробные сведения об использовании с диапазоном дат</span><span class="sxs-lookup"><span data-stu-id="79eec-109">Example 2: Get usage details with date range</span></span>
```powershell
PS C:\> Get-AzConsumptionUsageDetail -StartDate 2017-10-02 -EndDate 2017-10-05 -Top 10
AccountName:  AAAA
BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001
ConsumedService:  Storage
CostCenter:  XYZ987
Currency:  USD
DepartmentName:  Ama
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001/providers/Microsoft.Consumption/usageDetails/732582e5-40ad-bb23-7a69-ca1ff7c8b004
InstanceId:  storsimplezc9q6r2t7f
InstanceLocation:  US West Central
InstanceName:  storsimplezc9q6r2t7f
IsEstimated:  false
MeterId:  ad22fac8-9da5-4577-8683-56ae94d39e42
Name:  732582e5-40ad-bb23-7a69-ca1ff7c8b004
PretaxCost:  0
Product:  Data Management Geo Redundant Standard IO - Table Write
SubscriptionGuid:  1caaa5a3-2b66-438e-8ab4-bce37d518c5d
SubscriptionName:  CCM - Microsoft Azure Enterprise - 1
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  10/2/2017 11:59:59 PM
UsageQuantity:  0.0006
UsageStart:  10/2/2017 12:00:00 AM
```

### <span data-ttu-id="79eec-110">Пример 3. Получите сведения об использовании BillingPeriodName с помощью фильтра InstanceName</span><span class="sxs-lookup"><span data-stu-id="79eec-110">Example 3: Get usage details of BillingPeriodName with InstanceName filter</span></span>
```powershell
PS C:\> Get-AzConsumptionUsageDetail -BillingPeriodName 201710 -InstanceName 1c2052westus -Top 10
AccountName:  AAAA
BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001
ConsumedService:  Microsoft.Storage
CostCenter:  XYZ987
Currency:  USD
DepartmentName:  Ama
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001/providers/Microsoft.Consumption/usageDetails/8abc8b65-e8f1-31e1-f02b-058a7572363f
InstanceId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/securitydata/providers/Microsoft.Storage/storageAccounts/1c2052westus
InstanceLocation:  uswest
InstanceName:  1c2052westus
IsEstimated:  false
MeterId:  9995d93a-7d35-4d3f-9c69-7a7fea447ef4
Name:  8abc8b65-e8f1-31e1-f02b-058a7572363f
PretaxCost:  0.000000693016692
Product:  Data Transfer Out - Zone 1
SubscriptionGuid:  1caaa5a3-2b66-438e-8ab4-bce37d518c5d
SubscriptionName:  CCM - Microsoft Azure Enterprise - 1
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  10/1/2017 11:59:59 PM
UsageQuantity:  0.000009
UsageStart:  10/1/2017 12:00:00 AM
```

## <span data-ttu-id="79eec-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79eec-111">PARAMETERS</span></span>

### <span data-ttu-id="79eec-112">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="79eec-112">-BillingPeriodName</span></span>
<span data-ttu-id="79eec-113">Название определенного периода вы выставления счета для получения сведений об использовании, которые с ним связываются.</span><span class="sxs-lookup"><span data-stu-id="79eec-113">Name of a specific billing period to get the usage details that associate with.</span></span>

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

### <span data-ttu-id="79eec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79eec-114">-DefaultProfile</span></span>
<span data-ttu-id="79eec-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79eec-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79eec-116">-EndDate</span><span class="sxs-lookup"><span data-stu-id="79eec-116">-EndDate</span></span>
<span data-ttu-id="79eec-117">Дата окончания фильтруемой информации (в UTC).</span><span class="sxs-lookup"><span data-stu-id="79eec-117">The end date (in UTC) of the usages to filter.</span></span>

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

### <span data-ttu-id="79eec-118">-Развернуть</span><span class="sxs-lookup"><span data-stu-id="79eec-118">-Expand</span></span>
<span data-ttu-id="79eec-119">Развяжите список использования на основе meterDetails или AdditionalInfo.</span><span class="sxs-lookup"><span data-stu-id="79eec-119">Expand the usages based on MeterDetails, or AdditionalInfo.</span></span>

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

### <span data-ttu-id="79eec-120">-IncludeAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="79eec-120">-IncludeAdditionalProperties</span></span>
<span data-ttu-id="79eec-121">Включить дополнительные свойства в использование.</span><span class="sxs-lookup"><span data-stu-id="79eec-121">Include additional properties in the usages.</span></span>

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

### <span data-ttu-id="79eec-122">-IncludeMeterDetails</span><span class="sxs-lookup"><span data-stu-id="79eec-122">-IncludeMeterDetails</span></span>
<span data-ttu-id="79eec-123">Включить сведения о метре в использование.</span><span class="sxs-lookup"><span data-stu-id="79eec-123">Include meter details in the usages.</span></span>

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

### <span data-ttu-id="79eec-124">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="79eec-124">-InstanceId</span></span>
<span data-ttu-id="79eec-125">ИД экземпляра фильтруемого пользования.</span><span class="sxs-lookup"><span data-stu-id="79eec-125">The instance id of the usages to filter.</span></span>

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

### <span data-ttu-id="79eec-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="79eec-126">-InstanceName</span></span>
<span data-ttu-id="79eec-127">Имя фильтруемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="79eec-127">The instance name of the usages to filter.</span></span>

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

### <span data-ttu-id="79eec-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="79eec-128">-MaxCount</span></span>
<span data-ttu-id="79eec-129">Определите максимальное количество возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="79eec-129">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="79eec-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="79eec-130">-ResourceGroup</span></span>
<span data-ttu-id="79eec-131">Группа ресурсов, в которые нужно отфильтровать данные.</span><span class="sxs-lookup"><span data-stu-id="79eec-131">The resource group of the usages to filter.</span></span>

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

### <span data-ttu-id="79eec-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="79eec-132">-StartDate</span></span>
<span data-ttu-id="79eec-133">Дата начала фильтруемой информации (в UTC).</span><span class="sxs-lookup"><span data-stu-id="79eec-133">The start date (in UTC) of the usages to filter.</span></span>

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

### <span data-ttu-id="79eec-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="79eec-134">-Tag</span></span>
<span data-ttu-id="79eec-135">Тег фильтруемого использования.</span><span class="sxs-lookup"><span data-stu-id="79eec-135">The tag of the usages to filter.</span></span>

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

### <span data-ttu-id="79eec-136">-Top</span><span class="sxs-lookup"><span data-stu-id="79eec-136">-Top</span></span>
<span data-ttu-id="79eec-137">Определите максимальное количество возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="79eec-137">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="79eec-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79eec-138">CommonParameters</span></span>
<span data-ttu-id="79eec-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79eec-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79eec-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79eec-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79eec-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79eec-141">INPUTS</span></span>

### <span data-ttu-id="79eec-142">Нет</span><span class="sxs-lookup"><span data-stu-id="79eec-142">None</span></span>

## <span data-ttu-id="79eec-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="79eec-143">OUTPUTS</span></span>

### <span data-ttu-id="79eec-144">Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail</span><span class="sxs-lookup"><span data-stu-id="79eec-144">Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail</span></span>

## <span data-ttu-id="79eec-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="79eec-145">NOTES</span></span>

## <span data-ttu-id="79eec-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79eec-146">RELATED LINKS</span></span>
