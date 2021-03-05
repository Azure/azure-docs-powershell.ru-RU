---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 9033082093d571fc60cd9b4c495688d11d87aea8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000803"
---
# <span data-ttu-id="1d853-101">Get-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="1d853-101">Get-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="1d853-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d853-102">SYNOPSIS</span></span>
<span data-ttu-id="1d853-103">Получает сведения о базе данных в кластере RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="1d853-103">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="1d853-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1d853-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1d853-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d853-105">DESCRIPTION</span></span>
<span data-ttu-id="1d853-106">Получает сведения о базе данных в кластере RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="1d853-106">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="1d853-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1d853-107">EXAMPLES</span></span>

### <span data-ttu-id="1d853-108">Пример 1. Получить базу данных</span><span class="sxs-lookup"><span data-stu-id="1d853-108">Example 1: Get database</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="1d853-109">Эта команда получает базу данных кэша Redis Enterprise под названием MyCache.</span><span class="sxs-lookup"><span data-stu-id="1d853-109">This command gets the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="1d853-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d853-110">PARAMETERS</span></span>

### <span data-ttu-id="1d853-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1d853-111">-ClusterName</span></span>
<span data-ttu-id="1d853-112">Название кластера RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="1d853-112">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="1d853-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d853-113">-DefaultProfile</span></span>
<span data-ttu-id="1d853-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1d853-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d853-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d853-115">-ResourceGroupName</span></span>
<span data-ttu-id="1d853-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1d853-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="1d853-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1d853-117">-SubscriptionId</span></span>
<span data-ttu-id="1d853-118">Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1d853-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1d853-119">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="1d853-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1d853-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d853-120">CommonParameters</span></span>
<span data-ttu-id="1d853-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d853-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d853-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d853-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d853-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d853-123">INPUTS</span></span>

## <span data-ttu-id="1d853-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1d853-124">OUTPUTS</span></span>

### <span data-ttu-id="1d853-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span><span class="sxs-lookup"><span data-stu-id="1d853-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="1d853-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1d853-126">NOTES</span></span>

<span data-ttu-id="1d853-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1d853-127">ALIASES</span></span>

## <span data-ttu-id="1d853-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d853-128">RELATED LINKS</span></span>

