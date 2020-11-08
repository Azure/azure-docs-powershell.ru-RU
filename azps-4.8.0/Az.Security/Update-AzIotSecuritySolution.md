---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Update-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
ms.openlocfilehash: ba84bccc92b58b7f8a21812e2f1599bbc9679d38
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078743"
---
# <span data-ttu-id="11d2e-101">Update-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="11d2e-101">Update-AzIotSecuritySolution</span></span>

## <span data-ttu-id="11d2e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="11d2e-102">SYNOPSIS</span></span>
<span data-ttu-id="11d2e-103">Обновите одно или несколько из следующих свойств в решении безопасности IoT: Теги, Настройка рекомендаций, пользовательские ресурсы</span><span class="sxs-lookup"><span data-stu-id="11d2e-103">Update one or more of the following properties in IoT security solution: tags, recommendation configuration, user defined resources</span></span>

## <span data-ttu-id="11d2e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="11d2e-104">SYNTAX</span></span>

### <span data-ttu-id="11d2e-105">ResourceGroupLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="11d2e-105">ResourceGroupLevelResource (Default)</span></span>
```
Update-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11d2e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="11d2e-106">ResourceId</span></span>
```
Update-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11d2e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="11d2e-107">InputObject</span></span>
```
Update-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11d2e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11d2e-108">DESCRIPTION</span></span>
<span data-ttu-id="11d2e-109">Командлет Update-AzIotSecuritySolution updayes одно или несколько из следующих свойств в определенном решении безопасности IoT: Теги, Настройка рекомендаций, пользовательские ресурсы.</span><span class="sxs-lookup"><span data-stu-id="11d2e-109">The Update-AzIotSecuritySolution cmdlet updayes one or more of the following properties in a specific IoT security solution: tags, recommendation configuration, user defined resources.</span></span>
<span data-ttu-id="11d2e-110">В решении безопасности IOT будут обновляться только указанные свойства.</span><span class="sxs-lookup"><span data-stu-id="11d2e-110">Only the specified properties will be updated inside the iot security solution.</span></span>
<span data-ttu-id="11d2e-111">Решение для обеспечения безопасности IoT собирает данные о безопасности и события на устройствах Интернет вещей и центре Интернета, которые помогают предотвратить и обнаруживать угрозы.</span><span class="sxs-lookup"><span data-stu-id="11d2e-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="11d2e-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="11d2e-112">EXAMPLES</span></span>

### <span data-ttu-id="11d2e-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="11d2e-113">Example 1</span></span>
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

<span data-ttu-id="11d2e-114">Обновление решения для системы безопасности IOT "MySample" из группы ресурсов "MyResourceGroup" с конфигурацией рекомендаций и пользовательскими ресурсами</span><span class="sxs-lookup"><span data-stu-id="11d2e-114">Update iot security solution "MySample" from resource group "MyResourceGroup" with recommendation configuration and user defined resources</span></span>

## <span data-ttu-id="11d2e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="11d2e-115">PARAMETERS</span></span>

### <span data-ttu-id="11d2e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11d2e-116">-DefaultProfile</span></span>
<span data-ttu-id="11d2e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="11d2e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11d2e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11d2e-118">-InputObject</span></span>
<span data-ttu-id="11d2e-119">Объект input.</span><span class="sxs-lookup"><span data-stu-id="11d2e-119">Input Object.</span></span>

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

### <span data-ttu-id="11d2e-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="11d2e-120">-Name</span></span>
<span data-ttu-id="11d2e-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="11d2e-121">Resource name.</span></span>

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

### <span data-ttu-id="11d2e-122">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="11d2e-122">-RecommendationsConfiguration</span></span>
<span data-ttu-id="11d2e-123">Настройка рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="11d2e-123">Recommendations configuration.</span></span>

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

### <span data-ttu-id="11d2e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11d2e-124">-ResourceGroupName</span></span>
<span data-ttu-id="11d2e-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="11d2e-125">Resource group name.</span></span>

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

### <span data-ttu-id="11d2e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11d2e-126">-ResourceId</span></span>
<span data-ttu-id="11d2e-127">Идентификатор ресурса безопасности, для которого нужно вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="11d2e-127">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="11d2e-128">-Тег</span><span class="sxs-lookup"><span data-stu-id="11d2e-128">-Tag</span></span>
<span data-ttu-id="11d2e-129">Embed.</span><span class="sxs-lookup"><span data-stu-id="11d2e-129">Tags.</span></span>

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

### <span data-ttu-id="11d2e-130">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="11d2e-130">-UserDefinedResource</span></span>
<span data-ttu-id="11d2e-131">Пользовательские ресурсы.</span><span class="sxs-lookup"><span data-stu-id="11d2e-131">User defined resources.</span></span>

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

### <span data-ttu-id="11d2e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11d2e-132">-Confirm</span></span>
<span data-ttu-id="11d2e-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="11d2e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11d2e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11d2e-134">-WhatIf</span></span>
<span data-ttu-id="11d2e-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="11d2e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11d2e-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="11d2e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11d2e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11d2e-137">CommonParameters</span></span>
<span data-ttu-id="11d2e-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="11d2e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11d2e-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11d2e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11d2e-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="11d2e-140">INPUTS</span></span>

### <span data-ttu-id="11d2e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="11d2e-141">System.String</span></span>

### <span data-ttu-id="11d2e-142">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="11d2e-142">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="11d2e-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="11d2e-143">System.Collections.Hashtable</span></span>

### <span data-ttu-id="11d2e-144">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="11d2e-144">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="11d2e-145">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSRecommendationConfiguration []</span><span class="sxs-lookup"><span data-stu-id="11d2e-145">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="11d2e-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="11d2e-146">OUTPUTS</span></span>

### <span data-ttu-id="11d2e-147">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="11d2e-147">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="11d2e-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="11d2e-148">NOTES</span></span>

## <span data-ttu-id="11d2e-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11d2e-149">RELATED LINKS</span></span>
