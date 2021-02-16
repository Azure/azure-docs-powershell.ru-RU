---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowsperformancecounterdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: 23154fe78b25ab469cc1f993af879c8b1e5bdad1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220793"
---
# <span data-ttu-id="f6817-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="f6817-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="f6817-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6817-102">SYNOPSIS</span></span>
<span data-ttu-id="f6817-103">Добавляет счетчик производительности Windows для подключенных компьютеров, на которые работает операционная система Windows.</span><span class="sxs-lookup"><span data-stu-id="f6817-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="f6817-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f6817-104">SYNTAX</span></span>

### <span data-ttu-id="f6817-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f6817-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6817-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f6817-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6817-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6817-107">DESCRIPTION</span></span>
<span data-ttu-id="f6817-108">**Новый-AzOperationalInsightsWindowsPerformanceCounterDataSource** добавляет источник данных счетчика производительности Windows для подключенных компьютеров, на которые работает операционная система Windows.</span><span class="sxs-lookup"><span data-stu-id="f6817-108">The **New-AzOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="f6817-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f6817-109">EXAMPLES</span></span>

## <span data-ttu-id="f6817-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6817-110">PARAMETERS</span></span>

### <span data-ttu-id="f6817-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="f6817-111">-CounterName</span></span>
<span data-ttu-id="f6817-112">Указывает имя счетчика.</span><span class="sxs-lookup"><span data-stu-id="f6817-112">Specifies the name of a counter.</span></span>

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

### <span data-ttu-id="f6817-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6817-113">-DefaultProfile</span></span>
<span data-ttu-id="f6817-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f6817-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6817-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f6817-115">-Force</span></span>
<span data-ttu-id="f6817-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="f6817-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f6817-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="f6817-117">-InstanceName</span></span>
<span data-ttu-id="f6817-118">Указывает имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f6817-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="f6817-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="f6817-119">-IntervalSeconds</span></span>
<span data-ttu-id="f6817-120">Определяет интервал сбора.</span><span class="sxs-lookup"><span data-stu-id="f6817-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="f6817-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f6817-121">-Name</span></span>
<span data-ttu-id="f6817-122">Указывает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="f6817-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="f6817-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="f6817-123">-ObjectName</span></span>
<span data-ttu-id="f6817-124">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="f6817-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="f6817-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6817-125">-ResourceGroupName</span></span>
<span data-ttu-id="f6817-126">Имя группы ресурсов, которая содержит компьютеры.</span><span class="sxs-lookup"><span data-stu-id="f6817-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="f6817-127">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="f6817-127">-UseLegacyCollector</span></span>
<span data-ttu-id="f6817-128">Используйте устаревший или стандартный сборщик.</span><span class="sxs-lookup"><span data-stu-id="f6817-128">Use legacy collector or the default collector.</span></span>

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

### <span data-ttu-id="f6817-129">-Workspace</span><span class="sxs-lookup"><span data-stu-id="f6817-129">-Workspace</span></span>
<span data-ttu-id="f6817-130">Определяет рабочее пространство, в котором выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6817-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="f6817-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f6817-131">-WorkspaceName</span></span>
<span data-ttu-id="f6817-132">Указывает имя рабочей области, в которой выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6817-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="f6817-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6817-133">-Confirm</span></span>
<span data-ttu-id="f6817-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f6817-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6817-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6817-135">-WhatIf</span></span>
<span data-ttu-id="f6817-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6817-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6817-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f6817-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6817-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6817-138">CommonParameters</span></span>
<span data-ttu-id="f6817-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6817-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6817-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6817-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6817-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6817-141">INPUTS</span></span>

### <span data-ttu-id="f6817-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="f6817-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="f6817-143">System.String</span><span class="sxs-lookup"><span data-stu-id="f6817-143">System.String</span></span>

### <span data-ttu-id="f6817-144">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f6817-144">System.Int32</span></span>

## <span data-ttu-id="f6817-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f6817-145">OUTPUTS</span></span>

### <span data-ttu-id="f6817-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="f6817-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="f6817-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f6817-147">NOTES</span></span>

## <span data-ttu-id="f6817-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6817-148">RELATED LINKS</span></span>
