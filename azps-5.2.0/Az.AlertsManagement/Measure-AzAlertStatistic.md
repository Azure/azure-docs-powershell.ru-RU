---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/measure-azalertstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
ms.openlocfilehash: 96b83f6792babed9fed7c39cad44aec0ea0f26ed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397071"
---
# <span data-ttu-id="19621-101">Measure-AzAlertStatistic</span><span class="sxs-lookup"><span data-stu-id="19621-101">Measure-AzAlertStatistic</span></span>

## <span data-ttu-id="19621-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19621-102">SYNOPSIS</span></span>
<span data-ttu-id="19621-103">Получает сводную информацию об оповещении</span><span class="sxs-lookup"><span data-stu-id="19621-103">Gets Alert Summary Information</span></span>

## <span data-ttu-id="19621-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="19621-104">SYNTAX</span></span>

### <span data-ttu-id="19621-105">SummaryTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="19621-105">SummaryTargetResourceIdFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceId <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19621-106">SummaryFilter</span><span class="sxs-lookup"><span data-stu-id="19621-106">SummaryFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceType <String>] [-TargetResourceGroup <String>]
 [-MonitorService <String>] [-MonitorCondition <String>] [-Severity <String>] [-State <String>]
 [-AlertRuleId <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19621-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19621-107">DESCRIPTION</span></span>
<span data-ttu-id="19621-108">**Измеритель-AzAlertStatistic** получает сводные сведения об оповещении.</span><span class="sxs-lookup"><span data-stu-id="19621-108">**Measure-AzAlertStatistic** cmdlet gets alert summary details.</span></span>

## <span data-ttu-id="19621-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="19621-109">EXAMPLES</span></span>

### <span data-ttu-id="19621-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="19621-110">Example 1</span></span>
```powershell
PS C:\> Measure-AzAlertStatistic -GroupBy "severity,alertstate" -State "Active"
```

<span data-ttu-id="19621-111">Сгруппировать количество оповещений по серьезности и состояниям, отфильтрованным по состояниям активности.</span><span class="sxs-lookup"><span data-stu-id="19621-111">Summarize alerts count grouped by severity and state filtered by Active state.</span></span>

## <span data-ttu-id="19621-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19621-112">PARAMETERS</span></span>

### <span data-ttu-id="19621-113">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="19621-113">-AlertRuleId</span></span>
<span data-ttu-id="19621-114">Фильтрация по ИД правила оповещения</span><span class="sxs-lookup"><span data-stu-id="19621-114">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="19621-115">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="19621-115">-CustomTimeRange</span></span>
<span data-ttu-id="19621-116">Поддерживаемый формат \<start-time\> / \<end-time\> ( время в формате ISO-8601)</span><span class="sxs-lookup"><span data-stu-id="19621-116">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="19621-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19621-117">-DefaultProfile</span></span>
<span data-ttu-id="19621-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19621-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19621-119">-GroupBy</span><span class="sxs-lookup"><span data-stu-id="19621-119">-GroupBy</span></span>
<span data-ttu-id="19621-120">Обобщение по свойству</span><span class="sxs-lookup"><span data-stu-id="19621-120">Summarize by property</span></span>

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

### <span data-ttu-id="19621-121">-IncludeSmartGroupsCount</span><span class="sxs-lookup"><span data-stu-id="19621-121">-IncludeSmartGroupsCount</span></span>
<span data-ttu-id="19621-122">Включить SmartGroups Count</span><span class="sxs-lookup"><span data-stu-id="19621-122">Include SmartGroups Count</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19621-123">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="19621-123">-MonitorCondition</span></span>
<span data-ttu-id="19621-124">Фильтр по условию монитора</span><span class="sxs-lookup"><span data-stu-id="19621-124">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="19621-125">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="19621-125">-MonitorService</span></span>
<span data-ttu-id="19621-126">Фильтр по службе Moniter</span><span class="sxs-lookup"><span data-stu-id="19621-126">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="19621-127">-Severity</span><span class="sxs-lookup"><span data-stu-id="19621-127">-Severity</span></span>
<span data-ttu-id="19621-128">Фильтрация по важности оповещения</span><span class="sxs-lookup"><span data-stu-id="19621-128">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="19621-129">-State</span><span class="sxs-lookup"><span data-stu-id="19621-129">-State</span></span>
<span data-ttu-id="19621-130">Фильтрация оповещений</span><span class="sxs-lookup"><span data-stu-id="19621-130">Filter on State of alert</span></span>

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

### <span data-ttu-id="19621-131">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="19621-131">-TargetResourceGroup</span></span>
<span data-ttu-id="19621-132">Фильтрация по имени группы ресурсов целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="19621-132">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19621-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="19621-133">-TargetResourceId</span></span>
<span data-ttu-id="19621-134">Фильтрация по ИД ресурса конечного ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="19621-134">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19621-135">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="19621-135">-TargetResourceType</span></span>
<span data-ttu-id="19621-136">Фильтрация по типу ресурса целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="19621-136">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19621-137">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="19621-137">-TimeRange</span></span>
<span data-ttu-id="19621-138">Поддерживаемые значения диапазонов времени: 1h, 1d, 7d, 30d (значение по умолчанию — 1d)</span><span class="sxs-lookup"><span data-stu-id="19621-138">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="19621-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19621-139">CommonParameters</span></span>
<span data-ttu-id="19621-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19621-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19621-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19621-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19621-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19621-142">INPUTS</span></span>

### <span data-ttu-id="19621-143">Нет</span><span class="sxs-lookup"><span data-stu-id="19621-143">None</span></span>

## <span data-ttu-id="19621-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="19621-144">OUTPUTS</span></span>

### <span data-ttu-id="19621-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span><span class="sxs-lookup"><span data-stu-id="19621-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span></span>

## <span data-ttu-id="19621-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="19621-146">NOTES</span></span>

## <span data-ttu-id="19621-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19621-147">RELATED LINKS</span></span>