---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
ms.openlocfilehash: d27f3ece14e18465fc534bff1a3451eaec2c40a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246559"
---
# <span data-ttu-id="f5dba-101">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="f5dba-101">New-AzRedisCacheLink</span></span>

## <span data-ttu-id="f5dba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f5dba-102">SYNOPSIS</span></span>
<span data-ttu-id="f5dba-103">Создайте ссылку на георепликацию между двумя кэшами Redis.</span><span class="sxs-lookup"><span data-stu-id="f5dba-103">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="f5dba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f5dba-104">SYNTAX</span></span>

```
New-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5dba-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5dba-105">DESCRIPTION</span></span>
<span data-ttu-id="f5dba-106">Создайте ссылку на георепликацию между двумя кэшами Redis.</span><span class="sxs-lookup"><span data-stu-id="f5dba-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="f5dba-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f5dba-107">EXAMPLES</span></span>

### <span data-ttu-id="f5dba-108">Пример 1: Создание связи между двумя кэшами</span><span class="sxs-lookup"><span data-stu-id="f5dba-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="f5dba-109">Эта команда создает связь Geo-Replication между Redis кэша mycache1 и mycache2.</span><span class="sxs-lookup"><span data-stu-id="f5dba-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="f5dba-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f5dba-110">PARAMETERS</span></span>

### <span data-ttu-id="f5dba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5dba-111">-DefaultProfile</span></span>
<span data-ttu-id="f5dba-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5dba-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5dba-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="f5dba-113">-PrimaryServerName</span></span>
<span data-ttu-id="f5dba-114">Имя основного кэша Redis в ссылке.</span><span class="sxs-lookup"><span data-stu-id="f5dba-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="f5dba-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="f5dba-115">-SecondaryServerName</span></span>
<span data-ttu-id="f5dba-116">Имя вспомогательного кэша Redis в ссылке.</span><span class="sxs-lookup"><span data-stu-id="f5dba-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="f5dba-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5dba-117">-Confirm</span></span>
<span data-ttu-id="f5dba-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f5dba-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5dba-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5dba-119">-WhatIf</span></span>
<span data-ttu-id="f5dba-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f5dba-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5dba-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f5dba-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5dba-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5dba-122">CommonParameters</span></span>
<span data-ttu-id="f5dba-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f5dba-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5dba-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5dba-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5dba-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f5dba-125">INPUTS</span></span>

### <span data-ttu-id="f5dba-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f5dba-126">System.String</span></span>

## <span data-ttu-id="f5dba-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5dba-127">OUTPUTS</span></span>

### <span data-ttu-id="f5dba-128">Microsoft. Azure. Commands. RedisCache. Models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="f5dba-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="f5dba-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="f5dba-129">NOTES</span></span>

## <span data-ttu-id="f5dba-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5dba-130">RELATED LINKS</span></span>

[<span data-ttu-id="f5dba-131">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="f5dba-131">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="f5dba-132">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="f5dba-132">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="f5dba-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f5dba-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="f5dba-134">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f5dba-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="f5dba-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f5dba-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="f5dba-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f5dba-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)