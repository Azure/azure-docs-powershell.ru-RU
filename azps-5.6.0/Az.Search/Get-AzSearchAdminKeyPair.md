---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-azsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
ms.openlocfilehash: bef03e951982854e00412d08c609146b55e54ef3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953043"
---
# <span data-ttu-id="a132a-101">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="a132a-101">Get-AzSearchAdminKeyPair</span></span>

## <span data-ttu-id="a132a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a132a-102">SYNOPSIS</span></span>
<span data-ttu-id="a132a-103">Возвращает пару ключей администратора для службы azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="a132a-103">Gets admin key pair of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="a132a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a132a-104">SYNTAX</span></span>

### <span data-ttu-id="a132a-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a132a-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a132a-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a132a-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a132a-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a132a-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a132a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a132a-108">DESCRIPTION</span></span>
<span data-ttu-id="a132a-109">С **помощью cmdlet get-AzSearchAdminKeyPair** можно получить ключевую пару администратора службы azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="a132a-109">The **Get-AzSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="a132a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a132a-110">EXAMPLES</span></span>

### <span data-ttu-id="a132a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a132a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="a132a-112">В этом примере используется пара ключей администратора для службы azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="a132a-112">The example gets admin key pair of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="a132a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a132a-113">PARAMETERS</span></span>

### <span data-ttu-id="a132a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a132a-114">-DefaultProfile</span></span>
<span data-ttu-id="a132a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a132a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a132a-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a132a-116">-ParentObject</span></span>
<span data-ttu-id="a132a-117">Объект ввода службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="a132a-117">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="a132a-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a132a-118">-ParentResourceId</span></span>
<span data-ttu-id="a132a-119">ИД ресурса службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="a132a-119">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="a132a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a132a-120">-ResourceGroupName</span></span>
<span data-ttu-id="a132a-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a132a-121">Resource Group name.</span></span>

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

### <span data-ttu-id="a132a-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a132a-122">-ServiceName</span></span>
<span data-ttu-id="a132a-123">Имя службы поиска данных Azure.</span><span class="sxs-lookup"><span data-stu-id="a132a-123">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="a132a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a132a-124">CommonParameters</span></span>
<span data-ttu-id="a132a-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a132a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a132a-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a132a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a132a-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a132a-127">INPUTS</span></span>

### <span data-ttu-id="a132a-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="a132a-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="a132a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a132a-129">System.String</span></span>

## <span data-ttu-id="a132a-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a132a-130">OUTPUTS</span></span>

### <span data-ttu-id="a132a-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="a132a-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="a132a-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a132a-132">NOTES</span></span>

## <span data-ttu-id="a132a-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a132a-133">RELATED LINKS</span></span>

[<span data-ttu-id="a132a-134">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="a132a-134">New-AzSearchAdminKey</span></span>](./New-AzSearchAdminKey.md)
