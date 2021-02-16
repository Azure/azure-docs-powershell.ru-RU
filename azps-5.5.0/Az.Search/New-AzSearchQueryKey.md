---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: 7edca2e338c4972550d44cc6409187dbc53ab40b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226769"
---
# <span data-ttu-id="2f812-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="2f812-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="2f812-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f812-102">SYNOPSIS</span></span>
<span data-ttu-id="2f812-103">Создайте ключ запроса для службы поиска когнитивных функций Azure.</span><span class="sxs-lookup"><span data-stu-id="2f812-103">Create a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="2f812-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2f812-104">SYNTAX</span></span>

### <span data-ttu-id="2f812-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2f812-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f812-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f812-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f812-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f812-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f812-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f812-108">DESCRIPTION</span></span>
<span data-ttu-id="2f812-109">Для **службы azure Cognitive** Search создается новый ключ запроса.</span><span class="sxs-lookup"><span data-stu-id="2f812-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="2f812-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2f812-110">EXAMPLES</span></span>

### <span data-ttu-id="2f812-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2f812-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="2f812-112">В этом примере создается новый ключ запроса для службы azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="2f812-112">The example creates a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="2f812-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f812-113">PARAMETERS</span></span>

### <span data-ttu-id="2f812-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f812-114">-DefaultProfile</span></span>
<span data-ttu-id="2f812-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f812-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f812-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2f812-116">-Name</span></span>
<span data-ttu-id="2f812-117">Имя ключа запроса службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="2f812-117">Azure Cognitive Search Service query key name.</span></span>

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

### <span data-ttu-id="2f812-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2f812-118">-ParentObject</span></span>
<span data-ttu-id="2f812-119">Объект ввода службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="2f812-119">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f812-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2f812-120">-ParentResourceId</span></span>
<span data-ttu-id="2f812-121">ИД ресурса службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="2f812-121">Azure Cognitive Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f812-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f812-122">-ResourceGroupName</span></span>
<span data-ttu-id="2f812-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2f812-123">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f812-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2f812-124">-ServiceName</span></span>
<span data-ttu-id="2f812-125">Имя службы поиска данных Azure.</span><span class="sxs-lookup"><span data-stu-id="2f812-125">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f812-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f812-126">-Confirm</span></span>
<span data-ttu-id="2f812-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f812-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f812-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f812-128">-WhatIf</span></span>
<span data-ttu-id="2f812-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f812-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f812-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2f812-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f812-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f812-131">CommonParameters</span></span>
<span data-ttu-id="2f812-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f812-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f812-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f812-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f812-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2f812-134">INPUTS</span></span>

### <span data-ttu-id="2f812-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="2f812-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="2f812-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2f812-136">System.String</span></span>

## <span data-ttu-id="2f812-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2f812-137">OUTPUTS</span></span>

### <span data-ttu-id="2f812-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="2f812-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="2f812-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2f812-139">NOTES</span></span>

## <span data-ttu-id="2f812-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f812-140">RELATED LINKS</span></span>

[<span data-ttu-id="2f812-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="2f812-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="2f812-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="2f812-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)
