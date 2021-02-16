---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: 94cb37a6f98195534e7effcbff8c19b2613923d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233876"
---
# <span data-ttu-id="8620f-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="8620f-101">Get-AzAlert</span></span>

## <span data-ttu-id="8620f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8620f-102">SYNOPSIS</span></span>
<span data-ttu-id="8620f-103">"Получать оповещения"</span><span class="sxs-lookup"><span data-stu-id="8620f-103">Get Alerts Information</span></span>

## <span data-ttu-id="8620f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8620f-104">SYNTAX</span></span>

### <span data-ttu-id="8620f-105">AlertsListByFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8620f-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8620f-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="8620f-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8620f-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="8620f-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8620f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8620f-108">DESCRIPTION</span></span>
<span data-ttu-id="8620f-109">**Для оповещений get-AzAlert** вы получаете оповещение об этом.</span><span class="sxs-lookup"><span data-stu-id="8620f-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="8620f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8620f-110">EXAMPLES</span></span>

### <span data-ttu-id="8620f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8620f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="8620f-112">Список всех оповещений со степенью серьезности Sev2 и состоянием "Неавно"</span><span class="sxs-lookup"><span data-stu-id="8620f-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="8620f-113">Если параметр IncludeContext должен быть истинным, включите настраиваемую загрузку оповещений.</span><span class="sxs-lookup"><span data-stu-id="8620f-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="8620f-114">Используйте Format-List для получения полных сведений о каждом оповещении в списке.</span><span class="sxs-lookup"><span data-stu-id="8620f-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="8620f-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8620f-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="8620f-116">Получите сведения об оповещении по ИД (GUID) или ид ресурса (ARM завершения)</span><span class="sxs-lookup"><span data-stu-id="8620f-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

### <span data-ttu-id="8620f-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8620f-117">Example 3</span></span>

