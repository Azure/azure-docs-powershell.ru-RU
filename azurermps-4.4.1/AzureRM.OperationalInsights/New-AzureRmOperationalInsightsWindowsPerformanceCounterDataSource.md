---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: dfdea6498ac7f553dafeea186a8b60f157cbd904
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732428"
---
# <span data-ttu-id="79fe6-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="79fe6-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="79fe6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79fe6-102">SYNOPSIS</span></span>
<span data-ttu-id="79fe6-103">Добавляет источник данных счетчика производительности Windows для подключенных компьютеров, работающих под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="79fe6-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79fe6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79fe6-104">SYNTAX</span></span>

### <span data-ttu-id="79fe6-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="79fe6-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79fe6-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="79fe6-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79fe6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79fe6-107">DESCRIPTION</span></span>
<span data-ttu-id="79fe6-108">Командлет **New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** добавляет источник данных счетчика производительности Windows для подключенных компьютеров, работающих под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="79fe6-108">The **New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="79fe6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79fe6-109">EXAMPLES</span></span>

## <span data-ttu-id="79fe6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79fe6-110">PARAMETERS</span></span>

### <span data-ttu-id="79fe6-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="79fe6-111">-CounterName</span></span>
<span data-ttu-id="79fe6-112">Указывает имя счетчика.</span><span class="sxs-lookup"><span data-stu-id="79fe6-112">Specifies the name of a counter.</span></span>

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

### <span data-ttu-id="79fe6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="79fe6-113">-Force</span></span>
<span data-ttu-id="79fe6-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="79fe6-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="79fe6-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="79fe6-115">-InstanceName</span></span>
<span data-ttu-id="79fe6-116">Указывает имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="79fe6-116">Specifies an instance name.</span></span>

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

### <span data-ttu-id="79fe6-117">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="79fe6-117">-IntervalSeconds</span></span>
<span data-ttu-id="79fe6-118">Указывает интервал сбора.</span><span class="sxs-lookup"><span data-stu-id="79fe6-118">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="79fe6-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="79fe6-119">-Name</span></span>
<span data-ttu-id="79fe6-120">Задает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="79fe6-120">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="79fe6-121">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="79fe6-121">-ObjectName</span></span>
<span data-ttu-id="79fe6-122">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="79fe6-122">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="79fe6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79fe6-123">-ResourceGroupName</span></span>
<span data-ttu-id="79fe6-124">Указывает имя группы ресурсов, содержащей компьютеры.</span><span class="sxs-lookup"><span data-stu-id="79fe6-124">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="79fe6-125">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="79fe6-125">-UseLegacyCollector</span></span>
<span data-ttu-id="79fe6-126">Использование устаревшего сборщика или сборщика по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="79fe6-126">Use legacy collector or the default collector.</span></span>

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

### <span data-ttu-id="79fe6-127">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="79fe6-127">-Workspace</span></span>
<span data-ttu-id="79fe6-128">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="79fe6-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="79fe6-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="79fe6-129">-WorkspaceName</span></span>
<span data-ttu-id="79fe6-130">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="79fe6-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="79fe6-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79fe6-131">-Confirm</span></span>
<span data-ttu-id="79fe6-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="79fe6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79fe6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79fe6-133">-WhatIf</span></span>
<span data-ttu-id="79fe6-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="79fe6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79fe6-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="79fe6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79fe6-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79fe6-136">-DefaultProfile</span></span>
<span data-ttu-id="79fe6-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79fe6-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79fe6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79fe6-138">CommonParameters</span></span>
<span data-ttu-id="79fe6-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79fe6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79fe6-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79fe6-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79fe6-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79fe6-141">INPUTS</span></span>

### <span data-ttu-id="79fe6-142">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="79fe6-142">PSWorkspace</span></span>
<span data-ttu-id="79fe6-143">Параметр "Рабочая область" принимает значение типа "PSWorkspace" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="79fe6-143">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="79fe6-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79fe6-144">OUTPUTS</span></span>

### <span data-ttu-id="79fe6-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="79fe6-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="79fe6-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="79fe6-146">NOTES</span></span>

## <span data-ttu-id="79fe6-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79fe6-147">RELATED LINKS</span></span>

