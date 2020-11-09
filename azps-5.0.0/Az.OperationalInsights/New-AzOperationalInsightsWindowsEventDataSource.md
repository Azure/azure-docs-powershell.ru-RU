---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 5d7c10227876c2ee5b8eeab12623457be0f64aa8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318962"
---
# <span data-ttu-id="ed7e0-101">New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="ed7e0-101">New-AzOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="ed7e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed7e0-102">SYNOPSIS</span></span>
<span data-ttu-id="ed7e0-103">Сбор журналов событий на компьютерах под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-103">Collects event logs from computers that run the Windows operating system.</span></span>

## <span data-ttu-id="ed7e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed7e0-104">SYNTAX</span></span>

### <span data-ttu-id="ed7e0-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ed7e0-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed7e0-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ed7e0-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed7e0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed7e0-107">DESCRIPTION</span></span>
<span data-ttu-id="ed7e0-108">Командлет **New-AzOperationalInsightsWindowsEventDataSource** добавляет источник данных, который собирает журналы событий Windows из подключенных компьютеров, работающих под управлением операционной системы Windows в Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-108">The **New-AzOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="ed7e0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed7e0-109">EXAMPLES</span></span>

### <span data-ttu-id="ed7e0-110">Пример 1: создание источника данных системных событий Windows</span><span class="sxs-lookup"><span data-stu-id="ed7e0-110">Example 1: Create system Windows event data source</span></span>
```
$EventLogNames       = @()
$EventLogNames      += 'Directory Service'
$EventLogNames      += 'Microsoft-Windows-EventCollector/Operational'
$EventLogNames      += 'System'
$ResourceGroupName   = 'MyResourceGroup'
$WorkspaceName       = 'MyWorkspaceName'

$Count = 0
foreach ($EventLogName in $EventLogNames) {
    $Count++
    $null = New-AzOperationalInsightsWindowsEventDataSource `
    -ResourceGroupName $ResourceGroupName `
    -WorkspaceName $WorkspaceName `
    -Name "Windows-event-$($Count)" `
    -EventLogName $EventLogName `
    -CollectErrors `
    -CollectWarnings `
    -CollectInformation
}

Get-AzOperationalInsightsDataSource `
   -ResourceGroupName $ResourceGroupName `
   -WorkspaceName $WorkspaceName `
   -Kind 'WindowsEvent'
```

## <span data-ttu-id="ed7e0-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed7e0-111">PARAMETERS</span></span>

### <span data-ttu-id="ed7e0-112">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="ed7e0-112">-CollectErrors</span></span>
<span data-ttu-id="ed7e0-113">Указывает на то, что оперативная аналитика собирает сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-113">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="ed7e0-114">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="ed7e0-114">-CollectInformation</span></span>
<span data-ttu-id="ed7e0-115">Указывает, что оперативная аналитика собирает информационные сообщения.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-115">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="ed7e0-116">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="ed7e0-116">-CollectWarnings</span></span>
<span data-ttu-id="ed7e0-117">Указывает, что оперативная аналитика собирает предупреждающие сообщения.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-117">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="ed7e0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed7e0-118">-DefaultProfile</span></span>
<span data-ttu-id="ed7e0-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ed7e0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed7e0-120">-EventLogName</span><span class="sxs-lookup"><span data-stu-id="ed7e0-120">-EventLogName</span></span>
<span data-ttu-id="ed7e0-121">Указывает имя журнала событий.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-121">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="ed7e0-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ed7e0-122">-Force</span></span>
<span data-ttu-id="ed7e0-123">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ed7e0-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ed7e0-124">-Name</span></span>
<span data-ttu-id="ed7e0-125">Задает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-125">Specifies a name for the data source.</span></span> <span data-ttu-id="ed7e0-126">Имя не отображается на портале Azure, и любая строка может быть использована в том случае, если она является уникальной.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-126">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="ed7e0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed7e0-127">-ResourceGroupName</span></span>
<span data-ttu-id="ed7e0-128">Указывает имя группы ресурсов, содержащей компьютеры.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-128">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="ed7e0-129">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="ed7e0-129">-Workspace</span></span>
<span data-ttu-id="ed7e0-130">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ed7e0-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ed7e0-131">-WorkspaceName</span></span>
<span data-ttu-id="ed7e0-132">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ed7e0-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed7e0-133">-Confirm</span></span>
<span data-ttu-id="ed7e0-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed7e0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed7e0-135">-WhatIf</span></span>
<span data-ttu-id="ed7e0-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed7e0-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed7e0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed7e0-138">CommonParameters</span></span>
<span data-ttu-id="ed7e0-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed7e0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed7e0-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed7e0-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed7e0-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed7e0-141">INPUTS</span></span>

### <span data-ttu-id="ed7e0-142">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ed7e0-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="ed7e0-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ed7e0-143">System.String</span></span>

## <span data-ttu-id="ed7e0-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed7e0-144">OUTPUTS</span></span>

### <span data-ttu-id="ed7e0-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="ed7e0-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="ed7e0-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed7e0-146">NOTES</span></span>

## <span data-ttu-id="ed7e0-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed7e0-147">RELATED LINKS</span></span>