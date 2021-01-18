---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E3D7A3FE-40D4-4495-BA39-493F85F304AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsapplicationinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
ms.openlocfilehash: 0f238a417ac83cac82305ceb9c9ce20586328976
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519820"
---
# <span data-ttu-id="44027-101">New-AzOperationalInsightsApplicationInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="44027-101">New-AzOperationalInsightsApplicationInsightsDataSource</span></span>

## <span data-ttu-id="44027-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44027-102">SYNOPSIS</span></span>
<span data-ttu-id="44027-103">Собирайте журналы из Application-Insights приложения.</span><span class="sxs-lookup"><span data-stu-id="44027-103">Collect logs from given Application-Insights application.</span></span>

## <span data-ttu-id="44027-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="44027-104">SYNTAX</span></span>

### <span data-ttu-id="44027-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="44027-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44027-106">ByWorkspaceObjectByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="44027-106">ByWorkspaceObjectByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44027-107">ByWorkspaceObjectByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="44027-107">ByWorkspaceObjectByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44027-108">ByWorkspaceNameByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="44027-108">ByWorkspaceNameByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44027-109">ByWorkspaceNameByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="44027-109">ByWorkspaceNameByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44027-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44027-110">DESCRIPTION</span></span>
<span data-ttu-id="44027-111">С помощью cmdlet **New-AzOperationalInsightsApplicationInsightsDataSource** можно получить журналы из Application-Insights приложения.</span><span class="sxs-lookup"><span data-stu-id="44027-111">The **New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet enables the collection of logs from a given Application-Insights application.</span></span>

## <span data-ttu-id="44027-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="44027-112">EXAMPLES</span></span>

### <span data-ttu-id="44027-113">Пример 1. Создание источника данных application-insights в рабочей области</span><span class="sxs-lookup"><span data-stu-id="44027-113">Example 1: Create application-insights data source in workspace</span></span>
```
PS C:\> New-AzOperationalInsightsApplicationInsightsDataSource -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -ApplicationSubscriptionId "e791a474-ee54-46a2-bb06-5e058302d234" -ApplicationResourceGroupName "ContosoResourceGroup" -ApplicationName "MyAIApplication"

Name              : subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="44027-114">Эта команда создает источник данных для анализа приложений в рабочей области аналитики журналов.</span><span class="sxs-lookup"><span data-stu-id="44027-114">This command creates an application-insights data source of a given application in a given log analytics workspace.</span></span> <span data-ttu-id="44027-115">Это позволяет получить журналы из данного приложения в область аналитики журналов.</span><span class="sxs-lookup"><span data-stu-id="44027-115">This enables the collection of logs from given application to the log analytics workspace.</span></span>

### <span data-ttu-id="44027-116">Пример 2. Получение объекта рабочей области и создание источника данных application-insights с помощью ид ресурса приложения</span><span class="sxs-lookup"><span data-stu-id="44027-116">Example 2: Get workspace object and create application-insights data source by the application resource id</span></span>
```
PS C:\> Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup" | New-AzOperationalInsightsApplicationInsightsDataSource -ApplicationResourceId "/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication"

Name              : subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="44027-117">Эта команда демонстрирует получение объекта рабочей области аналитики журнала и передачу результатов для создания связанного источника данных application-insights с помощью ид ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="44027-117">This command demonstrates getting a log analytics workspace object and then passing the output to create an associated application-insights data source by the application resource id.</span></span> 

## <span data-ttu-id="44027-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44027-118">PARAMETERS</span></span>

### <span data-ttu-id="44027-119">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="44027-119">-ApplicationName</span></span>
<span data-ttu-id="44027-120">Имя связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="44027-120">The name of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44027-121">-ApplicationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44027-121">-ApplicationResourceGroupName</span></span>
<span data-ttu-id="44027-122">Имя группы ресурсов связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="44027-122">The resource group name of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44027-123">-ApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="44027-123">-ApplicationResourceId</span></span>
<span data-ttu-id="44027-124">Связанный ид ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="44027-124">The linked application resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationResourceId, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44027-125">-ApplicationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44027-125">-ApplicationSubscriptionId</span></span>
<span data-ttu-id="44027-126">ИД подписки связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="44027-126">The subscription id of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44027-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44027-127">-DefaultProfile</span></span>
<span data-ttu-id="44027-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44027-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44027-129">-Force</span><span class="sxs-lookup"><span data-stu-id="44027-129">-Force</span></span>
<span data-ttu-id="44027-130">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="44027-130">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44027-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44027-131">-ResourceGroupName</span></span>
<span data-ttu-id="44027-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="44027-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByApplicationParameters, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44027-133">-Workspace</span><span class="sxs-lookup"><span data-stu-id="44027-133">-Workspace</span></span>
<span data-ttu-id="44027-134">Рабочее пространство, которое будет содержать источник данных.</span><span class="sxs-lookup"><span data-stu-id="44027-134">The workspace that will contain the data source.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceObjectByApplicationResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44027-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="44027-135">-WorkspaceName</span></span>
<span data-ttu-id="44027-136">Имя рабочей области, которая будет содержать источник данных.</span><span class="sxs-lookup"><span data-stu-id="44027-136">The name of the workspace that will contain the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByApplicationParameters, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44027-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44027-137">-Confirm</span></span>
<span data-ttu-id="44027-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44027-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44027-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44027-139">-WhatIf</span></span>
<span data-ttu-id="44027-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44027-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44027-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="44027-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44027-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44027-142">CommonParameters</span></span>
<span data-ttu-id="44027-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44027-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44027-144">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44027-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44027-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44027-145">INPUTS</span></span>

### <span data-ttu-id="44027-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="44027-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="44027-147">System.String</span><span class="sxs-lookup"><span data-stu-id="44027-147">System.String</span></span>

## <span data-ttu-id="44027-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="44027-148">OUTPUTS</span></span>

### <span data-ttu-id="44027-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="44027-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="44027-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="44027-150">NOTES</span></span>

## <span data-ttu-id="44027-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44027-151">RELATED LINKS</span></span>
