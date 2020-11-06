---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
ms.openlocfilehash: dff5f565e27f89360465ede3eb8fbe2c3d5620a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561587"
---
# <span data-ttu-id="99355-101">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="99355-101">Get-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="99355-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="99355-102">SYNOPSIS</span></span>
<span data-ttu-id="99355-103">Получение ссылки на георепликацию для Redis кэша.</span><span class="sxs-lookup"><span data-stu-id="99355-103">Get geo replication link for Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99355-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="99355-104">SYNTAX</span></span>

### <span data-ttu-id="99355-105">AllLinksForCache (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="99355-105">AllLinksForCache (Default)</span></span>
```
Get-AzureRmRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99355-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="99355-106">AllLinksForPrimaryCache</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="99355-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="99355-107">SingleLink</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99355-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="99355-108">AllLinksForSecondaryCache</span></span>
```
Get-AzureRmRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99355-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99355-109">DESCRIPTION</span></span>
<span data-ttu-id="99355-110">Существует четыре способа получения сведений о ссылке георепликации.</span><span class="sxs-lookup"><span data-stu-id="99355-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="99355-111">Укажите имя параметра или PrimaryServerName или SecondaryServerName.</span><span class="sxs-lookup"><span data-stu-id="99355-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="99355-112">Имя, после чего будет возвращена ссылка на то, где находится кэш.</span><span class="sxs-lookup"><span data-stu-id="99355-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="99355-113">Если задано только PrimaryServerName, будут возвращены все ссылки, в которых хранится кэш PRIMARY.</span><span class="sxs-lookup"><span data-stu-id="99355-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="99355-114">Если задано только SecondaryServerName, будут возвращены все ссылки, в которых должен быть указан дополнительный кэш.</span><span class="sxs-lookup"><span data-stu-id="99355-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="99355-115">Если заданы оба PrimaryServerName и SecondaryServerName, будет возвращена определенная ссылка на соответствующую роль.</span><span class="sxs-lookup"><span data-stu-id="99355-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="99355-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="99355-116">EXAMPLES</span></span>

### <span data-ttu-id="99355-117">Пример 1: получение параметров с помощью Set AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="99355-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="99355-118">Эта команда получает все ссылки георепликации для кэша Redis с именем mycache1.</span><span class="sxs-lookup"><span data-stu-id="99355-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="99355-119">Пример 2: получение параметров с помощью Set AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="99355-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="99355-120">Эта команда получает ссылки на георепликацию, где кэш Redis с именем mycache1 является основным.</span><span class="sxs-lookup"><span data-stu-id="99355-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="99355-121">Пример 3: получение параметров с помощью Set AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="99355-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="99355-122">Эта команда получает ссылки на георепликацию, где кэш Redis с именем mycache2 является дополнительным.</span><span class="sxs-lookup"><span data-stu-id="99355-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="99355-123">Пример 4: получение параметров с помощью Set SingleLink</span><span class="sxs-lookup"><span data-stu-id="99355-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="99355-124">Эта команда получает одну ссылку на георепликацию, в которой кэш Redis с именем mycache1 является основным, а Redis кэш с именем mycache2 — дополнительным.</span><span class="sxs-lookup"><span data-stu-id="99355-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="99355-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="99355-125">PARAMETERS</span></span>

### <span data-ttu-id="99355-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99355-126">-DefaultProfile</span></span>
<span data-ttu-id="99355-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99355-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99355-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="99355-128">-Name</span></span>
<span data-ttu-id="99355-129">Имя кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="99355-129">Name of redis cache.</span></span>

```yaml
Type: String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99355-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="99355-130">-PrimaryServerName</span></span>
<span data-ttu-id="99355-131">Имя основного кэша Redis в ссылке.</span><span class="sxs-lookup"><span data-stu-id="99355-131">Name of primary redis cache in link.</span></span>

```yaml
Type: String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99355-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="99355-132">-SecondaryServerName</span></span>
<span data-ttu-id="99355-133">Имя вспомогательного кэша Redis в ссылке.</span><span class="sxs-lookup"><span data-stu-id="99355-133">Name of secondary redis cache in link.</span></span>

```yaml
Type: String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99355-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99355-134">CommonParameters</span></span>
<span data-ttu-id="99355-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="99355-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99355-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99355-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99355-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="99355-137">INPUTS</span></span>

### <span data-ttu-id="99355-138">System. String</span><span class="sxs-lookup"><span data-stu-id="99355-138">System.String</span></span>
<span data-ttu-id="99355-139">Вы можете передавать входные данные командлету по имени, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="99355-139">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="99355-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="99355-140">OUTPUTS</span></span>

### <span data-ttu-id="99355-141">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. RedisCache. Models. PSRedisLinkedServer, Microsoft. Azure. Commands. RedisCache, Version = 4.0.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="99355-141">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer, Microsoft.Azure.Commands.RedisCache, Version=4.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="99355-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="99355-142">NOTES</span></span>

## <span data-ttu-id="99355-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99355-143">RELATED LINKS</span></span>

[<span data-ttu-id="99355-144">New-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="99355-144">New-AzureRmRedisCacheLink</span></span>](./New-AzureRmRedisCacheLink.md)

[<span data-ttu-id="99355-145">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="99355-145">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="99355-146">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="99355-146">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="99355-147">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="99355-147">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="99355-148">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="99355-148">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="99355-149">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="99355-149">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
