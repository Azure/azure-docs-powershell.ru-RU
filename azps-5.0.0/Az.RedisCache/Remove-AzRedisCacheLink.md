---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
ms.openlocfilehash: 38c72a19e73d87272fb91fb6472a41496658e7d6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247676"
---
# <span data-ttu-id="2c456-101">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="2c456-101">Remove-AzRedisCacheLink</span></span>

## <span data-ttu-id="2c456-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c456-102">SYNOPSIS</span></span>
<span data-ttu-id="2c456-103">Удаление ссылки на георепликацию между двумя кэшами Redis.</span><span class="sxs-lookup"><span data-stu-id="2c456-103">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="2c456-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c456-104">SYNTAX</span></span>

```
Remove-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c456-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c456-105">DESCRIPTION</span></span>
<span data-ttu-id="2c456-106">Удаление ссылки на георепликацию между двумя кэшами Redis.</span><span class="sxs-lookup"><span data-stu-id="2c456-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="2c456-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c456-107">EXAMPLES</span></span>

### <span data-ttu-id="2c456-108">Пример 1: Удаление ссылки на Geo Replication</span><span class="sxs-lookup"><span data-stu-id="2c456-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="2c456-109">Эта команда удаляет ссылки на георепликацию, где кэш Redis с именем mycache1 является основным, а Redis кэш с именем mycache2 — дополнительным.</span><span class="sxs-lookup"><span data-stu-id="2c456-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="2c456-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c456-110">PARAMETERS</span></span>

### <span data-ttu-id="2c456-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c456-111">-DefaultProfile</span></span>
<span data-ttu-id="2c456-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c456-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c456-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c456-113">-PassThru</span></span>
<span data-ttu-id="2c456-114">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="2c456-114">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2c456-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="2c456-115">-PrimaryServerName</span></span>
<span data-ttu-id="2c456-116">Имя основного кэша Redis в ссылке.</span><span class="sxs-lookup"><span data-stu-id="2c456-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="2c456-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="2c456-117">-SecondaryServerName</span></span>
<span data-ttu-id="2c456-118">Имя вспомогательного кэша Redis в ссылке.</span><span class="sxs-lookup"><span data-stu-id="2c456-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="2c456-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c456-119">-Confirm</span></span>
<span data-ttu-id="2c456-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2c456-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c456-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c456-121">-WhatIf</span></span>
<span data-ttu-id="2c456-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2c456-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c456-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2c456-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c456-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c456-124">CommonParameters</span></span>
<span data-ttu-id="2c456-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c456-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c456-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c456-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c456-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c456-127">INPUTS</span></span>

### <span data-ttu-id="2c456-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2c456-128">System.String</span></span>

## <span data-ttu-id="2c456-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c456-129">OUTPUTS</span></span>

### <span data-ttu-id="2c456-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2c456-130">System.Boolean</span></span>

## <span data-ttu-id="2c456-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c456-131">NOTES</span></span>

## <span data-ttu-id="2c456-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c456-132">RELATED LINKS</span></span>

[<span data-ttu-id="2c456-133">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="2c456-133">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="2c456-134">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="2c456-134">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="2c456-135">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2c456-135">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="2c456-136">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2c456-136">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="2c456-137">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2c456-137">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="2c456-138">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2c456-138">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)