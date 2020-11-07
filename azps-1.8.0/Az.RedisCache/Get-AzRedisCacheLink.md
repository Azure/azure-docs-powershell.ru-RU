---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 8129634e940624fe09dad4a1199f96dbcf5162bb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729558"
---
# <span data-ttu-id="14638-101">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="14638-101">Get-AzRedisCacheLink</span></span>

## <span data-ttu-id="14638-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14638-102">SYNOPSIS</span></span>
<span data-ttu-id="14638-103">Получение ссылки на георепликацию для Redis кэша.</span><span class="sxs-lookup"><span data-stu-id="14638-103">Get geo replication link for Redis Cache.</span></span>

## <span data-ttu-id="14638-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14638-104">SYNTAX</span></span>

### <span data-ttu-id="14638-105">AllLinksForCache (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="14638-105">AllLinksForCache (Default)</span></span>
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14638-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="14638-106">AllLinksForPrimaryCache</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="14638-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="14638-107">SingleLink</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14638-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="14638-108">AllLinksForSecondaryCache</span></span>
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="14638-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14638-109">DESCRIPTION</span></span>
<span data-ttu-id="14638-110">Существует четыре способа получения сведений о ссылке георепликации.</span><span class="sxs-lookup"><span data-stu-id="14638-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="14638-111">Укажите имя параметра или PrimaryServerName или SecondaryServerName.</span><span class="sxs-lookup"><span data-stu-id="14638-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="14638-112">Имя, после чего будет возвращена ссылка на то, где находится кэш.</span><span class="sxs-lookup"><span data-stu-id="14638-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="14638-113">Если задано только PrimaryServerName, будут возвращены все ссылки, в которых хранится кэш PRIMARY.</span><span class="sxs-lookup"><span data-stu-id="14638-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="14638-114">Если задано только SecondaryServerName, будут возвращены все ссылки, в которых должен быть указан дополнительный кэш.</span><span class="sxs-lookup"><span data-stu-id="14638-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="14638-115">Если заданы оба PrimaryServerName и SecondaryServerName, будет возвращена определенная ссылка на соответствующую роль.</span><span class="sxs-lookup"><span data-stu-id="14638-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="14638-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14638-116">EXAMPLES</span></span>

### <span data-ttu-id="14638-117">Пример 1: получение параметров с помощью Set AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="14638-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="14638-118">Эта команда получает все ссылки георепликации для кэша Redis с именем mycache1.</span><span class="sxs-lookup"><span data-stu-id="14638-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="14638-119">Пример 2: получение параметров с помощью Set AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="14638-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="14638-120">Эта команда получает ссылки на георепликацию, где кэш Redis с именем mycache1 является основным.</span><span class="sxs-lookup"><span data-stu-id="14638-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="14638-121">Пример 3: получение параметров с помощью Set AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="14638-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="14638-122">Эта команда получает ссылки на георепликацию, где кэш Redis с именем mycache2 является дополнительным.</span><span class="sxs-lookup"><span data-stu-id="14638-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="14638-123">Пример 4: получение параметров с помощью Set SingleLink</span><span class="sxs-lookup"><span data-stu-id="14638-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="14638-124">Эта команда получает одну ссылку на георепликацию, в которой кэш Redis с именем mycache1 является основным, а Redis кэш с именем mycache2 — дополнительным.</span><span class="sxs-lookup"><span data-stu-id="14638-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="14638-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14638-125">PARAMETERS</span></span>

### <span data-ttu-id="14638-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14638-126">-DefaultProfile</span></span>
<span data-ttu-id="14638-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14638-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14638-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="14638-128">-Name</span></span>
<span data-ttu-id="14638-129">Имя кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="14638-129">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14638-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="14638-130">-PrimaryServerName</span></span>
<span data-ttu-id="14638-131">Имя основного кэша Redis в ссылке.</span><span class="sxs-lookup"><span data-stu-id="14638-131">Name of primary redis cache in link.</span></span>

```yaml
Type: System.String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14638-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="14638-132">-SecondaryServerName</span></span>
<span data-ttu-id="14638-133">Имя вспомогательного кэша Redis в ссылке.</span><span class="sxs-lookup"><span data-stu-id="14638-133">Name of secondary redis cache in link.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14638-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14638-134">CommonParameters</span></span>
<span data-ttu-id="14638-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14638-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14638-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14638-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14638-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14638-137">INPUTS</span></span>

### <span data-ttu-id="14638-138">System. String</span><span class="sxs-lookup"><span data-stu-id="14638-138">System.String</span></span>

## <span data-ttu-id="14638-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14638-139">OUTPUTS</span></span>

### <span data-ttu-id="14638-140">Microsoft. Azure. Commands. RedisCache. Models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="14638-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="14638-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="14638-141">NOTES</span></span>

## <span data-ttu-id="14638-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14638-142">RELATED LINKS</span></span>

[<span data-ttu-id="14638-143">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="14638-143">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="14638-144">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="14638-144">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="14638-145">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="14638-145">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="14638-146">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="14638-146">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="14638-147">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="14638-147">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="14638-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="14638-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)