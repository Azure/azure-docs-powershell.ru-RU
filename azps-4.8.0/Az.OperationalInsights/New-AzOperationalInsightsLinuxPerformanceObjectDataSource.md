---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 656d25e69e2739df7e196ba9e584c3890bf4028f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235951"
---
# <span data-ttu-id="76260-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="76260-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="76260-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="76260-102">SYNOPSIS</span></span>
<span data-ttu-id="76260-103">Добавляет счетчики производительности на все компьютеры Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="76260-103">Adds performance counters to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="76260-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="76260-104">SYNTAX</span></span>

### <span data-ttu-id="76260-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="76260-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76260-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="76260-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76260-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76260-107">DESCRIPTION</span></span>
<span data-ttu-id="76260-108">Командлет **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** добавляет счетчики производительности, с помощью которых оперативная аналитика Azure собирает данные на все компьютеры Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="76260-108">The **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="76260-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="76260-109">EXAMPLES</span></span>

## <span data-ttu-id="76260-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="76260-110">PARAMETERS</span></span>

### <span data-ttu-id="76260-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="76260-111">-CounterNames</span></span>
<span data-ttu-id="76260-112">Указывает массив имен счетчиков.</span><span class="sxs-lookup"><span data-stu-id="76260-112">Specifies an array of names of counters.</span></span>

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

### <span data-ttu-id="76260-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76260-113">-DefaultProfile</span></span>
<span data-ttu-id="76260-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="76260-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76260-115">-Force</span><span class="sxs-lookup"><span data-stu-id="76260-115">-Force</span></span>
<span data-ttu-id="76260-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="76260-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="76260-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="76260-117">-InstanceName</span></span>
<span data-ttu-id="76260-118">Указывает имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="76260-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="76260-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="76260-119">-IntervalSeconds</span></span>
<span data-ttu-id="76260-120">Указывает интервал сбора.</span><span class="sxs-lookup"><span data-stu-id="76260-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="76260-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="76260-121">-Name</span></span>
<span data-ttu-id="76260-122">Задает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="76260-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="76260-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="76260-123">-ObjectName</span></span>
<span data-ttu-id="76260-124">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="76260-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="76260-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76260-125">-ResourceGroupName</span></span>
<span data-ttu-id="76260-126">Указывает имя группы ресурсов, которая содержит компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="76260-126">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="76260-127">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="76260-127">-Workspace</span></span>
<span data-ttu-id="76260-128">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="76260-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="76260-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="76260-129">-WorkspaceName</span></span>
<span data-ttu-id="76260-130">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="76260-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="76260-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76260-131">-Confirm</span></span>
<span data-ttu-id="76260-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="76260-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76260-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76260-133">-WhatIf</span></span>
<span data-ttu-id="76260-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="76260-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76260-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="76260-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76260-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76260-136">CommonParameters</span></span>
<span data-ttu-id="76260-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="76260-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76260-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76260-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76260-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="76260-139">INPUTS</span></span>

### <span data-ttu-id="76260-140">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="76260-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="76260-141">System. String</span><span class="sxs-lookup"><span data-stu-id="76260-141">System.String</span></span>

### <span data-ttu-id="76260-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="76260-142">System.String[]</span></span>

### <span data-ttu-id="76260-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="76260-143">System.Int32</span></span>

## <span data-ttu-id="76260-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="76260-144">OUTPUTS</span></span>

### <span data-ttu-id="76260-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="76260-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="76260-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="76260-146">NOTES</span></span>

## <span data-ttu-id="76260-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76260-147">RELATED LINKS</span></span>

[<span data-ttu-id="76260-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="76260-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="76260-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="76260-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)


