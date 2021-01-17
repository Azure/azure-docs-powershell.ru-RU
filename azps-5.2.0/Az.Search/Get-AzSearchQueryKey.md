---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: a0dddf6e7cc5080ca4028b1348381c1b5fb72df6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393703"
---
# <span data-ttu-id="e0be8-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="e0be8-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="e0be8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0be8-102">SYNOPSIS</span></span>
<span data-ttu-id="e0be8-103">Получает ключи запросов службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="e0be8-103">Gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="e0be8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e0be8-104">SYNTAX</span></span>

### <span data-ttu-id="e0be8-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e0be8-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0be8-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0be8-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0be8-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0be8-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0be8-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0be8-108">DESCRIPTION</span></span>
<span data-ttu-id="e0be8-109">Для получения ключей запроса в службе поиска Azure возвращается cmdlet **Get-AzSearchQueryKey.**</span><span class="sxs-lookup"><span data-stu-id="e0be8-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="e0be8-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e0be8-110">EXAMPLES</span></span>

### <span data-ttu-id="e0be8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e0be8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="e0be8-112">В этом примере получаются все клавиши запросов службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="e0be8-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="e0be8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0be8-113">PARAMETERS</span></span>

### <span data-ttu-id="e0be8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0be8-114">-DefaultProfile</span></span>
<span data-ttu-id="e0be8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0be8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0be8-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e0be8-116">-ParentObject</span></span>
<span data-ttu-id="e0be8-117">Объект ввода службы поиска.</span><span class="sxs-lookup"><span data-stu-id="e0be8-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="e0be8-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e0be8-118">-ParentResourceId</span></span>
<span data-ttu-id="e0be8-119">ИД ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="e0be8-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="e0be8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0be8-120">-ResourceGroupName</span></span>
<span data-ttu-id="e0be8-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e0be8-121">Resource Group name.</span></span>

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

### <span data-ttu-id="e0be8-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e0be8-122">-ServiceName</span></span>
<span data-ttu-id="e0be8-123">Название службы поиска.</span><span class="sxs-lookup"><span data-stu-id="e0be8-123">Search Service name.</span></span>

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

### <span data-ttu-id="e0be8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0be8-124">CommonParameters</span></span>
<span data-ttu-id="e0be8-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0be8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0be8-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0be8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0be8-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0be8-127">INPUTS</span></span>

### <span data-ttu-id="e0be8-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="e0be8-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="e0be8-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e0be8-129">System.String</span></span>

## <span data-ttu-id="e0be8-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e0be8-130">OUTPUTS</span></span>

### <span data-ttu-id="e0be8-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="e0be8-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="e0be8-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e0be8-132">NOTES</span></span>

## <span data-ttu-id="e0be8-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0be8-133">RELATED LINKS</span></span>

[<span data-ttu-id="e0be8-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="e0be8-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="e0be8-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="e0be8-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)