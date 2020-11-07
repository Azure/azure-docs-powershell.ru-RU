---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E3D7A3FE-40D4-4495-BA39-493F85F304AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsapplicationinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
ms.openlocfilehash: 92ef4802ce842fa88389da19f1b5ba1aacf84b3e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729851"
---
# <span data-ttu-id="c894e-101">New-AzOperationalInsightsApplicationInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="c894e-101">New-AzOperationalInsightsApplicationInsightsDataSource</span></span>

## <span data-ttu-id="c894e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c894e-102">SYNOPSIS</span></span>
<span data-ttu-id="c894e-103">Сбор журналов из заданной Application-Insights приложения.</span><span class="sxs-lookup"><span data-stu-id="c894e-103">Collect logs from given Application-Insights application.</span></span>

## <span data-ttu-id="c894e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c894e-104">SYNTAX</span></span>

### <span data-ttu-id="c894e-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c894e-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c894e-106">ByWorkspaceObjectByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="c894e-106">ByWorkspaceObjectByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c894e-107">ByWorkspaceObjectByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="c894e-107">ByWorkspaceObjectByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c894e-108">ByWorkspaceNameByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="c894e-108">ByWorkspaceNameByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c894e-109">ByWorkspaceNameByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="c894e-109">ByWorkspaceNameByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c894e-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c894e-110">DESCRIPTION</span></span>
<span data-ttu-id="c894e-111">Командлет **New-AzOperationalInsightsApplicationInsightsDataSource** включает сбор журналов из заданной Application-Insights приложения.</span><span class="sxs-lookup"><span data-stu-id="c894e-111">The **New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet enables the collection of logs from a given Application-Insights application.</span></span>

## <span data-ttu-id="c894e-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c894e-112">EXAMPLES</span></span>

### <span data-ttu-id="c894e-113">Пример 1: создание источника данных Application-Insights в рабочей области</span><span class="sxs-lookup"><span data-stu-id="c894e-113">Example 1: Create application-insights data source in workspace</span></span>
```
PS C:\> New-AzOperationalInsightsApplicationInsightsDataSource -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -ApplicationSubscriptionId "e791a474-ee54-46a2-bb06-5e058302d234" -ApplicationResourceGroupName "ContosoResourceGroup" -ApplicationName "MyAIApplication"

Name              : subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="c894e-114">Эта команда создает источник данных Application-Insights для данного приложения в данной службе аналитики журнала workpsace.</span><span class="sxs-lookup"><span data-stu-id="c894e-114">This command creates an application-insights data source of a given application in a given log analytics workpsace.</span></span> <span data-ttu-id="c894e-115">Это позволяет коллекции журналов из данного приложения в службе аналитики журнала workpsace.</span><span class="sxs-lookup"><span data-stu-id="c894e-115">This enables the collection of logs from given application to the log analytics workpsace.</span></span>

### <span data-ttu-id="c894e-116">Пример 2: получение объекта Workspace и создание источника данных Application-Insight с помощью идентификатора ресурса приложения</span><span class="sxs-lookup"><span data-stu-id="c894e-116">Example 2: Get workspace object and create application-insights data source by the application resource id</span></span>
```
PS C:\> Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup" | New-AzOperationalInsightsApplicationInsightsDataSource -ApplicationResourceId "/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication"

Name              : subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="c894e-117">В этой команде показано, как получить объект рабочей области для аналитики журнала и затем передать выходные данные, чтобы создать соответствующий источник данных Application Insights с помощью идентификатора ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="c894e-117">This command demonstrates getting a log analytics workspace object and then passing the output to create an associated application-insights data source by the application resource id.</span></span> 

## <span data-ttu-id="c894e-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c894e-118">PARAMETERS</span></span>

### <span data-ttu-id="c894e-119">-ИмяПриложения</span><span class="sxs-lookup"><span data-stu-id="c894e-119">-ApplicationName</span></span>
<span data-ttu-id="c894e-120">Имя связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="c894e-120">The name of the linked application.</span></span>

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

### <span data-ttu-id="c894e-121">-ApplicationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c894e-121">-ApplicationResourceGroupName</span></span>
<span data-ttu-id="c894e-122">Имя группы ресурсов связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="c894e-122">The resource group name of the linked application.</span></span>

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

### <span data-ttu-id="c894e-123">-ApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="c894e-123">-ApplicationResourceId</span></span>
<span data-ttu-id="c894e-124">Идентификатор ресурса связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="c894e-124">The linked application resource id.</span></span>

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

### <span data-ttu-id="c894e-125">-ApplicationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c894e-125">-ApplicationSubscriptionId</span></span>
<span data-ttu-id="c894e-126">Идентификатор подписки связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="c894e-126">The subscription id of the linked application.</span></span>

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

### <span data-ttu-id="c894e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c894e-127">-DefaultProfile</span></span>
<span data-ttu-id="c894e-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c894e-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c894e-129">-Force</span><span class="sxs-lookup"><span data-stu-id="c894e-129">-Force</span></span>
<span data-ttu-id="c894e-130">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="c894e-130">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c894e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c894e-131">-ResourceGroupName</span></span>
<span data-ttu-id="c894e-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c894e-132">The resource group name.</span></span>

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

### <span data-ttu-id="c894e-133">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="c894e-133">-Workspace</span></span>
<span data-ttu-id="c894e-134">Рабочая область, в которой будет находиться источник данных.</span><span class="sxs-lookup"><span data-stu-id="c894e-134">The workspace that will contain the data source.</span></span>

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

### <span data-ttu-id="c894e-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c894e-135">-WorkspaceName</span></span>
<span data-ttu-id="c894e-136">Имя рабочей области, в которой будет находиться источник данных.</span><span class="sxs-lookup"><span data-stu-id="c894e-136">The name of the workspace that will contain the data source.</span></span>

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

### <span data-ttu-id="c894e-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c894e-137">-Confirm</span></span>
<span data-ttu-id="c894e-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c894e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c894e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c894e-139">-WhatIf</span></span>
<span data-ttu-id="c894e-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c894e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c894e-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c894e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c894e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c894e-142">CommonParameters</span></span>
<span data-ttu-id="c894e-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c894e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c894e-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c894e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c894e-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c894e-145">INPUTS</span></span>

### <span data-ttu-id="c894e-146">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c894e-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="c894e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="c894e-147">System.String</span></span>

## <span data-ttu-id="c894e-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c894e-148">OUTPUTS</span></span>

### <span data-ttu-id="c894e-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="c894e-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="c894e-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="c894e-150">NOTES</span></span>

## <span data-ttu-id="c894e-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c894e-151">RELATED LINKS</span></span>
