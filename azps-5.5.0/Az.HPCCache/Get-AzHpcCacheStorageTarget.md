---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
ms.openlocfilehash: c32b47b7300c7da0a6517ca5e3802af60bd0f571
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243488"
---
# <span data-ttu-id="b7a38-101">Get-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="b7a38-101">Get-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="b7a38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7a38-102">SYNOPSIS</span></span>
<span data-ttu-id="b7a38-103">Получите целевые объекты кэша HPC.</span><span class="sxs-lookup"><span data-stu-id="b7a38-103">Get HPC cache storage target(s).</span></span>

## <span data-ttu-id="b7a38-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b7a38-104">SYNTAX</span></span>

### <span data-ttu-id="b7a38-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b7a38-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7a38-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7a38-106">ByResourceIdParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7a38-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7a38-107">ByObjectParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheObject <PSHPCCache> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7a38-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7a38-108">DESCRIPTION</span></span>
<span data-ttu-id="b7a38-109">Для получения целевых объектов хранилища, которые существуют в кэше, получаются целевые объекты хранилища, которые существуют на сайте **Get-AzHpcCacheStorageTarget.**</span><span class="sxs-lookup"><span data-stu-id="b7a38-109">The **Get-AzHpcCacheStorageTarget** cmdlet gets storage target(s) that exist on cache.</span></span>

## <span data-ttu-id="b7a38-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b7a38-110">EXAMPLES</span></span>

### <span data-ttu-id="b7a38-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b7a38-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest
```

### <span data-ttu-id="b7a38-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b7a38-112">Example 2</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest -StorageTargetName stTest
```

## <span data-ttu-id="b7a38-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7a38-113">PARAMETERS</span></span>

### <span data-ttu-id="b7a38-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="b7a38-114">-CacheId</span></span>
<span data-ttu-id="b7a38-115">ИД ресурса кэша</span><span class="sxs-lookup"><span data-stu-id="b7a38-115">The resource id of the Cache</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a38-116">-CacheName</span><span class="sxs-lookup"><span data-stu-id="b7a38-116">-CacheName</span></span>
<span data-ttu-id="b7a38-117">Имя кэша.</span><span class="sxs-lookup"><span data-stu-id="b7a38-117">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a38-118">-CacheObject</span><span class="sxs-lookup"><span data-stu-id="b7a38-118">-CacheObject</span></span>
<span data-ttu-id="b7a38-119">Объект кэша, который нужно запустить.</span><span class="sxs-lookup"><span data-stu-id="b7a38-119">The cache object to start.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a38-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7a38-120">-DefaultProfile</span></span>
<span data-ttu-id="b7a38-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7a38-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7a38-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b7a38-122">-Name</span></span>
<span data-ttu-id="b7a38-123">Имя целевого хранилища.</span><span class="sxs-lookup"><span data-stu-id="b7a38-123">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: StorageTargetName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a38-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7a38-124">-ResourceGroupName</span></span>
<span data-ttu-id="b7a38-125">Имя кэша группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b7a38-125">Name of resource group cache is in.</span></span>


```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a38-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7a38-126">CommonParameters</span></span>
<span data-ttu-id="b7a38-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7a38-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7a38-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7a38-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7a38-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7a38-129">INPUTS</span></span>

### <span data-ttu-id="b7a38-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b7a38-130">System.String</span></span>

## <span data-ttu-id="b7a38-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b7a38-131">OUTPUTS</span></span>

### <span data-ttu-id="b7a38-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="b7a38-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span></span>

## <span data-ttu-id="b7a38-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b7a38-133">NOTES</span></span>

## <span data-ttu-id="b7a38-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7a38-134">RELATED LINKS</span></span>
