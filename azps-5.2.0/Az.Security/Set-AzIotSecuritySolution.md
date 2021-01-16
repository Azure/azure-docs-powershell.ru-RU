---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
ms.openlocfilehash: 30b6979be7f3aae23bec5d1ca45d48d4dd2290f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394791"
---
# <span data-ttu-id="509e9-101">Set-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="509e9-101">Set-AzIotSecuritySolution</span></span>

## <span data-ttu-id="509e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="509e9-102">SYNOPSIS</span></span>
<span data-ttu-id="509e9-103">Создание и обновление решения для безопасности IoT</span><span class="sxs-lookup"><span data-stu-id="509e9-103">Create or update IoT security solution</span></span>

## <span data-ttu-id="509e9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="509e9-104">SYNTAX</span></span>

### <span data-ttu-id="509e9-105">ResourceGroupLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="509e9-105">ResourceGroupLevelResource (Default)</span></span>
```
Set-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="509e9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="509e9-106">InputObject</span></span>
```
Set-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="509e9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="509e9-107">ResourceId</span></span>
```
Set-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>] -Location <String> -Workspace <String>
 -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>] [-DisabledDataSource <String[]>]
 -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="509e9-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="509e9-108">DESCRIPTION</span></span>
<span data-ttu-id="509e9-109">Новый Set-AzIotSecuritySolution создает или обновляет определенное решение безопасности iOT.</span><span class="sxs-lookup"><span data-stu-id="509e9-109">The Set-AzIotSecuritySolution cmdlet creates or updates a specific iot security solution.</span></span> <span data-ttu-id="509e9-110">Решение для защиты IoT собирает данные безопасности и события с устройств iot и iot-концентратора для предотвращения и обнаружения угроз.</span><span class="sxs-lookup"><span data-stu-id="509e9-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>
<span data-ttu-id="509e9-111">Имя решения безопасности iOT должно совпадать с именем концентратора iot.</span><span class="sxs-lookup"><span data-stu-id="509e9-111">The name of iot security solution should be identical to the name of the iot hub.</span></span>

## <span data-ttu-id="509e9-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="509e9-112">EXAMPLES</span></span>

### <span data-ttu-id="509e9-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="509e9-113">Example 1</span></span>
```powershell
PS C:\> $Workspace = "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.OperationalInsights/workspaces/IoTHubWorkspace"
PS C:\> $IotHubs = @("/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample")
PS C:\> Set-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup" -Location "West US" 
-Workspace $Workspace -DisplayName "MySample" -Enabled $true -IotHub $IotHubs

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
    Query: "" 
    QuerySubscriptions: []
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
    }]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
