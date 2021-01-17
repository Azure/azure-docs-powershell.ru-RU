---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecacheoperationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
ms.openlocfilehash: 8416c18ac945eaab5ae9dbd758d2660c4f950417
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421199"
---
# <span data-ttu-id="25efb-101">Get-AzRedisEnterpriseCacheOperationStatus</span><span class="sxs-lookup"><span data-stu-id="25efb-101">Get-AzRedisEnterpriseCacheOperationStatus</span></span>

## <span data-ttu-id="25efb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25efb-102">SYNOPSIS</span></span>
<span data-ttu-id="25efb-103">Возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="25efb-103">Gets the status of operation.</span></span>

## <span data-ttu-id="25efb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="25efb-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheOperationStatus -Location <String> -OperationId <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="25efb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25efb-105">DESCRIPTION</span></span>
<span data-ttu-id="25efb-106">Возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="25efb-106">Gets the status of operation.</span></span>

## <span data-ttu-id="25efb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="25efb-107">EXAMPLES</span></span>

### <span data-ttu-id="25efb-108">Пример 1. Получить состояние операции</span><span class="sxs-lookup"><span data-stu-id="25efb-108">Example 1: Get operation status</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheOperationStatus -Location "East US" -OperationId "6432a8f9-0fe6-4339-9303-772c92f35d02"

EndTime                           Name                                 StartTime                         Status
-------                           ----                                 ---------                         ------
2020-12-01T00:12:45.7107366+00:00 6432a8f9-0fe6-4339-9303-772c92f35d02 2020-12-01T00:04:35.7061294+00:00 Succeeded

```

<span data-ttu-id="25efb-109">Эта команда получает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="25efb-109">This command gets the status of an operation.</span></span>

## <span data-ttu-id="25efb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25efb-110">PARAMETERS</span></span>

### <span data-ttu-id="25efb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25efb-111">-DefaultProfile</span></span>
<span data-ttu-id="25efb-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="25efb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25efb-113">-Location</span><span class="sxs-lookup"><span data-stu-id="25efb-113">-Location</span></span>
<span data-ttu-id="25efb-114">Регион, в который она веется.</span><span class="sxs-lookup"><span data-stu-id="25efb-114">The region the operation is in.</span></span>

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

### <span data-ttu-id="25efb-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="25efb-115">-OperationId</span></span>
<span data-ttu-id="25efb-116">Уникальный идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="25efb-116">The operation's unique identifier.</span></span>

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

### <span data-ttu-id="25efb-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="25efb-117">-SubscriptionId</span></span>
<span data-ttu-id="25efb-118">Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="25efb-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="25efb-119">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="25efb-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="25efb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25efb-120">CommonParameters</span></span>
<span data-ttu-id="25efb-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25efb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25efb-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25efb-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25efb-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25efb-123">INPUTS</span></span>

## <span data-ttu-id="25efb-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="25efb-124">OUTPUTS</span></span>

### <span data-ttu-id="25efb-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="25efb-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IOperationStatus</span></span>

## <span data-ttu-id="25efb-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="25efb-126">NOTES</span></span>

<span data-ttu-id="25efb-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="25efb-127">ALIASES</span></span>

## <span data-ttu-id="25efb-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25efb-128">RELATED LINKS</span></span>

