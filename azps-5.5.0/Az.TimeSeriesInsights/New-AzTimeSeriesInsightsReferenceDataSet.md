---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 39bbdf61a5068ea32f1febf66249213264235dfc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224617"
---
# <span data-ttu-id="bd95f-101">New-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="bd95f-101">New-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="bd95f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd95f-102">SYNOPSIS</span></span>
<span data-ttu-id="bd95f-103">Создание или обновление набора справочных данных в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="bd95f-103">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="bd95f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bd95f-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -KeyProperty <IReferenceDataSetKeyProperty[]> -Location <String> [-SubscriptionId <String>]
 [-DataStringComparisonBehavior <DataStringComparisonBehavior>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bd95f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd95f-105">DESCRIPTION</span></span>
<span data-ttu-id="bd95f-106">Создание или обновление набора справочных данных в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="bd95f-106">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="bd95f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bd95f-107">EXAMPLES</span></span>

### <span data-ttu-id="bd95f-108">Пример 1. Создание набора справочных данных для указанной среды</span><span class="sxs-lookup"><span data-stu-id="bd95f-108">Example 1: Create a reference data set for a specified environment</span></span>  
```powershell
PS C:\> $mykeyproperties = @{ "name" = "device01"; "type" = "Double"}
PS C:\> New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Location eastus -DataStringComparisonBehavior Ordinal -KeyProperty $mykeyproperties

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="bd95f-109">Эта команда создает набор справочных данных для конкретной среды.</span><span class="sxs-lookup"><span data-stu-id="bd95f-109">This command creates a reference data set for a specific environment.</span></span>

## <span data-ttu-id="bd95f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd95f-110">PARAMETERS</span></span>

### <span data-ttu-id="bd95f-111">-DataStringComparisonBehavior</span><span class="sxs-lookup"><span data-stu-id="bd95f-111">-DataStringComparisonBehavior</span></span>
<span data-ttu-id="bd95f-112">С помощью этого свойства можно настроить поведение при сравнении ключа набора справочных данных.</span><span class="sxs-lookup"><span data-stu-id="bd95f-112">The reference data set key comparison behavior can be set using this property.</span></span>
<span data-ttu-id="bd95f-113">По умолчанию это значение имеет значение "Ordinal", то есть при объединении справочных данных с событиями или при добавлении новых справочных данных выполняется сравнение с клавишей с клавишей case.</span><span class="sxs-lookup"><span data-stu-id="bd95f-113">By default, the value is 'Ordinal' - which means case sensitive key comparison will be performed while joining reference data with events or while adding new reference data.</span></span>
<span data-ttu-id="bd95f-114">Если за установлено сравнение OrdinalIgnoreCase, будет использоваться сравнение без регистра.</span><span class="sxs-lookup"><span data-stu-id="bd95f-114">When 'OrdinalIgnoreCase' is set, case insensitive comparison will be used.</span></span>

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

### <span data-ttu-id="bd95f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd95f-115">-DefaultProfile</span></span>
<span data-ttu-id="bd95f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd95f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd95f-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="bd95f-117">-EnvironmentName</span></span>
<span data-ttu-id="bd95f-118">Имя среды Time Series Insights, связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bd95f-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="bd95f-119">-KeyProperty</span><span class="sxs-lookup"><span data-stu-id="bd95f-119">-KeyProperty</span></span>
<span data-ttu-id="bd95f-120">Список ключевых свойств для набора справочных данных.</span><span class="sxs-lookup"><span data-stu-id="bd95f-120">The list of key properties for the reference data set.</span></span>
<span data-ttu-id="bd95f-121">Чтобы построить новую таблицу, см. раздел "ПРИМЕЧАНИЯ" для свойств KEYPROPERTY и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="bd95f-121">To construct, see NOTES section for KEYPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="bd95f-122">-Location</span><span class="sxs-lookup"><span data-stu-id="bd95f-122">-Location</span></span>
<span data-ttu-id="bd95f-123">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="bd95f-123">The location of the resource.</span></span>

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

### <span data-ttu-id="bd95f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="bd95f-124">-Name</span></span>
<span data-ttu-id="bd95f-125">Имя набора справочных данных.</span><span class="sxs-lookup"><span data-stu-id="bd95f-125">Name of the reference data set.</span></span>

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

### <span data-ttu-id="bd95f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd95f-126">-ResourceGroupName</span></span>
<span data-ttu-id="bd95f-127">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="bd95f-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="bd95f-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bd95f-128">-SubscriptionId</span></span>
<span data-ttu-id="bd95f-129">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="bd95f-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="bd95f-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="bd95f-130">-Tag</span></span>
<span data-ttu-id="bd95f-131">Пары ключевых значений дополнительных свойств для ресурса.</span><span class="sxs-lookup"><span data-stu-id="bd95f-131">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="bd95f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd95f-132">-Confirm</span></span>
<span data-ttu-id="bd95f-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="bd95f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd95f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd95f-134">-WhatIf</span></span>
<span data-ttu-id="bd95f-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd95f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd95f-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bd95f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd95f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd95f-137">CommonParameters</span></span>
<span data-ttu-id="bd95f-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd95f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd95f-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd95f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd95f-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd95f-140">INPUTS</span></span>

## <span data-ttu-id="bd95f-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bd95f-141">OUTPUTS</span></span>

### <span data-ttu-id="bd95f-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="bd95f-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="bd95f-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bd95f-143">NOTES</span></span>

<span data-ttu-id="bd95f-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="bd95f-144">ALIASES</span></span>

<span data-ttu-id="bd95f-145">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="bd95f-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bd95f-146">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="bd95f-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bd95f-147">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bd95f-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bd95f-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: список ключевых свойств для набора справочных данных.</span><span class="sxs-lookup"><span data-stu-id="bd95f-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: The list of key properties for the reference data set.</span></span>
  - <span data-ttu-id="bd95f-149">`[Name <String>]`: Имя свойства ключа.</span><span class="sxs-lookup"><span data-stu-id="bd95f-149">`[Name <String>]`: The name of the key property.</span></span>
  - <span data-ttu-id="bd95f-150">`[Type <ReferenceDataKeyPropertyType?>]`Тип свойства ключа.</span><span class="sxs-lookup"><span data-stu-id="bd95f-150">`[Type <ReferenceDataKeyPropertyType?>]`: The type of the key property.</span></span>

## <span data-ttu-id="bd95f-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd95f-151">RELATED LINKS</span></span>

