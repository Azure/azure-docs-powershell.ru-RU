---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
ms.openlocfilehash: c32b47b7300c7da0a6517ca5e3802af60bd0f571
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079623"
---
# <span data-ttu-id="f7878-101">Get-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="f7878-101">Get-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="f7878-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7878-102">SYNOPSIS</span></span>
<span data-ttu-id="f7878-103">Приобретите целевые объекты хранилища для кэша HPC (s).</span><span class="sxs-lookup"><span data-stu-id="f7878-103">Get HPC cache storage target(s).</span></span>

## <span data-ttu-id="f7878-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7878-104">SYNTAX</span></span>

### <span data-ttu-id="f7878-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f7878-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7878-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7878-106">ByResourceIdParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7878-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7878-107">ByObjectParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheObject <PSHPCCache> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7878-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7878-108">DESCRIPTION</span></span>
<span data-ttu-id="f7878-109">Командлет **Get-AzHpcCacheStorageTarget** получает целевые объекты хранилища (s), которые существуют в кэше.</span><span class="sxs-lookup"><span data-stu-id="f7878-109">The **Get-AzHpcCacheStorageTarget** cmdlet gets storage target(s) that exist on cache.</span></span>

## <span data-ttu-id="f7878-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7878-110">EXAMPLES</span></span>

### <span data-ttu-id="f7878-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f7878-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest
```

### <span data-ttu-id="f7878-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f7878-112">Example 2</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest -StorageTargetName stTest
```

## <span data-ttu-id="f7878-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7878-113">PARAMETERS</span></span>

### <span data-ttu-id="f7878-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="f7878-114">-CacheId</span></span>
<span data-ttu-id="f7878-115">Идентификатор ресурса кэша</span><span class="sxs-lookup"><span data-stu-id="f7878-115">The resource id of the Cache</span></span>

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

### <span data-ttu-id="f7878-116">-CacheName</span><span class="sxs-lookup"><span data-stu-id="f7878-116">-CacheName</span></span>
<span data-ttu-id="f7878-117">Имя кэша.</span><span class="sxs-lookup"><span data-stu-id="f7878-117">Name of cache.</span></span>

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

### <span data-ttu-id="f7878-118">-CacheObject</span><span class="sxs-lookup"><span data-stu-id="f7878-118">-CacheObject</span></span>
<span data-ttu-id="f7878-119">Объект кэша, который нужно запустить.</span><span class="sxs-lookup"><span data-stu-id="f7878-119">The cache object to start.</span></span>

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

### <span data-ttu-id="f7878-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7878-120">-DefaultProfile</span></span>
<span data-ttu-id="f7878-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7878-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7878-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f7878-122">-Name</span></span>
<span data-ttu-id="f7878-123">Имя целевого объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="f7878-123">Name of storage target.</span></span>

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

### <span data-ttu-id="f7878-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7878-124">-ResourceGroupName</span></span>
<span data-ttu-id="f7878-125">Имя кэша групп ресурсов: in.</span><span class="sxs-lookup"><span data-stu-id="f7878-125">Name of resource group cache is in.</span></span>


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

### <span data-ttu-id="f7878-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7878-126">CommonParameters</span></span>
<span data-ttu-id="f7878-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7878-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7878-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7878-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7878-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7878-129">INPUTS</span></span>

### <span data-ttu-id="f7878-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f7878-130">System.String</span></span>

## <span data-ttu-id="f7878-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7878-131">OUTPUTS</span></span>

### <span data-ttu-id="f7878-132">Microsoft. Azure. PowerShell. командлеты. HPCCache. Models. PSHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="f7878-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span></span>

## <span data-ttu-id="f7878-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7878-133">NOTES</span></span>

## <span data-ttu-id="f7878-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7878-134">RELATED LINKS</span></span>