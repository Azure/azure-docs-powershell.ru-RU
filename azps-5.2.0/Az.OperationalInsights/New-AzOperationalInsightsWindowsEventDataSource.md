---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 5d7c10227876c2ee5b8eeab12623457be0f64aa8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406223"
---
# <span data-ttu-id="ad8dc-101">New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="ad8dc-101">New-AzOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="ad8dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad8dc-102">SYNOPSIS</span></span>
<span data-ttu-id="ad8dc-103">Собирает журналы событий с компьютеров, на которые работает операционная система Windows.</span><span class="sxs-lookup"><span data-stu-id="ad8dc-103">Collects event logs from computers that run the Windows operating system.</span></span>

## <span data-ttu-id="ad8dc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ad8dc-104">SYNTAX</span></span>

### <span data-ttu-id="ad8dc-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ad8dc-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad8dc-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ad8dc-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad8dc-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad8dc-107">DESCRIPTION</span></span>
<span data-ttu-id="ad8dc-108">**Новый-AzOperationalInsightsWindowsEventDataSource** добавляет источник данных, который собирает журналы событий Windows с подключенных компьютеров, которые запускают операционную систему Windows в Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="ad8dc-108">The **New-AzOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="ad8dc-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ad8dc-109">EXAMPLES</span></span>

### <span data-ttu-id="ad8dc-110">Пример 1. Создание системного источника данных событий Windows</span><span class="sxs-lookup"><span data-stu-id="ad8dc-110">Example 1: Create system Windows event data source</span></span>
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

## <span data-ttu-id="ad8dc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad8dc-111">PARAMETERS</span></span>

### <span data-ttu-id="ad8dc-112">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="ad8dc-112">-CollectErrors</span></span>
<span data-ttu-id="ad8dc-113">Указывает на то, что операционная информация собирает сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="ad8dc-113">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="ad8dc-114">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="ad8dc-114">-CollectInformation</span></span>
<span data-ttu-id="ad8dc-115">Указывает на то, что операционная информация собирает сообщения.</span><span class="sxs-lookup"><span data-stu-id="ad8dc-115">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="ad8dc-116">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="ad8dc-116">-CollectWarnings</span></span>
<span data-ttu-id="ad8dc-117">Указывает на то, что операционная информация собирает предупреждающие сообщения.</span><span class="sxs-lookup"><span data-stu-id="ad8dc-117">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="ad8dc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad8dc-118">-DefaultProfile</span></span>
<span data-ttu-id="ad8dc-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ad8dc-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad8dc-120">-EventLogName</span><span class="sxs-lookup"><span data-stu-id="ad8dc-120">-EventLogName</span></span>
<span data-ttu-id="ad8dc-121">Указывает имя журнала событий.</span><span class="sxs-lookup"><span data-stu-id="ad8dc-121">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="ad8dc-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ad8dc-122">-Force</span></span>
<span data-ttu-id="ad8dc-123">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="ad8dc-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ad8dc-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ad8dc-124">-Name</span></span>
<span data-ttu-id="ad8dc-125">Указывает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="ad8dc-125">Specifies a name for the data source.</span></span> <span data-ttu-id="ad8dc-126">Имя не используется на портале Azure, и любую строку можно использовать, если она является уникальной.</span><span class="sxs-lookup"><span data-stu-id="ad8dc-126">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="ad8dc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad8dc-127">-ResourceGroupName</span></span>
<span data-ttu-id="ad8dc-128">Имя группы ресурсов, которая содержит компьютеры.</span><span class="sxs-lookup"><span data-stu-id="ad8dc-128">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="ad8dc-129">-Workspace</span><span class="sxs-lookup"><span data-stu-id="ad8dc-129">-Workspace</span></span>
<span data-ttu-id="ad8dc-130">Определяет рабочее пространство, в котором выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad8dc-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ad8dc-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ad8dc-131">-WorkspaceName</span></span>
<span data-ttu-id="ad8dc-132">Указывает имя рабочей области, в которой выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad8dc-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ad8dc-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad8dc-133">-Confirm</span></span>
<span data-ttu-id="ad8dc-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ad8dc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad8dc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad8dc-135">-WhatIf</span></span>
<span data-ttu-id="ad8dc-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad8dc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad8dc-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ad8dc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad8dc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad8dc-138">CommonParameters</span></span>
<span data-ttu-id="ad8dc-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad8dc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad8dc-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad8dc-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad8dc-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad8dc-141">INPUTS</span></span>

### <span data-ttu-id="ad8dc-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ad8dc-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="ad8dc-143">System.String</span><span class="sxs-lookup"><span data-stu-id="ad8dc-143">System.String</span></span>

## <span data-ttu-id="ad8dc-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ad8dc-144">OUTPUTS</span></span>

### <span data-ttu-id="ad8dc-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="ad8dc-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="ad8dc-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ad8dc-146">NOTES</span></span>

## <span data-ttu-id="ad8dc-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad8dc-147">RELATED LINKS</span></span>
