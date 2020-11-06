---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheLink.md
ms.openlocfilehash: a0532feb24966cfe05b0175080fa2333307f33e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563371"
---
# <span data-ttu-id="79f16-101">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="79f16-101">Remove-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="79f16-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79f16-102">SYNOPSIS</span></span>
<span data-ttu-id="79f16-103">Удаление ссылки на георепликацию между двумя кэшами Redis.</span><span class="sxs-lookup"><span data-stu-id="79f16-103">Remove a geo replication link between two Redis Caches.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79f16-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79f16-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79f16-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79f16-105">DESCRIPTION</span></span>
<span data-ttu-id="79f16-106">Удаление ссылки на георепликацию между двумя кэшами Redis.</span><span class="sxs-lookup"><span data-stu-id="79f16-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="79f16-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79f16-107">EXAMPLES</span></span>

### <span data-ttu-id="79f16-108">Пример 1: Удаление ссылки на Geo Replication</span><span class="sxs-lookup"><span data-stu-id="79f16-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="79f16-109">Эта команда удаляет ссылки на георепликацию, где кэш Redis с именем mycache1 является основным, а Redis кэш с именем mycache2 — дополнительным.</span><span class="sxs-lookup"><span data-stu-id="79f16-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="79f16-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79f16-110">PARAMETERS</span></span>

### <span data-ttu-id="79f16-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79f16-111">-DefaultProfile</span></span>
<span data-ttu-id="79f16-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79f16-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79f16-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79f16-113">-PassThru</span></span>
<span data-ttu-id="79f16-114">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="79f16-114">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79f16-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="79f16-115">-PrimaryServerName</span></span>
<span data-ttu-id="79f16-116">Имя основного кэша Redis в ссылке.</span><span class="sxs-lookup"><span data-stu-id="79f16-116">Name of primary redis cache in link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79f16-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="79f16-117">-SecondaryServerName</span></span>
<span data-ttu-id="79f16-118">Имя вспомогательного кэша Redis в ссылке.</span><span class="sxs-lookup"><span data-stu-id="79f16-118">Name of secondary redis cache in link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79f16-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79f16-119">-Confirm</span></span>
<span data-ttu-id="79f16-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="79f16-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79f16-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79f16-121">-WhatIf</span></span>
<span data-ttu-id="79f16-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="79f16-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79f16-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="79f16-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79f16-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79f16-124">CommonParameters</span></span>
<span data-ttu-id="79f16-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79f16-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79f16-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79f16-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79f16-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79f16-127">INPUTS</span></span>

### <span data-ttu-id="79f16-128">System. String</span><span class="sxs-lookup"><span data-stu-id="79f16-128">System.String</span></span>

## <span data-ttu-id="79f16-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79f16-129">OUTPUTS</span></span>

### <span data-ttu-id="79f16-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="79f16-130">System.Boolean</span></span>

## <span data-ttu-id="79f16-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="79f16-131">NOTES</span></span>

## <span data-ttu-id="79f16-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79f16-132">RELATED LINKS</span></span>

[<span data-ttu-id="79f16-133">New-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="79f16-133">New-AzureRmRedisCacheLink</span></span>](./New-AzureRmRedisCacheLink.md)

[<span data-ttu-id="79f16-134">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="79f16-134">Get-AzureRmRedisCacheLink</span></span>](./Get-AzureRmRedisCacheLink.md)

[<span data-ttu-id="79f16-135">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="79f16-135">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="79f16-136">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="79f16-136">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="79f16-137">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="79f16-137">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="79f16-138">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="79f16-138">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
