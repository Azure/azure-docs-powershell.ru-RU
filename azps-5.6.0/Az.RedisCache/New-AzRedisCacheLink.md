---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
ms.openlocfilehash: 41a2172fffdbd83edc8ab72a4fe922d600362731
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972707"
---
# <span data-ttu-id="9ba54-101">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="9ba54-101">New-AzRedisCacheLink</span></span>

## <span data-ttu-id="9ba54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ba54-102">SYNOPSIS</span></span>
<span data-ttu-id="9ba54-103">Создайте геокопию между двумя кэшами Redis.</span><span class="sxs-lookup"><span data-stu-id="9ba54-103">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="9ba54-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9ba54-104">SYNTAX</span></span>

```
New-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ba54-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ba54-105">DESCRIPTION</span></span>
<span data-ttu-id="9ba54-106">Создайте геокопию между двумя кэшами Redis.</span><span class="sxs-lookup"><span data-stu-id="9ba54-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="9ba54-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9ba54-107">EXAMPLES</span></span>

### <span data-ttu-id="9ba54-108">Пример 1. Создание связи между двумя кэшами</span><span class="sxs-lookup"><span data-stu-id="9ba54-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="9ba54-109">Эта команда создает связь гео-репликации между кэшом Redis 1 и mycache2.</span><span class="sxs-lookup"><span data-stu-id="9ba54-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="9ba54-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ba54-110">PARAMETERS</span></span>

### <span data-ttu-id="9ba54-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ba54-111">-DefaultProfile</span></span>
<span data-ttu-id="9ba54-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ba54-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ba54-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="9ba54-113">-PrimaryServerName</span></span>
<span data-ttu-id="9ba54-114">Имя основного кэша redis в ссылке.</span><span class="sxs-lookup"><span data-stu-id="9ba54-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="9ba54-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="9ba54-115">-SecondaryServerName</span></span>
<span data-ttu-id="9ba54-116">Имя дополнительного кэша redis в ссылке.</span><span class="sxs-lookup"><span data-stu-id="9ba54-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="9ba54-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ba54-117">-Confirm</span></span>
<span data-ttu-id="9ba54-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9ba54-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ba54-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ba54-119">-WhatIf</span></span>
<span data-ttu-id="9ba54-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ba54-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ba54-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9ba54-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ba54-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ba54-122">CommonParameters</span></span>
<span data-ttu-id="9ba54-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ba54-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ba54-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ba54-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ba54-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9ba54-125">INPUTS</span></span>

### <span data-ttu-id="9ba54-126">System.String</span><span class="sxs-lookup"><span data-stu-id="9ba54-126">System.String</span></span>

## <span data-ttu-id="9ba54-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9ba54-127">OUTPUTS</span></span>

### <span data-ttu-id="9ba54-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="9ba54-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="9ba54-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9ba54-129">NOTES</span></span>

## <span data-ttu-id="9ba54-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ba54-130">RELATED LINKS</span></span>

[<span data-ttu-id="9ba54-131">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="9ba54-131">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="9ba54-132">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="9ba54-132">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="9ba54-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9ba54-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="9ba54-134">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9ba54-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="9ba54-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9ba54-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="9ba54-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9ba54-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)