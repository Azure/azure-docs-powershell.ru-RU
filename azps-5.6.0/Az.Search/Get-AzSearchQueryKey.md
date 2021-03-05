---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: 9bd662c5164660f6bc330e3b2ee2eced2893dbce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988851"
---
# <span data-ttu-id="335d0-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="335d0-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="335d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="335d0-102">SYNOPSIS</span></span>
<span data-ttu-id="335d0-103">Получает клавиши запросов службы поиска когнитивных функций Azure.</span><span class="sxs-lookup"><span data-stu-id="335d0-103">Gets query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="335d0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="335d0-104">SYNTAX</span></span>

### <span data-ttu-id="335d0-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="335d0-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="335d0-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="335d0-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="335d0-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="335d0-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="335d0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="335d0-108">DESCRIPTION</span></span>
<span data-ttu-id="335d0-109">Для получения ключей запроса от службы azure Cognitive Search возвращается ключ запроса **get-azSearchQueryKey.**</span><span class="sxs-lookup"><span data-stu-id="335d0-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="335d0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="335d0-110">EXAMPLES</span></span>

### <span data-ttu-id="335d0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="335d0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="335d0-112">В этом примере выберем все клавиши запросов службы поиска когнитивных функций Azure.</span><span class="sxs-lookup"><span data-stu-id="335d0-112">The example gets all query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="335d0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="335d0-113">PARAMETERS</span></span>

### <span data-ttu-id="335d0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="335d0-114">-DefaultProfile</span></span>
<span data-ttu-id="335d0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="335d0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="335d0-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="335d0-116">-ParentObject</span></span>
<span data-ttu-id="335d0-117">Объект ввода службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="335d0-117">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="335d0-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="335d0-118">-ParentResourceId</span></span>
<span data-ttu-id="335d0-119">ИД ресурса службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="335d0-119">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="335d0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="335d0-120">-ResourceGroupName</span></span>
<span data-ttu-id="335d0-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="335d0-121">Resource Group name.</span></span>

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

### <span data-ttu-id="335d0-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="335d0-122">-ServiceName</span></span>
<span data-ttu-id="335d0-123">Имя службы поиска данных Azure.</span><span class="sxs-lookup"><span data-stu-id="335d0-123">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="335d0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="335d0-124">CommonParameters</span></span>
<span data-ttu-id="335d0-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="335d0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="335d0-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="335d0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="335d0-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="335d0-127">INPUTS</span></span>

### <span data-ttu-id="335d0-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="335d0-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="335d0-129">System.String</span><span class="sxs-lookup"><span data-stu-id="335d0-129">System.String</span></span>

## <span data-ttu-id="335d0-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="335d0-130">OUTPUTS</span></span>

### <span data-ttu-id="335d0-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="335d0-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="335d0-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="335d0-132">NOTES</span></span>

## <span data-ttu-id="335d0-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="335d0-133">RELATED LINKS</span></span>

[<span data-ttu-id="335d0-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="335d0-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="335d0-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="335d0-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)