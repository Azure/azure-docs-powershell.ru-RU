---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
ms.openlocfilehash: b25e99766c4dc0433b14810352968300fd5bd129
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986404"
---
# <span data-ttu-id="c501c-101">Get-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="c501c-101">Get-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="c501c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c501c-102">SYNOPSIS</span></span>
<span data-ttu-id="c501c-103">Получите комментарий об инциденте.</span><span class="sxs-lookup"><span data-stu-id="c501c-103">Get an Incident Comment.</span></span>

## <span data-ttu-id="c501c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c501c-104">SYNTAX</span></span>

### <span data-ttu-id="c501c-105">IncidentId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c501c-105">IncidentId (Default)</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c501c-106">IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="c501c-106">IncidentCommentId</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 -IncidentCommentId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c501c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c501c-107">ResourceId</span></span>
```
Get-AzSentinelIncidentComment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c501c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c501c-108">DESCRIPTION</span></span>
<span data-ttu-id="c501c-109">Cmdlet **Get-AzSentinelIncidentComment** получает комментарий об инциденте из указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c501c-109">The **Get-AzSentinelIncidentComment** cmdlet gets a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="c501c-110">Если указать *параметры IncidentCommentId* и *IncidentId,* возвращается один объект **IncidentComment.**</span><span class="sxs-lookup"><span data-stu-id="c501c-110">If you specify the *IncidentCommentId* and *IncidentId* parameters, a single **IncidentComment** object is returned.</span></span>
<span data-ttu-id="c501c-111">Если не указать параметр *IncidentCommentId,* возвращается массив, содержащий все комментарии об инциденте для указанного инцидента в указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c501c-111">If you do not specify the *IncidentCommentId* parameter, an array containing all of the Incident Comments for the specified Incident in the specified workspace are returned.</span></span>

## <span data-ttu-id="c501c-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c501c-112">EXAMPLES</span></span>

### <span data-ttu-id="c501c-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c501c-113">Example 1</span></span>
```powershell
PS C:\> $IncidentComments = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="c501c-114">В этом примере все **incidentComments** для указанного инцидента в указанной рабочей области, а затем хранится в переменной $IncidentComments инцидентов.</span><span class="sxs-lookup"><span data-stu-id="c501c-114">This example gets all of the **IncidentComments** for the specified Incident in the specified workspace, and then stores it in the $IncidentComments variable.</span></span>

### <span data-ttu-id="c501c-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c501c-115">Example 2</span></span>
```powershell
PS C:\> $IncidentComment = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -IncidentCommentId "MyIncidentCommentId"
```

<span data-ttu-id="c501c-116">В этом примере **возвращается incidentComment** для указанного инцидента в указанной рабочей области, а затем он сохраняется в переменной $IncidentComment инцидентов.</span><span class="sxs-lookup"><span data-stu-id="c501c-116">This example gets an **IncidentComment** for the specified Incident in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="c501c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c501c-117">PARAMETERS</span></span>

### <span data-ttu-id="c501c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c501c-118">-DefaultProfile</span></span>
<span data-ttu-id="c501c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c501c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c501c-120">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="c501c-120">-IncidentCommentId</span></span>
<span data-ttu-id="c501c-121">ИД комментария к инциденту.</span><span class="sxs-lookup"><span data-stu-id="c501c-121">Incident Comment Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c501c-122">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="c501c-122">-IncidentId</span></span>
<span data-ttu-id="c501c-123">ИД инцидента.</span><span class="sxs-lookup"><span data-stu-id="c501c-123">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c501c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c501c-124">-ResourceGroupName</span></span>
<span data-ttu-id="c501c-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c501c-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c501c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c501c-126">-ResourceId</span></span>
<span data-ttu-id="c501c-127">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="c501c-127">Resource Id.</span></span>

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

### <span data-ttu-id="c501c-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c501c-128">-WorkspaceName</span></span>
<span data-ttu-id="c501c-129">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c501c-129">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c501c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c501c-130">CommonParameters</span></span>
<span data-ttu-id="c501c-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c501c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c501c-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c501c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c501c-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c501c-133">INPUTS</span></span>

### <span data-ttu-id="c501c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c501c-134">System.String</span></span>
## <span data-ttu-id="c501c-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c501c-135">OUTPUTS</span></span>

### <span data-ttu-id="c501c-136">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="c501c-136">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="c501c-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c501c-137">NOTES</span></span>

## <span data-ttu-id="c501c-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c501c-138">RELATED LINKS</span></span>
