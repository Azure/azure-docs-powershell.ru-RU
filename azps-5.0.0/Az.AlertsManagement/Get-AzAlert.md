---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: 94cb37a6f98195534e7effcbff8c19b2613923d8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319400"
---
# <span data-ttu-id="df03d-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="df03d-101">Get-AzAlert</span></span>

## <span data-ttu-id="df03d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="df03d-102">SYNOPSIS</span></span>
<span data-ttu-id="df03d-103">Получение сведений об оповещениях</span><span class="sxs-lookup"><span data-stu-id="df03d-103">Get Alerts Information</span></span>

## <span data-ttu-id="df03d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="df03d-104">SYNTAX</span></span>

### <span data-ttu-id="df03d-105">AlertsListByFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="df03d-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df03d-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="df03d-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df03d-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="df03d-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df03d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df03d-108">DESCRIPTION</span></span>
<span data-ttu-id="df03d-109">Командлет **Get-AzAlert** вызывает срабатывание экземпляров оповещений.</span><span class="sxs-lookup"><span data-stu-id="df03d-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="df03d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="df03d-110">EXAMPLES</span></span>

### <span data-ttu-id="df03d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="df03d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="df03d-112">Список всех оповещений с уровнем серьезности Sev2 и срабатыванием состояния монитора.</span><span class="sxs-lookup"><span data-stu-id="df03d-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="df03d-113">Если задать для IncludeContext значение true, включите пользовательские полезные данные оповещения.</span><span class="sxs-lookup"><span data-stu-id="df03d-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="df03d-114">Используйте Format-List для получения подробных сведений о каждом оповещении в списке.</span><span class="sxs-lookup"><span data-stu-id="df03d-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="df03d-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="df03d-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="df03d-116">Получение сведений о предупреждении по идентификатору (GUID) или идентификатору ресурса (полный идентификатор ARM)</span><span class="sxs-lookup"><span data-stu-id="df03d-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

### <span data-ttu-id="df03d-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="df03d-117">Example 3</span></span>

