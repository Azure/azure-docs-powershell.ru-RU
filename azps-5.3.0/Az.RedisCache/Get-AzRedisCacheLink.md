---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 58c52e30270af309eb5104bbc0a9308f83df91ea
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421207"
---
# <span data-ttu-id="5588a-101">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="5588a-101">Get-AzRedisCacheLink</span></span>

## <span data-ttu-id="5588a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5588a-102">SYNOPSIS</span></span>
<span data-ttu-id="5588a-103">Получить ссылку на геокопию для Кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="5588a-103">Get geo replication link for Redis Cache.</span></span>

## <span data-ttu-id="5588a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5588a-104">SYNTAX</span></span>

### <span data-ttu-id="5588a-105">AllLinksForCache (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5588a-105">AllLinksForCache (Default)</span></span>
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5588a-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="5588a-106">AllLinksForPrimaryCache</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5588a-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="5588a-107">SingleLink</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5588a-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="5588a-108">AllLinksForSecondaryCache</span></span>
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5588a-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5588a-109">DESCRIPTION</span></span>
<span data-ttu-id="5588a-110">Существует четыре разных способа получить подробные ссылки геопрои репликации.</span><span class="sxs-lookup"><span data-stu-id="5588a-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="5588a-111">Укайте имя параметра или PrimaryServerName и/или SecondaryServerName.</span><span class="sxs-lookup"><span data-stu-id="5588a-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="5588a-112">После этого будет возвращена вся ссылка, в которой есть кэш.</span><span class="sxs-lookup"><span data-stu-id="5588a-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="5588a-113">Если задано только имя PrimaryServerName, возвращаются все ссылки, для которых кэш является основным.</span><span class="sxs-lookup"><span data-stu-id="5588a-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="5588a-114">Если задано только имя SecondaryServerName, возвращаются все ссылки, кэш которых является дополнительным.</span><span class="sxs-lookup"><span data-stu-id="5588a-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="5588a-115">Если primaryServerName и SecondaryServerName both are given then specific link with correct role will be returned.</span><span class="sxs-lookup"><span data-stu-id="5588a-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="5588a-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5588a-116">EXAMPLES</span></span>

### <span data-ttu-id="5588a-117">Пример 1. Использование набора параметров AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="5588a-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="5588a-118">Эта команда получает все ссылки гео-репликации для кэша Redis с именем mycache1.</span><span class="sxs-lookup"><span data-stu-id="5588a-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="5588a-119">Пример 2. Использование набора параметров AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="5588a-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="5588a-120">Эта команда получает ссылки гео-репликации, где кэш Redis с именем mycache1 является основным.</span><span class="sxs-lookup"><span data-stu-id="5588a-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="5588a-121">Пример 3. Использование набора параметров AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="5588a-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="5588a-122">Эта команда получает ссылки гео-репликации, где кэш Redis с именем mycache2 является дополнительным.</span><span class="sxs-lookup"><span data-stu-id="5588a-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="5588a-123">Пример 4. Использование набора параметров SingleLink</span><span class="sxs-lookup"><span data-stu-id="5588a-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="5588a-124">Эта команда получает одну ссылку гео-репликации, где кэш Redis с именем mycache1 является основным, а кэш Redis с именем mycache2 — дополнительным.</span><span class="sxs-lookup"><span data-stu-id="5588a-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="5588a-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5588a-125">PARAMETERS</span></span>

### <span data-ttu-id="5588a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5588a-126">-DefaultProfile</span></span>
<span data-ttu-id="5588a-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5588a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5588a-128">-Name</span><span class="sxs-lookup"><span data-stu-id="5588a-128">-Name</span></span>
<span data-ttu-id="5588a-129">Имя кэша redis.</span><span class="sxs-lookup"><span data-stu-id="5588a-129">Name of redis cache.</span></span>

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

### <span data-ttu-id="5588a-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="5588a-130">-PrimaryServerName</span></span>
<span data-ttu-id="5588a-131">Имя основного кэша redis в ссылке.</span><span class="sxs-lookup"><span data-stu-id="5588a-131">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="5588a-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="5588a-132">-SecondaryServerName</span></span>
<span data-ttu-id="5588a-133">Имя дополнительного кэша redis в ссылке.</span><span class="sxs-lookup"><span data-stu-id="5588a-133">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="5588a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5588a-134">CommonParameters</span></span>
<span data-ttu-id="5588a-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5588a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5588a-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5588a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5588a-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5588a-137">INPUTS</span></span>

### <span data-ttu-id="5588a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5588a-138">System.String</span></span>

## <span data-ttu-id="5588a-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5588a-139">OUTPUTS</span></span>

### <span data-ttu-id="5588a-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="5588a-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="5588a-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5588a-141">NOTES</span></span>

## <span data-ttu-id="5588a-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5588a-142">RELATED LINKS</span></span>

[<span data-ttu-id="5588a-143">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="5588a-143">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="5588a-144">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="5588a-144">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="5588a-145">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5588a-145">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="5588a-146">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5588a-146">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="5588a-147">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5588a-147">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="5588a-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5588a-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)