<span data-ttu-id="8620f-118">"Получать оповещения".</span><span class="sxs-lookup"><span data-stu-id="8620f-118">Get Alerts Information.</span></span> <span data-ttu-id="8620f-119">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="8620f-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAlert -IncludeContext $true -TimeRange '1h'
```

## <span data-ttu-id="8620f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8620f-120">PARAMETERS</span></span>

### <span data-ttu-id="8620f-121">-AlertId</span><span class="sxs-lookup"><span data-stu-id="8620f-121">-AlertId</span></span>
<span data-ttu-id="8620f-122">Уникальный идентификатор оповещения и идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="8620f-122">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="8620f-123">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="8620f-123">-AlertRuleId</span></span>
<span data-ttu-id="8620f-124">Фильтрация по ИД правила оповещения</span><span class="sxs-lookup"><span data-stu-id="8620f-124">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="8620f-125">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="8620f-125">-CustomTimeRange</span></span>
<span data-ttu-id="8620f-126">Поддерживаемый формат \<start-time\> / \<end-time\> ( время в формате ISO-8601)</span><span class="sxs-lookup"><span data-stu-id="8620f-126">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="8620f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8620f-127">-DefaultProfile</span></span>
<span data-ttu-id="8620f-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8620f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8620f-129">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="8620f-129">-IncludeContext</span></span>
<span data-ttu-id="8620f-130">Включить контекст (настраиваемую нагрузку) оповещений</span><span class="sxs-lookup"><span data-stu-id="8620f-130">Include context (custom payload) of alert</span></span>

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

### <span data-ttu-id="8620f-131">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="8620f-131">-IncludeEgressConfig</span></span>
<span data-ttu-id="8620f-132">Включить EgressConfig</span><span class="sxs-lookup"><span data-stu-id="8620f-132">Include EgressConfig</span></span>

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

### <span data-ttu-id="8620f-133">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="8620f-133">-MonitorCondition</span></span>
<span data-ttu-id="8620f-134">Фильтр по условию монитора</span><span class="sxs-lookup"><span data-stu-id="8620f-134">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="8620f-135">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="8620f-135">-MonitorService</span></span>
<span data-ttu-id="8620f-136">Фильтр по службе Moniter</span><span class="sxs-lookup"><span data-stu-id="8620f-136">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="8620f-137">-PageCount</span><span class="sxs-lookup"><span data-stu-id="8620f-137">-PageCount</span></span>
<span data-ttu-id="8620f-138">Количество оповещений, извлекаемого на странице.</span><span class="sxs-lookup"><span data-stu-id="8620f-138">Number of alerts to be fetched in a page.</span></span>

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

### <span data-ttu-id="8620f-139">-Select</span><span class="sxs-lookup"><span data-stu-id="8620f-139">-Select</span></span>
<span data-ttu-id="8620f-140">Проецируемые необходимые поля.</span><span class="sxs-lookup"><span data-stu-id="8620f-140">Project the required fields out of essentials.</span></span>
<span data-ttu-id="8620f-141">Ожидаемые данные разделены запятой.</span><span class="sxs-lookup"><span data-stu-id="8620f-141">Expected input is comma-separated.</span></span>

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

### <span data-ttu-id="8620f-142">-Severity</span><span class="sxs-lookup"><span data-stu-id="8620f-142">-Severity</span></span>
<span data-ttu-id="8620f-143">Фильтрация по важности оповещения</span><span class="sxs-lookup"><span data-stu-id="8620f-143">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="8620f-144">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="8620f-144">-SmartGroupId</span></span>
<span data-ttu-id="8620f-145">Фильтрация всех оповещений с ид smart Group</span><span class="sxs-lookup"><span data-stu-id="8620f-145">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="8620f-146">-SortBy</span><span class="sxs-lookup"><span data-stu-id="8620f-146">-SortBy</span></span>
<span data-ttu-id="8620f-147">Свойство оповещения, используемее при сортировке</span><span class="sxs-lookup"><span data-stu-id="8620f-147">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="8620f-148">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="8620f-148">-SortOrder</span></span>
<span data-ttu-id="8620f-149">Порядок сортировки</span><span class="sxs-lookup"><span data-stu-id="8620f-149">Sort Order</span></span>

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

### <span data-ttu-id="8620f-150">-State</span><span class="sxs-lookup"><span data-stu-id="8620f-150">-State</span></span>
<span data-ttu-id="8620f-151">Фильтрация оповещений</span><span class="sxs-lookup"><span data-stu-id="8620f-151">Filter on State of alert</span></span>

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

### <span data-ttu-id="8620f-152">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8620f-152">-TargetResourceGroup</span></span>
<span data-ttu-id="8620f-153">Фильтрация по имени группы ресурсов целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="8620f-153">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="8620f-154">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="8620f-154">-TargetResourceId</span></span>
<span data-ttu-id="8620f-155">Фильтрация по ИД ресурса целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="8620f-155">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="8620f-156">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="8620f-156">-TargetResourceType</span></span>
<span data-ttu-id="8620f-157">Фильтрация по типу ресурса целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="8620f-157">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="8620f-158">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="8620f-158">-TimeRange</span></span>
<span data-ttu-id="8620f-159">Поддерживаемые значения диапазонов времени: 1h, 1d, 7d, 30d (значение по умолчанию — 1d)</span><span class="sxs-lookup"><span data-stu-id="8620f-159">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="8620f-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8620f-160">CommonParameters</span></span>
<span data-ttu-id="8620f-161">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8620f-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8620f-162">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8620f-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8620f-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8620f-163">INPUTS</span></span>

### <span data-ttu-id="8620f-164">Нет</span><span class="sxs-lookup"><span data-stu-id="8620f-164">None</span></span>

## <span data-ttu-id="8620f-165">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8620f-165">OUTPUTS</span></span>

### <span data-ttu-id="8620f-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span><span class="sxs-lookup"><span data-stu-id="8620f-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="8620f-167">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8620f-167">NOTES</span></span>

## <span data-ttu-id="8620f-168">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8620f-168">RELATED LINKS</span></span>
