---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 6dc016e717e89ad60e066be1c1d86e5871309d9e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408860"
---
# <span data-ttu-id="e149c-101">New-AzOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="e149c-101">New-AzOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="e149c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e149c-102">SYNOPSIS</span></span>
<span data-ttu-id="e149c-103">Сбор журнала действий Azure из данной подписки.</span><span class="sxs-lookup"><span data-stu-id="e149c-103">Collect Azure Activity log from given subscription.</span></span>

## <span data-ttu-id="e149c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e149c-104">SYNTAX</span></span>

### <span data-ttu-id="e149c-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e149c-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e149c-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e149c-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e149c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e149c-107">DESCRIPTION</span></span>
<span data-ttu-id="e149c-108">Данные New-AzOperationalInsightsAzureActivityLogDataSource позволяют средству аналитики журналов собирать журнал действий Azure из данной подписки.</span><span class="sxs-lookup"><span data-stu-id="e149c-108">The New-AzOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="e149c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e149c-109">EXAMPLES</span></span>

### <span data-ttu-id="e149c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e149c-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="e149c-111">{{ Добавьте здесь описание примера }}</span><span class="sxs-lookup"><span data-stu-id="e149c-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="e149c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e149c-112">PARAMETERS</span></span>

### <span data-ttu-id="e149c-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="e149c-113">-BackfillStartTime</span></span>
<span data-ttu-id="e149c-114">Вы можете сделать это неделю назад.</span><span class="sxs-lookup"><span data-stu-id="e149c-114">You can choose to backfill logs from a week ago.</span></span>

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

### <span data-ttu-id="e149c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e149c-115">-DefaultProfile</span></span>
<span data-ttu-id="e149c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e149c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e149c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e149c-117">-Force</span></span>
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

### <span data-ttu-id="e149c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e149c-118">-Name</span></span>
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

### <span data-ttu-id="e149c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e149c-119">-ResourceGroupName</span></span>
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

### <span data-ttu-id="e149c-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e149c-120">-SubscriptionId</span></span>
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

### <span data-ttu-id="e149c-121">-Workspace</span><span class="sxs-lookup"><span data-stu-id="e149c-121">-Workspace</span></span>
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

### <span data-ttu-id="e149c-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e149c-122">-WorkspaceName</span></span>
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

### <span data-ttu-id="e149c-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e149c-123">-Confirm</span></span>
<span data-ttu-id="e149c-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e149c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e149c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e149c-125">-WhatIf</span></span>
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

### <span data-ttu-id="e149c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e149c-126">CommonParameters</span></span>
<span data-ttu-id="e149c-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e149c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e149c-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e149c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e149c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e149c-129">INPUTS</span></span>

### <span data-ttu-id="e149c-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e149c-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="e149c-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e149c-131">System.String</span></span>

### <span data-ttu-id="e149c-132">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e149c-132">System.DateTimeOffset</span></span>

## <span data-ttu-id="e149c-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e149c-133">OUTPUTS</span></span>

### <span data-ttu-id="e149c-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="e149c-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="e149c-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e149c-135">NOTES</span></span>

## <span data-ttu-id="e149c-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e149c-136">RELATED LINKS</span></span>