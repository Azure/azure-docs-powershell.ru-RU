---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: e01e5e244bd34e3e18aa287e0f2f5709c5e208ec
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912615"
---
# <span data-ttu-id="d65e2-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="d65e2-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="d65e2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d65e2-102">SYNOPSIS</span></span>
<span data-ttu-id="d65e2-103">Создание нового ключа запроса для службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="d65e2-103">Create a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="d65e2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d65e2-104">SYNTAX</span></span>

### <span data-ttu-id="d65e2-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d65e2-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d65e2-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d65e2-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d65e2-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d65e2-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d65e2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d65e2-108">DESCRIPTION</span></span>
<span data-ttu-id="d65e2-109">Командлет **New-AzSearchQueryKey** создает новый ключ запроса для службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="d65e2-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Search Service.</span></span>

## <span data-ttu-id="d65e2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d65e2-110">EXAMPLES</span></span>

### <span data-ttu-id="d65e2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d65e2-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="d65e2-112">В примере создается новый ключ запроса для службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="d65e2-112">The example creates a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="d65e2-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d65e2-113">PARAMETERS</span></span>

### <span data-ttu-id="d65e2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d65e2-114">-DefaultProfile</span></span>
<span data-ttu-id="d65e2-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d65e2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d65e2-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d65e2-116">-Name</span></span>
<span data-ttu-id="d65e2-117">Имя ключа запроса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="d65e2-117">Search Service query key name.</span></span>

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

### <span data-ttu-id="d65e2-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d65e2-118">-ParentObject</span></span>
<span data-ttu-id="d65e2-119">Объект ввода службы поиска.</span><span class="sxs-lookup"><span data-stu-id="d65e2-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="d65e2-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d65e2-120">-ParentResourceId</span></span>
<span data-ttu-id="d65e2-121">Идентификатор ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="d65e2-121">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="d65e2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d65e2-122">-ResourceGroupName</span></span>
<span data-ttu-id="d65e2-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d65e2-123">Resource Group name.</span></span>

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

### <span data-ttu-id="d65e2-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d65e2-124">-ServiceName</span></span>
<span data-ttu-id="d65e2-125">Имя службы поиска.</span><span class="sxs-lookup"><span data-stu-id="d65e2-125">Search Service name.</span></span>

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

### <span data-ttu-id="d65e2-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d65e2-126">-Confirm</span></span>
<span data-ttu-id="d65e2-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d65e2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d65e2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d65e2-128">-WhatIf</span></span>
<span data-ttu-id="d65e2-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d65e2-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d65e2-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d65e2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d65e2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d65e2-131">CommonParameters</span></span>
<span data-ttu-id="d65e2-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d65e2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d65e2-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d65e2-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d65e2-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d65e2-134">INPUTS</span></span>

### <span data-ttu-id="d65e2-135">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="d65e2-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="d65e2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d65e2-136">System.String</span></span>

## <span data-ttu-id="d65e2-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d65e2-137">OUTPUTS</span></span>

### <span data-ttu-id="d65e2-138">Microsoft. Azure. Commands. Management. Search. Models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="d65e2-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="d65e2-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="d65e2-139">NOTES</span></span>

## <span data-ttu-id="d65e2-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d65e2-140">RELATED LINKS</span></span>

[<span data-ttu-id="d65e2-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="d65e2-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="d65e2-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="d65e2-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)