Tags: {}
```

<span data-ttu-id="509e9-114">Создайте новое решение безопасности iot "MySample" для концентратора IoT с ид ресурса "/subscriptions/XXXXXXXX-XXXXX-XXXXX-XXXXXXXXXX/resourceGroups/MicamResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (имя решения должно совпадать с именем концентратора IoT)</span><span class="sxs-lookup"><span data-stu-id="509e9-114">Create new iot security solution "MySample" for IoT hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (the name of the solution should be identical to the name of the IoT hub)</span></span>

## <span data-ttu-id="509e9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="509e9-115">PARAMETERS</span></span>

### <span data-ttu-id="509e9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="509e9-116">-DefaultProfile</span></span>
<span data-ttu-id="509e9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="509e9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="509e9-118">-DisabledDataSource</span><span class="sxs-lookup"><span data-stu-id="509e9-118">-DisabledDataSource</span></span>
<span data-ttu-id="509e9-119">Отключенные источники данных.</span><span class="sxs-lookup"><span data-stu-id="509e9-119">Disabled data sources.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509e9-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="509e9-120">-DisplayName</span></span>
<span data-ttu-id="509e9-121">Отображаемая имя.</span><span class="sxs-lookup"><span data-stu-id="509e9-121">Display name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509e9-122">-Enabled</span><span class="sxs-lookup"><span data-stu-id="509e9-122">-Enabled</span></span>
<span data-ttu-id="509e9-123">Состояние.</span><span class="sxs-lookup"><span data-stu-id="509e9-123">Status .</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509e9-124">-Экспорт</span><span class="sxs-lookup"><span data-stu-id="509e9-124">-Export</span></span>
<span data-ttu-id="509e9-125">Экспорт данных.</span><span class="sxs-lookup"><span data-stu-id="509e9-125">Export data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509e9-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="509e9-126">-InputObject</span></span>
<span data-ttu-id="509e9-127">Объект ввода.</span><span class="sxs-lookup"><span data-stu-id="509e9-127">Input Object.</span></span>

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

### <span data-ttu-id="509e9-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="509e9-128">-IotHub</span></span>
<span data-ttu-id="509e9-129">Концентраторы Iot.</span><span class="sxs-lookup"><span data-stu-id="509e9-129">Iot hubs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509e9-130">-Location</span><span class="sxs-lookup"><span data-stu-id="509e9-130">-Location</span></span>
<span data-ttu-id="509e9-131">"Расположение".</span><span class="sxs-lookup"><span data-stu-id="509e9-131">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509e9-132">-Name</span><span class="sxs-lookup"><span data-stu-id="509e9-132">-Name</span></span>
<span data-ttu-id="509e9-133">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="509e9-133">Resource name.</span></span>

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

### <span data-ttu-id="509e9-134">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="509e9-134">-RecommendationsConfiguration</span></span>
<span data-ttu-id="509e9-135">Конфигурация рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="509e9-135">Recommendations configuration.</span></span>

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

### <span data-ttu-id="509e9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="509e9-136">-ResourceGroupName</span></span>
<span data-ttu-id="509e9-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="509e9-137">Resource group name.</span></span>

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

### <span data-ttu-id="509e9-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="509e9-138">-ResourceId</span></span>
<span data-ttu-id="509e9-139">ИД ресурса безопасности, для который требуется вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="509e9-139">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="509e9-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="509e9-140">-Tag</span></span>
<span data-ttu-id="509e9-141">Теги.</span><span class="sxs-lookup"><span data-stu-id="509e9-141">Tags.</span></span>

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

### <span data-ttu-id="509e9-142">-UnmaskedIpLoggingStatus</span><span class="sxs-lookup"><span data-stu-id="509e9-142">-UnmaskedIpLoggingStatus</span></span>
<span data-ttu-id="509e9-143">"Unmasked ip logging status".</span><span class="sxs-lookup"><span data-stu-id="509e9-143">Unmasked ip logging status.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509e9-144">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="509e9-144">-UserDefinedResource</span></span>
<span data-ttu-id="509e9-145">Ресурсы, определенные пользователем.</span><span class="sxs-lookup"><span data-stu-id="509e9-145">User defined resources.</span></span>

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

### <span data-ttu-id="509e9-146">-Workspace</span><span class="sxs-lookup"><span data-stu-id="509e9-146">-Workspace</span></span>
<span data-ttu-id="509e9-147">ИД рабочей области.</span><span class="sxs-lookup"><span data-stu-id="509e9-147">Workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509e9-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="509e9-148">-Confirm</span></span>
<span data-ttu-id="509e9-149">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="509e9-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="509e9-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="509e9-150">-WhatIf</span></span>
<span data-ttu-id="509e9-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="509e9-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="509e9-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="509e9-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="509e9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="509e9-153">CommonParameters</span></span>
<span data-ttu-id="509e9-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="509e9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="509e9-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="509e9-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="509e9-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="509e9-156">INPUTS</span></span>

### <span data-ttu-id="509e9-157">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="509e9-157">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="509e9-158">System.String</span><span class="sxs-lookup"><span data-stu-id="509e9-158">System.String</span></span>

### <span data-ttu-id="509e9-159">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="509e9-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="509e9-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="509e9-160">System.String[]</span></span>

### <span data-ttu-id="509e9-161">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="509e9-161">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="509e9-162">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="509e9-162">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="509e9-163">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="509e9-163">OUTPUTS</span></span>

### <span data-ttu-id="509e9-164">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="509e9-164">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="509e9-165">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="509e9-165">NOTES</span></span>

## <span data-ttu-id="509e9-166">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="509e9-166">RELATED LINKS</span></span>
