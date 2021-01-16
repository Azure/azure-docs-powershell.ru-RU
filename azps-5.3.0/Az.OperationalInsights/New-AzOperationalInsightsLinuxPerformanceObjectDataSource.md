---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 656d25e69e2739df7e196ba9e584c3890bf4028f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506826"
---
# <span data-ttu-id="e2be2-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="e2be2-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="e2be2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2be2-102">SYNOPSIS</span></span>
<span data-ttu-id="e2be2-103">Добавляет счетчики производительности на все компьютеры Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e2be2-103">Adds performance counters to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="e2be2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e2be2-104">SYNTAX</span></span>

### <span data-ttu-id="e2be2-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e2be2-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2be2-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e2be2-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2be2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2be2-107">DESCRIPTION</span></span>
<span data-ttu-id="e2be2-108">**Новый-AzOperationalInsightsLinuxPerformanceObjectDataSource** добавляет счетчики производительности, из которых Azure Operational Insights собирает данные на всех компьютерах Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e2be2-108">The **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="e2be2-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e2be2-109">EXAMPLES</span></span>

## <span data-ttu-id="e2be2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2be2-110">PARAMETERS</span></span>

### <span data-ttu-id="e2be2-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="e2be2-111">-CounterNames</span></span>
<span data-ttu-id="e2be2-112">Определяет массив имен счетчиков.</span><span class="sxs-lookup"><span data-stu-id="e2be2-112">Specifies an array of names of counters.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2be2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2be2-113">-DefaultProfile</span></span>
<span data-ttu-id="e2be2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e2be2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2be2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e2be2-115">-Force</span></span>
<span data-ttu-id="e2be2-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="e2be2-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e2be2-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e2be2-117">-InstanceName</span></span>
<span data-ttu-id="e2be2-118">Указывает имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e2be2-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="e2be2-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="e2be2-119">-IntervalSeconds</span></span>
<span data-ttu-id="e2be2-120">Определяет интервал сбора.</span><span class="sxs-lookup"><span data-stu-id="e2be2-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="e2be2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e2be2-121">-Name</span></span>
<span data-ttu-id="e2be2-122">Указывает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="e2be2-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="e2be2-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="e2be2-123">-ObjectName</span></span>
<span data-ttu-id="e2be2-124">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="e2be2-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="e2be2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2be2-125">-ResourceGroupName</span></span>
<span data-ttu-id="e2be2-126">Имя группы ресурсов, которая содержит компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="e2be2-126">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="e2be2-127">-Workspace</span><span class="sxs-lookup"><span data-stu-id="e2be2-127">-Workspace</span></span>
<span data-ttu-id="e2be2-128">Определяет рабочее пространство, в котором выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2be2-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e2be2-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e2be2-129">-WorkspaceName</span></span>
<span data-ttu-id="e2be2-130">Указывает имя рабочей области, в которой выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2be2-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e2be2-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2be2-131">-Confirm</span></span>
<span data-ttu-id="e2be2-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e2be2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2be2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2be2-133">-WhatIf</span></span>
<span data-ttu-id="e2be2-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2be2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2be2-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e2be2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2be2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2be2-136">CommonParameters</span></span>
<span data-ttu-id="e2be2-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2be2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2be2-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2be2-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2be2-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2be2-139">INPUTS</span></span>

### <span data-ttu-id="e2be2-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e2be2-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="e2be2-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e2be2-141">System.String</span></span>

### <span data-ttu-id="e2be2-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e2be2-142">System.String[]</span></span>

### <span data-ttu-id="e2be2-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e2be2-143">System.Int32</span></span>

## <span data-ttu-id="e2be2-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e2be2-144">OUTPUTS</span></span>

### <span data-ttu-id="e2be2-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="e2be2-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="e2be2-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e2be2-146">NOTES</span></span>

## <span data-ttu-id="e2be2-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2be2-147">RELATED LINKS</span></span>

[<span data-ttu-id="e2be2-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="e2be2-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="e2be2-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="e2be2-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)

