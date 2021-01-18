---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: e01e5e244bd34e3e18aa287e0f2f5709c5e208ec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505952"
---
# <span data-ttu-id="105a2-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="105a2-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="105a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="105a2-102">SYNOPSIS</span></span>
<span data-ttu-id="105a2-103">Создайте ключ запроса для службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="105a2-103">Create a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="105a2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="105a2-104">SYNTAX</span></span>

### <span data-ttu-id="105a2-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="105a2-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="105a2-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="105a2-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="105a2-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="105a2-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="105a2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="105a2-108">DESCRIPTION</span></span>
<span data-ttu-id="105a2-109">Для **нового ключа** запроса для службы поиска Azure создается новый ключ запроса.</span><span class="sxs-lookup"><span data-stu-id="105a2-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Search Service.</span></span>

## <span data-ttu-id="105a2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="105a2-110">EXAMPLES</span></span>

### <span data-ttu-id="105a2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="105a2-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="105a2-112">В этом примере создается новый ключ запроса для службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="105a2-112">The example creates a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="105a2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="105a2-113">PARAMETERS</span></span>

### <span data-ttu-id="105a2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="105a2-114">-DefaultProfile</span></span>
<span data-ttu-id="105a2-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="105a2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="105a2-116">-Name</span><span class="sxs-lookup"><span data-stu-id="105a2-116">-Name</span></span>
<span data-ttu-id="105a2-117">Имя ключа запроса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="105a2-117">Search Service query key name.</span></span>

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

### <span data-ttu-id="105a2-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="105a2-118">-ParentObject</span></span>
<span data-ttu-id="105a2-119">Объект ввода службы поиска.</span><span class="sxs-lookup"><span data-stu-id="105a2-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="105a2-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="105a2-120">-ParentResourceId</span></span>
<span data-ttu-id="105a2-121">ИД ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="105a2-121">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="105a2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="105a2-122">-ResourceGroupName</span></span>
<span data-ttu-id="105a2-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="105a2-123">Resource Group name.</span></span>

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

### <span data-ttu-id="105a2-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="105a2-124">-ServiceName</span></span>
<span data-ttu-id="105a2-125">Название службы поиска.</span><span class="sxs-lookup"><span data-stu-id="105a2-125">Search Service name.</span></span>

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

### <span data-ttu-id="105a2-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="105a2-126">-Confirm</span></span>
<span data-ttu-id="105a2-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="105a2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="105a2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="105a2-128">-WhatIf</span></span>
<span data-ttu-id="105a2-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="105a2-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="105a2-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="105a2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="105a2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="105a2-131">CommonParameters</span></span>
<span data-ttu-id="105a2-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="105a2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="105a2-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="105a2-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="105a2-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="105a2-134">INPUTS</span></span>

### <span data-ttu-id="105a2-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="105a2-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="105a2-136">System.String</span><span class="sxs-lookup"><span data-stu-id="105a2-136">System.String</span></span>

## <span data-ttu-id="105a2-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="105a2-137">OUTPUTS</span></span>

### <span data-ttu-id="105a2-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="105a2-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="105a2-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="105a2-139">NOTES</span></span>

## <span data-ttu-id="105a2-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="105a2-140">RELATED LINKS</span></span>

[<span data-ttu-id="105a2-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="105a2-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="105a2-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="105a2-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)
