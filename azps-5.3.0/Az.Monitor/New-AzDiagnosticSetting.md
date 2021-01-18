---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticSetting.md
ms.openlocfilehash: 8fa796b9b8940662c091e160cea55235816a29d6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507087"
---
# <span data-ttu-id="4d907-101">New-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="4d907-101">New-AzDiagnosticSetting</span></span>

## <span data-ttu-id="4d907-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d907-102">SYNOPSIS</span></span>
<span data-ttu-id="4d907-103">Создание объекта PSServiceDiagnosticSettings.</span><span class="sxs-lookup"><span data-stu-id="4d907-103">Create PSServiceDiagnosticSettings object.</span></span>

## <span data-ttu-id="4d907-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4d907-104">SYNTAX</span></span>

```
New-AzDiagnosticSetting -TargetResourceId <String> -Name <String> [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-WorkspaceId <String>] [-DedicatedLogAnalyticsDestinationType] [-Setting <PSDiagnosticDetailSettings[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d907-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d907-105">DESCRIPTION</span></span>
<span data-ttu-id="4d907-106">Создание объекта PSServiceDiagnosticSettings.</span><span class="sxs-lookup"><span data-stu-id="4d907-106">Create PSServiceDiagnosticSettings object.</span></span>
<span data-ttu-id="4d907-107">Его можно использовать в качестве `-InputObject` параметра для `Set-AzDiagnosticSetting`</span><span class="sxs-lookup"><span data-stu-id="4d907-107">This can be used as parameter `-InputObject` for `Set-AzDiagnosticSetting`</span></span>

## <span data-ttu-id="4d907-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4d907-108">EXAMPLES</span></span>

### <span data-ttu-id="4d907-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4d907-109">Example 1</span></span>
```powershell
$TimeGrain=New-TimeSpan -Days 90
$metric = New-AzDiagnosticDetailSetting -Metric -RetentionInDays 1 -RetentionEnabled -Category AllMetrics
$log = New-AzDiagnosticDetailSetting -Log -RetentionInDays 1 -RetentionEnabled -Category Audit -Enabled
$setting = New-AzDiagnosticSetting -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX -Name diagnostic-test -WorkspaceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.OperationalInsights/workspaces/XXXXXXXXX -DedicatedLogAnalyticsDestinationType -Setting $log,$metric
Location                    :
Tags                        :
Id                          : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/diagnosticSettings/diagnostic-test
Name                        : diagnostic-test
StorageAccountId            :
ServiceBusRuleId            :
EventHubAuthorizationRuleId :
EventHubName                :
Metrics
    TimeGrain       :
    Category        : AllMetrics
    Enabled         : False
    RetentionPolicy
    Enabled : True
    Days    : 1


Logs
    Category        : Audit
    Enabled         : True
    RetentionPolicy
    Enabled : True
    Days    : 1


WorkspaceId                 : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.OperationalInsights/workspaces/XXXXXXXXX
LogAnalyticsDestinationType : Dedicated
Type                        :

Set-AzDiagnosticSetting -InputObject $setting
```

<span data-ttu-id="4d907-110">Создание объекта PSServiceDiagnosticSettings.</span><span class="sxs-lookup"><span data-stu-id="4d907-110">Create PSServiceDiagnosticSettings object.</span></span> <span data-ttu-id="4d907-111">И создайте параметр диагностики для целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="4d907-111">And create diagnostic setting for target resource.</span></span>

## <span data-ttu-id="4d907-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d907-112">PARAMETERS</span></span>

### <span data-ttu-id="4d907-113">-DedicatedLogAnalyticsDestinationType</span><span class="sxs-lookup"><span data-stu-id="4d907-113">-DedicatedLogAnalyticsDestinationType</span></span>
<span data-ttu-id="4d907-114">Значение, указывающее, следует ли экспортировать (в ODS) в конкретный ресурс (если он имеется) или в AzureDiagnostics (по умолчанию, не присутствует).</span><span class="sxs-lookup"><span data-stu-id="4d907-114">The value indicating whether to export (to ODS) to resource-specific (if present) or to AzureDiagnostics (default, not present)</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d907-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d907-115">-DefaultProfile</span></span>
<span data-ttu-id="4d907-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4d907-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d907-117">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="4d907-117">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="4d907-118">The event hub rule id</span><span class="sxs-lookup"><span data-stu-id="4d907-118">The event hub rule id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d907-119">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="4d907-119">-EventHubName</span></span>
<span data-ttu-id="4d907-120">The service bus rule id</span><span class="sxs-lookup"><span data-stu-id="4d907-120">The service bus rule id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d907-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4d907-121">-Name</span></span>
<span data-ttu-id="4d907-122">Имя параметра диагностики.</span><span class="sxs-lookup"><span data-stu-id="4d907-122">The name of the diagnostic setting.</span></span>
<span data-ttu-id="4d907-123">По умолчанию служба</span><span class="sxs-lookup"><span data-stu-id="4d907-123">Defaults to 'service'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d907-124">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="4d907-124">-ServiceBusRuleId</span></span>
<span data-ttu-id="4d907-125">The service bus rule id</span><span class="sxs-lookup"><span data-stu-id="4d907-125">The service bus rule id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d907-126">-Setting</span><span class="sxs-lookup"><span data-stu-id="4d907-126">-Setting</span></span>
<span data-ttu-id="4d907-127">Параметры метрики или журнал</span><span class="sxs-lookup"><span data-stu-id="4d907-127">Metric settings or Log settings</span></span>

```yaml
Type: PSDiagnosticDetailSettings[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d907-128">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4d907-128">-StorageAccountId</span></span>
<span data-ttu-id="4d907-129">ИД учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="4d907-129">The storage account id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d907-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="4d907-130">-TargetResourceId</span></span>
<span data-ttu-id="4d907-131">ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="4d907-131">The resource id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d907-132">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="4d907-132">-WorkspaceId</span></span>
<span data-ttu-id="4d907-133">ИД ресурса рабочей области "Аналитика журналов" для отправки журналов и метрик в</span><span class="sxs-lookup"><span data-stu-id="4d907-133">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d907-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d907-134">CommonParameters</span></span>
<span data-ttu-id="4d907-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d907-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d907-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d907-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d907-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d907-137">INPUTS</span></span>

### <span data-ttu-id="4d907-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4d907-138">System.String</span></span>

### <span data-ttu-id="4d907-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4d907-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4d907-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings[]</span><span class="sxs-lookup"><span data-stu-id="4d907-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings[]</span></span>

## <span data-ttu-id="4d907-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4d907-141">OUTPUTS</span></span>

### <span data-ttu-id="4d907-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="4d907-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="4d907-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4d907-143">NOTES</span></span>

## <span data-ttu-id="4d907-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d907-144">RELATED LINKS</span></span>
