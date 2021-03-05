---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: 3c6335264c0d658b0c068efba30c39b4caca407b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971752"
---
# <span data-ttu-id="dcd07-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="dcd07-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="dcd07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcd07-102">SYNOPSIS</span></span>
<span data-ttu-id="dcd07-103">Создайте ключ запроса для службы поиска когнитивных функций Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd07-103">Create a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="dcd07-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dcd07-104">SYNTAX</span></span>

### <span data-ttu-id="dcd07-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dcd07-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd07-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcd07-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd07-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcd07-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcd07-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcd07-108">DESCRIPTION</span></span>
<span data-ttu-id="dcd07-109">Для **службы azure Cognitive** Search создается новый ключ запроса.</span><span class="sxs-lookup"><span data-stu-id="dcd07-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="dcd07-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dcd07-110">EXAMPLES</span></span>

### <span data-ttu-id="dcd07-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dcd07-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="dcd07-112">В этом примере создается новый ключ запроса для службы azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="dcd07-112">The example creates a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="dcd07-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcd07-113">PARAMETERS</span></span>

### <span data-ttu-id="dcd07-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcd07-114">-DefaultProfile</span></span>
<span data-ttu-id="dcd07-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd07-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcd07-116">-Name</span><span class="sxs-lookup"><span data-stu-id="dcd07-116">-Name</span></span>
<span data-ttu-id="dcd07-117">Имя ключа запроса службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd07-117">Azure Cognitive Search Service query key name.</span></span>

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

### <span data-ttu-id="dcd07-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dcd07-118">-ParentObject</span></span>
<span data-ttu-id="dcd07-119">Объект ввода службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd07-119">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="dcd07-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="dcd07-120">-ParentResourceId</span></span>
<span data-ttu-id="dcd07-121">ИД ресурса службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd07-121">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="dcd07-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcd07-122">-ResourceGroupName</span></span>
<span data-ttu-id="dcd07-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dcd07-123">Resource Group name.</span></span>

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

### <span data-ttu-id="dcd07-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="dcd07-124">-ServiceName</span></span>
<span data-ttu-id="dcd07-125">Имя службы поиска данных Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd07-125">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="dcd07-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dcd07-126">-Confirm</span></span>
<span data-ttu-id="dcd07-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="dcd07-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcd07-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcd07-128">-WhatIf</span></span>
<span data-ttu-id="dcd07-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcd07-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dcd07-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dcd07-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcd07-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcd07-131">CommonParameters</span></span>
<span data-ttu-id="dcd07-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcd07-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcd07-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dcd07-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcd07-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dcd07-134">INPUTS</span></span>

### <span data-ttu-id="dcd07-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="dcd07-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="dcd07-136">System.String</span><span class="sxs-lookup"><span data-stu-id="dcd07-136">System.String</span></span>

## <span data-ttu-id="dcd07-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dcd07-137">OUTPUTS</span></span>

### <span data-ttu-id="dcd07-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="dcd07-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="dcd07-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dcd07-139">NOTES</span></span>

## <span data-ttu-id="dcd07-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dcd07-140">RELATED LINKS</span></span>

[<span data-ttu-id="dcd07-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="dcd07-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="dcd07-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="dcd07-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)
