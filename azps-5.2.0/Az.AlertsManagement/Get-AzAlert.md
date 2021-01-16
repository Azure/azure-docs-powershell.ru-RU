---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: 94cb37a6f98195534e7effcbff8c19b2613923d8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417495"
---
# <span data-ttu-id="3b0e5-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="3b0e5-101">Get-AzAlert</span></span>

## <span data-ttu-id="3b0e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b0e5-102">SYNOPSIS</span></span>
<span data-ttu-id="3b0e5-103">"Получить сведения об оповещениях"</span><span class="sxs-lookup"><span data-stu-id="3b0e5-103">Get Alerts Information</span></span>

## <span data-ttu-id="3b0e5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3b0e5-104">SYNTAX</span></span>

### <span data-ttu-id="3b0e5-105">AlertsListByFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3b0e5-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b0e5-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="3b0e5-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b0e5-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="3b0e5-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b0e5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b0e5-108">DESCRIPTION</span></span>
<span data-ttu-id="3b0e5-109">**Для оповещений** об этом возвращается оповещение Get-AzAlert.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="3b0e5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3b0e5-110">EXAMPLES</span></span>

### <span data-ttu-id="3b0e5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3b0e5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="3b0e5-112">Список всех оповещений с состоянием серьезности Sev2 и состоянием "Неавно"</span><span class="sxs-lookup"><span data-stu-id="3b0e5-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="3b0e5-113">Если параметр IncludeContext должен быть истинным, включите настраиваемую загрузку оповещений.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="3b0e5-114">Используйте Format-List для получения полных сведений о каждом оповещении в списке.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="3b0e5-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3b0e5-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="3b0e5-116">Получите сведения об оповещении по ИД (GUID) или ид ресурса (ARM завершения)</span><span class="sxs-lookup"><span data-stu-id="3b0e5-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

### <span data-ttu-id="3b0e5-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3b0e5-117">Example 3</span></span>

