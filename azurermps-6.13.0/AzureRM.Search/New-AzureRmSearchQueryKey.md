---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/new-azurermsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchQueryKey.md
ms.openlocfilehash: 417e1a546777824df86b72f3740079ac91835192
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566768"
---
# <span data-ttu-id="9bb93-101">New-AzureRmSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="9bb93-101">New-AzureRmSearchQueryKey</span></span>

## <span data-ttu-id="9bb93-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9bb93-102">SYNOPSIS</span></span>
<span data-ttu-id="9bb93-103">Создание нового ключа запроса для службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="9bb93-103">Create a new query key for the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bb93-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9bb93-104">SYNTAX</span></span>

### <span data-ttu-id="9bb93-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9bb93-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bb93-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bb93-106">ParentObjectParameterSet</span></span>
```
New-AzureRmSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bb93-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bb93-107">ParentResourceIdParameterSet</span></span>
```
New-AzureRmSearchQueryKey [-ParentResourceId] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bb93-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bb93-108">DESCRIPTION</span></span>
<span data-ttu-id="9bb93-109">Командлет **New-AzureRmSearchQueryKey** создает новый ключ запроса для службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="9bb93-109">The **New-AzureRmSearchQueryKey** cmdlet creates a new query key for the Azure Search Service.</span></span>

## <span data-ttu-id="9bb93-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9bb93-110">EXAMPLES</span></span>

### <span data-ttu-id="9bb93-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9bb93-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="9bb93-112">В примере создается новый ключ запроса для службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="9bb93-112">The example creates a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="9bb93-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9bb93-113">PARAMETERS</span></span>

### <span data-ttu-id="9bb93-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bb93-114">-DefaultProfile</span></span>
<span data-ttu-id="9bb93-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9bb93-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bb93-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9bb93-116">-Name</span></span>
<span data-ttu-id="9bb93-117">Имя ключа запроса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="9bb93-117">Search Service query key name.</span></span>

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

### <span data-ttu-id="9bb93-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9bb93-118">-ParentObject</span></span>
<span data-ttu-id="9bb93-119">Объект ввода службы поиска.</span><span class="sxs-lookup"><span data-stu-id="9bb93-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="9bb93-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9bb93-120">-ParentResourceId</span></span>
<span data-ttu-id="9bb93-121">Идентификатор ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="9bb93-121">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="9bb93-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bb93-122">-ResourceGroupName</span></span>
<span data-ttu-id="9bb93-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9bb93-123">Resource Group name.</span></span>

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

### <span data-ttu-id="9bb93-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9bb93-124">-ServiceName</span></span>
<span data-ttu-id="9bb93-125">Имя службы поиска.</span><span class="sxs-lookup"><span data-stu-id="9bb93-125">Search Service name.</span></span>

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

### <span data-ttu-id="9bb93-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9bb93-126">-Confirm</span></span>
<span data-ttu-id="9bb93-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9bb93-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bb93-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bb93-128">-WhatIf</span></span>
<span data-ttu-id="9bb93-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9bb93-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9bb93-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9bb93-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bb93-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bb93-131">CommonParameters</span></span>
<span data-ttu-id="9bb93-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9bb93-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bb93-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bb93-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bb93-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9bb93-134">INPUTS</span></span>

### <span data-ttu-id="9bb93-135">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="9bb93-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="9bb93-136">Параметры: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9bb93-136">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="9bb93-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9bb93-137">System.String</span></span>

## <span data-ttu-id="9bb93-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bb93-138">OUTPUTS</span></span>

### <span data-ttu-id="9bb93-139">Microsoft. Azure. Commands. Management. Search. Models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="9bb93-139">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="9bb93-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="9bb93-140">NOTES</span></span>

## <span data-ttu-id="9bb93-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9bb93-141">RELATED LINKS</span></span>

[<span data-ttu-id="9bb93-142">Get-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="9bb93-142">Get-AzureRmSearchQueryKey.md</span></span>](./Get-AzureRmSearchQueryKey.md)

[<span data-ttu-id="9bb93-143">Remove-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="9bb93-143">Remove-AzureRmSearchQueryKey.md</span></span>](./Remove-AzureRmSearchQueryKey.md)
