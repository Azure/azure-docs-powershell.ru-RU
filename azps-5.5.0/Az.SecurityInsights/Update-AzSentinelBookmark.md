---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
ms.openlocfilehash: ebc0ffd78f653276e66b85d263db41803a48c356
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232780"
---
# <span data-ttu-id="9f276-101">Update-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="9f276-101">Update-AzSentinelBookmark</span></span>

## <span data-ttu-id="9f276-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f276-102">SYNOPSIS</span></span>
<span data-ttu-id="9f276-103">Обновление закладки.</span><span class="sxs-lookup"><span data-stu-id="9f276-103">Update a Bookmark.</span></span>

## <span data-ttu-id="9f276-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9f276-104">SYNTAX</span></span>

### <span data-ttu-id="9f276-105">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="9f276-105">BookmarkId.</span></span> <span data-ttu-id="9f276-106">(По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f276-106">(Default)</span></span>
```
Update-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DisplayName <String>] [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] [-Query <String>]
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f276-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="9f276-107">InputObject</span></span>
```
Update-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f276-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f276-108">ResourceId</span></span>
```
Update-AzSentinelBookmark -ResourceId <String> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f276-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f276-109">DESCRIPTION</span></span>
<span data-ttu-id="9f276-110">Для закладки в указанной рабочей области обновляется **cmdlet Update-AzSentinelBook.**</span><span class="sxs-lookup"><span data-stu-id="9f276-110">The **Update-AzSentinelBookmark** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="9f276-111">Объект **Bookmark** можно передать в качестве параметра или с помощью оператора конвейера. Кроме того, можно указать необходимые параметры *BookmarkId.*</span><span class="sxs-lookup"><span data-stu-id="9f276-111">You can pass an **Bookmark** object as a parameter or by using the pipeline operator, or alternatively you can specify the required *BookmarkId* parameters.</span></span>
<span data-ttu-id="9f276-112">Параметр Confirm  и переменная $ConfirmPreference Windows PowerShell можно использовать для управления запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f276-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="9f276-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9f276-113">EXAMPLES</span></span>

### <span data-ttu-id="9f276-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9f276-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId" -Notes "Found something interesting"
```

<span data-ttu-id="9f276-115">Команда обновляет закладку, настраивая свойство *"Заметки".*</span><span class="sxs-lookup"><span data-stu-id="9f276-115">The command updates the Bookmark by setting the *Notes* property.</span></span>  <span data-ttu-id="9f276-116">Все остальные возможности остаются без сбоя.</span><span class="sxs-lookup"><span data-stu-id="9f276-116">All other propreties stay the same.</span></span>

### <span data-ttu-id="9f276-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9f276-117">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId"
PS C:\> $Bookmark | Set-AzSentinelBookmark -Notes "Found something interesting"
```

<span data-ttu-id="9f276-118">Первая команда получает закладку *bookmarkId* из указанной рабочей области, а затем сохраняет ее в переменной $Bookmark.</span><span class="sxs-lookup"><span data-stu-id="9f276-118">The first command gets the Bookmark by *BookmarkId* from the specified workspace, and then stores it in the $Bookmark variable.</span></span>
<span data-ttu-id="9f276-119">Вторая команда обновляет свойство "Заметки".</span><span class="sxs-lookup"><span data-stu-id="9f276-119">The second command updates the Notes property.</span></span>   <span data-ttu-id="9f276-120">Все остальные возможности остаются без сбоя.</span><span class="sxs-lookup"><span data-stu-id="9f276-120">All other propreties stay the same.</span></span>

## <span data-ttu-id="9f276-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f276-121">PARAMETERS</span></span>

### <span data-ttu-id="9f276-122">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="9f276-122">-BookmarkId</span></span>
<span data-ttu-id="9f276-123">"ИД закладки",</span><span class="sxs-lookup"><span data-stu-id="9f276-123">Bookmark Id,</span></span>

```yaml
Type: String
Parameter Sets: BookmarkId., ParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f276-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f276-124">-DefaultProfile</span></span>
<span data-ttu-id="9f276-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f276-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f276-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9f276-126">-DisplayName</span></span>
<span data-ttu-id="9f276-127">Отображаемая имя правила закладки.</span><span class="sxs-lookup"><span data-stu-id="9f276-127">Bookmark Rule Display Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f276-128">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="9f276-128">-IncidentInfo</span></span>
<span data-ttu-id="9f276-129">"Сведения об инциденте закладки".</span><span class="sxs-lookup"><span data-stu-id="9f276-129">Bookmark Incident Info.</span></span>

```yaml
Type: PSSentinelBookmarkIncidentInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f276-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f276-130">-InputObject</span></span>
<span data-ttu-id="9f276-131">InputObject.</span><span class="sxs-lookup"><span data-stu-id="9f276-131">InputObject.</span></span>

```yaml
Type: PSSentinelBookmark
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f276-132">-Label</span><span class="sxs-lookup"><span data-stu-id="9f276-132">-Label</span></span>
<span data-ttu-id="9f276-133">Метки инцидентов.</span><span class="sxs-lookup"><span data-stu-id="9f276-133">Incident Labels.</span></span>

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

### <span data-ttu-id="9f276-134">-Notes</span><span class="sxs-lookup"><span data-stu-id="9f276-134">-Notes</span></span>
<span data-ttu-id="9f276-135">Заметки закладки.</span><span class="sxs-lookup"><span data-stu-id="9f276-135">Bookmark Notes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f276-136">-Query</span><span class="sxs-lookup"><span data-stu-id="9f276-136">-Query</span></span>
<span data-ttu-id="9f276-137">Запрос закладок.</span><span class="sxs-lookup"><span data-stu-id="9f276-137">Bookmark Query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f276-138">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="9f276-138">-QueryResult</span></span>
<span data-ttu-id="9f276-139">Результат запроса на закладку.</span><span class="sxs-lookup"><span data-stu-id="9f276-139">Bookmark Query Result.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f276-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f276-140">-ResourceGroupName</span></span>
<span data-ttu-id="9f276-141">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f276-141">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f276-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f276-142">-ResourceId</span></span>
<span data-ttu-id="9f276-143">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="9f276-143">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f276-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9f276-144">-WorkspaceName</span></span>
<span data-ttu-id="9f276-145">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9f276-145">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f276-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f276-146">-Confirm</span></span>
<span data-ttu-id="9f276-147">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9f276-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f276-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f276-148">-WhatIf</span></span>
<span data-ttu-id="9f276-149">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f276-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f276-150">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9f276-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f276-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f276-151">CommonParameters</span></span>
<span data-ttu-id="9f276-152">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f276-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f276-153">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f276-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f276-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f276-154">INPUTS</span></span>

### <span data-ttu-id="9f276-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="9f276-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

### <span data-ttu-id="9f276-156">System.String</span><span class="sxs-lookup"><span data-stu-id="9f276-156">System.String</span></span>

### <span data-ttu-id="9f276-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="9f276-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>

## <span data-ttu-id="9f276-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9f276-158">OUTPUTS</span></span>

### <span data-ttu-id="9f276-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="9f276-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

## <span data-ttu-id="9f276-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9f276-160">NOTES</span></span>

## <span data-ttu-id="9f276-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f276-161">RELATED LINKS</span></span>
