---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightswindowsperformancecounterdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: 2e3cd573c337d7ff13401939aaf127fa64a6c765
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989887"
---
# <span data-ttu-id="e24e2-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="e24e2-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="e24e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e24e2-102">SYNOPSIS</span></span>
<span data-ttu-id="e24e2-103">Добавляет счетчик производительности Windows для подключенных компьютеров, на которые работает операционная система Windows.</span><span class="sxs-lookup"><span data-stu-id="e24e2-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="e24e2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e24e2-104">SYNTAX</span></span>

### <span data-ttu-id="e24e2-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e24e2-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e24e2-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e24e2-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e24e2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e24e2-107">DESCRIPTION</span></span>
<span data-ttu-id="e24e2-108">**Новый-AzOperationalInsightsWindowsPerformanceCounterDataSource** добавляет источник данных счетчика производительности Windows для подключенных компьютеров, на которые работает операционная система Windows.</span><span class="sxs-lookup"><span data-stu-id="e24e2-108">The **New-AzOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="e24e2-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e24e2-109">EXAMPLES</span></span>

## <span data-ttu-id="e24e2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e24e2-110">PARAMETERS</span></span>

### <span data-ttu-id="e24e2-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="e24e2-111">-CounterName</span></span>
<span data-ttu-id="e24e2-112">Указывает имя счетчика.</span><span class="sxs-lookup"><span data-stu-id="e24e2-112">Specifies the name of a counter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e24e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e24e2-113">-DefaultProfile</span></span>
<span data-ttu-id="e24e2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e24e2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e24e2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e24e2-115">-Force</span></span>
<span data-ttu-id="e24e2-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="e24e2-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e24e2-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e24e2-117">-InstanceName</span></span>
<span data-ttu-id="e24e2-118">Указывает имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e24e2-118">Specifies an instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e24e2-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="e24e2-119">-IntervalSeconds</span></span>
<span data-ttu-id="e24e2-120">Определяет интервал сбора.</span><span class="sxs-lookup"><span data-stu-id="e24e2-120">Specifies the interval of collection.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e24e2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e24e2-121">-Name</span></span>
<span data-ttu-id="e24e2-122">Указывает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="e24e2-122">Specifies a name for the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e24e2-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="e24e2-123">-ObjectName</span></span>
<span data-ttu-id="e24e2-124">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="e24e2-124">Specifies the name of an object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e24e2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e24e2-125">-ResourceGroupName</span></span>
<span data-ttu-id="e24e2-126">Имя группы ресурсов, которая содержит компьютеры.</span><span class="sxs-lookup"><span data-stu-id="e24e2-126">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e24e2-127">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="e24e2-127">-UseLegacyCollector</span></span>
<span data-ttu-id="e24e2-128">Используйте устаревший или стандартный сборщик.</span><span class="sxs-lookup"><span data-stu-id="e24e2-128">Use legacy collector or the default collector.</span></span>

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

### <span data-ttu-id="e24e2-129">-Workspace</span><span class="sxs-lookup"><span data-stu-id="e24e2-129">-Workspace</span></span>
<span data-ttu-id="e24e2-130">Определяет рабочее пространство, в котором выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e24e2-130">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e24e2-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e24e2-131">-WorkspaceName</span></span>
<span data-ttu-id="e24e2-132">Указывает имя рабочей области, в которой выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e24e2-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e24e2-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e24e2-133">-Confirm</span></span>
<span data-ttu-id="e24e2-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e24e2-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e24e2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e24e2-135">-WhatIf</span></span>
<span data-ttu-id="e24e2-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e24e2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e24e2-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e24e2-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e24e2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e24e2-138">CommonParameters</span></span>
<span data-ttu-id="e24e2-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e24e2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e24e2-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e24e2-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e24e2-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e24e2-141">INPUTS</span></span>

### <span data-ttu-id="e24e2-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e24e2-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="e24e2-143">System.String</span><span class="sxs-lookup"><span data-stu-id="e24e2-143">System.String</span></span>

### <span data-ttu-id="e24e2-144">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e24e2-144">System.Int32</span></span>

## <span data-ttu-id="e24e2-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e24e2-145">OUTPUTS</span></span>

### <span data-ttu-id="e24e2-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="e24e2-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="e24e2-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e24e2-147">NOTES</span></span>

## <span data-ttu-id="e24e2-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e24e2-148">RELATED LINKS</span></span>
