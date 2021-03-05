---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/powershell/module/az.rediscache/reset-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
ms.openlocfilehash: 797ea800962e00dfd94e1be14e39293fc303ef38
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000920"
---
# <span data-ttu-id="e38c4-101">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e38c4-101">Reset-AzRedisCache</span></span>

## <span data-ttu-id="e38c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e38c4-102">SYNOPSIS</span></span>
<span data-ttu-id="e38c4-103">Перезапуск узлов кэша.</span><span class="sxs-lookup"><span data-stu-id="e38c4-103">Restarts nodes of a cache.</span></span>

## <span data-ttu-id="e38c4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e38c4-104">SYNTAX</span></span>

```
Reset-AzRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e38c4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e38c4-105">DESCRIPTION</span></span>
<span data-ttu-id="e38c4-106">**Cmdlet Reset-AzRedisCache** перезапускет узлы экземпляра Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="e38c4-106">The **Reset-AzRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="e38c4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e38c4-107">EXAMPLES</span></span>

### <span data-ttu-id="e38c4-108">Пример 1. Перезапуск обоих узлов</span><span class="sxs-lookup"><span data-stu-id="e38c4-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="e38c4-109">Эта команда перезапускет оба узла для кэша RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="e38c4-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="e38c4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e38c4-110">PARAMETERS</span></span>

### <span data-ttu-id="e38c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e38c4-111">-DefaultProfile</span></span>
<span data-ttu-id="e38c4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e38c4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e38c4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e38c4-113">-Force</span></span>
<span data-ttu-id="e38c4-114">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="e38c4-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e38c4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e38c4-115">-Name</span></span>
<span data-ttu-id="e38c4-116">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="e38c4-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="e38c4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e38c4-117">-PassThru</span></span>
<span data-ttu-id="e38c4-118">Указывает на то, что этот cmdlet возвращает boolean that indicates whether the operation succeeds.)</span><span class="sxs-lookup"><span data-stu-id="e38c4-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="e38c4-119">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e38c4-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e38c4-120">-RebootType</span><span class="sxs-lookup"><span data-stu-id="e38c4-120">-RebootType</span></span>
<span data-ttu-id="e38c4-121">Указывает, какой узел или узлы нужно перезапустить.</span><span class="sxs-lookup"><span data-stu-id="e38c4-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="e38c4-122">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="e38c4-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e38c4-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="e38c4-123">PrimaryNode</span></span> 
- <span data-ttu-id="e38c4-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="e38c4-124">SecondaryNode</span></span> 
- <span data-ttu-id="e38c4-125">AllNodes</span><span class="sxs-lookup"><span data-stu-id="e38c4-125">AllNodes</span></span>

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

### <span data-ttu-id="e38c4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e38c4-126">-ResourceGroupName</span></span>
<span data-ttu-id="e38c4-127">Имя группы ресурсов, которая содержит кэш.</span><span class="sxs-lookup"><span data-stu-id="e38c4-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="e38c4-128">-ShardId</span><span class="sxs-lookup"><span data-stu-id="e38c4-128">-ShardId</span></span>
<span data-ttu-id="e38c4-129">Определяет код shard, который будет перезапущен этим cmdlet для кэша премиум-класса с включенной кластеризаем.</span><span class="sxs-lookup"><span data-stu-id="e38c4-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

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

### <span data-ttu-id="e38c4-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e38c4-130">-Confirm</span></span>
<span data-ttu-id="e38c4-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e38c4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e38c4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e38c4-132">-WhatIf</span></span>
<span data-ttu-id="e38c4-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e38c4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e38c4-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e38c4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e38c4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e38c4-135">CommonParameters</span></span>
<span data-ttu-id="e38c4-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e38c4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e38c4-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e38c4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e38c4-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e38c4-138">INPUTS</span></span>

### <span data-ttu-id="e38c4-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e38c4-139">System.String</span></span>

### <span data-ttu-id="e38c4-140">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e38c4-140">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e38c4-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e38c4-141">OUTPUTS</span></span>

### <span data-ttu-id="e38c4-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e38c4-142">System.Boolean</span></span>

## <span data-ttu-id="e38c4-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e38c4-143">NOTES</span></span>
* <span data-ttu-id="e38c4-144">Ключевые слова: azure, azurerm, arm, resource, management, manager, redis, cache, webapp, website</span><span class="sxs-lookup"><span data-stu-id="e38c4-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="e38c4-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e38c4-145">RELATED LINKS</span></span>

[<span data-ttu-id="e38c4-146">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e38c4-146">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="e38c4-147">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e38c4-147">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="e38c4-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e38c4-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="e38c4-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e38c4-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="e38c4-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e38c4-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


