---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: 1c5845b0273d47f1aa1a18782a9243bc5ee5ca9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242429"
---
# <span data-ttu-id="fd47a-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="fd47a-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="fd47a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd47a-102">SYNOPSIS</span></span>
<span data-ttu-id="fd47a-103">Получает клавиши запросов службы поиска когнитивных функций Azure.</span><span class="sxs-lookup"><span data-stu-id="fd47a-103">Gets query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="fd47a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fd47a-104">SYNTAX</span></span>

### <span data-ttu-id="fd47a-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fd47a-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd47a-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd47a-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fd47a-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd47a-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd47a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd47a-108">DESCRIPTION</span></span>
<span data-ttu-id="fd47a-109">Для получения ключей запроса от службы azure Cognitive Search возвращается ключ запроса **get-azSearchQueryKey.**</span><span class="sxs-lookup"><span data-stu-id="fd47a-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="fd47a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fd47a-110">EXAMPLES</span></span>

### <span data-ttu-id="fd47a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fd47a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="fd47a-112">В этом примере выберем все клавиши запросов службы поиска когнитивных функций Azure.</span><span class="sxs-lookup"><span data-stu-id="fd47a-112">The example gets all query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="fd47a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd47a-113">PARAMETERS</span></span>

### <span data-ttu-id="fd47a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd47a-114">-DefaultProfile</span></span>
<span data-ttu-id="fd47a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd47a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd47a-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fd47a-116">-ParentObject</span></span>
<span data-ttu-id="fd47a-117">Объект ввода службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="fd47a-117">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="fd47a-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fd47a-118">-ParentResourceId</span></span>
<span data-ttu-id="fd47a-119">ИД ресурса службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="fd47a-119">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="fd47a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd47a-120">-ResourceGroupName</span></span>
<span data-ttu-id="fd47a-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fd47a-121">Resource Group name.</span></span>

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

### <span data-ttu-id="fd47a-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fd47a-122">-ServiceName</span></span>
<span data-ttu-id="fd47a-123">Имя службы поиска данных Azure.</span><span class="sxs-lookup"><span data-stu-id="fd47a-123">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="fd47a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd47a-124">CommonParameters</span></span>
<span data-ttu-id="fd47a-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd47a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd47a-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd47a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd47a-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd47a-127">INPUTS</span></span>

### <span data-ttu-id="fd47a-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="fd47a-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="fd47a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="fd47a-129">System.String</span></span>

## <span data-ttu-id="fd47a-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fd47a-130">OUTPUTS</span></span>

### <span data-ttu-id="fd47a-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="fd47a-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="fd47a-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fd47a-132">NOTES</span></span>

## <span data-ttu-id="fd47a-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd47a-133">RELATED LINKS</span></span>

[<span data-ttu-id="fd47a-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="fd47a-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="fd47a-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="fd47a-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)