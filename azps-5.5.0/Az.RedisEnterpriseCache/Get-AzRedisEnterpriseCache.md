---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
ms.openlocfilehash: a6fe478aa8221060974f54e75b63a64edf0beae4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240173"
---
# <span data-ttu-id="7bd4b-101">Get-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="7bd4b-101">Get-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="7bd4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bd4b-102">SYNOPSIS</span></span>
<span data-ttu-id="7bd4b-103">Сведения о кластере RedisEnterprise и связанной с ней базе данных</span><span class="sxs-lookup"><span data-stu-id="7bd4b-103">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="7bd4b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7bd4b-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCache -ResourceGroupName <String> [-ClusterName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7bd4b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7bd4b-105">DESCRIPTION</span></span>
<span data-ttu-id="7bd4b-106">Сведения о кластере RedisEnterprise и связанной с ней базе данных</span><span class="sxs-lookup"><span data-stu-id="7bd4b-106">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="7bd4b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7bd4b-107">EXAMPLES</span></span>

### <span data-ttu-id="7bd4b-108">Пример 1. Получить корпоративный кэш Redis по имени</span><span class="sxs-lookup"><span data-stu-id="7bd4b-108">Example 1: Get a Redis Enterprise Cache by name</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup" -Name "MyCache"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="7bd4b-109">Эта команда получает кэш Redis Enterprise под названием MyCache.</span><span class="sxs-lookup"><span data-stu-id="7bd4b-109">This command gets the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="7bd4b-110">Пример 2. Все кэш Redis Enterprise в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="7bd4b-110">Example 2: Get every Redis Enterprise Cache in a resource group</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup"

Location Name     Type                            Zone      Database
-------- ----     ----                            ----      --------
East US  MyCache1 Microsoft.Cache/redisEnterprise           {default}
East US  MyCache2 Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="7bd4b-111">Эта команда возвращает каждый кэш Redis Enterprise в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7bd4b-111">This command gets every Redis Enterprise Cache in the specified resource group.</span></span>

## <span data-ttu-id="7bd4b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bd4b-112">PARAMETERS</span></span>

### <span data-ttu-id="7bd4b-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7bd4b-113">-ClusterName</span></span>
<span data-ttu-id="7bd4b-114">Название кластера RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="7bd4b-114">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd4b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bd4b-115">-DefaultProfile</span></span>
<span data-ttu-id="7bd4b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7bd4b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bd4b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bd4b-117">-ResourceGroupName</span></span>
<span data-ttu-id="7bd4b-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7bd4b-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="7bd4b-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7bd4b-119">-SubscriptionId</span></span>
<span data-ttu-id="7bd4b-120">Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7bd4b-120">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7bd4b-121">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="7bd4b-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7bd4b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bd4b-122">CommonParameters</span></span>
<span data-ttu-id="7bd4b-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bd4b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bd4b-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7bd4b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bd4b-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7bd4b-125">INPUTS</span></span>

## <span data-ttu-id="7bd4b-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7bd4b-126">OUTPUTS</span></span>

### <span data-ttu-id="7bd4b-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="7bd4b-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="7bd4b-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7bd4b-128">NOTES</span></span>

<span data-ttu-id="7bd4b-129">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7bd4b-129">ALIASES</span></span>

## <span data-ttu-id="7bd4b-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7bd4b-130">RELATED LINKS</span></span>

