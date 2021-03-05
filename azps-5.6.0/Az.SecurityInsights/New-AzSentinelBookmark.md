---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
ms.openlocfilehash: 31c9728a95e5cfc52b283a8dddc0e24ffffe1630
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976355"
---
# <span data-ttu-id="02328-101">New-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="02328-101">New-AzSentinelBookmark</span></span>

## <span data-ttu-id="02328-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02328-102">SYNOPSIS</span></span>
<span data-ttu-id="02328-103">Создание закладки.</span><span class="sxs-lookup"><span data-stu-id="02328-103">Create a Bookmark.</span></span>

## <span data-ttu-id="02328-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="02328-104">SYNTAX</span></span>

```
New-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> [-BookmarkId <String>]
 -DisplayName <String> [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] -Query <String>
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02328-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02328-105">DESCRIPTION</span></span>
<span data-ttu-id="02328-106">Для создания закладки из указанной рабочей области создается **cmdlet New-AzSentinelBookmark.**</span><span class="sxs-lookup"><span data-stu-id="02328-106">The **New-AzSentinelBookmark** cmdlet creates a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="02328-107">С помощью переменных *Confirm* и $ConfirmPreference Windows PowerShell можно управлять запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02328-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="02328-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="02328-108">EXAMPLES</span></span>

### <span data-ttu-id="02328-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="02328-109">Example 1</span></span>
```powershell
PS C:\> $Bookmark = New-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DisplayName "MyBookmark" -Query "SecurityAlert | take 1"
```

<span data-ttu-id="02328-110">В этом примере **закладка** создается в указанной рабочей области, а затем сохраняется в $Bookmark переменной.</span><span class="sxs-lookup"><span data-stu-id="02328-110">This example creates a **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="02328-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02328-111">PARAMETERS</span></span>

### <span data-ttu-id="02328-112">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="02328-112">-BookmarkId</span></span>
<span data-ttu-id="02328-113">"ИД закладки",</span><span class="sxs-lookup"><span data-stu-id="02328-113">Bookmark Id,</span></span>

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

### <span data-ttu-id="02328-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02328-114">-DefaultProfile</span></span>
<span data-ttu-id="02328-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="02328-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02328-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="02328-116">-DisplayName</span></span>
<span data-ttu-id="02328-117">Отображаемая имя правила для закладок.</span><span class="sxs-lookup"><span data-stu-id="02328-117">Bookmark Rule Display Name.</span></span>

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

### <span data-ttu-id="02328-118">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="02328-118">-IncidentInfo</span></span>
<span data-ttu-id="02328-119">"Сведения об инциденте закладки".</span><span class="sxs-lookup"><span data-stu-id="02328-119">Bookmark Incident Info.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02328-120">-Label</span><span class="sxs-lookup"><span data-stu-id="02328-120">-Label</span></span>
<span data-ttu-id="02328-121">Метки инцидентов.</span><span class="sxs-lookup"><span data-stu-id="02328-121">Incident Labels.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02328-122">-Notes</span><span class="sxs-lookup"><span data-stu-id="02328-122">-Notes</span></span>
<span data-ttu-id="02328-123">Заметки закладки.</span><span class="sxs-lookup"><span data-stu-id="02328-123">Bookmark Notes.</span></span>

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

### <span data-ttu-id="02328-124">-Query</span><span class="sxs-lookup"><span data-stu-id="02328-124">-Query</span></span>
<span data-ttu-id="02328-125">Запрос закладок.</span><span class="sxs-lookup"><span data-stu-id="02328-125">Bookmark Query.</span></span>

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

### <span data-ttu-id="02328-126">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="02328-126">-QueryResult</span></span>
<span data-ttu-id="02328-127">Результат запроса на закладку.</span><span class="sxs-lookup"><span data-stu-id="02328-127">Bookmark Query Result.</span></span>

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

### <span data-ttu-id="02328-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02328-128">-ResourceGroupName</span></span>
<span data-ttu-id="02328-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="02328-129">Resource group name.</span></span>

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

### <span data-ttu-id="02328-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="02328-130">-WorkspaceName</span></span>
<span data-ttu-id="02328-131">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="02328-131">Workspace Name.</span></span>

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

### <span data-ttu-id="02328-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02328-132">-Confirm</span></span>
<span data-ttu-id="02328-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02328-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02328-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02328-134">-WhatIf</span></span>
<span data-ttu-id="02328-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02328-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02328-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="02328-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02328-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02328-137">CommonParameters</span></span>
<span data-ttu-id="02328-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02328-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02328-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02328-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02328-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02328-140">INPUTS</span></span>

### <span data-ttu-id="02328-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="02328-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>
## <span data-ttu-id="02328-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="02328-142">OUTPUTS</span></span>

### <span data-ttu-id="02328-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="02328-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="02328-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="02328-144">NOTES</span></span>

## <span data-ttu-id="02328-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02328-145">RELATED LINKS</span></span>
