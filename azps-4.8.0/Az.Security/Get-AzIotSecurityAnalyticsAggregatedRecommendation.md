---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
ms.openlocfilehash: 944c029b4085316225887b821c4f6c8f52e7f92b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243986"
---
# <span data-ttu-id="4312e-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="4312e-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span></span>

## <span data-ttu-id="4312e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4312e-102">SYNOPSIS</span></span>
<span data-ttu-id="4312e-103">Получение обобщенной рекомендации по безопасности IoT</span><span class="sxs-lookup"><span data-stu-id="4312e-103">Get IoT security aggregated recommendation</span></span>

## <span data-ttu-id="4312e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4312e-104">SYNTAX</span></span>

### <span data-ttu-id="4312e-105">SolutionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4312e-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4312e-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="4312e-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4312e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4312e-107">DESCRIPTION</span></span>
<span data-ttu-id="4312e-108">Командлет Get-AzIotSecurityAnalyticsAggregatedAlert возвращает один или несколько обобщенных рекомендаций на устройствах центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="4312e-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated recommendations on devices of iot hub.</span></span> <span data-ttu-id="4312e-109">Имя агрегатной рекомендации — ее тип</span><span class="sxs-lookup"><span data-stu-id="4312e-109">The name of an aggregated recommendation is its type</span></span>

## <span data-ttu-id="4312e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4312e-110">EXAMPLES</span></span>

### <span data-ttu-id="4312e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4312e-111">Example 1</span></span>
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

<span data-ttu-id="4312e-112">Получение обобщенной рекомендации "IoT_OpenPorts" в решении для безопасности "MySolution" и "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="4312e-112">Get the aggregated recommendation "IoT_OpenPorts" in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="4312e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4312e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated recommendation items as shown in example 1
```

<span data-ttu-id="4312e-114">Получение списка обобщенных рекомендаций в решениях для обеспечения безопасности "MySolution" и "Группа ресурсов" MyResourceGroup "</span><span class="sxs-lookup"><span data-stu-id="4312e-114">Get a list of aggregated recommendations in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="4312e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4312e-115">PARAMETERS</span></span>

### <span data-ttu-id="4312e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4312e-116">-DefaultProfile</span></span>
<span data-ttu-id="4312e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4312e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4312e-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4312e-118">-Name</span></span>
<span data-ttu-id="4312e-119">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="4312e-119">Resource name.</span></span>

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

### <span data-ttu-id="4312e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4312e-120">-ResourceGroupName</span></span>
<span data-ttu-id="4312e-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4312e-121">Resource group name.</span></span>

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

### <span data-ttu-id="4312e-122">-Имя_решения</span><span class="sxs-lookup"><span data-stu-id="4312e-122">-SolutionName</span></span>
<span data-ttu-id="4312e-123">Имя решения</span><span class="sxs-lookup"><span data-stu-id="4312e-123">Solution name</span></span>

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

### <span data-ttu-id="4312e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4312e-124">CommonParameters</span></span>
<span data-ttu-id="4312e-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4312e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4312e-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4312e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4312e-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4312e-127">INPUTS</span></span>

### <span data-ttu-id="4312e-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="4312e-128">None</span></span>

## <span data-ttu-id="4312e-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4312e-129">OUTPUTS</span></span>

### <span data-ttu-id="4312e-130">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutionAnalytics. PSIoTSecurityAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="4312e-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span></span>

## <span data-ttu-id="4312e-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="4312e-131">NOTES</span></span>

## <span data-ttu-id="4312e-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4312e-132">RELATED LINKS</span></span>
