---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: a1f37a96d5be5443d2fb28c5a52964dd1612fc6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565823"
---
# <span data-ttu-id="aee61-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="aee61-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="aee61-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aee61-102">SYNOPSIS</span></span>
<span data-ttu-id="aee61-103">Добавляет счетчики производительности на все компьютеры Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="aee61-103">Adds performance counters to all Linux computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aee61-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aee61-104">SYNTAX</span></span>

### <span data-ttu-id="aee61-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aee61-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aee61-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="aee61-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aee61-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aee61-107">DESCRIPTION</span></span>
<span data-ttu-id="aee61-108">Командлет **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** добавляет счетчики производительности, с помощью которых оперативная аналитика Azure собирает данные на все компьютеры Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="aee61-108">The **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="aee61-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aee61-109">EXAMPLES</span></span>

## <span data-ttu-id="aee61-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aee61-110">PARAMETERS</span></span>

### <span data-ttu-id="aee61-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="aee61-111">-CounterNames</span></span>
<span data-ttu-id="aee61-112">Указывает массив имен счетчиков.</span><span class="sxs-lookup"><span data-stu-id="aee61-112">Specifies an array of names of counters.</span></span>

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

### <span data-ttu-id="aee61-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aee61-113">-DefaultProfile</span></span>
<span data-ttu-id="aee61-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="aee61-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aee61-115">-Force</span><span class="sxs-lookup"><span data-stu-id="aee61-115">-Force</span></span>
<span data-ttu-id="aee61-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="aee61-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aee61-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="aee61-117">-InstanceName</span></span>
<span data-ttu-id="aee61-118">Указывает имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="aee61-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="aee61-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="aee61-119">-IntervalSeconds</span></span>
<span data-ttu-id="aee61-120">Указывает интервал сбора.</span><span class="sxs-lookup"><span data-stu-id="aee61-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="aee61-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aee61-121">-Name</span></span>
<span data-ttu-id="aee61-122">Задает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="aee61-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="aee61-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="aee61-123">-ObjectName</span></span>
<span data-ttu-id="aee61-124">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="aee61-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="aee61-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aee61-125">-ResourceGroupName</span></span>
<span data-ttu-id="aee61-126">Указывает имя группы ресурсов, которая содержит компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="aee61-126">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="aee61-127">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="aee61-127">-Workspace</span></span>
<span data-ttu-id="aee61-128">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="aee61-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="aee61-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="aee61-129">-WorkspaceName</span></span>
<span data-ttu-id="aee61-130">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="aee61-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="aee61-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aee61-131">-Confirm</span></span>
<span data-ttu-id="aee61-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aee61-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aee61-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aee61-133">-WhatIf</span></span>
<span data-ttu-id="aee61-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aee61-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aee61-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aee61-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aee61-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aee61-136">CommonParameters</span></span>
<span data-ttu-id="aee61-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aee61-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aee61-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aee61-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aee61-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aee61-139">INPUTS</span></span>

### <span data-ttu-id="aee61-140">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="aee61-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="aee61-141">Параметры: Workspace (ByValue)</span><span class="sxs-lookup"><span data-stu-id="aee61-141">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="aee61-142">System. String</span><span class="sxs-lookup"><span data-stu-id="aee61-142">System.String</span></span>

### <span data-ttu-id="aee61-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="aee61-143">System.String[]</span></span>

### <span data-ttu-id="aee61-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="aee61-144">System.Int32</span></span>

## <span data-ttu-id="aee61-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aee61-145">OUTPUTS</span></span>

### <span data-ttu-id="aee61-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="aee61-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="aee61-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="aee61-147">NOTES</span></span>

## <span data-ttu-id="aee61-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aee61-148">RELATED LINKS</span></span>

[<span data-ttu-id="aee61-149">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="aee61-149">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="aee61-150">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="aee61-150">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)


