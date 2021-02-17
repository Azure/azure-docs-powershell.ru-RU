---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 5687497c55c6da914b28022320df1d7241f2eba1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210425"
---
# <span data-ttu-id="58692-101">Get-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="58692-101">Get-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="58692-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58692-102">SYNOPSIS</span></span>
<span data-ttu-id="58692-103">Получить агрегированное оповещение системы безопасности IoT</span><span class="sxs-lookup"><span data-stu-id="58692-103">Get IoT security aggregated alert</span></span>

## <span data-ttu-id="58692-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="58692-104">SYNTAX</span></span>

### <span data-ttu-id="58692-105">SolutionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="58692-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58692-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="58692-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58692-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58692-107">DESCRIPTION</span></span>
<span data-ttu-id="58692-108">Этот Get-AzIotSecurityAnalyticsAggregatedAlert возвращает одно или несколько агрегированных оповещений на устройствах концентратора iot.</span><span class="sxs-lookup"><span data-stu-id="58692-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated alerts on devices of iot hub.</span></span>
<span data-ttu-id="58692-109">Имя агрегированных оповещений — это сочетание типа оповещений и совокупной даты, разделенных на "/".</span><span class="sxs-lookup"><span data-stu-id="58692-109">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="58692-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="58692-110">EXAMPLES</span></span>

### <span data-ttu-id="58692-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="58692-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Name "IoT_Bruteforce_Fail/2019-02-02"

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default/aggregatedAlerts/IoT_Bruteforce_Fail/2019-02-02"
Name: "IoT_Bruteforce_Fail/2019-02-02"
Type: "Microsoft.Security/IoTSecurityAggregatedAlert"
AlertType: "IoT_Bruteforce_Fail"
AlertDisplayName: "Failed Bruteforce"
AggregatedDateUtc: "2019-02-02"
VendorName: "Microsoft"
ReportedSeverity: "Low"
RemediationSteps: ""
Description: "Multiple unsuccsseful login attempts identified. A Bruteforce attack on the device failed."
Count: 50
EffectedResourceType: "IoT Device"
SystemSource: "Devices"
ActionTaken: "Detected"
LogAnalyticsQuery: "SecurityAlert | where tolower(ResourceId) == tolower('/subscriptions/b77ec8a9-04ed-48d2-a87a-e5887b978ba6/resourceGroups/IoT-Solution-DemoEnv/providers/Microsoft.Devices/IotHubs/rtogm-hub') and tolower(AlertName) == tolower('Custom Alert - number of device to cloud messages in MQTT protocol is not in the allowed range') | extend DeviceId=parse_json(ExtendedProperties)['DeviceId'] | project DeviceId, TimeGenerated, DisplayName, AlertSeverity, Description, RemediationSteps, ExtendedProperties"
TopDevicesList: [
                {
                  DeviceId: "testDevice1"
                  AlertsCount: 45
                  LastOccurrence: "10:42"
                }
                {
                  DeviceId: "testDevice2"
                  AlertsCount: 30
                  LastOccurrence: "15:42"
                }
              ]
```

<span data-ttu-id="58692-112">Получите агрегированное оповещение "IoT_Bruteforce_Fail/2019-02-02" (имя из типа оповещения и его даты) в решении "MySolution" и группе ресурсов "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="58692-112">Get the aggregated alert "IoT_Bruteforce_Fail/2019-02-02" (the name combined from the alert type and its aggregated date) in solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="58692-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="58692-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated alert items as shown in example 1
```

<span data-ttu-id="58692-114">Получить список всех агрегированных оповещений в решение "MySolution" и группе ресурсов "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="58692-114">Get a list of all aggregated alerts in solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="58692-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58692-115">PARAMETERS</span></span>

### <span data-ttu-id="58692-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58692-116">-DefaultProfile</span></span>
<span data-ttu-id="58692-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="58692-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58692-118">-Name</span><span class="sxs-lookup"><span data-stu-id="58692-118">-Name</span></span>
<span data-ttu-id="58692-119">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="58692-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58692-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58692-120">-ResourceGroupName</span></span>
<span data-ttu-id="58692-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="58692-121">Resource group name.</span></span>

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

### <span data-ttu-id="58692-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="58692-122">-SolutionName</span></span>
<span data-ttu-id="58692-123">Название решения</span><span class="sxs-lookup"><span data-stu-id="58692-123">Solution name</span></span>

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

### <span data-ttu-id="58692-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58692-124">CommonParameters</span></span>
<span data-ttu-id="58692-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58692-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58692-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58692-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58692-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58692-127">INPUTS</span></span>

### <span data-ttu-id="58692-128">Нет</span><span class="sxs-lookup"><span data-stu-id="58692-128">None</span></span>

## <span data-ttu-id="58692-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="58692-129">OUTPUTS</span></span>

### <span data-ttu-id="58692-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="58692-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

## <span data-ttu-id="58692-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="58692-131">NOTES</span></span>

## <span data-ttu-id="58692-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58692-132">RELATED LINKS</span></span>
