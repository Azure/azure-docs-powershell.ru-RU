---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowsperformancecounterdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: e775f07249b9ec8a8987986d4e614e9fc66a25f8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729841"
---
# <span data-ttu-id="be956-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="be956-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="be956-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be956-102">SYNOPSIS</span></span>
<span data-ttu-id="be956-103">Добавляет источник данных счетчика производительности Windows для подключенных компьютеров, работающих под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="be956-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="be956-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be956-104">SYNTAX</span></span>

### <span data-ttu-id="be956-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="be956-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be956-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="be956-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be956-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be956-107">DESCRIPTION</span></span>
<span data-ttu-id="be956-108">Командлет **New-AzOperationalInsightsWindowsPerformanceCounterDataSource** добавляет источник данных счетчика производительности Windows для подключенных компьютеров, работающих под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="be956-108">The **New-AzOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="be956-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be956-109">EXAMPLES</span></span>

## <span data-ttu-id="be956-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be956-110">PARAMETERS</span></span>

### <span data-ttu-id="be956-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="be956-111">-CounterName</span></span>
<span data-ttu-id="be956-112">Указывает имя счетчика.</span><span class="sxs-lookup"><span data-stu-id="be956-112">Specifies the name of a counter.</span></span>

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

### <span data-ttu-id="be956-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be956-113">-DefaultProfile</span></span>
<span data-ttu-id="be956-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="be956-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be956-115">-Force</span><span class="sxs-lookup"><span data-stu-id="be956-115">-Force</span></span>
<span data-ttu-id="be956-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="be956-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="be956-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="be956-117">-InstanceName</span></span>
<span data-ttu-id="be956-118">Указывает имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="be956-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="be956-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="be956-119">-IntervalSeconds</span></span>
<span data-ttu-id="be956-120">Указывает интервал сбора.</span><span class="sxs-lookup"><span data-stu-id="be956-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="be956-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="be956-121">-Name</span></span>
<span data-ttu-id="be956-122">Задает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="be956-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="be956-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="be956-123">-ObjectName</span></span>
<span data-ttu-id="be956-124">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="be956-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="be956-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be956-125">-ResourceGroupName</span></span>
<span data-ttu-id="be956-126">Указывает имя группы ресурсов, содержащей компьютеры.</span><span class="sxs-lookup"><span data-stu-id="be956-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="be956-127">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="be956-127">-UseLegacyCollector</span></span>
<span data-ttu-id="be956-128">Использование устаревшего сборщика или сборщика по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="be956-128">Use legacy collector or the default collector.</span></span>

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

### <span data-ttu-id="be956-129">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="be956-129">-Workspace</span></span>
<span data-ttu-id="be956-130">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="be956-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="be956-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="be956-131">-WorkspaceName</span></span>
<span data-ttu-id="be956-132">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="be956-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="be956-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be956-133">-Confirm</span></span>
<span data-ttu-id="be956-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="be956-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be956-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be956-135">-WhatIf</span></span>
<span data-ttu-id="be956-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="be956-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be956-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="be956-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be956-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be956-138">CommonParameters</span></span>
<span data-ttu-id="be956-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be956-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be956-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be956-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be956-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be956-141">INPUTS</span></span>

### <span data-ttu-id="be956-142">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="be956-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="be956-143">System. String</span><span class="sxs-lookup"><span data-stu-id="be956-143">System.String</span></span>

### <span data-ttu-id="be956-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="be956-144">System.Int32</span></span>

## <span data-ttu-id="be956-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be956-145">OUTPUTS</span></span>

### <span data-ttu-id="be956-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="be956-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="be956-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="be956-147">NOTES</span></span>

## <span data-ttu-id="be956-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be956-148">RELATED LINKS</span></span>