<span data-ttu-id="df03d-118">Получение сведений об оповещениях.</span><span class="sxs-lookup"><span data-stu-id="df03d-118">Get Alerts Information.</span></span> <span data-ttu-id="df03d-119">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="df03d-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAlert -IncludeContext $true -TimeRange '1h'
```

## <span data-ttu-id="df03d-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="df03d-120">PARAMETERS</span></span>

### <span data-ttu-id="df03d-121">-AlertId</span><span class="sxs-lookup"><span data-stu-id="df03d-121">-AlertId</span></span>
<span data-ttu-id="df03d-122">Уникальный идентификатор оповещения/ResourceId для оповещения.</span><span class="sxs-lookup"><span data-stu-id="df03d-122">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="df03d-123">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="df03d-123">-AlertRuleId</span></span>
<span data-ttu-id="df03d-124">Фильтр по коду правила генерации оповещений</span><span class="sxs-lookup"><span data-stu-id="df03d-124">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="df03d-125">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="df03d-125">-CustomTimeRange</span></span>
<span data-ttu-id="df03d-126">Поддерживаемый формат: \<start-time\> / \<end-time\> время в формате ISO-8601</span><span class="sxs-lookup"><span data-stu-id="df03d-126">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="df03d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df03d-127">-DefaultProfile</span></span>
<span data-ttu-id="df03d-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="df03d-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df03d-129">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="df03d-129">-IncludeContext</span></span>
<span data-ttu-id="df03d-130">Включить контекст (настраиваемый набор полезных данных) оповещения</span><span class="sxs-lookup"><span data-stu-id="df03d-130">Include context (custom payload) of alert</span></span>

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

### <span data-ttu-id="df03d-131">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="df03d-131">-IncludeEgressConfig</span></span>
<span data-ttu-id="df03d-132">Включить EgressConfig</span><span class="sxs-lookup"><span data-stu-id="df03d-132">Include EgressConfig</span></span>

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

### <span data-ttu-id="df03d-133">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="df03d-133">-MonitorCondition</span></span>
<span data-ttu-id="df03d-134">Фильтр по условию для монитора</span><span class="sxs-lookup"><span data-stu-id="df03d-134">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="df03d-135">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="df03d-135">-MonitorService</span></span>
<span data-ttu-id="df03d-136">Фильтрация в службе moniter</span><span class="sxs-lookup"><span data-stu-id="df03d-136">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="df03d-137">-PageCount</span><span class="sxs-lookup"><span data-stu-id="df03d-137">-PageCount</span></span>
<span data-ttu-id="df03d-138">Количество оповещений, которые нужно получить на странице.</span><span class="sxs-lookup"><span data-stu-id="df03d-138">Number of alerts to be fetched in a page.</span></span>

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

### <span data-ttu-id="df03d-139">-SELECT</span><span class="sxs-lookup"><span data-stu-id="df03d-139">-Select</span></span>
<span data-ttu-id="df03d-140">Заполните поля, необходимые для проекта Essentials.</span><span class="sxs-lookup"><span data-stu-id="df03d-140">Project the required fields out of essentials.</span></span>
<span data-ttu-id="df03d-141">Ожидаемые входные данные разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="df03d-141">Expected input is comma-separated.</span></span>

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

### <span data-ttu-id="df03d-142">-Серьезность</span><span class="sxs-lookup"><span data-stu-id="df03d-142">-Severity</span></span>
<span data-ttu-id="df03d-143">Фильтрация по уровню серьезности оповещений</span><span class="sxs-lookup"><span data-stu-id="df03d-143">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="df03d-144">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="df03d-144">-SmartGroupId</span></span>
<span data-ttu-id="df03d-145">Фильтрация всех оповещений с кодом Smart Group</span><span class="sxs-lookup"><span data-stu-id="df03d-145">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="df03d-146">-SortBy</span><span class="sxs-lookup"><span data-stu-id="df03d-146">-SortBy</span></span>
<span data-ttu-id="df03d-147">Свойство Alert для использования во время сортировки</span><span class="sxs-lookup"><span data-stu-id="df03d-147">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="df03d-148">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="df03d-148">-SortOrder</span></span>
<span data-ttu-id="df03d-149">Порядок сортировки</span><span class="sxs-lookup"><span data-stu-id="df03d-149">Sort Order</span></span>

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

### <span data-ttu-id="df03d-150">-State</span><span class="sxs-lookup"><span data-stu-id="df03d-150">-State</span></span>
<span data-ttu-id="df03d-151">Фильтрация по состоянию оповещения</span><span class="sxs-lookup"><span data-stu-id="df03d-151">Filter on State of alert</span></span>

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

### <span data-ttu-id="df03d-152">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="df03d-152">-TargetResourceGroup</span></span>
<span data-ttu-id="df03d-153">Фильтрация по имени группы ресурсов для целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="df03d-153">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="df03d-154">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="df03d-154">-TargetResourceId</span></span>
<span data-ttu-id="df03d-155">Фильтрация по идентификатору ресурса целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="df03d-155">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="df03d-156">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="df03d-156">-TargetResourceType</span></span>
<span data-ttu-id="df03d-157">Фильтрация по типу ресурса целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="df03d-157">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="df03d-158">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="df03d-158">-TimeRange</span></span>
<span data-ttu-id="df03d-159">Поддерживаемые значения временных диапазонов: 1ч, 1Д, 7D, 30d (значение по умолчанию — 1д)</span><span class="sxs-lookup"><span data-stu-id="df03d-159">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="df03d-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df03d-160">CommonParameters</span></span>
<span data-ttu-id="df03d-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="df03d-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df03d-162">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df03d-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df03d-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="df03d-163">INPUTS</span></span>

### <span data-ttu-id="df03d-164">Ничего</span><span class="sxs-lookup"><span data-stu-id="df03d-164">None</span></span>

## <span data-ttu-id="df03d-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="df03d-165">OUTPUTS</span></span>

### <span data-ttu-id="df03d-166">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="df03d-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="df03d-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="df03d-167">NOTES</span></span>

## <span data-ttu-id="df03d-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df03d-168">RELATED LINKS</span></span>
