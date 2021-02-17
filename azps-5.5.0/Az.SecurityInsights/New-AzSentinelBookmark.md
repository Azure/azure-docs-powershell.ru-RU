---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
ms.openlocfilehash: 3c30edd841eb2e773c5d813e798e63fc9858437d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235804"
---
# <span data-ttu-id="17bec-101">New-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="17bec-101">New-AzSentinelBookmark</span></span>

## <span data-ttu-id="17bec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17bec-102">SYNOPSIS</span></span>
<span data-ttu-id="17bec-103">Создание закладки.</span><span class="sxs-lookup"><span data-stu-id="17bec-103">Create a Bookmark.</span></span>

## <span data-ttu-id="17bec-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="17bec-104">SYNTAX</span></span>

```
New-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> [-BookmarkId <String>]
 -DisplayName <String> [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] -Query <String>
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17bec-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17bec-105">DESCRIPTION</span></span>
<span data-ttu-id="17bec-106">Для создания закладки из указанной рабочей области создается **cmdlet New-AzSentinelBookmark.**</span><span class="sxs-lookup"><span data-stu-id="17bec-106">The **New-AzSentinelBookmark** cmdlet creates a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="17bec-107">С помощью переменных *Confirm* и $ConfirmPreference Windows PowerShell можно управлять запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17bec-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="17bec-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="17bec-108">EXAMPLES</span></span>

### <span data-ttu-id="17bec-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="17bec-109">Example 1</span></span>
```powershell
PS C:\> $Bookmark = New-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DisplayName "MyBookmark" -Query "SecurityAlert | take 1"
```

<span data-ttu-id="17bec-110">В этом примере **закладка** создается в указанной рабочей области, а затем сохраняется в $Bookmark переменной.</span><span class="sxs-lookup"><span data-stu-id="17bec-110">This example creates a **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="17bec-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17bec-111">PARAMETERS</span></span>

### <span data-ttu-id="17bec-112">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="17bec-112">-BookmarkId</span></span>
<span data-ttu-id="17bec-113">"ИД закладки",</span><span class="sxs-lookup"><span data-stu-id="17bec-113">Bookmark Id,</span></span>

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

### <span data-ttu-id="17bec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17bec-114">-DefaultProfile</span></span>
<span data-ttu-id="17bec-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="17bec-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17bec-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="17bec-116">-DisplayName</span></span>
<span data-ttu-id="17bec-117">Отображаемая имя правила закладки.</span><span class="sxs-lookup"><span data-stu-id="17bec-117">Bookmark Rule Display Name.</span></span>

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

### <span data-ttu-id="17bec-118">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="17bec-118">-IncidentInfo</span></span>
<span data-ttu-id="17bec-119">"Сведения об инциденте закладки".</span><span class="sxs-lookup"><span data-stu-id="17bec-119">Bookmark Incident Info.</span></span>

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

### <span data-ttu-id="17bec-120">-Label</span><span class="sxs-lookup"><span data-stu-id="17bec-120">-Label</span></span>
<span data-ttu-id="17bec-121">Метки инцидентов.</span><span class="sxs-lookup"><span data-stu-id="17bec-121">Incident Labels.</span></span>

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

### <span data-ttu-id="17bec-122">-Notes</span><span class="sxs-lookup"><span data-stu-id="17bec-122">-Notes</span></span>
<span data-ttu-id="17bec-123">Заметки закладки.</span><span class="sxs-lookup"><span data-stu-id="17bec-123">Bookmark Notes.</span></span>

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

### <span data-ttu-id="17bec-124">-Query</span><span class="sxs-lookup"><span data-stu-id="17bec-124">-Query</span></span>
<span data-ttu-id="17bec-125">Запрос закладок.</span><span class="sxs-lookup"><span data-stu-id="17bec-125">Bookmark Query.</span></span>

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

### <span data-ttu-id="17bec-126">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="17bec-126">-QueryResult</span></span>
<span data-ttu-id="17bec-127">Результат запроса на закладку.</span><span class="sxs-lookup"><span data-stu-id="17bec-127">Bookmark Query Result.</span></span>

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

### <span data-ttu-id="17bec-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17bec-128">-ResourceGroupName</span></span>
<span data-ttu-id="17bec-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="17bec-129">Resource group name.</span></span>

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

### <span data-ttu-id="17bec-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="17bec-130">-WorkspaceName</span></span>
<span data-ttu-id="17bec-131">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="17bec-131">Workspace Name.</span></span>

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

### <span data-ttu-id="17bec-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17bec-132">-Confirm</span></span>
<span data-ttu-id="17bec-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17bec-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17bec-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17bec-134">-WhatIf</span></span>
<span data-ttu-id="17bec-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17bec-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17bec-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="17bec-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17bec-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17bec-137">CommonParameters</span></span>
<span data-ttu-id="17bec-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17bec-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17bec-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17bec-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17bec-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17bec-140">INPUTS</span></span>

### <span data-ttu-id="17bec-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="17bec-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>
## <span data-ttu-id="17bec-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="17bec-142">OUTPUTS</span></span>

### <span data-ttu-id="17bec-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="17bec-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="17bec-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="17bec-144">NOTES</span></span>

## <span data-ttu-id="17bec-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17bec-145">RELATED LINKS</span></span>
