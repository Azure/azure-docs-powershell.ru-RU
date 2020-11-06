---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchAdminKeyPair.md
ms.openlocfilehash: 92b2e7304c0f837e47f7464e84769478902c973a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566413"
---
# <span data-ttu-id="d2a37-101">Get-AzureRmSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="d2a37-101">Get-AzureRmSearchAdminKeyPair</span></span>

## <span data-ttu-id="d2a37-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2a37-102">SYNOPSIS</span></span>
<span data-ttu-id="d2a37-103">Возвращает пару ключей администратора службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="d2a37-103">Gets admin key pair of the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2a37-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2a37-104">SYNTAX</span></span>

### <span data-ttu-id="d2a37-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d2a37-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2a37-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2a37-106">ParentObjectParameterSet</span></span>
```
Get-AzureRmSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2a37-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2a37-107">ParentResourceIdParameterSet</span></span>
```
Get-AzureRmSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2a37-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2a37-108">DESCRIPTION</span></span>
<span data-ttu-id="d2a37-109">Командлет **Get-AzureRmSearchAdminKeyPair** получает пару ключей администратора службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="d2a37-109">The **Get-AzureRmSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="d2a37-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2a37-110">EXAMPLES</span></span>

### <span data-ttu-id="d2a37-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d2a37-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="d2a37-112">Пример получает пару ключей администратора службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="d2a37-112">The example gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="d2a37-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2a37-113">PARAMETERS</span></span>

### <span data-ttu-id="d2a37-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2a37-114">-DefaultProfile</span></span>
<span data-ttu-id="d2a37-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2a37-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2a37-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d2a37-116">-ParentObject</span></span>
<span data-ttu-id="d2a37-117">Объект ввода службы поиска.</span><span class="sxs-lookup"><span data-stu-id="d2a37-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="d2a37-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d2a37-118">-ParentResourceId</span></span>
<span data-ttu-id="d2a37-119">Идентификатор ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="d2a37-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="d2a37-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2a37-120">-ResourceGroupName</span></span>
<span data-ttu-id="d2a37-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d2a37-121">Resource Group name.</span></span>

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

### <span data-ttu-id="d2a37-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d2a37-122">-ServiceName</span></span>
<span data-ttu-id="d2a37-123">Имя службы поиска.</span><span class="sxs-lookup"><span data-stu-id="d2a37-123">Search Service name.</span></span>

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

### <span data-ttu-id="d2a37-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2a37-124">CommonParameters</span></span>
<span data-ttu-id="d2a37-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2a37-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2a37-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2a37-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2a37-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2a37-127">INPUTS</span></span>

### <span data-ttu-id="d2a37-128">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="d2a37-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="d2a37-129">Параметры: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d2a37-129">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="d2a37-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d2a37-130">System.String</span></span>

## <span data-ttu-id="d2a37-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2a37-131">OUTPUTS</span></span>

### <span data-ttu-id="d2a37-132">Microsoft. Azure. Commands. Management. Search. Models. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="d2a37-132">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="d2a37-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2a37-133">NOTES</span></span>

## <span data-ttu-id="d2a37-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2a37-134">RELATED LINKS</span></span>

[<span data-ttu-id="d2a37-135">New-AzureRmSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="d2a37-135">New-AzureRmSearchAdminKey</span></span>](./New-AzureRmSearchAdminKey.md)
