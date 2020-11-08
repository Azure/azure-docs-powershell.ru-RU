---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: da462e5a8fd95b32275e37097bef18a2e7928d6e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065677"
---
# <span data-ttu-id="32200-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="32200-101">Get-AzAlert</span></span>

## <span data-ttu-id="32200-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32200-102">SYNOPSIS</span></span>
<span data-ttu-id="32200-103">Получение сведений об оповещениях</span><span class="sxs-lookup"><span data-stu-id="32200-103">Get Alerts Information</span></span>

## <span data-ttu-id="32200-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32200-104">SYNTAX</span></span>

### <span data-ttu-id="32200-105">AlertsListByFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="32200-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32200-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="32200-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32200-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="32200-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32200-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32200-108">DESCRIPTION</span></span>
<span data-ttu-id="32200-109">Командлет **Get-AzAlert** вызывает срабатывание экземпляров оповещений.</span><span class="sxs-lookup"><span data-stu-id="32200-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="32200-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32200-110">EXAMPLES</span></span>

### <span data-ttu-id="32200-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="32200-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="32200-112">Список всех оповещений с уровнем серьезности Sev2 и срабатыванием состояния монитора.</span><span class="sxs-lookup"><span data-stu-id="32200-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="32200-113">Если задать для IncludeContext значение true, включите пользовательские полезные данные оповещения.</span><span class="sxs-lookup"><span data-stu-id="32200-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="32200-114">Используйте Format-List для получения подробных сведений о каждом оповещении в списке.</span><span class="sxs-lookup"><span data-stu-id="32200-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="32200-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="32200-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="32200-116">Получение сведений о предупреждении по идентификатору (GUID) или идентификатору ресурса (полный идентификатор ARM)</span><span class="sxs-lookup"><span data-stu-id="32200-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="32200-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32200-117">PARAMETERS</span></span>

### <span data-ttu-id="32200-118">-AlertId</span><span class="sxs-lookup"><span data-stu-id="32200-118">-AlertId</span></span>
<span data-ttu-id="32200-119">Уникальный идентификатор оповещения/ResourceId для оповещения.</span><span class="sxs-lookup"><span data-stu-id="32200-119">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="32200-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="32200-120">-AlertRuleId</span></span>
<span data-ttu-id="32200-121">Фильтр по коду правила генерации оповещений</span><span class="sxs-lookup"><span data-stu-id="32200-121">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="32200-122">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="32200-122">-CustomTimeRange</span></span>
<span data-ttu-id="32200-123">Поддерживаемый формат — время \< \> / \< \> , когда время начала в формате ISO-8601</span><span class="sxs-lookup"><span data-stu-id="32200-123">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="32200-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32200-124">-DefaultProfile</span></span>
<span data-ttu-id="32200-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32200-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32200-126">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="32200-126">-IncludeContext</span></span>
<span data-ttu-id="32200-127">Включить контекст (настраиваемый набор полезных данных) оповещения</span><span class="sxs-lookup"><span data-stu-id="32200-127">Include context (custom payload) of alert</span></span>

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

### <span data-ttu-id="32200-128">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="32200-128">-IncludeEgressConfig</span></span>
<span data-ttu-id="32200-129">Включить EgressConfig</span><span class="sxs-lookup"><span data-stu-id="32200-129">Include EgressConfig</span></span>

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

### <span data-ttu-id="32200-130">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="32200-130">-MonitorCondition</span></span>
<span data-ttu-id="32200-131">Фильтр по условию для монитора</span><span class="sxs-lookup"><span data-stu-id="32200-131">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="32200-132">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="32200-132">-MonitorService</span></span>
<span data-ttu-id="32200-133">Фильтрация в службе moniter</span><span class="sxs-lookup"><span data-stu-id="32200-133">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="32200-134">-PageCount</span><span class="sxs-lookup"><span data-stu-id="32200-134">-PageCount</span></span>
<span data-ttu-id="32200-135">Количество оповещений, которые нужно получить на странице.</span><span class="sxs-lookup"><span data-stu-id="32200-135">Number of alerts to be fetched in a page.</span></span>

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

### <span data-ttu-id="32200-136">-SELECT</span><span class="sxs-lookup"><span data-stu-id="32200-136">-Select</span></span>
<span data-ttu-id="32200-137">Заполните поля, необходимые для проекта Essentials.</span><span class="sxs-lookup"><span data-stu-id="32200-137">Project the required fields out of essentials.</span></span>
<span data-ttu-id="32200-138">Ожидаемые входные данные разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="32200-138">Expected input is comma-separated.</span></span>

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

### <span data-ttu-id="32200-139">-Серьезность</span><span class="sxs-lookup"><span data-stu-id="32200-139">-Severity</span></span>
<span data-ttu-id="32200-140">Фильтрация по уровню серьезности оповещений</span><span class="sxs-lookup"><span data-stu-id="32200-140">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="32200-141">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="32200-141">-SmartGroupId</span></span>
<span data-ttu-id="32200-142">Фильтрация всех оповещений с кодом Smart Group</span><span class="sxs-lookup"><span data-stu-id="32200-142">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="32200-143">-SortBy</span><span class="sxs-lookup"><span data-stu-id="32200-143">-SortBy</span></span>
<span data-ttu-id="32200-144">Свойство Alert для использования во время сортировки</span><span class="sxs-lookup"><span data-stu-id="32200-144">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="32200-145">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="32200-145">-SortOrder</span></span>
<span data-ttu-id="32200-146">Порядок сортировки</span><span class="sxs-lookup"><span data-stu-id="32200-146">Sort Order</span></span>

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

### <span data-ttu-id="32200-147">-State</span><span class="sxs-lookup"><span data-stu-id="32200-147">-State</span></span>
<span data-ttu-id="32200-148">Фильтрация по состоянию оповещения</span><span class="sxs-lookup"><span data-stu-id="32200-148">Filter on State of alert</span></span>

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

### <span data-ttu-id="32200-149">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="32200-149">-TargetResourceGroup</span></span>
<span data-ttu-id="32200-150">Фильтрация по имени группы ресурсов для целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="32200-150">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="32200-151">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="32200-151">-TargetResourceId</span></span>
<span data-ttu-id="32200-152">Фильтрация по идентификатору ресурса целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="32200-152">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="32200-153">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="32200-153">-TargetResourceType</span></span>
<span data-ttu-id="32200-154">Фильтрация по типу ресурса целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="32200-154">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="32200-155">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="32200-155">-TimeRange</span></span>
<span data-ttu-id="32200-156">Поддерживаемые значения временных диапазонов: 1ч, 1Д, 7D, 30d (значение по умолчанию — 1д)</span><span class="sxs-lookup"><span data-stu-id="32200-156">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="32200-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32200-157">CommonParameters</span></span>
<span data-ttu-id="32200-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32200-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32200-159">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32200-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32200-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32200-160">INPUTS</span></span>

### <span data-ttu-id="32200-161">Ничего</span><span class="sxs-lookup"><span data-stu-id="32200-161">None</span></span>

## <span data-ttu-id="32200-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32200-162">OUTPUTS</span></span>

### <span data-ttu-id="32200-163">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="32200-163">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="32200-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="32200-164">NOTES</span></span>

## <span data-ttu-id="32200-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32200-165">RELATED LINKS</span></span>
