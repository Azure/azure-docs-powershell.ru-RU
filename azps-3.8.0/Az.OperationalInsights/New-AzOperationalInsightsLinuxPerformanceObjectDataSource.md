---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 656d25e69e2739df7e196ba9e584c3890bf4028f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065101"
---
# <span data-ttu-id="e7038-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="e7038-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="e7038-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7038-102">SYNOPSIS</span></span>
<span data-ttu-id="e7038-103">Добавляет счетчики производительности на все компьютеры Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e7038-103">Adds performance counters to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="e7038-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7038-104">SYNTAX</span></span>

### <span data-ttu-id="e7038-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e7038-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7038-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e7038-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7038-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7038-107">DESCRIPTION</span></span>
<span data-ttu-id="e7038-108">Командлет **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** добавляет счетчики производительности, с помощью которых оперативная аналитика Azure собирает данные на все компьютеры Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e7038-108">The **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="e7038-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7038-109">EXAMPLES</span></span>

## <span data-ttu-id="e7038-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7038-110">PARAMETERS</span></span>

### <span data-ttu-id="e7038-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="e7038-111">-CounterNames</span></span>
<span data-ttu-id="e7038-112">Указывает массив имен счетчиков.</span><span class="sxs-lookup"><span data-stu-id="e7038-112">Specifies an array of names of counters.</span></span>

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

### <span data-ttu-id="e7038-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7038-113">-DefaultProfile</span></span>
<span data-ttu-id="e7038-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e7038-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7038-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e7038-115">-Force</span></span>
<span data-ttu-id="e7038-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e7038-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e7038-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e7038-117">-InstanceName</span></span>
<span data-ttu-id="e7038-118">Указывает имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e7038-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="e7038-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="e7038-119">-IntervalSeconds</span></span>
<span data-ttu-id="e7038-120">Указывает интервал сбора.</span><span class="sxs-lookup"><span data-stu-id="e7038-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="e7038-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e7038-121">-Name</span></span>
<span data-ttu-id="e7038-122">Задает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="e7038-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="e7038-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="e7038-123">-ObjectName</span></span>
<span data-ttu-id="e7038-124">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="e7038-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="e7038-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7038-125">-ResourceGroupName</span></span>
<span data-ttu-id="e7038-126">Указывает имя группы ресурсов, которая содержит компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="e7038-126">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="e7038-127">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="e7038-127">-Workspace</span></span>
<span data-ttu-id="e7038-128">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e7038-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e7038-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e7038-129">-WorkspaceName</span></span>
<span data-ttu-id="e7038-130">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e7038-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e7038-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7038-131">-Confirm</span></span>
<span data-ttu-id="e7038-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e7038-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7038-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7038-133">-WhatIf</span></span>
<span data-ttu-id="e7038-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e7038-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7038-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e7038-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7038-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7038-136">CommonParameters</span></span>
<span data-ttu-id="e7038-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7038-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7038-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7038-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7038-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7038-139">INPUTS</span></span>

### <span data-ttu-id="e7038-140">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e7038-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="e7038-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e7038-141">System.String</span></span>

### <span data-ttu-id="e7038-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="e7038-142">System.String[]</span></span>

### <span data-ttu-id="e7038-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e7038-143">System.Int32</span></span>

## <span data-ttu-id="e7038-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7038-144">OUTPUTS</span></span>

### <span data-ttu-id="e7038-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="e7038-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="e7038-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7038-146">NOTES</span></span>

## <span data-ttu-id="e7038-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7038-147">RELATED LINKS</span></span>

[<span data-ttu-id="e7038-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="e7038-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="e7038-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="e7038-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)


