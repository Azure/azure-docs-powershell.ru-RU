---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/reset-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
ms.openlocfilehash: c2373bb4ef093a35abc12b14f55f4c977fc54d64
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235929"
---
# <span data-ttu-id="9c202-101">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9c202-101">Reset-AzRedisCache</span></span>

## <span data-ttu-id="9c202-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c202-102">SYNOPSIS</span></span>
<span data-ttu-id="9c202-103">Перезапускает узлы кэша.</span><span class="sxs-lookup"><span data-stu-id="9c202-103">Restarts nodes of a cache.</span></span>

## <span data-ttu-id="9c202-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c202-104">SYNTAX</span></span>

```
Reset-AzRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c202-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c202-105">DESCRIPTION</span></span>
<span data-ttu-id="9c202-106">Командлет **Reset-AzRedisCache** перезапустит узлы экземпляра кэша Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="9c202-106">The **Reset-AzRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="9c202-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c202-107">EXAMPLES</span></span>

### <span data-ttu-id="9c202-108">Пример 1: перезапуск обоих узлов</span><span class="sxs-lookup"><span data-stu-id="9c202-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="9c202-109">Эта команда перезапустит оба узла для кэша с именем RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="9c202-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="9c202-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c202-110">PARAMETERS</span></span>

### <span data-ttu-id="9c202-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c202-111">-DefaultProfile</span></span>
<span data-ttu-id="9c202-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c202-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c202-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9c202-113">-Force</span></span>
<span data-ttu-id="9c202-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="9c202-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9c202-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9c202-115">-Name</span></span>
<span data-ttu-id="9c202-116">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="9c202-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="9c202-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c202-117">-PassThru</span></span>
<span data-ttu-id="9c202-118">Указывает на то, что этот командлет возвращает логическое значение, которое указывает, успешно ли выполняется операция.</span><span class="sxs-lookup"><span data-stu-id="9c202-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="9c202-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9c202-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9c202-120">-RebootType</span><span class="sxs-lookup"><span data-stu-id="9c202-120">-RebootType</span></span>
<span data-ttu-id="9c202-121">Указывает, какой узел или узлы нужно перезапустить.</span><span class="sxs-lookup"><span data-stu-id="9c202-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="9c202-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9c202-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9c202-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="9c202-123">PrimaryNode</span></span> 
- <span data-ttu-id="9c202-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="9c202-124">SecondaryNode</span></span> 
- <span data-ttu-id="9c202-125">AllNodes</span><span class="sxs-lookup"><span data-stu-id="9c202-125">AllNodes</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryNode, SecondaryNode, AllNodes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c202-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c202-126">-ResourceGroupName</span></span>
<span data-ttu-id="9c202-127">Указывает имя группы ресурсов, содержащей кэш.</span><span class="sxs-lookup"><span data-stu-id="9c202-127">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c202-128">-ShardId</span><span class="sxs-lookup"><span data-stu-id="9c202-128">-ShardId</span></span>
<span data-ttu-id="9c202-129">Указывает идентификатор сегмента, который перезапускает этот командлет для расширенного кэша с включенной кластеризацией.</span><span class="sxs-lookup"><span data-stu-id="9c202-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c202-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c202-130">-Confirm</span></span>
<span data-ttu-id="9c202-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9c202-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c202-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c202-132">-WhatIf</span></span>
<span data-ttu-id="9c202-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9c202-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c202-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9c202-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c202-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c202-135">CommonParameters</span></span>
<span data-ttu-id="9c202-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c202-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c202-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c202-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c202-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c202-138">INPUTS</span></span>

### <span data-ttu-id="9c202-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9c202-139">System.String</span></span>

### <span data-ttu-id="9c202-140">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9c202-140">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9c202-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c202-141">OUTPUTS</span></span>

### <span data-ttu-id="9c202-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c202-142">System.Boolean</span></span>

## <span data-ttu-id="9c202-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c202-143">NOTES</span></span>
* <span data-ttu-id="9c202-144">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Redis, кэш, Интернет, webapp, веб-сайт</span><span class="sxs-lookup"><span data-stu-id="9c202-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="9c202-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c202-145">RELATED LINKS</span></span>

[<span data-ttu-id="9c202-146">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9c202-146">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="9c202-147">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9c202-147">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="9c202-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9c202-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="9c202-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9c202-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="9c202-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9c202-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


