---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/measure-azalertstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
ms.openlocfilehash: 96b83f6792babed9fed7c39cad44aec0ea0f26ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245635"
---
# <span data-ttu-id="935a5-101">Measure-AzAlertStatistic</span><span class="sxs-lookup"><span data-stu-id="935a5-101">Measure-AzAlertStatistic</span></span>

## <span data-ttu-id="935a5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="935a5-102">SYNOPSIS</span></span>
<span data-ttu-id="935a5-103">Получение сводных данных об оповещениях</span><span class="sxs-lookup"><span data-stu-id="935a5-103">Gets Alert Summary Information</span></span>

## <span data-ttu-id="935a5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="935a5-104">SYNTAX</span></span>

### <span data-ttu-id="935a5-105">SummaryTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="935a5-105">SummaryTargetResourceIdFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceId <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="935a5-106">SummaryFilter</span><span class="sxs-lookup"><span data-stu-id="935a5-106">SummaryFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceType <String>] [-TargetResourceGroup <String>]
 [-MonitorService <String>] [-MonitorCondition <String>] [-Severity <String>] [-State <String>]
 [-AlertRuleId <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="935a5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="935a5-107">DESCRIPTION</span></span>
<span data-ttu-id="935a5-108">Командлет **Measure-AzAlertStatistic** Возвращает сводную информацию об оповещениях.</span><span class="sxs-lookup"><span data-stu-id="935a5-108">**Measure-AzAlertStatistic** cmdlet gets alert summary details.</span></span>

## <span data-ttu-id="935a5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="935a5-109">EXAMPLES</span></span>

### <span data-ttu-id="935a5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="935a5-110">Example 1</span></span>
```powershell
PS C:\> Measure-AzAlertStatistic -GroupBy "severity,alertstate" -State "Active"
```

<span data-ttu-id="935a5-111">Суммарное количество оповещений, сгруппированных по уровню серьезности и состоянию, отфильтрованному по активному состоянию.</span><span class="sxs-lookup"><span data-stu-id="935a5-111">Summarize alerts count grouped by severity and state filtered by Active state.</span></span>

## <span data-ttu-id="935a5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="935a5-112">PARAMETERS</span></span>

### <span data-ttu-id="935a5-113">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="935a5-113">-AlertRuleId</span></span>
<span data-ttu-id="935a5-114">Фильтр по коду правила генерации оповещений</span><span class="sxs-lookup"><span data-stu-id="935a5-114">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="935a5-115">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="935a5-115">-CustomTimeRange</span></span>
<span data-ttu-id="935a5-116">Поддерживаемый формат: \<start-time\> / \<end-time\> время в формате ISO-8601</span><span class="sxs-lookup"><span data-stu-id="935a5-116">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="935a5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="935a5-117">-DefaultProfile</span></span>
<span data-ttu-id="935a5-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="935a5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="935a5-119">-GroupBy</span><span class="sxs-lookup"><span data-stu-id="935a5-119">-GroupBy</span></span>
<span data-ttu-id="935a5-120">Обобщение по свойству</span><span class="sxs-lookup"><span data-stu-id="935a5-120">Summarize by property</span></span>

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

### <span data-ttu-id="935a5-121">-IncludeSmartGroupsCount</span><span class="sxs-lookup"><span data-stu-id="935a5-121">-IncludeSmartGroupsCount</span></span>
<span data-ttu-id="935a5-122">Включить число SmartGroups</span><span class="sxs-lookup"><span data-stu-id="935a5-122">Include SmartGroups Count</span></span>

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

### <span data-ttu-id="935a5-123">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="935a5-123">-MonitorCondition</span></span>
<span data-ttu-id="935a5-124">Фильтр по условию для монитора</span><span class="sxs-lookup"><span data-stu-id="935a5-124">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="935a5-125">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="935a5-125">-MonitorService</span></span>
<span data-ttu-id="935a5-126">Фильтрация в службе moniter</span><span class="sxs-lookup"><span data-stu-id="935a5-126">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="935a5-127">-Серьезность</span><span class="sxs-lookup"><span data-stu-id="935a5-127">-Severity</span></span>
<span data-ttu-id="935a5-128">Фильтрация по уровню серьезности оповещений</span><span class="sxs-lookup"><span data-stu-id="935a5-128">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="935a5-129">-State</span><span class="sxs-lookup"><span data-stu-id="935a5-129">-State</span></span>
<span data-ttu-id="935a5-130">Фильтрация по состоянию оповещения</span><span class="sxs-lookup"><span data-stu-id="935a5-130">Filter on State of alert</span></span>

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

### <span data-ttu-id="935a5-131">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="935a5-131">-TargetResourceGroup</span></span>
<span data-ttu-id="935a5-132">Фильтрация по имени группы ресурсов для целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="935a5-132">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="935a5-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="935a5-133">-TargetResourceId</span></span>
<span data-ttu-id="935a5-134">Фильтрация по идентификатору ресурса целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="935a5-134">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="935a5-135">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="935a5-135">-TargetResourceType</span></span>
<span data-ttu-id="935a5-136">Фильтрация по типу ресурса целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="935a5-136">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="935a5-137">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="935a5-137">-TimeRange</span></span>
<span data-ttu-id="935a5-138">Поддерживаемые значения временных диапазонов: 1ч, 1Д, 7D, 30d (значение по умолчанию — 1д)</span><span class="sxs-lookup"><span data-stu-id="935a5-138">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="935a5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="935a5-139">CommonParameters</span></span>
<span data-ttu-id="935a5-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="935a5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="935a5-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="935a5-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="935a5-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="935a5-142">INPUTS</span></span>

### <span data-ttu-id="935a5-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="935a5-143">None</span></span>

## <span data-ttu-id="935a5-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="935a5-144">OUTPUTS</span></span>

### <span data-ttu-id="935a5-145">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlertsSummary</span><span class="sxs-lookup"><span data-stu-id="935a5-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span></span>

## <span data-ttu-id="935a5-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="935a5-146">NOTES</span></span>

## <span data-ttu-id="935a5-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="935a5-147">RELATED LINKS</span></span>