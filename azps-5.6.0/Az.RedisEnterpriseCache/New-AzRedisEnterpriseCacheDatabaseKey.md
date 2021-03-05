---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/new-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: 3d28515ede93abf2ebb5be8bad2e961f2e22b572
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000755"
---
# <span data-ttu-id="33333-101">New-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="33333-101">New-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="33333-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33333-102">SYNOPSIS</span></span>
<span data-ttu-id="33333-103">Повторно сгенерирует ключи доступа к базе данных RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="33333-103">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="33333-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="33333-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 -KeyType <AccessKeyType> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="33333-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="33333-105">DESCRIPTION</span></span>
<span data-ttu-id="33333-106">Повторно сгенерирует ключи доступа к базе данных RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="33333-106">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="33333-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="33333-107">EXAMPLES</span></span>

### <span data-ttu-id="33333-108">Пример 1. Повторное сгенерировать первичный ключ доступа</span><span class="sxs-lookup"><span data-stu-id="33333-108">Example 1: Regenerate primary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Primary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
new-primary-key                              secondary-key

```

<span data-ttu-id="33333-109">Эта команда повторно сгенерирует первичный ключ доступа, используемый для проверки подлинности подключений к базе данных кэша Redis Enterprise под названием MyCache.</span><span class="sxs-lookup"><span data-stu-id="33333-109">This command regenerates the primary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="33333-110">Пример 2. Повторное сгенерировать клавишу дополнительного доступа</span><span class="sxs-lookup"><span data-stu-id="33333-110">Example 2: Regenerate secondary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Secondary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  new-secondary-key

```

<span data-ttu-id="33333-111">Эта команда повторно сгенерирует ключ доступа дополнительного секретного доступа, используемый для проверки подлинности подключений к базе данных кэша Redis Enterprise под названием MyCache.</span><span class="sxs-lookup"><span data-stu-id="33333-111">This command regenerates the secondary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="33333-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33333-112">PARAMETERS</span></span>

### <span data-ttu-id="33333-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33333-113">-AsJob</span></span>
<span data-ttu-id="33333-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="33333-114">Run the command as a job</span></span>

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

### <span data-ttu-id="33333-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="33333-115">-ClusterName</span></span>
<span data-ttu-id="33333-116">Название кластера RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="33333-116">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33333-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33333-117">-DefaultProfile</span></span>
<span data-ttu-id="33333-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="33333-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33333-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="33333-119">-KeyType</span></span>
<span data-ttu-id="33333-120">Клавиша доступа, которую нужно сгенерировать повторно.</span><span class="sxs-lookup"><span data-stu-id="33333-120">Which access key to regenerate.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.AccessKeyType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33333-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="33333-121">-NoWait</span></span>
<span data-ttu-id="33333-122">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="33333-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="33333-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33333-123">-ResourceGroupName</span></span>
<span data-ttu-id="33333-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="33333-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33333-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="33333-125">-SubscriptionId</span></span>
<span data-ttu-id="33333-126">Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="33333-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="33333-127">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="33333-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33333-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33333-128">-Confirm</span></span>
<span data-ttu-id="33333-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="33333-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33333-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33333-130">-WhatIf</span></span>
<span data-ttu-id="33333-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33333-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33333-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="33333-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33333-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33333-133">CommonParameters</span></span>
<span data-ttu-id="33333-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33333-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33333-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33333-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33333-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="33333-136">INPUTS</span></span>

## <span data-ttu-id="33333-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="33333-137">OUTPUTS</span></span>

### <span data-ttu-id="33333-138">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="33333-138">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="33333-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="33333-139">NOTES</span></span>

<span data-ttu-id="33333-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="33333-140">ALIASES</span></span>

## <span data-ttu-id="33333-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="33333-141">RELATED LINKS</span></span>

