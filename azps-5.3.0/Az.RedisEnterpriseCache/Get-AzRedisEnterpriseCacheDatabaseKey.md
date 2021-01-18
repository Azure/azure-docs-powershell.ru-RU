---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: e602cb4fc86ede6a4e1f7cc894c1825fd1d560fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505355"
---
# <span data-ttu-id="b5d4f-101">Get-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="b5d4f-101">Get-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="b5d4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5d4f-102">SYNOPSIS</span></span>
<span data-ttu-id="b5d4f-103">Извлекает ключи доступа для базы данных RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="b5d4f-103">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="b5d4f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b5d4f-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b5d4f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5d4f-105">DESCRIPTION</span></span>
<span data-ttu-id="b5d4f-106">Извлекает ключи доступа для базы данных RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="b5d4f-106">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="b5d4f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b5d4f-107">EXAMPLES</span></span>

### <span data-ttu-id="b5d4f-108">Пример 1. Получить ключи доступа к базе данных</span><span class="sxs-lookup"><span data-stu-id="b5d4f-108">Example 1: Get database access keys</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  secondary-key

```

<span data-ttu-id="b5d4f-109">Эта команда получает секретные ключи доступа, используемые для проверки подлинности подключений к базе данных кэша Redis Enterprise под названием MyCache.</span><span class="sxs-lookup"><span data-stu-id="b5d4f-109">This command gets the secret access keys used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="b5d4f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5d4f-110">PARAMETERS</span></span>

### <span data-ttu-id="b5d4f-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b5d4f-111">-ClusterName</span></span>
<span data-ttu-id="b5d4f-112">Название кластера RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="b5d4f-112">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="b5d4f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5d4f-113">-DefaultProfile</span></span>
<span data-ttu-id="b5d4f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b5d4f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5d4f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5d4f-115">-ResourceGroupName</span></span>
<span data-ttu-id="b5d4f-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b5d4f-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="b5d4f-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b5d4f-117">-SubscriptionId</span></span>
<span data-ttu-id="b5d4f-118">Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b5d4f-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b5d4f-119">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="b5d4f-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d4f-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5d4f-120">-Confirm</span></span>
<span data-ttu-id="b5d4f-121">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b5d4f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5d4f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5d4f-122">-WhatIf</span></span>
<span data-ttu-id="b5d4f-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5d4f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5d4f-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b5d4f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5d4f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5d4f-125">CommonParameters</span></span>
<span data-ttu-id="b5d4f-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5d4f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5d4f-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5d4f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5d4f-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5d4f-128">INPUTS</span></span>

## <span data-ttu-id="b5d4f-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b5d4f-129">OUTPUTS</span></span>

### <span data-ttu-id="b5d4f-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="b5d4f-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="b5d4f-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b5d4f-131">NOTES</span></span>

<span data-ttu-id="b5d4f-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b5d4f-132">ALIASES</span></span>

## <span data-ttu-id="b5d4f-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5d4f-133">RELATED LINKS</span></span>

