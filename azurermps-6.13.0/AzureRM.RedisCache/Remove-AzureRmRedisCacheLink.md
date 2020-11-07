---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheLink.md
ms.openlocfilehash: e4c45095dba8ec72e00fa26eee2d8a3fb6f029fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734124"
---
# <span data-ttu-id="ea9f7-101">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="ea9f7-101">Remove-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="ea9f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea9f7-102">SYNOPSIS</span></span>
<span data-ttu-id="ea9f7-103">Удаление ссылки на георепликацию между двумя кэшами Redis.</span><span class="sxs-lookup"><span data-stu-id="ea9f7-103">Remove a geo replication link between two Redis Caches.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea9f7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea9f7-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea9f7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea9f7-105">DESCRIPTION</span></span>
<span data-ttu-id="ea9f7-106">Удаление ссылки на георепликацию между двумя кэшами Redis.</span><span class="sxs-lookup"><span data-stu-id="ea9f7-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="ea9f7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea9f7-107">EXAMPLES</span></span>

### <span data-ttu-id="ea9f7-108">Пример 1: Удаление ссылки на Geo Replication</span><span class="sxs-lookup"><span data-stu-id="ea9f7-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="ea9f7-109">Эта команда удаляет ссылки на георепликацию, где кэш Redis с именем mycache1 является основным, а Redis кэш с именем mycache2 — дополнительным.</span><span class="sxs-lookup"><span data-stu-id="ea9f7-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="ea9f7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea9f7-110">PARAMETERS</span></span>

### <span data-ttu-id="ea9f7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea9f7-111">-DefaultProfile</span></span>
<span data-ttu-id="ea9f7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea9f7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea9f7-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea9f7-113">-PassThru</span></span>
<span data-ttu-id="ea9f7-114">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="ea9f7-114">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea9f7-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="ea9f7-115">-PrimaryServerName</span></span>
<span data-ttu-id="ea9f7-116">Имя основного кэша Redis в ссылке.</span><span class="sxs-lookup"><span data-stu-id="ea9f7-116">Name of primary redis cache in link.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea9f7-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="ea9f7-117">-SecondaryServerName</span></span>
<span data-ttu-id="ea9f7-118">Имя вспомогательного кэша Redis в ссылке.</span><span class="sxs-lookup"><span data-stu-id="ea9f7-118">Name of secondary redis cache in link.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea9f7-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea9f7-119">-Confirm</span></span>
<span data-ttu-id="ea9f7-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ea9f7-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea9f7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea9f7-121">-WhatIf</span></span>
<span data-ttu-id="ea9f7-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ea9f7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea9f7-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ea9f7-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea9f7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea9f7-124">CommonParameters</span></span>
<span data-ttu-id="ea9f7-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea9f7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea9f7-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea9f7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea9f7-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea9f7-127">INPUTS</span></span>

### <span data-ttu-id="ea9f7-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ea9f7-128">System.String</span></span>

## <span data-ttu-id="ea9f7-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea9f7-129">OUTPUTS</span></span>

### <span data-ttu-id="ea9f7-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ea9f7-130">System.Boolean</span></span>

## <span data-ttu-id="ea9f7-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea9f7-131">NOTES</span></span>

## <span data-ttu-id="ea9f7-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea9f7-132">RELATED LINKS</span></span>

[<span data-ttu-id="ea9f7-133">New-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="ea9f7-133">New-AzureRmRedisCacheLink</span></span>](./New-AzureRmRedisCacheLink.md)

[<span data-ttu-id="ea9f7-134">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="ea9f7-134">Get-AzureRmRedisCacheLink</span></span>](./Get-AzureRmRedisCacheLink.md)

[<span data-ttu-id="ea9f7-135">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ea9f7-135">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="ea9f7-136">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ea9f7-136">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="ea9f7-137">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ea9f7-137">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="ea9f7-138">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ea9f7-138">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
