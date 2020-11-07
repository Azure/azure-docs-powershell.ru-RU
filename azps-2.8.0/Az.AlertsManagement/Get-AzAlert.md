---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: e3a5cbe95bf524a70194cfce7e0b8bb80b701dec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728190"
---
# <span data-ttu-id="fbd64-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="fbd64-101">Get-AzAlert</span></span>

## <span data-ttu-id="fbd64-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fbd64-102">SYNOPSIS</span></span>
<span data-ttu-id="fbd64-103">Получение сведений об оповещениях</span><span class="sxs-lookup"><span data-stu-id="fbd64-103">Get Alerts Information</span></span>

## <span data-ttu-id="fbd64-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fbd64-104">SYNTAX</span></span>

### <span data-ttu-id="fbd64-105">AlertsListByFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fbd64-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbd64-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="fbd64-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbd64-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="fbd64-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbd64-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbd64-108">DESCRIPTION</span></span>
<span data-ttu-id="fbd64-109">Командлет **Get-AzAlert** вызывает срабатывание экземпляров оповещений.</span><span class="sxs-lookup"><span data-stu-id="fbd64-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="fbd64-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fbd64-110">EXAMPLES</span></span>

### <span data-ttu-id="fbd64-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fbd64-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="fbd64-112">Список всех оповещений с уровнем серьезности Sev2 и срабатыванием состояния монитора.</span><span class="sxs-lookup"><span data-stu-id="fbd64-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="fbd64-113">Если задать для IncludeContext значение true, включите пользовательские полезные данные оповещения.</span><span class="sxs-lookup"><span data-stu-id="fbd64-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="fbd64-114">Используйте Format-List для получения подробных сведений о каждом оповещении в списке.</span><span class="sxs-lookup"><span data-stu-id="fbd64-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="fbd64-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fbd64-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="fbd64-116">Получение сведений о предупреждении по идентификатору (GUID) или идентификатору ресурса (полный идентификатор ARM)</span><span class="sxs-lookup"><span data-stu-id="fbd64-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="fbd64-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fbd64-117">PARAMETERS</span></span>

### <span data-ttu-id="fbd64-118">-AlertId</span><span class="sxs-lookup"><span data-stu-id="fbd64-118">-AlertId</span></span>
<span data-ttu-id="fbd64-119">Уникальный идентификатор оповещения/ResourceId для оповещения.</span><span class="sxs-lookup"><span data-stu-id="fbd64-119">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd64-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="fbd64-120">-AlertRuleId</span></span>
<span data-ttu-id="fbd64-121">Фильтр по коду правила генерации оповещений</span><span class="sxs-lookup"><span data-stu-id="fbd64-121">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd64-122">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="fbd64-122">-CustomTimeRange</span></span>
<span data-ttu-id="fbd64-123">Поддерживаемый формат — время \< \> / \< \> , когда время начала в формате ISO-8601</span><span class="sxs-lookup"><span data-stu-id="fbd64-123">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd64-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbd64-124">-DefaultProfile</span></span>
<span data-ttu-id="fbd64-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fbd64-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbd64-126">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="fbd64-126">-IncludeContext</span></span>
<span data-ttu-id="fbd64-127">Включить контекст (настраиваемый набор полезных данных) оповещения</span><span class="sxs-lookup"><span data-stu-id="fbd64-127">Include context (custom payload) of alert</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd64-128">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="fbd64-128">-IncludeEgressConfig</span></span>
<span data-ttu-id="fbd64-129">Включить EgressConfig</span><span class="sxs-lookup"><span data-stu-id="fbd64-129">Include EgressConfig</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd64-130">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="fbd64-130">-MonitorCondition</span></span>
<span data-ttu-id="fbd64-131">Фильтр по условию для монитора</span><span class="sxs-lookup"><span data-stu-id="fbd64-131">Filter on Monitor Condition</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd64-132">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="fbd64-132">-MonitorService</span></span>
<span data-ttu-id="fbd64-133">Фильтрация в службе moniter</span><span class="sxs-lookup"><span data-stu-id="fbd64-133">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd64-134">-PageCount</span><span class="sxs-lookup"><span data-stu-id="fbd64-134">-PageCount</span></span>
<span data-ttu-id="fbd64-135">Количество оповещений, которые нужно получить на странице.</span><span class="sxs-lookup"><span data-stu-id="fbd64-135">Number of alerts to be fetched in a page.</span></span>