<span data-ttu-id="3b0e5-118">"Получать оповещения".</span><span class="sxs-lookup"><span data-stu-id="3b0e5-118">Get Alerts Information.</span></span> <span data-ttu-id="3b0e5-119">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="3b0e5-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAlert -IncludeContext $true -TimeRange '1h'
```

## <span data-ttu-id="3b0e5-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b0e5-120">PARAMETERS</span></span>

### <span data-ttu-id="3b0e5-121">-AlertId</span><span class="sxs-lookup"><span data-stu-id="3b0e5-121">-AlertId</span></span>
<span data-ttu-id="3b0e5-122">Уникальный идентификатор оповещения и идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-122">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="3b0e5-123">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="3b0e5-123">-AlertRuleId</span></span>
<span data-ttu-id="3b0e5-124">Фильтрация по ИД правила оповещения</span><span class="sxs-lookup"><span data-stu-id="3b0e5-124">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="3b0e5-125">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="3b0e5-125">-CustomTimeRange</span></span>
<span data-ttu-id="3b0e5-126">Поддерживаемый формат \<start-time\> / \<end-time\> ( время в формате ISO-8601)</span><span class="sxs-lookup"><span data-stu-id="3b0e5-126">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="3b0e5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b0e5-127">-DefaultProfile</span></span>
<span data-ttu-id="3b0e5-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b0e5-129">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="3b0e5-129">-IncludeContext</span></span>
<span data-ttu-id="3b0e5-130">Включить контекст (настраиваемую нагрузку) оповещения</span><span class="sxs-lookup"><span data-stu-id="3b0e5-130">Include context (custom payload) of alert</span></span>

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

### <span data-ttu-id="3b0e5-131">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="3b0e5-131">-IncludeEgressConfig</span></span>
<span data-ttu-id="3b0e5-132">Включить EgressConfig</span><span class="sxs-lookup"><span data-stu-id="3b0e5-132">Include EgressConfig</span></span>

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

### <span data-ttu-id="3b0e5-133">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="3b0e5-133">-MonitorCondition</span></span>
<span data-ttu-id="3b0e5-134">Фильтр по условию монитора</span><span class="sxs-lookup"><span data-stu-id="3b0e5-134">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="3b0e5-135">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="3b0e5-135">-MonitorService</span></span>
<span data-ttu-id="3b0e5-136">Фильтр по службе Moniter</span><span class="sxs-lookup"><span data-stu-id="3b0e5-136">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="3b0e5-137">-PageCount</span><span class="sxs-lookup"><span data-stu-id="3b0e5-137">-PageCount</span></span>
<span data-ttu-id="3b0e5-138">Количество оповещений, извлекаемого на странице.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-138">Number of alerts to be fetched in a page.</span></span>

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

### <span data-ttu-id="3b0e5-139">-Select</span><span class="sxs-lookup"><span data-stu-id="3b0e5-139">-Select</span></span>
<span data-ttu-id="3b0e5-140">Проецируемые необходимые поля.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-140">Project the required fields out of essentials.</span></span>
<span data-ttu-id="3b0e5-141">Ожидаемые данные разделены запятой.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-141">Expected input is comma-separated.</span></span>

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

### <span data-ttu-id="3b0e5-142">-Severity</span><span class="sxs-lookup"><span data-stu-id="3b0e5-142">-Severity</span></span>
<span data-ttu-id="3b0e5-143">Фильтрация по важности оповещения</span><span class="sxs-lookup"><span data-stu-id="3b0e5-143">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="3b0e5-144">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="3b0e5-144">-SmartGroupId</span></span>
<span data-ttu-id="3b0e5-145">Фильтрация всех оповещений с ид smart Group</span><span class="sxs-lookup"><span data-stu-id="3b0e5-145">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="3b0e5-146">-SortBy</span><span class="sxs-lookup"><span data-stu-id="3b0e5-146">-SortBy</span></span>
<span data-ttu-id="3b0e5-147">Свойство оповещения, используемее при сортировке</span><span class="sxs-lookup"><span data-stu-id="3b0e5-147">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="3b0e5-148">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="3b0e5-148">-SortOrder</span></span>
<span data-ttu-id="3b0e5-149">Порядок сортировки</span><span class="sxs-lookup"><span data-stu-id="3b0e5-149">Sort Order</span></span>

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

### <span data-ttu-id="3b0e5-150">-State</span><span class="sxs-lookup"><span data-stu-id="3b0e5-150">-State</span></span>
<span data-ttu-id="3b0e5-151">Фильтрация оповещений</span><span class="sxs-lookup"><span data-stu-id="3b0e5-151">Filter on State of alert</span></span>

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

### <span data-ttu-id="3b0e5-152">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3b0e5-152">-TargetResourceGroup</span></span>
<span data-ttu-id="3b0e5-153">Фильтрация по имени группы ресурсов целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-153">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="3b0e5-154">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="3b0e5-154">-TargetResourceId</span></span>
<span data-ttu-id="3b0e5-155">Фильтрация по ИД ресурса конечного ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-155">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="3b0e5-156">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="3b0e5-156">-TargetResourceType</span></span>
<span data-ttu-id="3b0e5-157">Фильтрация по типу ресурса целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-157">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="3b0e5-158">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="3b0e5-158">-TimeRange</span></span>
<span data-ttu-id="3b0e5-159">Поддерживаемые значения диапазонов времени: 1h, 1d, 7d, 30d (значение по умолчанию — 1d)</span><span class="sxs-lookup"><span data-stu-id="3b0e5-159">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="3b0e5-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b0e5-160">CommonParameters</span></span>
<span data-ttu-id="3b0e5-161">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b0e5-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b0e5-162">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b0e5-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b0e5-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3b0e5-163">INPUTS</span></span>

### <span data-ttu-id="3b0e5-164">Нет</span><span class="sxs-lookup"><span data-stu-id="3b0e5-164">None</span></span>

## <span data-ttu-id="3b0e5-165">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3b0e5-165">OUTPUTS</span></span>

### <span data-ttu-id="3b0e5-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span><span class="sxs-lookup"><span data-stu-id="3b0e5-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="3b0e5-167">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3b0e5-167">NOTES</span></span>

## <span data-ttu-id="3b0e5-168">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b0e5-168">RELATED LINKS</span></span>
