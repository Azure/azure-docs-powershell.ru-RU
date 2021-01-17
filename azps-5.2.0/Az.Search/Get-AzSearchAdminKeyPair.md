---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
ms.openlocfilehash: dafc9da9669a7c07f982e4fee87a37e1581af40a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416836"
---
# <span data-ttu-id="aea5d-101">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="aea5d-101">Get-AzSearchAdminKeyPair</span></span>

## <span data-ttu-id="aea5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aea5d-102">SYNOPSIS</span></span>
<span data-ttu-id="aea5d-103">Получает пару ключей администратора для службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="aea5d-103">Gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="aea5d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aea5d-104">SYNTAX</span></span>

### <span data-ttu-id="aea5d-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aea5d-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aea5d-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aea5d-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aea5d-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aea5d-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aea5d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aea5d-108">DESCRIPTION</span></span>
<span data-ttu-id="aea5d-109">Для получения ключевой пары службы поиска Azure используется cmdlet **Get-AzSearchAdminKeyPair.**</span><span class="sxs-lookup"><span data-stu-id="aea5d-109">The **Get-AzSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="aea5d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aea5d-110">EXAMPLES</span></span>

### <span data-ttu-id="aea5d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aea5d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="aea5d-112">В этом примере используется пара ключей администратора для службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="aea5d-112">The example gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="aea5d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aea5d-113">PARAMETERS</span></span>

### <span data-ttu-id="aea5d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aea5d-114">-DefaultProfile</span></span>
<span data-ttu-id="aea5d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aea5d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aea5d-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="aea5d-116">-ParentObject</span></span>
<span data-ttu-id="aea5d-117">Объект ввода службы поиска.</span><span class="sxs-lookup"><span data-stu-id="aea5d-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="aea5d-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="aea5d-118">-ParentResourceId</span></span>
<span data-ttu-id="aea5d-119">ИД ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="aea5d-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="aea5d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aea5d-120">-ResourceGroupName</span></span>
<span data-ttu-id="aea5d-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aea5d-121">Resource Group name.</span></span>

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

### <span data-ttu-id="aea5d-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="aea5d-122">-ServiceName</span></span>
<span data-ttu-id="aea5d-123">Название службы поиска.</span><span class="sxs-lookup"><span data-stu-id="aea5d-123">Search Service name.</span></span>

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

### <span data-ttu-id="aea5d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea5d-124">CommonParameters</span></span>
<span data-ttu-id="aea5d-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aea5d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea5d-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aea5d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea5d-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aea5d-127">INPUTS</span></span>

### <span data-ttu-id="aea5d-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="aea5d-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="aea5d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="aea5d-129">System.String</span></span>

## <span data-ttu-id="aea5d-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aea5d-130">OUTPUTS</span></span>

### <span data-ttu-id="aea5d-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="aea5d-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="aea5d-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aea5d-132">NOTES</span></span>

## <span data-ttu-id="aea5d-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aea5d-133">RELATED LINKS</span></span>

[<span data-ttu-id="aea5d-134">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="aea5d-134">New-AzSearchAdminKey</span></span>](./New-AzSearchAdminKey.md)
