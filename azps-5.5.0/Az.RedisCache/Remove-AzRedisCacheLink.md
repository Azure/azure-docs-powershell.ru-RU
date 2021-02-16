---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
ms.openlocfilehash: 38c72a19e73d87272fb91fb6472a41496658e7d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217860"
---
# <span data-ttu-id="191f8-101">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="191f8-101">Remove-AzRedisCacheLink</span></span>

## <span data-ttu-id="191f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="191f8-102">SYNOPSIS</span></span>
<span data-ttu-id="191f8-103">Удаление связи геокопии между двумя кэшами Redis.</span><span class="sxs-lookup"><span data-stu-id="191f8-103">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="191f8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="191f8-104">SYNTAX</span></span>

```
Remove-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="191f8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="191f8-105">DESCRIPTION</span></span>
<span data-ttu-id="191f8-106">Удаление связи геокопии между двумя кэшами Redis.</span><span class="sxs-lookup"><span data-stu-id="191f8-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="191f8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="191f8-107">EXAMPLES</span></span>

### <span data-ttu-id="191f8-108">Пример 1. Удаление ссылки на геокопию</span><span class="sxs-lookup"><span data-stu-id="191f8-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="191f8-109">Эта команда удаляет ссылки гео-репликации, где кэш Redis с именем mycache1 является основным, а кэш Redis с именем mycache2 — дополнительным.</span><span class="sxs-lookup"><span data-stu-id="191f8-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="191f8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="191f8-110">PARAMETERS</span></span>

### <span data-ttu-id="191f8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="191f8-111">-DefaultProfile</span></span>
<span data-ttu-id="191f8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="191f8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="191f8-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="191f8-113">-PassThru</span></span>
<span data-ttu-id="191f8-114">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="191f8-114">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="191f8-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="191f8-115">-PrimaryServerName</span></span>
<span data-ttu-id="191f8-116">Имя основного кэша redis в ссылке.</span><span class="sxs-lookup"><span data-stu-id="191f8-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="191f8-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="191f8-117">-SecondaryServerName</span></span>
<span data-ttu-id="191f8-118">Имя дополнительного кэша redis в ссылке.</span><span class="sxs-lookup"><span data-stu-id="191f8-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="191f8-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="191f8-119">-Confirm</span></span>
<span data-ttu-id="191f8-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="191f8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="191f8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="191f8-121">-WhatIf</span></span>
<span data-ttu-id="191f8-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="191f8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="191f8-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="191f8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="191f8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="191f8-124">CommonParameters</span></span>
<span data-ttu-id="191f8-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="191f8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="191f8-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="191f8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="191f8-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="191f8-127">INPUTS</span></span>

### <span data-ttu-id="191f8-128">System.String</span><span class="sxs-lookup"><span data-stu-id="191f8-128">System.String</span></span>

## <span data-ttu-id="191f8-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="191f8-129">OUTPUTS</span></span>

### <span data-ttu-id="191f8-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="191f8-130">System.Boolean</span></span>

## <span data-ttu-id="191f8-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="191f8-131">NOTES</span></span>

## <span data-ttu-id="191f8-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="191f8-132">RELATED LINKS</span></span>

[<span data-ttu-id="191f8-133">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="191f8-133">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="191f8-134">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="191f8-134">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="191f8-135">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="191f8-135">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="191f8-136">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="191f8-136">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="191f8-137">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="191f8-137">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="191f8-138">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="191f8-138">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)