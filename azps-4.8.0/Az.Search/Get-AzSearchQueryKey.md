---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: a0dddf6e7cc5080ca4028b1348381c1b5fb72df6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236629"
---
# <span data-ttu-id="b03df-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="b03df-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="b03df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b03df-102">SYNOPSIS</span></span>
<span data-ttu-id="b03df-103">Возвращает ключи запроса службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="b03df-103">Gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="b03df-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b03df-104">SYNTAX</span></span>

### <span data-ttu-id="b03df-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b03df-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b03df-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b03df-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b03df-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b03df-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b03df-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b03df-108">DESCRIPTION</span></span>
<span data-ttu-id="b03df-109">Командлет **Get-AzSearchQueryKey** получает ключи запросов службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="b03df-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="b03df-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b03df-110">EXAMPLES</span></span>

### <span data-ttu-id="b03df-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b03df-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="b03df-112">В примере получается список всех ключей запроса службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="b03df-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="b03df-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b03df-113">PARAMETERS</span></span>

### <span data-ttu-id="b03df-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b03df-114">-DefaultProfile</span></span>
<span data-ttu-id="b03df-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b03df-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b03df-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b03df-116">-ParentObject</span></span>
<span data-ttu-id="b03df-117">Объект ввода службы поиска.</span><span class="sxs-lookup"><span data-stu-id="b03df-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="b03df-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b03df-118">-ParentResourceId</span></span>
<span data-ttu-id="b03df-119">Идентификатор ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="b03df-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="b03df-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b03df-120">-ResourceGroupName</span></span>
<span data-ttu-id="b03df-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b03df-121">Resource Group name.</span></span>

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

### <span data-ttu-id="b03df-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b03df-122">-ServiceName</span></span>
<span data-ttu-id="b03df-123">Имя службы поиска.</span><span class="sxs-lookup"><span data-stu-id="b03df-123">Search Service name.</span></span>

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

### <span data-ttu-id="b03df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b03df-124">CommonParameters</span></span>
<span data-ttu-id="b03df-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b03df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b03df-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b03df-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b03df-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b03df-127">INPUTS</span></span>

### <span data-ttu-id="b03df-128">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="b03df-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="b03df-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b03df-129">System.String</span></span>

## <span data-ttu-id="b03df-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b03df-130">OUTPUTS</span></span>

### <span data-ttu-id="b03df-131">Microsoft. Azure. Commands. Management. Search. Models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="b03df-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="b03df-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="b03df-132">NOTES</span></span>

## <span data-ttu-id="b03df-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b03df-133">RELATED LINKS</span></span>

[<span data-ttu-id="b03df-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="b03df-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="b03df-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="b03df-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)