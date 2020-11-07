---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 4230eadc005ca53600feb2e6bc7ee2e001d7b209
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729842"
---
# <span data-ttu-id="ed90f-101">New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="ed90f-101">New-AzOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="ed90f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed90f-102">SYNOPSIS</span></span>
<span data-ttu-id="ed90f-103">Сбор журналов событий на компьютерах под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="ed90f-103">Collects event logs from computers that run the Windows operating system.</span></span>

## <span data-ttu-id="ed90f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed90f-104">SYNTAX</span></span>

### <span data-ttu-id="ed90f-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ed90f-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed90f-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ed90f-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed90f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed90f-107">DESCRIPTION</span></span>
<span data-ttu-id="ed90f-108">Командлет **New-AzOperationalInsightsWindowsEventDataSource** добавляет источник данных, который собирает журналы событий Windows из подключенных компьютеров, работающих под управлением операционной системы Windows в Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="ed90f-108">The **New-AzOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="ed90f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed90f-109">EXAMPLES</span></span>

## <span data-ttu-id="ed90f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed90f-110">PARAMETERS</span></span>

### <span data-ttu-id="ed90f-111">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="ed90f-111">-CollectErrors</span></span>
<span data-ttu-id="ed90f-112">Указывает на то, что оперативная аналитика собирает сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="ed90f-112">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="ed90f-113">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="ed90f-113">-CollectInformation</span></span>
<span data-ttu-id="ed90f-114">Указывает, что оперативная аналитика собирает информационные сообщения.</span><span class="sxs-lookup"><span data-stu-id="ed90f-114">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="ed90f-115">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="ed90f-115">-CollectWarnings</span></span>
<span data-ttu-id="ed90f-116">Указывает, что оперативная аналитика собирает предупреждающие сообщения.</span><span class="sxs-lookup"><span data-stu-id="ed90f-116">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="ed90f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed90f-117">-DefaultProfile</span></span>
<span data-ttu-id="ed90f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ed90f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed90f-119">-EventLogName</span><span class="sxs-lookup"><span data-stu-id="ed90f-119">-EventLogName</span></span>
<span data-ttu-id="ed90f-120">Указывает имя журнала событий.</span><span class="sxs-lookup"><span data-stu-id="ed90f-120">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="ed90f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ed90f-121">-Force</span></span>
<span data-ttu-id="ed90f-122">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ed90f-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ed90f-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ed90f-123">-Name</span></span>
<span data-ttu-id="ed90f-124">Задает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="ed90f-124">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="ed90f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed90f-125">-ResourceGroupName</span></span>
<span data-ttu-id="ed90f-126">Указывает имя группы ресурсов, содержащей компьютеры.</span><span class="sxs-lookup"><span data-stu-id="ed90f-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="ed90f-127">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="ed90f-127">-Workspace</span></span>
<span data-ttu-id="ed90f-128">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ed90f-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ed90f-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ed90f-129">-WorkspaceName</span></span>
<span data-ttu-id="ed90f-130">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ed90f-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ed90f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed90f-131">-Confirm</span></span>
<span data-ttu-id="ed90f-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ed90f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed90f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed90f-133">-WhatIf</span></span>
<span data-ttu-id="ed90f-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ed90f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed90f-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ed90f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed90f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed90f-136">CommonParameters</span></span>
<span data-ttu-id="ed90f-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed90f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed90f-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed90f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed90f-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed90f-139">INPUTS</span></span>

### <span data-ttu-id="ed90f-140">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ed90f-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="ed90f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ed90f-141">System.String</span></span>

## <span data-ttu-id="ed90f-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed90f-142">OUTPUTS</span></span>

### <span data-ttu-id="ed90f-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="ed90f-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="ed90f-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed90f-144">NOTES</span></span>

## <span data-ttu-id="ed90f-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed90f-145">RELATED LINKS</span></span>
