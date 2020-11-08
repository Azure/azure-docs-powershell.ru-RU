---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
ms.openlocfilehash: 30b6979be7f3aae23bec5d1ca45d48d4dd2290f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235361"
---
# <span data-ttu-id="3767b-101">Set-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="3767b-101">Set-AzIotSecuritySolution</span></span>

## <span data-ttu-id="3767b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3767b-102">SYNOPSIS</span></span>
<span data-ttu-id="3767b-103">Создание и обновление решения для обеспечения безопасности IoT</span><span class="sxs-lookup"><span data-stu-id="3767b-103">Create or update IoT security solution</span></span>

## <span data-ttu-id="3767b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3767b-104">SYNTAX</span></span>

### <span data-ttu-id="3767b-105">ResourceGroupLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3767b-105">ResourceGroupLevelResource (Default)</span></span>
```
Set-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3767b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3767b-106">InputObject</span></span>
```
Set-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3767b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3767b-107">ResourceId</span></span>
```
Set-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>] -Location <String> -Workspace <String>
 -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>] [-DisabledDataSource <String[]>]
 -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3767b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3767b-108">DESCRIPTION</span></span>
<span data-ttu-id="3767b-109">Командлет Set-AzIotSecuritySolution создает или обновляет конкретное решение для обеспечения безопасности IOT.</span><span class="sxs-lookup"><span data-stu-id="3767b-109">The Set-AzIotSecuritySolution cmdlet creates or updates a specific iot security solution.</span></span> <span data-ttu-id="3767b-110">Решение для обеспечения безопасности IoT собирает данные о безопасности и события на устройствах Интернет вещей и центре Интернета, которые помогают предотвратить и обнаруживать угрозы.</span><span class="sxs-lookup"><span data-stu-id="3767b-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>
<span data-ttu-id="3767b-111">Имя решения для обеспечения безопасности IOT должно совпадать с именем центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="3767b-111">The name of iot security solution should be identical to the name of the iot hub.</span></span>

## <span data-ttu-id="3767b-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3767b-112">EXAMPLES</span></span>

### <span data-ttu-id="3767b-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3767b-113">Example 1</span></span>
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

<span data-ttu-id="3767b-114">Создание решения для системы безопасности IOT "MySample" для центра Интернета вещей с идентификатором ресурса "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (имя решения должно совпадать с именем центра Интернета вещей)</span><span class="sxs-lookup"><span data-stu-id="3767b-114">Create new iot security solution "MySample" for IoT hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (the name of the solution should be identical to the name of the IoT hub)</span></span>

## <span data-ttu-id="3767b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3767b-115">PARAMETERS</span></span>

### <span data-ttu-id="3767b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3767b-116">-DefaultProfile</span></span>
<span data-ttu-id="3767b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3767b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3767b-118">-DisabledDataSource</span><span class="sxs-lookup"><span data-stu-id="3767b-118">-DisabledDataSource</span></span>
<span data-ttu-id="3767b-119">Отключенные источники данных.</span><span class="sxs-lookup"><span data-stu-id="3767b-119">Disabled data sources.</span></span>

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

### <span data-ttu-id="3767b-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3767b-120">-DisplayName</span></span>
<span data-ttu-id="3767b-121">Отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="3767b-121">Display name.</span></span>

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

### <span data-ttu-id="3767b-122">-Включено</span><span class="sxs-lookup"><span data-stu-id="3767b-122">-Enabled</span></span>
<span data-ttu-id="3767b-123">Состояни.</span><span class="sxs-lookup"><span data-stu-id="3767b-123">Status .</span></span>

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

### <span data-ttu-id="3767b-124">-Экспорт</span><span class="sxs-lookup"><span data-stu-id="3767b-124">-Export</span></span>
<span data-ttu-id="3767b-125">Экспорт данных.</span><span class="sxs-lookup"><span data-stu-id="3767b-125">Export data.</span></span>

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

### <span data-ttu-id="3767b-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3767b-126">-InputObject</span></span>
<span data-ttu-id="3767b-127">Объект input.</span><span class="sxs-lookup"><span data-stu-id="3767b-127">Input Object.</span></span>

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

### <span data-ttu-id="3767b-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="3767b-128">-IotHub</span></span>
<span data-ttu-id="3767b-129">Центры Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="3767b-129">Iot hubs.</span></span>

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

### <span data-ttu-id="3767b-130">-Location</span><span class="sxs-lookup"><span data-stu-id="3767b-130">-Location</span></span>
<span data-ttu-id="3767b-131">Поиска.</span><span class="sxs-lookup"><span data-stu-id="3767b-131">Location.</span></span>

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

### <span data-ttu-id="3767b-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3767b-132">-Name</span></span>
<span data-ttu-id="3767b-133">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="3767b-133">Resource name.</span></span>

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

### <span data-ttu-id="3767b-134">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="3767b-134">-RecommendationsConfiguration</span></span>
<span data-ttu-id="3767b-135">Настройка рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="3767b-135">Recommendations configuration.</span></span>

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

### <span data-ttu-id="3767b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3767b-136">-ResourceGroupName</span></span>
<span data-ttu-id="3767b-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3767b-137">Resource group name.</span></span>

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

### <span data-ttu-id="3767b-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3767b-138">-ResourceId</span></span>
<span data-ttu-id="3767b-139">Идентификатор ресурса безопасности, для которого нужно вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="3767b-139">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="3767b-140">-Тег</span><span class="sxs-lookup"><span data-stu-id="3767b-140">-Tag</span></span>
<span data-ttu-id="3767b-141">Embed.</span><span class="sxs-lookup"><span data-stu-id="3767b-141">Tags.</span></span>

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

### <span data-ttu-id="3767b-142">-UnmaskedIpLoggingStatus</span><span class="sxs-lookup"><span data-stu-id="3767b-142">-UnmaskedIpLoggingStatus</span></span>
<span data-ttu-id="3767b-143">Состояние журналирования IP в немаскированном виде.</span><span class="sxs-lookup"><span data-stu-id="3767b-143">Unmasked ip logging status.</span></span>

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

### <span data-ttu-id="3767b-144">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="3767b-144">-UserDefinedResource</span></span>
<span data-ttu-id="3767b-145">Пользовательские ресурсы.</span><span class="sxs-lookup"><span data-stu-id="3767b-145">User defined resources.</span></span>

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

### <span data-ttu-id="3767b-146">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="3767b-146">-Workspace</span></span>
<span data-ttu-id="3767b-147">ИДЕНТИФИКАТОР рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3767b-147">Workspace ID.</span></span>

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

### <span data-ttu-id="3767b-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3767b-148">-Confirm</span></span>
<span data-ttu-id="3767b-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3767b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3767b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3767b-150">-WhatIf</span></span>
<span data-ttu-id="3767b-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3767b-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3767b-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3767b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3767b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3767b-153">CommonParameters</span></span>
<span data-ttu-id="3767b-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3767b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3767b-155">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3767b-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3767b-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3767b-156">INPUTS</span></span>

### <span data-ttu-id="3767b-157">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="3767b-157">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="3767b-158">System. String</span><span class="sxs-lookup"><span data-stu-id="3767b-158">System.String</span></span>

### <span data-ttu-id="3767b-159">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3767b-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3767b-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="3767b-160">System.String[]</span></span>

### <span data-ttu-id="3767b-161">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="3767b-161">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="3767b-162">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSRecommendationConfiguration []</span><span class="sxs-lookup"><span data-stu-id="3767b-162">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="3767b-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3767b-163">OUTPUTS</span></span>

### <span data-ttu-id="3767b-164">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="3767b-164">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="3767b-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="3767b-165">NOTES</span></span>

## <span data-ttu-id="3767b-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3767b-166">RELATED LINKS</span></span>
