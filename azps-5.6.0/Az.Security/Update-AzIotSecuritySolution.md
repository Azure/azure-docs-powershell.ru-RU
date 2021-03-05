---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Update-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
ms.openlocfilehash: aec6fb98b5894b075cea7cf9b087b9f9c042779a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005715"
---
# <span data-ttu-id="72e4c-101">Update-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="72e4c-101">Update-AzIotSecuritySolution</span></span>

## <span data-ttu-id="72e4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72e4c-102">SYNOPSIS</span></span>
<span data-ttu-id="72e4c-103">Обновление одного или двух из следующих свойств в решении для обеспечения безопасности IoT: теги, конфигурация рекомендации, ресурсы, определенные пользователем</span><span class="sxs-lookup"><span data-stu-id="72e4c-103">Update one or more of the following properties in IoT security solution: tags, recommendation configuration, user defined resources</span></span>

## <span data-ttu-id="72e4c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="72e4c-104">SYNTAX</span></span>

### <span data-ttu-id="72e4c-105">ResourceGroupLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="72e4c-105">ResourceGroupLevelResource (Default)</span></span>
```
Update-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72e4c-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="72e4c-106">ResourceId</span></span>
```
Update-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72e4c-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="72e4c-107">InputObject</span></span>
```
Update-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72e4c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72e4c-108">DESCRIPTION</span></span>
<span data-ttu-id="72e4c-109">Командлет Update-AzIotSecuritySolution с рабочими днями одно или несколько из следующих свойств в определенном решении для защиты IoT: теги, конфигурация рекомендации, ресурсы, определенные пользователем.</span><span class="sxs-lookup"><span data-stu-id="72e4c-109">The Update-AzIotSecuritySolution cmdlet updayes one or more of the following properties in a specific IoT security solution: tags, recommendation configuration, user defined resources.</span></span>
<span data-ttu-id="72e4c-110">В решении безопасности iOT будут обновлены только указанные свойства.</span><span class="sxs-lookup"><span data-stu-id="72e4c-110">Only the specified properties will be updated inside the iot security solution.</span></span>
<span data-ttu-id="72e4c-111">Решение для защиты IoT собирает данные безопасности и события с устройств iot и iot-концентратора для предотвращения и обнаружения угроз.</span><span class="sxs-lookup"><span data-stu-id="72e4c-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="72e4c-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="72e4c-112">EXAMPLES</span></span>

### <span data-ttu-id="72e4c-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="72e4c-113">Example 1</span></span>
```powershell
PS C:\> $RecConfig = New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_OpenPorts" -Enabled $false
PS C:\> $UserDefinedResource = New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")   
PS C:\> Update-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup" -RecommendationsConfiguration @($RecConfig) -UserDefinedResource $UserDefinedResource

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/IoTSecuritySolutions/MySample"
Name: "MySample"
Type: "Microsoft.Security/IoTSecuritySolutions"
Location: "westus"
DisplayName: "MySample"
status: "Enabled"
Export: ["RawEvents"]
DisabledDataSources: ["TwinData"]
Workspace: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.operationalinsights/workspaces/MyLA"
AdditionalWorkspaces: null
IotHubs: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UserDefinedResources: {
    Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
    QuerySubscriptions: ["XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"]
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_OpenPorts"
    Name: "Device has open port"
    Status: "Disabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
}]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
```

<span data-ttu-id="72e4c-114">Обновление решения для безопасности iot "MySample" из группы ресурсов "MyResourceGroup" с помощью конфигурации рекомендации и ресурсов, определенных пользователем</span><span class="sxs-lookup"><span data-stu-id="72e4c-114">Update iot security solution "MySample" from resource group "MyResourceGroup" with recommendation configuration and user defined resources</span></span>

## <span data-ttu-id="72e4c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72e4c-115">PARAMETERS</span></span>

### <span data-ttu-id="72e4c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72e4c-116">-DefaultProfile</span></span>
<span data-ttu-id="72e4c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="72e4c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72e4c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72e4c-118">-InputObject</span></span>
<span data-ttu-id="72e4c-119">Объект ввода.</span><span class="sxs-lookup"><span data-stu-id="72e4c-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72e4c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="72e4c-120">-Name</span></span>
<span data-ttu-id="72e4c-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="72e4c-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e4c-122">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="72e4c-122">-RecommendationsConfiguration</span></span>
<span data-ttu-id="72e4c-123">Конфигурация рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="72e4c-123">Recommendations configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e4c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72e4c-124">-ResourceGroupName</span></span>
<span data-ttu-id="72e4c-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="72e4c-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e4c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72e4c-126">-ResourceId</span></span>
<span data-ttu-id="72e4c-127">ИД ресурса безопасности, для который требуется вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="72e4c-127">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72e4c-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="72e4c-128">-Tag</span></span>
<span data-ttu-id="72e4c-129">Теги.</span><span class="sxs-lookup"><span data-stu-id="72e4c-129">Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e4c-130">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="72e4c-130">-UserDefinedResource</span></span>
<span data-ttu-id="72e4c-131">Ресурсы, определенные пользователем.</span><span class="sxs-lookup"><span data-stu-id="72e4c-131">User defined resources.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e4c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72e4c-132">-Confirm</span></span>
<span data-ttu-id="72e4c-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72e4c-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e4c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72e4c-134">-WhatIf</span></span>
<span data-ttu-id="72e4c-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72e4c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72e4c-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="72e4c-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e4c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e4c-137">CommonParameters</span></span>
<span data-ttu-id="72e4c-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72e4c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e4c-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72e4c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e4c-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="72e4c-140">INPUTS</span></span>

### <span data-ttu-id="72e4c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="72e4c-141">System.String</span></span>

### <span data-ttu-id="72e4c-142">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="72e4c-142">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="72e4c-143">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="72e4c-143">System.Collections.Hashtable</span></span>

### <span data-ttu-id="72e4c-144">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="72e4c-144">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="72e4c-145">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="72e4c-145">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="72e4c-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="72e4c-146">OUTPUTS</span></span>

### <span data-ttu-id="72e4c-147">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="72e4c-147">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="72e4c-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="72e4c-148">NOTES</span></span>

## <span data-ttu-id="72e4c-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72e4c-149">RELATED LINKS</span></span>
