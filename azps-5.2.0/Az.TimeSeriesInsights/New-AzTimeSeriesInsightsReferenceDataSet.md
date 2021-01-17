---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 39bbdf61a5068ea32f1febf66249213264235dfc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417332"
---
# <span data-ttu-id="f728e-101">New-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="f728e-101">New-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="f728e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f728e-102">SYNOPSIS</span></span>
<span data-ttu-id="f728e-103">Создание или обновление набора справочных данных в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="f728e-103">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="f728e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f728e-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -KeyProperty <IReferenceDataSetKeyProperty[]> -Location <String> [-SubscriptionId <String>]
 [-DataStringComparisonBehavior <DataStringComparisonBehavior>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f728e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f728e-105">DESCRIPTION</span></span>
<span data-ttu-id="f728e-106">Создание или обновление набора справочных данных в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="f728e-106">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="f728e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f728e-107">EXAMPLES</span></span>

### <span data-ttu-id="f728e-108">Пример 1. Создание набора справочных данных для указанной среды</span><span class="sxs-lookup"><span data-stu-id="f728e-108">Example 1: Create a reference data set for a specified environment</span></span>  
```powershell
PS C:\> $mykeyproperties = @{ "name" = "device01"; "type" = "Double"}
PS C:\> New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Location eastus -DataStringComparisonBehavior Ordinal -KeyProperty $mykeyproperties

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="f728e-109">Эта команда создает набор справочных данных для конкретной среды.</span><span class="sxs-lookup"><span data-stu-id="f728e-109">This command creates a reference data set for a specific environment.</span></span>

## <span data-ttu-id="f728e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f728e-110">PARAMETERS</span></span>

### <span data-ttu-id="f728e-111">-DataStringComparisonBehavior</span><span class="sxs-lookup"><span data-stu-id="f728e-111">-DataStringComparisonBehavior</span></span>
<span data-ttu-id="f728e-112">С помощью этого свойства можно настроить поведение для сравнения набора справочных данных.</span><span class="sxs-lookup"><span data-stu-id="f728e-112">The reference data set key comparison behavior can be set using this property.</span></span>
<span data-ttu-id="f728e-113">По умолчанию это значение имеет значение "Ordinal", то есть при объединении справочных данных с событиями или при добавлении новых справочных данных выполняется сравнение с клавишей с клавишей case.</span><span class="sxs-lookup"><span data-stu-id="f728e-113">By default, the value is 'Ordinal' - which means case sensitive key comparison will be performed while joining reference data with events or while adding new reference data.</span></span>
<span data-ttu-id="f728e-114">Если за установлено сравнение OrdinalIgnoreCase, будет использоваться сравнение без регистра.</span><span class="sxs-lookup"><span data-stu-id="f728e-114">When 'OrdinalIgnoreCase' is set, case insensitive comparison will be used.</span></span>

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

### <span data-ttu-id="f728e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f728e-115">-DefaultProfile</span></span>
<span data-ttu-id="f728e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f728e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f728e-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="f728e-117">-EnvironmentName</span></span>
<span data-ttu-id="f728e-118">Имя среды Time Series Insights, связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f728e-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="f728e-119">-KeyProperty</span><span class="sxs-lookup"><span data-stu-id="f728e-119">-KeyProperty</span></span>
<span data-ttu-id="f728e-120">Список ключевых свойств для набора справочных данных.</span><span class="sxs-lookup"><span data-stu-id="f728e-120">The list of key properties for the reference data set.</span></span>
<span data-ttu-id="f728e-121">Чтобы построить новую таблицу, см. раздел "ПРИМЕЧАНИЯ" для свойств KEYPROPERTY и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="f728e-121">To construct, see NOTES section for KEYPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="f728e-122">-Location</span><span class="sxs-lookup"><span data-stu-id="f728e-122">-Location</span></span>
<span data-ttu-id="f728e-123">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="f728e-123">The location of the resource.</span></span>

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

### <span data-ttu-id="f728e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f728e-124">-Name</span></span>
<span data-ttu-id="f728e-125">Имя набора справочных данных.</span><span class="sxs-lookup"><span data-stu-id="f728e-125">Name of the reference data set.</span></span>

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

### <span data-ttu-id="f728e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f728e-126">-ResourceGroupName</span></span>
<span data-ttu-id="f728e-127">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f728e-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="f728e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f728e-128">-SubscriptionId</span></span>
<span data-ttu-id="f728e-129">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="f728e-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="f728e-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="f728e-130">-Tag</span></span>
<span data-ttu-id="f728e-131">Пары ключевых значений дополнительных свойств для ресурса.</span><span class="sxs-lookup"><span data-stu-id="f728e-131">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="f728e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f728e-132">-Confirm</span></span>
<span data-ttu-id="f728e-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f728e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f728e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f728e-134">-WhatIf</span></span>
<span data-ttu-id="f728e-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f728e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f728e-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f728e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f728e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f728e-137">CommonParameters</span></span>
<span data-ttu-id="f728e-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f728e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f728e-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f728e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f728e-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f728e-140">INPUTS</span></span>

## <span data-ttu-id="f728e-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f728e-141">OUTPUTS</span></span>

### <span data-ttu-id="f728e-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="f728e-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="f728e-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f728e-143">NOTES</span></span>

<span data-ttu-id="f728e-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f728e-144">ALIASES</span></span>

<span data-ttu-id="f728e-145">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="f728e-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f728e-146">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="f728e-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f728e-147">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f728e-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f728e-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: список ключевых свойств для набора справочных данных.</span><span class="sxs-lookup"><span data-stu-id="f728e-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: The list of key properties for the reference data set.</span></span>
  - <span data-ttu-id="f728e-149">`[Name <String>]`: Имя свойства ключа.</span><span class="sxs-lookup"><span data-stu-id="f728e-149">`[Name <String>]`: The name of the key property.</span></span>
  - <span data-ttu-id="f728e-150">`[Type <ReferenceDataKeyPropertyType?>]`: Тип свойства ключа.</span><span class="sxs-lookup"><span data-stu-id="f728e-150">`[Type <ReferenceDataKeyPropertyType?>]`: The type of the key property.</span></span>

## <span data-ttu-id="f728e-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f728e-151">RELATED LINKS</span></span>

