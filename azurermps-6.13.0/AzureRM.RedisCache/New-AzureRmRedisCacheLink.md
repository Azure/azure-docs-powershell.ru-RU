---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheLink.md
ms.openlocfilehash: f625c9180287166b01607c468c44b5e0623c11cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556536"
---
# <span data-ttu-id="57464-101">New-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="57464-101">New-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="57464-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="57464-102">SYNOPSIS</span></span>
<span data-ttu-id="57464-103">Создайте ссылку на георепликацию между двумя кэшами Redis.</span><span class="sxs-lookup"><span data-stu-id="57464-103">Create a geo replication link between two Redis Caches.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57464-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="57464-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57464-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57464-105">DESCRIPTION</span></span>
<span data-ttu-id="57464-106">Создайте ссылку на георепликацию между двумя кэшами Redis.</span><span class="sxs-lookup"><span data-stu-id="57464-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="57464-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="57464-107">EXAMPLES</span></span>

### <span data-ttu-id="57464-108">Пример 1: Создание связи между двумя кэшами</span><span class="sxs-lookup"><span data-stu-id="57464-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="57464-109">Эта команда создает связь Geo-Replication между Redis кэша mycache1 и mycache2.</span><span class="sxs-lookup"><span data-stu-id="57464-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="57464-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="57464-110">PARAMETERS</span></span>

### <span data-ttu-id="57464-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57464-111">-DefaultProfile</span></span>
<span data-ttu-id="57464-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57464-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57464-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="57464-113">-PrimaryServerName</span></span>
<span data-ttu-id="57464-114">Имя основного кэша Redis в ссылке.</span><span class="sxs-lookup"><span data-stu-id="57464-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="57464-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="57464-115">-SecondaryServerName</span></span>
<span data-ttu-id="57464-116">Имя вспомогательного кэша Redis в ссылке.</span><span class="sxs-lookup"><span data-stu-id="57464-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="57464-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57464-117">-Confirm</span></span>
<span data-ttu-id="57464-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="57464-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57464-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57464-119">-WhatIf</span></span>
<span data-ttu-id="57464-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="57464-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57464-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="57464-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57464-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57464-122">CommonParameters</span></span>
<span data-ttu-id="57464-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="57464-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57464-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57464-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57464-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="57464-125">INPUTS</span></span>

### <span data-ttu-id="57464-126">System. String</span><span class="sxs-lookup"><span data-stu-id="57464-126">System.String</span></span>

## <span data-ttu-id="57464-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="57464-127">OUTPUTS</span></span>

### <span data-ttu-id="57464-128">Microsoft. Azure. Commands. RedisCache. Models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="57464-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="57464-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="57464-129">NOTES</span></span>

## <span data-ttu-id="57464-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57464-130">RELATED LINKS</span></span>

[<span data-ttu-id="57464-131">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="57464-131">Get-AzureRmRedisCacheLink</span></span>](./Get-AzureRmRedisCacheLink.md)

[<span data-ttu-id="57464-132">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="57464-132">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="57464-133">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="57464-133">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="57464-134">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="57464-134">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="57464-135">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="57464-135">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="57464-136">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="57464-136">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
