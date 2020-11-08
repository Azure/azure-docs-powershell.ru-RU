---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: e01e5e244bd34e3e18aa287e0f2f5709c5e208ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235379"
---
# <span data-ttu-id="1c86f-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="1c86f-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="1c86f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1c86f-102">SYNOPSIS</span></span>
<span data-ttu-id="1c86f-103">Создание нового ключа запроса для службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="1c86f-103">Create a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="1c86f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1c86f-104">SYNTAX</span></span>

### <span data-ttu-id="1c86f-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1c86f-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c86f-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c86f-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c86f-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c86f-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c86f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c86f-108">DESCRIPTION</span></span>
<span data-ttu-id="1c86f-109">Командлет **New-AzSearchQueryKey** создает новый ключ запроса для службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="1c86f-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Search Service.</span></span>

## <span data-ttu-id="1c86f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1c86f-110">EXAMPLES</span></span>

### <span data-ttu-id="1c86f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1c86f-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="1c86f-112">В примере создается новый ключ запроса для службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="1c86f-112">The example creates a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="1c86f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1c86f-113">PARAMETERS</span></span>

### <span data-ttu-id="1c86f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c86f-114">-DefaultProfile</span></span>
<span data-ttu-id="1c86f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1c86f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c86f-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1c86f-116">-Name</span></span>
<span data-ttu-id="1c86f-117">Имя ключа запроса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="1c86f-117">Search Service query key name.</span></span>

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

### <span data-ttu-id="1c86f-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1c86f-118">-ParentObject</span></span>
<span data-ttu-id="1c86f-119">Объект ввода службы поиска.</span><span class="sxs-lookup"><span data-stu-id="1c86f-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="1c86f-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1c86f-120">-ParentResourceId</span></span>
<span data-ttu-id="1c86f-121">Идентификатор ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="1c86f-121">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="1c86f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c86f-122">-ResourceGroupName</span></span>
<span data-ttu-id="1c86f-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c86f-123">Resource Group name.</span></span>

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

### <span data-ttu-id="1c86f-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1c86f-124">-ServiceName</span></span>
<span data-ttu-id="1c86f-125">Имя службы поиска.</span><span class="sxs-lookup"><span data-stu-id="1c86f-125">Search Service name.</span></span>

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

### <span data-ttu-id="1c86f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c86f-126">-Confirm</span></span>
<span data-ttu-id="1c86f-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1c86f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c86f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c86f-128">-WhatIf</span></span>
<span data-ttu-id="1c86f-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1c86f-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c86f-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1c86f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c86f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c86f-131">CommonParameters</span></span>
<span data-ttu-id="1c86f-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1c86f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c86f-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c86f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c86f-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1c86f-134">INPUTS</span></span>

### <span data-ttu-id="1c86f-135">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="1c86f-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="1c86f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1c86f-136">System.String</span></span>

## <span data-ttu-id="1c86f-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c86f-137">OUTPUTS</span></span>

### <span data-ttu-id="1c86f-138">Microsoft. Azure. Commands. Management. Search. Models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="1c86f-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="1c86f-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="1c86f-139">NOTES</span></span>

## <span data-ttu-id="1c86f-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c86f-140">RELATED LINKS</span></span>

[<span data-ttu-id="1c86f-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="1c86f-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="1c86f-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="1c86f-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)
