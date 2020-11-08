---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 39bbdf61a5068ea32f1febf66249213264235dfc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243151"
---
# <span data-ttu-id="39ef4-101">New-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="39ef4-101">New-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="39ef4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="39ef4-102">SYNOPSIS</span></span>
<span data-ttu-id="39ef4-103">Создайте или обновите набор эталонных данных в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="39ef4-103">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="39ef4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="39ef4-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -KeyProperty <IReferenceDataSetKeyProperty[]> -Location <String> [-SubscriptionId <String>]
 [-DataStringComparisonBehavior <DataStringComparisonBehavior>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="39ef4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39ef4-105">DESCRIPTION</span></span>
<span data-ttu-id="39ef4-106">Создайте или обновите набор эталонных данных в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="39ef4-106">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="39ef4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="39ef4-107">EXAMPLES</span></span>

### <span data-ttu-id="39ef4-108">Пример 1: Создание наборов эталонных данных для указанной среды</span><span class="sxs-lookup"><span data-stu-id="39ef4-108">Example 1: Create a reference data set for a specified environment</span></span>  
```powershell
PS C:\> $mykeyproperties = @{ "name" = "device01"; "type" = "Double"}
PS C:\> New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Location eastus -DataStringComparisonBehavior Ordinal -KeyProperty $mykeyproperties

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="39ef4-109">Эта команда создает набор эталонных данных для конкретной среды.</span><span class="sxs-lookup"><span data-stu-id="39ef4-109">This command creates a reference data set for a specific environment.</span></span>

## <span data-ttu-id="39ef4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="39ef4-110">PARAMETERS</span></span>

### <span data-ttu-id="39ef4-111">-DataStringComparisonBehavior</span><span class="sxs-lookup"><span data-stu-id="39ef4-111">-DataStringComparisonBehavior</span></span>
<span data-ttu-id="39ef4-112">Поведение сравнения ключа эталонных данных можно установить с помощью этого свойства.</span><span class="sxs-lookup"><span data-stu-id="39ef4-112">The reference data set key comparison behavior can be set using this property.</span></span>
<span data-ttu-id="39ef4-113">По умолчанию значением является порядковый номер — это означает, что сравнение ключей с учетом регистра выполняется при присоединении ссылочных данных к событиям или при добавлении новых справочных данных.</span><span class="sxs-lookup"><span data-stu-id="39ef4-113">By default, the value is 'Ordinal' - which means case sensitive key comparison will be performed while joining reference data with events or while adding new reference data.</span></span>
<span data-ttu-id="39ef4-114">Если задано значение "OrdinalIgnoreCase", будет использоваться сравнение без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="39ef4-114">When 'OrdinalIgnoreCase' is set, case insensitive comparison will be used.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.DataStringComparisonBehavior
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39ef4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39ef4-115">-DefaultProfile</span></span>
<span data-ttu-id="39ef4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39ef4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39ef4-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="39ef4-117">-EnvironmentName</span></span>
<span data-ttu-id="39ef4-118">Название среды "анализ временной последовательности", связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="39ef4-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="39ef4-119">-KeyProperty</span><span class="sxs-lookup"><span data-stu-id="39ef4-119">-KeyProperty</span></span>
<span data-ttu-id="39ef4-120">Список ключевых свойств для набора эталонных данных.</span><span class="sxs-lookup"><span data-stu-id="39ef4-120">The list of key properties for the reference data set.</span></span>
<span data-ttu-id="39ef4-121">Для конструирования ознакомьтесь с разделом "Заметки" для свойств KEYPROPERTY и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="39ef4-121">To construct, see NOTES section for KEYPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetKeyProperty[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39ef4-122">-Location</span><span class="sxs-lookup"><span data-stu-id="39ef4-122">-Location</span></span>
<span data-ttu-id="39ef4-123">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="39ef4-123">The location of the resource.</span></span>

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

### <span data-ttu-id="39ef4-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="39ef4-124">-Name</span></span>
<span data-ttu-id="39ef4-125">Имя набора эталонных данных.</span><span class="sxs-lookup"><span data-stu-id="39ef4-125">Name of the reference data set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39ef4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39ef4-126">-ResourceGroupName</span></span>
<span data-ttu-id="39ef4-127">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="39ef4-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="39ef4-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39ef4-128">-SubscriptionId</span></span>
<span data-ttu-id="39ef4-129">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="39ef4-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39ef4-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="39ef4-130">-Tag</span></span>
<span data-ttu-id="39ef4-131">Пары "ключ-значение" дополнительных свойств ресурса.</span><span class="sxs-lookup"><span data-stu-id="39ef4-131">Key-value pairs of additional properties for the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39ef4-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39ef4-132">-Confirm</span></span>
<span data-ttu-id="39ef4-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="39ef4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39ef4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39ef4-134">-WhatIf</span></span>
<span data-ttu-id="39ef4-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="39ef4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39ef4-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="39ef4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39ef4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39ef4-137">CommonParameters</span></span>
<span data-ttu-id="39ef4-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="39ef4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39ef4-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39ef4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39ef4-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="39ef4-140">INPUTS</span></span>

## <span data-ttu-id="39ef4-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="39ef4-141">OUTPUTS</span></span>

### <span data-ttu-id="39ef4-142">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. Api20200515. IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="39ef4-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="39ef4-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="39ef4-143">NOTES</span></span>

<span data-ttu-id="39ef4-144">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="39ef4-144">ALIASES</span></span>

<span data-ttu-id="39ef4-145">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="39ef4-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="39ef4-146">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="39ef4-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="39ef4-147">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="39ef4-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="39ef4-148">KEYPROPERTY <IReferenceDataSetKeyProperty [] >: список ключевых свойств для набора эталонных данных.</span><span class="sxs-lookup"><span data-stu-id="39ef4-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: The list of key properties for the reference data set.</span></span>
  - <span data-ttu-id="39ef4-149">`[Name <String>]`: Имя свойства ключа.</span><span class="sxs-lookup"><span data-stu-id="39ef4-149">`[Name <String>]`: The name of the key property.</span></span>
  - <span data-ttu-id="39ef4-150">`[Type <ReferenceDataKeyPropertyType?>]`: Тип свойства Key.</span><span class="sxs-lookup"><span data-stu-id="39ef4-150">`[Type <ReferenceDataKeyPropertyType?>]`: The type of the key property.</span></span>

## <span data-ttu-id="39ef4-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39ef4-151">RELATED LINKS</span></span>