```yaml
Type: System.Int32
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd64-136">-SELECT</span><span class="sxs-lookup"><span data-stu-id="fbd64-136">-Select</span></span>
<span data-ttu-id="fbd64-137">Заполните поля, необходимые для проекта Essentials.</span><span class="sxs-lookup"><span data-stu-id="fbd64-137">Project the required fields out of essentials.</span></span>
<span data-ttu-id="fbd64-138">Ожидаемые входные данные разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="fbd64-138">Expected input is comma-separated.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd64-139">-Серьезность</span><span class="sxs-lookup"><span data-stu-id="fbd64-139">-Severity</span></span>
<span data-ttu-id="fbd64-140">Фильтрация по уровню серьезности оповещений</span><span class="sxs-lookup"><span data-stu-id="fbd64-140">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd64-141">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="fbd64-141">-SmartGroupId</span></span>
<span data-ttu-id="fbd64-142">Фильтрация всех оповещений с кодом Smart Group</span><span class="sxs-lookup"><span data-stu-id="fbd64-142">Filter all the alerts having the Smart Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd64-143">-SortBy</span><span class="sxs-lookup"><span data-stu-id="fbd64-143">-SortBy</span></span>
<span data-ttu-id="fbd64-144">Свойство Alert для использования во время сортировки</span><span class="sxs-lookup"><span data-stu-id="fbd64-144">Alert property to use while sorting</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd64-145">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="fbd64-145">-SortOrder</span></span>
<span data-ttu-id="fbd64-146">Порядок сортировки</span><span class="sxs-lookup"><span data-stu-id="fbd64-146">Sort Order</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd64-147">-State</span><span class="sxs-lookup"><span data-stu-id="fbd64-147">-State</span></span>
<span data-ttu-id="fbd64-148">Фильтрация по состоянию оповещения</span><span class="sxs-lookup"><span data-stu-id="fbd64-148">Filter on State of alert</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd64-149">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fbd64-149">-TargetResourceGroup</span></span>
<span data-ttu-id="fbd64-150">Фильтрация по имени группы ресурсов для целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="fbd64-150">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd64-151">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="fbd64-151">-TargetResourceId</span></span>
<span data-ttu-id="fbd64-152">Фильтрация по идентификатору ресурса целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="fbd64-152">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd64-153">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="fbd64-153">-TargetResourceType</span></span>
<span data-ttu-id="fbd64-154">Фильтрация по типу ресурса целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="fbd64-154">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd64-155">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="fbd64-155">-TimeRange</span></span>
<span data-ttu-id="fbd64-156">Поддерживаемые значения временных диапазонов: 1ч, 1Д, 7D, 30d (значение по умолчанию — 1д)</span><span class="sxs-lookup"><span data-stu-id="fbd64-156">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd64-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbd64-157">CommonParameters</span></span>
<span data-ttu-id="fbd64-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fbd64-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbd64-159">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbd64-159">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbd64-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fbd64-160">INPUTS</span></span>

### <span data-ttu-id="fbd64-161">Ничего</span><span class="sxs-lookup"><span data-stu-id="fbd64-161">None</span></span>

## <span data-ttu-id="fbd64-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbd64-162">OUTPUTS</span></span>

### <span data-ttu-id="fbd64-163">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="fbd64-163">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="fbd64-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="fbd64-164">NOTES</span></span>

## <span data-ttu-id="fbd64-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fbd64-165">RELATED LINKS</span></span>
