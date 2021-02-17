---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
ms.openlocfilehash: 53dfedcfe4e61deb5064b20134bf063921532aec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232788"
---
# <span data-ttu-id="31f56-101">Get-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="31f56-101">Get-AzSentinelBookmark</span></span>

## <span data-ttu-id="31f56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31f56-102">SYNOPSIS</span></span>
<span data-ttu-id="31f56-103">Получить закладку.</span><span class="sxs-lookup"><span data-stu-id="31f56-103">Get a Bookmark.</span></span>

## <span data-ttu-id="31f56-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="31f56-104">SYNTAX</span></span>

### <span data-ttu-id="31f56-105">WorkspaceScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="31f56-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31f56-106">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="31f56-106">BookmarkId.</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31f56-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="31f56-107">ResourceId</span></span>
```
Get-AzSentinelBookmark -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31f56-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31f56-108">DESCRIPTION</span></span>
<span data-ttu-id="31f56-109">**Cmdlet Get-AzSentinelBookmark** получает закладку из указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="31f56-109">The **Get-AzSentinelBookmark** cmdlet gets a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="31f56-110">Если задан параметр *BookmarkId,* возвращается один объект **Bookmark.**</span><span class="sxs-lookup"><span data-stu-id="31f56-110">If you specify the *BookmarkId* parameter, a single **Bookmark** object is returned.</span></span>
<span data-ttu-id="31f56-111">Если параметр *BookmarkId* не задан, возвращается массив, содержащий все закладки в указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="31f56-111">If you do not specify the *BookmarkId* parameter, an array containing all of the Bookmarks in the specified workspace are returned.</span></span>
<span data-ttu-id="31f56-112">С помощью объекта **"Закладка"** можно обновить закладку, например добавить в нее **заметки.**</span><span class="sxs-lookup"><span data-stu-id="31f56-112">You can use the **Bookmark** object to update the Bookmark, for example you can add Notes the **Bookmark**.</span></span>

## <span data-ttu-id="31f56-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="31f56-113">EXAMPLES</span></span>

### <span data-ttu-id="31f56-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="31f56-114">Example 1</span></span>
```powershell
PS C:\> $Bookmarks = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="31f56-115">В этом примере  все закладки в указанной рабочей области, а затем в переменной $Bookmarks.</span><span class="sxs-lookup"><span data-stu-id="31f56-115">This example gets all of the **Bookmarks** in the specified workspace, and then stores it in the $Bookmarks variable.</span></span>

### <span data-ttu-id="31f56-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="31f56-116">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="31f56-117">В этом примере **закладка в** указанной рабочей области сохраняется в переменной $Bookmark.</span><span class="sxs-lookup"><span data-stu-id="31f56-117">This example gets an **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="31f56-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31f56-118">PARAMETERS</span></span>

### <span data-ttu-id="31f56-119">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="31f56-119">-BookmarkId</span></span>
<span data-ttu-id="31f56-120">"ИД закладки",</span><span class="sxs-lookup"><span data-stu-id="31f56-120">Bookmark Id,</span></span>

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

### <span data-ttu-id="31f56-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31f56-121">-DefaultProfile</span></span>
<span data-ttu-id="31f56-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31f56-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31f56-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31f56-123">-ResourceGroupName</span></span>
<span data-ttu-id="31f56-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="31f56-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f56-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31f56-125">-ResourceId</span></span>
<span data-ttu-id="31f56-126">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="31f56-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f56-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="31f56-127">-WorkspaceName</span></span>
<span data-ttu-id="31f56-128">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="31f56-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f56-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f56-129">CommonParameters</span></span>
<span data-ttu-id="31f56-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31f56-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f56-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31f56-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f56-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31f56-132">INPUTS</span></span>

### <span data-ttu-id="31f56-133">System.String</span><span class="sxs-lookup"><span data-stu-id="31f56-133">System.String</span></span>
## <span data-ttu-id="31f56-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="31f56-134">OUTPUTS</span></span>

### <span data-ttu-id="31f56-135">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="31f56-135">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="31f56-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="31f56-136">NOTES</span></span>

## <span data-ttu-id="31f56-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31f56-137">RELATED LINKS</span></span>
