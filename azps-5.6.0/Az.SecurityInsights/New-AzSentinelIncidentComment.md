---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
ms.openlocfilehash: 0fe04e773e02a8b6b61f9c57d8316ac8936f05aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963672"
---
# <span data-ttu-id="093e1-101">New-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="093e1-101">New-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="093e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="093e1-102">SYNOPSIS</span></span>
<span data-ttu-id="093e1-103">Добавьте комментарий к инциденту.</span><span class="sxs-lookup"><span data-stu-id="093e1-103">Add an Incident Comment to an Incident.</span></span>

## <span data-ttu-id="093e1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="093e1-104">SYNTAX</span></span>

```
New-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-IncidentCommentId <String>] -Message <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="093e1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="093e1-105">DESCRIPTION</span></span>
<span data-ttu-id="093e1-106">Cmdlet **New-AzSentinelIncidentComment** создает комментарий об инциденте из указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="093e1-106">The **New-AzSentinelIncidentComment** cmdlet creates a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="093e1-107">С помощью переменных *Confirm* и $ConfirmPreference Windows PowerShell можно управлять запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="093e1-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="093e1-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="093e1-108">EXAMPLES</span></span>

### <span data-ttu-id="093e1-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="093e1-109">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $IncidentComment = New-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId ($Incident.Name) -Message "Still needs investigation"
```

<span data-ttu-id="093e1-110">В этом примере создается **incidentComment в** указанной рабочей области, а затем сохраняется в переменной $IncidentComment.</span><span class="sxs-lookup"><span data-stu-id="093e1-110">This example creates an **IncidentComment** in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="093e1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="093e1-111">PARAMETERS</span></span>

### <span data-ttu-id="093e1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="093e1-112">-DefaultProfile</span></span>
<span data-ttu-id="093e1-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="093e1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="093e1-114">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="093e1-114">-IncidentCommentId</span></span>
<span data-ttu-id="093e1-115">ИД комментария к инциденту.</span><span class="sxs-lookup"><span data-stu-id="093e1-115">Incident Comment Id.</span></span>

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

### <span data-ttu-id="093e1-116">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="093e1-116">-IncidentId</span></span>
<span data-ttu-id="093e1-117">ИД инцидента.</span><span class="sxs-lookup"><span data-stu-id="093e1-117">Incident Id.</span></span>

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

### <span data-ttu-id="093e1-118">-Message</span><span class="sxs-lookup"><span data-stu-id="093e1-118">-Message</span></span>
<span data-ttu-id="093e1-119">Сообщение об инциденте.</span><span class="sxs-lookup"><span data-stu-id="093e1-119">Incident Message.</span></span>

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

### <span data-ttu-id="093e1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="093e1-120">-ResourceGroupName</span></span>
<span data-ttu-id="093e1-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="093e1-121">Resource group name.</span></span>

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

### <span data-ttu-id="093e1-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="093e1-122">-WorkspaceName</span></span>
<span data-ttu-id="093e1-123">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="093e1-123">Workspace Name.</span></span>

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

### <span data-ttu-id="093e1-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="093e1-124">-Confirm</span></span>
<span data-ttu-id="093e1-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="093e1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="093e1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="093e1-126">-WhatIf</span></span>
<span data-ttu-id="093e1-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="093e1-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="093e1-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="093e1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="093e1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="093e1-129">CommonParameters</span></span>
<span data-ttu-id="093e1-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="093e1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="093e1-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="093e1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="093e1-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="093e1-132">INPUTS</span></span>

### <span data-ttu-id="093e1-133">Нет</span><span class="sxs-lookup"><span data-stu-id="093e1-133">None</span></span>
## <span data-ttu-id="093e1-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="093e1-134">OUTPUTS</span></span>

### <span data-ttu-id="093e1-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="093e1-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="093e1-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="093e1-136">NOTES</span></span>

## <span data-ttu-id="093e1-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="093e1-137">RELATED LINKS</span></span>
