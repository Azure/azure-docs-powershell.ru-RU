---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchQueryKey.md
ms.openlocfilehash: 3535e9d7723c87e0f528192e47c921d3835ff9e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560647"
---
# <span data-ttu-id="8edb0-101">Get-AzureRmSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="8edb0-101">Get-AzureRmSearchQueryKey</span></span>

## <span data-ttu-id="8edb0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8edb0-102">SYNOPSIS</span></span>
<span data-ttu-id="8edb0-103">Возвращает ключи запроса службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="8edb0-103">Gets query key(s) of the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8edb0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8edb0-104">SYNTAX</span></span>

### <span data-ttu-id="8edb0-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8edb0-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8edb0-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8edb0-106">ParentObjectParameterSet</span></span>
```
Get-AzureRmSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8edb0-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8edb0-107">ParentResourceIdParameterSet</span></span>
```
Get-AzureRmSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8edb0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8edb0-108">DESCRIPTION</span></span>
<span data-ttu-id="8edb0-109">Командлет **Get-AzureRmSearchQueryKey** получает ключи запросов службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="8edb0-109">The **Get-AzureRmSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="8edb0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8edb0-110">EXAMPLES</span></span>

### <span data-ttu-id="8edb0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8edb0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="8edb0-112">В примере получается список всех ключей запроса службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="8edb0-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="8edb0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8edb0-113">PARAMETERS</span></span>

### <span data-ttu-id="8edb0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8edb0-114">-DefaultProfile</span></span>
<span data-ttu-id="8edb0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8edb0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8edb0-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8edb0-116">-ParentObject</span></span>
<span data-ttu-id="8edb0-117">Объект ввода службы поиска.</span><span class="sxs-lookup"><span data-stu-id="8edb0-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="8edb0-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8edb0-118">-ParentResourceId</span></span>
<span data-ttu-id="8edb0-119">Идентификатор ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="8edb0-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="8edb0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8edb0-120">-ResourceGroupName</span></span>
<span data-ttu-id="8edb0-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8edb0-121">Resource Group name.</span></span>

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

### <span data-ttu-id="8edb0-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8edb0-122">-ServiceName</span></span>
<span data-ttu-id="8edb0-123">Имя службы поиска.</span><span class="sxs-lookup"><span data-stu-id="8edb0-123">Search Service name.</span></span>

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

### <span data-ttu-id="8edb0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8edb0-124">CommonParameters</span></span>
<span data-ttu-id="8edb0-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8edb0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8edb0-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8edb0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8edb0-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8edb0-127">INPUTS</span></span>

### <span data-ttu-id="8edb0-128">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="8edb0-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="8edb0-129">Параметры: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8edb0-129">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="8edb0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8edb0-130">System.String</span></span>

## <span data-ttu-id="8edb0-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8edb0-131">OUTPUTS</span></span>

### <span data-ttu-id="8edb0-132">Microsoft. Azure. Commands. Management. Search. Models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="8edb0-132">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="8edb0-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="8edb0-133">NOTES</span></span>

## <span data-ttu-id="8edb0-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8edb0-134">RELATED LINKS</span></span>

[<span data-ttu-id="8edb0-135">New-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="8edb0-135">New-AzureRmSearchQueryKey.md</span></span>](./New-AzureRmSearchQueryKey.md)

[<span data-ttu-id="8edb0-136">Remove-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="8edb0-136">Remove-AzureRmSearchQueryKey.md</span></span>](./Remove-AzureRmSearchQueryKey.md)
