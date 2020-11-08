---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E3D7A3FE-40D4-4495-BA39-493F85F304AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsapplicationinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
ms.openlocfilehash: 0f238a417ac83cac82305ceb9c9ce20586328976
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065113"
---
# <span data-ttu-id="25d9f-101">New-AzOperationalInsightsApplicationInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="25d9f-101">New-AzOperationalInsightsApplicationInsightsDataSource</span></span>

## <span data-ttu-id="25d9f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="25d9f-102">SYNOPSIS</span></span>
<span data-ttu-id="25d9f-103">Сбор журналов из заданной Application-Insights приложения.</span><span class="sxs-lookup"><span data-stu-id="25d9f-103">Collect logs from given Application-Insights application.</span></span>

## <span data-ttu-id="25d9f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="25d9f-104">SYNTAX</span></span>

### <span data-ttu-id="25d9f-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="25d9f-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25d9f-106">ByWorkspaceObjectByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="25d9f-106">ByWorkspaceObjectByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25d9f-107">ByWorkspaceObjectByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="25d9f-107">ByWorkspaceObjectByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25d9f-108">ByWorkspaceNameByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="25d9f-108">ByWorkspaceNameByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25d9f-109">ByWorkspaceNameByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="25d9f-109">ByWorkspaceNameByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25d9f-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25d9f-110">DESCRIPTION</span></span>
<span data-ttu-id="25d9f-111">Командлет **New-AzOperationalInsightsApplicationInsightsDataSource** включает сбор журналов из заданной Application-Insights приложения.</span><span class="sxs-lookup"><span data-stu-id="25d9f-111">The **New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet enables the collection of logs from a given Application-Insights application.</span></span>

## <span data-ttu-id="25d9f-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="25d9f-112">EXAMPLES</span></span>

### <span data-ttu-id="25d9f-113">Пример 1: создание источника данных Application-Insights в рабочей области</span><span class="sxs-lookup"><span data-stu-id="25d9f-113">Example 1: Create application-insights data source in workspace</span></span>
```
PS C:\> New-AzOperationalInsightsApplicationInsightsDataSource -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -ApplicationSubscriptionId "e791a474-ee54-46a2-bb06-5e058302d234" -ApplicationResourceGroupName "ContosoResourceGroup" -ApplicationName "MyAIApplication"

Name              : subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="25d9f-114">Эта команда создает источник данных Application-Insights для данного приложения в указанной рабочей области для анализа журналов.</span><span class="sxs-lookup"><span data-stu-id="25d9f-114">This command creates an application-insights data source of a given application in a given log analytics workspace.</span></span> <span data-ttu-id="25d9f-115">Это обеспечивает сбор журналов из данного приложения в рабочую область "анализ журналов".</span><span class="sxs-lookup"><span data-stu-id="25d9f-115">This enables the collection of logs from given application to the log analytics workspace.</span></span>

### <span data-ttu-id="25d9f-116">Пример 2: получение объекта Workspace и создание источника данных Application-Insight с помощью идентификатора ресурса приложения</span><span class="sxs-lookup"><span data-stu-id="25d9f-116">Example 2: Get workspace object and create application-insights data source by the application resource id</span></span>
```
PS C:\> Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup" | New-AzOperationalInsightsApplicationInsightsDataSource -ApplicationResourceId "/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication"

Name              : subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="25d9f-117">В этой команде показано, как получить объект рабочей области для аналитики журнала и затем передать выходные данные, чтобы создать соответствующий источник данных Application Insights с помощью идентификатора ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="25d9f-117">This command demonstrates getting a log analytics workspace object and then passing the output to create an associated application-insights data source by the application resource id.</span></span> 

## <span data-ttu-id="25d9f-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="25d9f-118">PARAMETERS</span></span>

### <span data-ttu-id="25d9f-119">-ИмяПриложения</span><span class="sxs-lookup"><span data-stu-id="25d9f-119">-ApplicationName</span></span>
<span data-ttu-id="25d9f-120">Имя связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="25d9f-120">The name of the linked application.</span></span>

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

### <span data-ttu-id="25d9f-121">-ApplicationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25d9f-121">-ApplicationResourceGroupName</span></span>
<span data-ttu-id="25d9f-122">Имя группы ресурсов связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="25d9f-122">The resource group name of the linked application.</span></span>

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

### <span data-ttu-id="25d9f-123">-ApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="25d9f-123">-ApplicationResourceId</span></span>
<span data-ttu-id="25d9f-124">Идентификатор ресурса связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="25d9f-124">The linked application resource id.</span></span>

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

### <span data-ttu-id="25d9f-125">-ApplicationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="25d9f-125">-ApplicationSubscriptionId</span></span>
<span data-ttu-id="25d9f-126">Идентификатор подписки связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="25d9f-126">The subscription id of the linked application.</span></span>

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

### <span data-ttu-id="25d9f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25d9f-127">-DefaultProfile</span></span>
<span data-ttu-id="25d9f-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="25d9f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25d9f-129">-Force</span><span class="sxs-lookup"><span data-stu-id="25d9f-129">-Force</span></span>
<span data-ttu-id="25d9f-130">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="25d9f-130">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="25d9f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25d9f-131">-ResourceGroupName</span></span>
<span data-ttu-id="25d9f-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="25d9f-132">The resource group name.</span></span>

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

### <span data-ttu-id="25d9f-133">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="25d9f-133">-Workspace</span></span>
<span data-ttu-id="25d9f-134">Рабочая область, в которой будет находиться источник данных.</span><span class="sxs-lookup"><span data-stu-id="25d9f-134">The workspace that will contain the data source.</span></span>

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

### <span data-ttu-id="25d9f-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="25d9f-135">-WorkspaceName</span></span>
<span data-ttu-id="25d9f-136">Имя рабочей области, в которой будет находиться источник данных.</span><span class="sxs-lookup"><span data-stu-id="25d9f-136">The name of the workspace that will contain the data source.</span></span>

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

### <span data-ttu-id="25d9f-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25d9f-137">-Confirm</span></span>
<span data-ttu-id="25d9f-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="25d9f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25d9f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25d9f-139">-WhatIf</span></span>
<span data-ttu-id="25d9f-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="25d9f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25d9f-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="25d9f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25d9f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d9f-142">CommonParameters</span></span>
<span data-ttu-id="25d9f-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="25d9f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d9f-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25d9f-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d9f-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="25d9f-145">INPUTS</span></span>

### <span data-ttu-id="25d9f-146">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="25d9f-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="25d9f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="25d9f-147">System.String</span></span>

## <span data-ttu-id="25d9f-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25d9f-148">OUTPUTS</span></span>

### <span data-ttu-id="25d9f-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="25d9f-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="25d9f-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="25d9f-150">NOTES</span></span>

## <span data-ttu-id="25d9f-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25d9f-151">RELATED LINKS</span></span>
