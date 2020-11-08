---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
ms.openlocfilehash: dafc9da9669a7c07f982e4fee87a37e1581af40a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236630"
---
# <span data-ttu-id="908c7-101">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="908c7-101">Get-AzSearchAdminKeyPair</span></span>

## <span data-ttu-id="908c7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="908c7-102">SYNOPSIS</span></span>
<span data-ttu-id="908c7-103">Возвращает пару ключей администратора службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="908c7-103">Gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="908c7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="908c7-104">SYNTAX</span></span>

### <span data-ttu-id="908c7-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="908c7-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="908c7-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="908c7-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="908c7-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="908c7-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="908c7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="908c7-108">DESCRIPTION</span></span>
<span data-ttu-id="908c7-109">Командлет **Get-AzSearchAdminKeyPair** получает пару ключей администратора службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="908c7-109">The **Get-AzSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="908c7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="908c7-110">EXAMPLES</span></span>

### <span data-ttu-id="908c7-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="908c7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="908c7-112">Пример получает пару ключей администратора службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="908c7-112">The example gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="908c7-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="908c7-113">PARAMETERS</span></span>

### <span data-ttu-id="908c7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="908c7-114">-DefaultProfile</span></span>
<span data-ttu-id="908c7-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="908c7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="908c7-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="908c7-116">-ParentObject</span></span>
<span data-ttu-id="908c7-117">Объект ввода службы поиска.</span><span class="sxs-lookup"><span data-stu-id="908c7-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="908c7-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="908c7-118">-ParentResourceId</span></span>
<span data-ttu-id="908c7-119">Идентификатор ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="908c7-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="908c7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="908c7-120">-ResourceGroupName</span></span>
<span data-ttu-id="908c7-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="908c7-121">Resource Group name.</span></span>

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

### <span data-ttu-id="908c7-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="908c7-122">-ServiceName</span></span>
<span data-ttu-id="908c7-123">Имя службы поиска.</span><span class="sxs-lookup"><span data-stu-id="908c7-123">Search Service name.</span></span>

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

### <span data-ttu-id="908c7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="908c7-124">CommonParameters</span></span>
<span data-ttu-id="908c7-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="908c7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="908c7-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="908c7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="908c7-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="908c7-127">INPUTS</span></span>

### <span data-ttu-id="908c7-128">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="908c7-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="908c7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="908c7-129">System.String</span></span>

## <span data-ttu-id="908c7-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="908c7-130">OUTPUTS</span></span>

### <span data-ttu-id="908c7-131">Microsoft. Azure. Commands. Management. Search. Models. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="908c7-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="908c7-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="908c7-132">NOTES</span></span>

## <span data-ttu-id="908c7-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="908c7-133">RELATED LINKS</span></span>

[<span data-ttu-id="908c7-134">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="908c7-134">New-AzSearchAdminKey</span></span>](./New-AzSearchAdminKey.md)