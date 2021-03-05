---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 900f8de58eaa8118c15a7d3ae1a2d88b0bdf59d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970483"
---
# <span data-ttu-id="606db-101">New-AzOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="606db-101">New-AzOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="606db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="606db-102">SYNOPSIS</span></span>
<span data-ttu-id="606db-103">Сбор журнала действий Azure из данной подписки.</span><span class="sxs-lookup"><span data-stu-id="606db-103">Collect Azure Activity log from given subscription.</span></span>

## <span data-ttu-id="606db-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="606db-104">SYNTAX</span></span>

### <span data-ttu-id="606db-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="606db-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="606db-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="606db-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="606db-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="606db-107">DESCRIPTION</span></span>
<span data-ttu-id="606db-108">Данные New-AzOperationalInsightsAzureActivityLogDataSource позволяют средству аналитики журналов собирать журнал действий Azure из данной подписки.</span><span class="sxs-lookup"><span data-stu-id="606db-108">The New-AzOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="606db-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="606db-109">EXAMPLES</span></span>

### <span data-ttu-id="606db-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="606db-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="606db-111">{{ Добавьте здесь описание примера }}</span><span class="sxs-lookup"><span data-stu-id="606db-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="606db-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="606db-112">PARAMETERS</span></span>

### <span data-ttu-id="606db-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="606db-113">-BackfillStartTime</span></span>
<span data-ttu-id="606db-114">Вы можете сделать это неделю назад.</span><span class="sxs-lookup"><span data-stu-id="606db-114">You can choose to backfill logs from a week ago.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="606db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="606db-115">-DefaultProfile</span></span>
<span data-ttu-id="606db-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="606db-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="606db-117">-Force</span><span class="sxs-lookup"><span data-stu-id="606db-117">-Force</span></span>
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

### <span data-ttu-id="606db-118">-Name</span><span class="sxs-lookup"><span data-stu-id="606db-118">-Name</span></span>
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

### <span data-ttu-id="606db-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="606db-119">-ResourceGroupName</span></span>
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

### <span data-ttu-id="606db-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="606db-120">-SubscriptionId</span></span>
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

### <span data-ttu-id="606db-121">-Workspace</span><span class="sxs-lookup"><span data-stu-id="606db-121">-Workspace</span></span>
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

### <span data-ttu-id="606db-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="606db-122">-WorkspaceName</span></span>
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

### <span data-ttu-id="606db-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="606db-123">-Confirm</span></span>
<span data-ttu-id="606db-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="606db-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="606db-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="606db-125">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="606db-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="606db-126">CommonParameters</span></span>
<span data-ttu-id="606db-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="606db-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="606db-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="606db-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="606db-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="606db-129">INPUTS</span></span>

### <span data-ttu-id="606db-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="606db-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="606db-131">System.String</span><span class="sxs-lookup"><span data-stu-id="606db-131">System.String</span></span>

### <span data-ttu-id="606db-132">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="606db-132">System.DateTimeOffset</span></span>

## <span data-ttu-id="606db-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="606db-133">OUTPUTS</span></span>

### <span data-ttu-id="606db-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="606db-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="606db-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="606db-135">NOTES</span></span>

## <span data-ttu-id="606db-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="606db-136">RELATED LINKS</span></span>
