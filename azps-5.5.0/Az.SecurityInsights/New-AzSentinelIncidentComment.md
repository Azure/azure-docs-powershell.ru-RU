---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
ms.openlocfilehash: 8824832b1b3d09a24998891ad4636e3a3e0f1e19
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235788"
---
# <span data-ttu-id="19605-101">New-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="19605-101">New-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="19605-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19605-102">SYNOPSIS</span></span>
<span data-ttu-id="19605-103">Добавьте комментарий к инциденту.</span><span class="sxs-lookup"><span data-stu-id="19605-103">Add an Incident Comment to an Incident.</span></span>

## <span data-ttu-id="19605-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="19605-104">SYNTAX</span></span>

```
New-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-IncidentCommentId <String>] -Message <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19605-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19605-105">DESCRIPTION</span></span>
<span data-ttu-id="19605-106">Cmdlet **New-AzSentinelIncidentComment** создает комментарий об инциденте из указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="19605-106">The **New-AzSentinelIncidentComment** cmdlet creates a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="19605-107">С помощью переменных *Confirm* и $ConfirmPreference Windows PowerShell можно управлять запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19605-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="19605-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="19605-108">EXAMPLES</span></span>

### <span data-ttu-id="19605-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="19605-109">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $IncidentComment = New-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId ($Incident.Name) -Message "Still needs investigation"
```

<span data-ttu-id="19605-110">В этом примере создается **incidentComment в** указанной рабочей области, а затем сохраняется в переменной $IncidentComment.</span><span class="sxs-lookup"><span data-stu-id="19605-110">This example creates an **IncidentComment** in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="19605-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19605-111">PARAMETERS</span></span>

### <span data-ttu-id="19605-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19605-112">-DefaultProfile</span></span>
<span data-ttu-id="19605-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19605-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19605-114">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="19605-114">-IncidentCommentId</span></span>
<span data-ttu-id="19605-115">ИД комментария к инциденту.</span><span class="sxs-lookup"><span data-stu-id="19605-115">Incident Comment Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19605-116">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="19605-116">-IncidentId</span></span>
<span data-ttu-id="19605-117">ИД инцидента.</span><span class="sxs-lookup"><span data-stu-id="19605-117">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19605-118">-Message</span><span class="sxs-lookup"><span data-stu-id="19605-118">-Message</span></span>
<span data-ttu-id="19605-119">Сообщение об инциденте.</span><span class="sxs-lookup"><span data-stu-id="19605-119">Incident Message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19605-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19605-120">-ResourceGroupName</span></span>
<span data-ttu-id="19605-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="19605-121">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19605-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="19605-122">-WorkspaceName</span></span>
<span data-ttu-id="19605-123">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="19605-123">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19605-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19605-124">-Confirm</span></span>
<span data-ttu-id="19605-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19605-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19605-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19605-126">-WhatIf</span></span>
<span data-ttu-id="19605-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19605-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19605-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="19605-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19605-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19605-129">CommonParameters</span></span>
<span data-ttu-id="19605-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19605-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19605-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19605-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19605-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19605-132">INPUTS</span></span>

### <span data-ttu-id="19605-133">Нет</span><span class="sxs-lookup"><span data-stu-id="19605-133">None</span></span>
## <span data-ttu-id="19605-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="19605-134">OUTPUTS</span></span>

### <span data-ttu-id="19605-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="19605-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="19605-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="19605-136">NOTES</span></span>

## <span data-ttu-id="19605-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19605-137">RELATED LINKS</span></span>
