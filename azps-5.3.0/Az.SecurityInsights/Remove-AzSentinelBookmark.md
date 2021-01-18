---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
ms.openlocfilehash: 544c019fd52c0cb5723cbeafb5a82df072ac284e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517538"
---
# <span data-ttu-id="21225-101">Remove-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="21225-101">Remove-AzSentinelBookmark</span></span>

## <span data-ttu-id="21225-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21225-102">SYNOPSIS</span></span>
<span data-ttu-id="21225-103">Удаление закладки.</span><span class="sxs-lookup"><span data-stu-id="21225-103">Delete a Bookmark.</span></span>

## <span data-ttu-id="21225-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="21225-104">SYNTAX</span></span>

### <span data-ttu-id="21225-105">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="21225-105">BookmarkId.</span></span> <span data-ttu-id="21225-106">(По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="21225-106">(Default)</span></span>
```
Remove-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21225-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="21225-107">InputObject</span></span>
```
Remove-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21225-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="21225-108">DESCRIPTION</span></span>
<span data-ttu-id="21225-109">**Cmdlet Remove-AzSentinelBookmark** окончательно удаляет закладку из указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="21225-109">The **Remove-AzSentinelBookmark** cmdlet permanently deletes a Bookmark from a specified workspace.</span></span>
<span data-ttu-id="21225-110">Объект **закладки** можно передать с помощью оператора конвейера или указать необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="21225-110">You can pass an **Bookmark** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="21225-111">Параметр Confirm и переменная $ConfirmPreference Windows PowerShell можно использовать для управления запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21225-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="21225-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="21225-112">EXAMPLES</span></span>

### <span data-ttu-id="21225-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="21225-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="21225-114">Эта команда удаляет закладку из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="21225-114">This command removes the Bookmark from the workspace.</span></span>

## <span data-ttu-id="21225-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21225-115">PARAMETERS</span></span>

### <span data-ttu-id="21225-116">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="21225-116">-BookmarkId</span></span>
<span data-ttu-id="21225-117">"ИД закладки",</span><span class="sxs-lookup"><span data-stu-id="21225-117">Bookmark Id,</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21225-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21225-118">-DefaultProfile</span></span>
<span data-ttu-id="21225-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="21225-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21225-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21225-120">-InputObject</span></span>
<span data-ttu-id="21225-121">InputObject.</span><span class="sxs-lookup"><span data-stu-id="21225-121">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21225-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21225-122">-PassThru</span></span>
<span data-ttu-id="21225-123">PassThru</span><span class="sxs-lookup"><span data-stu-id="21225-123">PassThru</span></span>

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

### <span data-ttu-id="21225-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21225-124">-ResourceGroupName</span></span>
<span data-ttu-id="21225-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="21225-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21225-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="21225-126">-WorkspaceName</span></span>
<span data-ttu-id="21225-127">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="21225-127">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21225-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21225-128">-Confirm</span></span>
<span data-ttu-id="21225-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21225-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21225-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21225-130">-WhatIf</span></span>
<span data-ttu-id="21225-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21225-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21225-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="21225-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21225-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21225-133">CommonParameters</span></span>
<span data-ttu-id="21225-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21225-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21225-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21225-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21225-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="21225-136">INPUTS</span></span>

### <span data-ttu-id="21225-137">System.String</span><span class="sxs-lookup"><span data-stu-id="21225-137">System.String</span></span>
### <span data-ttu-id="21225-138">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="21225-138">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="21225-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="21225-139">OUTPUTS</span></span>

### <span data-ttu-id="21225-140">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="21225-140">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="21225-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="21225-141">NOTES</span></span>

## <span data-ttu-id="21225-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="21225-142">RELATED LINKS</span></span>
