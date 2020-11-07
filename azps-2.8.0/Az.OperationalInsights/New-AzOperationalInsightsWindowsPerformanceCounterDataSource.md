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
ms.locfileid: "93904654"
---
# <span data-ttu-id="f0080-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="f0080-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="f0080-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0080-102">SYNOPSIS</span></span>
<span data-ttu-id="f0080-103">Добавляет источник данных счетчика производительности Windows для подключенных компьютеров, работающих под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="f0080-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="f0080-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0080-104">SYNTAX</span></span>

### <span data-ttu-id="f0080-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f0080-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0080-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f0080-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0080-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0080-107">DESCRIPTION</span></span>
<span data-ttu-id="f0080-108">Командлет **New-AzOperationalInsightsWindowsPerformanceCounterDataSource** добавляет источник данных счетчика производительности Windows для подключенных компьютеров, работающих под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="f0080-108">The **New-AzOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="f0080-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0080-109">EXAMPLES</span></span>

## <span data-ttu-id="f0080-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0080-110">PARAMETERS</span></span>

### <span data-ttu-id="f0080-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="f0080-111">-CounterName</span></span>
<span data-ttu-id="f0080-112">Указывает имя счетчика.</span><span class="sxs-lookup"><span data-stu-id="f0080-112">Specifies the name of a counter.</span></span>

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

### <span data-ttu-id="f0080-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0080-113">-DefaultProfile</span></span>
<span data-ttu-id="f0080-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f0080-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0080-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f0080-115">-Force</span></span>
<span data-ttu-id="f0080-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f0080-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f0080-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="f0080-117">-InstanceName</span></span>
<span data-ttu-id="f0080-118">Указывает имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f0080-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="f0080-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="f0080-119">-IntervalSeconds</span></span>
<span data-ttu-id="f0080-120">Указывает интервал сбора.</span><span class="sxs-lookup"><span data-stu-id="f0080-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="f0080-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f0080-121">-Name</span></span>
<span data-ttu-id="f0080-122">Задает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="f0080-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="f0080-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="f0080-123">-ObjectName</span></span>
<span data-ttu-id="f0080-124">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="f0080-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="f0080-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0080-125">-ResourceGroupName</span></span>
<span data-ttu-id="f0080-126">Указывает имя группы ресурсов, содержащей компьютеры.</span><span class="sxs-lookup"><span data-stu-id="f0080-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="f0080-127">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="f0080-127">-UseLegacyCollector</span></span>
<span data-ttu-id="f0080-128">Использование устаревшего сборщика или сборщика по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f0080-128">Use legacy collector or the default collector.</span></span>

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

### <span data-ttu-id="f0080-129">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="f0080-129">-Workspace</span></span>
<span data-ttu-id="f0080-130">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f0080-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="f0080-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f0080-131">-WorkspaceName</span></span>
<span data-ttu-id="f0080-132">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f0080-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="f0080-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0080-133">-Confirm</span></span>
<span data-ttu-id="f0080-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f0080-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0080-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0080-135">-WhatIf</span></span>
<span data-ttu-id="f0080-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f0080-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0080-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f0080-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0080-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0080-138">CommonParameters</span></span>
<span data-ttu-id="f0080-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0080-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0080-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0080-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0080-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0080-141">INPUTS</span></span>

### <span data-ttu-id="f0080-142">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="f0080-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="f0080-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f0080-143">System.String</span></span>

### <span data-ttu-id="f0080-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f0080-144">System.Int32</span></span>

## <span data-ttu-id="f0080-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0080-145">OUTPUTS</span></span>

### <span data-ttu-id="f0080-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="f0080-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="f0080-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0080-147">NOTES</span></span>

## <span data-ttu-id="f0080-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0080-148">RELATED LINKS</span></span>
