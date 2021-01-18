---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
ms.openlocfilehash: dafc9da9669a7c07f982e4fee87a37e1581af40a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505959"
---
# <span data-ttu-id="e0092-101">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="e0092-101">Get-AzSearchAdminKeyPair</span></span>

## <span data-ttu-id="e0092-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0092-102">SYNOPSIS</span></span>
<span data-ttu-id="e0092-103">Получает пару ключей администратора для службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="e0092-103">Gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="e0092-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e0092-104">SYNTAX</span></span>

### <span data-ttu-id="e0092-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e0092-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0092-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0092-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0092-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0092-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0092-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0092-108">DESCRIPTION</span></span>
<span data-ttu-id="e0092-109">Для получения ключевой пары службы поиска Azure используется cmdlet **Get-AzSearchAdminKeyPair.**</span><span class="sxs-lookup"><span data-stu-id="e0092-109">The **Get-AzSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="e0092-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e0092-110">EXAMPLES</span></span>

### <span data-ttu-id="e0092-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e0092-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="e0092-112">В этом примере используется пара ключей администратора для службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="e0092-112">The example gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="e0092-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0092-113">PARAMETERS</span></span>

### <span data-ttu-id="e0092-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0092-114">-DefaultProfile</span></span>
<span data-ttu-id="e0092-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0092-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0092-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e0092-116">-ParentObject</span></span>
<span data-ttu-id="e0092-117">Объект ввода службы поиска.</span><span class="sxs-lookup"><span data-stu-id="e0092-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="e0092-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e0092-118">-ParentResourceId</span></span>
<span data-ttu-id="e0092-119">ИД ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="e0092-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="e0092-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0092-120">-ResourceGroupName</span></span>
<span data-ttu-id="e0092-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e0092-121">Resource Group name.</span></span>

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

### <span data-ttu-id="e0092-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e0092-122">-ServiceName</span></span>
<span data-ttu-id="e0092-123">Название службы поиска.</span><span class="sxs-lookup"><span data-stu-id="e0092-123">Search Service name.</span></span>

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

### <span data-ttu-id="e0092-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0092-124">CommonParameters</span></span>
<span data-ttu-id="e0092-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0092-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0092-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0092-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0092-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0092-127">INPUTS</span></span>

### <span data-ttu-id="e0092-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="e0092-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="e0092-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e0092-129">System.String</span></span>

## <span data-ttu-id="e0092-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e0092-130">OUTPUTS</span></span>

### <span data-ttu-id="e0092-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="e0092-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="e0092-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e0092-132">NOTES</span></span>

## <span data-ttu-id="e0092-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0092-133">RELATED LINKS</span></span>

[<span data-ttu-id="e0092-134">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="e0092-134">New-AzSearchAdminKey</span></span>](./New-AzSearchAdminKey.md)
