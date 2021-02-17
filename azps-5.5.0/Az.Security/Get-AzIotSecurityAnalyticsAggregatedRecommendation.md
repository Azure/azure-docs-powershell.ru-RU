---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
ms.openlocfilehash: 944c029b4085316225887b821c4f6c8f52e7f92b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210412"
---
# <span data-ttu-id="e2fbd-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="e2fbd-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span></span>

## <span data-ttu-id="e2fbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2fbd-102">SYNOPSIS</span></span>
<span data-ttu-id="e2fbd-103">Получить обобщенную рекомендацию по безопасности IoT</span><span class="sxs-lookup"><span data-stu-id="e2fbd-103">Get IoT security aggregated recommendation</span></span>

## <span data-ttu-id="e2fbd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e2fbd-104">SYNTAX</span></span>

### <span data-ttu-id="e2fbd-105">SolutionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e2fbd-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2fbd-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="e2fbd-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2fbd-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2fbd-107">DESCRIPTION</span></span>
<span data-ttu-id="e2fbd-108">Этот Get-AzIotSecurityAnalyticsAggregatedAlert возвращает одну или несколько обобщенных рекомендаций на устройствах концентратора iot.</span><span class="sxs-lookup"><span data-stu-id="e2fbd-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated recommendations on devices of iot hub.</span></span> <span data-ttu-id="e2fbd-109">Агрегированная рекомендация имеет тип</span><span class="sxs-lookup"><span data-stu-id="e2fbd-109">The name of an aggregated recommendation is its type</span></span>

## <span data-ttu-id="e2fbd-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e2fbd-110">EXAMPLES</span></span>

### <span data-ttu-id="e2fbd-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e2fbd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Name IoT_OpenPorts

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default/aggregatedRecommendations/IoT_OpenPorts"
Name: "IoT_OpenPorts"
Type: "Microsoft.Security/IoTSecurityAggregatedRecommendation"
RecommendationName: "IoT_OpenPorts"
RecommendationDisplayName: "Device has open ports"
RecommendationTypeId: ""
DetectedBy: "IoTSecurity"
HealthyDevices: -1
UnhealthyDeviceCount: 5
RemediationSteps: "Review open ports on the device and make sure they belong to legitimate and necessary processes for the device to function correctly."
ReportedSeverity: "Medium"
Description: "Found a listening endpoint on the device."
LogAnalyticsQuery: "SecurityRecommendation | where tolower(AssessedResourceId) == tolower('/subscriptions/075423e9-7d33-4166-8bdf-3920b04e3735/resourcegroups/iot-hub-demo/providers/microsoft.devices/iothubs/ascforiot-demo') and tolower(RecommendationName) == tolower('IoT_OpenPorts') and TimeGenerated  < now()"
```

<span data-ttu-id="e2fbd-112">Получите обобщенную рекомендацию "IoT_OpenPorts" в решение безопасности "MySolution" и группу ресурсов "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="e2fbd-112">Get the aggregated recommendation "IoT_OpenPorts" in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="e2fbd-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e2fbd-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated recommendation items as shown in example 1
```

<span data-ttu-id="e2fbd-114">Получить список сводных рекомендаций по решению безопасности "MySolution" и группе ресурсов "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="e2fbd-114">Get a list of aggregated recommendations in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="e2fbd-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2fbd-115">PARAMETERS</span></span>

### <span data-ttu-id="e2fbd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2fbd-116">-DefaultProfile</span></span>
<span data-ttu-id="e2fbd-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2fbd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2fbd-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e2fbd-118">-Name</span></span>
<span data-ttu-id="e2fbd-119">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="e2fbd-119">Resource name.</span></span>

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

### <span data-ttu-id="e2fbd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2fbd-120">-ResourceGroupName</span></span>
<span data-ttu-id="e2fbd-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2fbd-121">Resource group name.</span></span>

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

### <span data-ttu-id="e2fbd-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="e2fbd-122">-SolutionName</span></span>
<span data-ttu-id="e2fbd-123">Название решения</span><span class="sxs-lookup"><span data-stu-id="e2fbd-123">Solution name</span></span>

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

### <span data-ttu-id="e2fbd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2fbd-124">CommonParameters</span></span>
<span data-ttu-id="e2fbd-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2fbd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2fbd-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2fbd-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2fbd-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2fbd-127">INPUTS</span></span>

### <span data-ttu-id="e2fbd-128">Нет</span><span class="sxs-lookup"><span data-stu-id="e2fbd-128">None</span></span>

## <span data-ttu-id="e2fbd-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e2fbd-129">OUTPUTS</span></span>

### <span data-ttu-id="e2fbd-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="e2fbd-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span></span>

## <span data-ttu-id="e2fbd-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e2fbd-131">NOTES</span></span>

## <span data-ttu-id="e2fbd-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2fbd-132">RELATED LINKS</span></span>
