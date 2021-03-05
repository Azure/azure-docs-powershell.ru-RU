---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 297966fe0ad59948fd321ec52cf066ad5caa3d43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008659"
---
# <span data-ttu-id="a9093-101">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a9093-101">Get-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="a9093-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9093-102">SYNOPSIS</span></span>
<span data-ttu-id="a9093-103">Получает расписание исправлений.</span><span class="sxs-lookup"><span data-stu-id="a9093-103">Gets a patch schedule.</span></span>

## <span data-ttu-id="a9093-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a9093-104">SYNTAX</span></span>

```
Get-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9093-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9093-105">DESCRIPTION</span></span>
<span data-ttu-id="a9093-106">**Cmdlet Get-AzRedisCachePatchSchedule** получает расписание исправлений для кэша в кэше Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="a9093-106">The **Get-AzRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="a9093-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a9093-107">EXAMPLES</span></span>

### <span data-ttu-id="a9093-108">Пример 1. Получить расписание исправлений</span><span class="sxs-lookup"><span data-stu-id="a9093-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="a9093-109">Эта команда получает расписание исправлений из кэша RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="a9093-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="a9093-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9093-110">PARAMETERS</span></span>

### <span data-ttu-id="a9093-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9093-111">-DefaultProfile</span></span>
<span data-ttu-id="a9093-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a9093-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9093-113">-Name</span><span class="sxs-lookup"><span data-stu-id="a9093-113">-Name</span></span>
<span data-ttu-id="a9093-114">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="a9093-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="a9093-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9093-115">-ResourceGroupName</span></span>
<span data-ttu-id="a9093-116">Имя группы ресурсов, которая содержит кэш.</span><span class="sxs-lookup"><span data-stu-id="a9093-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="a9093-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9093-117">CommonParameters</span></span>
<span data-ttu-id="a9093-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9093-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9093-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9093-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9093-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9093-120">INPUTS</span></span>

### <span data-ttu-id="a9093-121">System.String</span><span class="sxs-lookup"><span data-stu-id="a9093-121">System.String</span></span>

## <span data-ttu-id="a9093-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a9093-122">OUTPUTS</span></span>

### <span data-ttu-id="a9093-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="a9093-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="a9093-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a9093-124">NOTES</span></span>
* <span data-ttu-id="a9093-125">Ключевые слова: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="a9093-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="a9093-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9093-126">RELATED LINKS</span></span>

[<span data-ttu-id="a9093-127">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a9093-127">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="a9093-128">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="a9093-128">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="a9093-129">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a9093-129">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


