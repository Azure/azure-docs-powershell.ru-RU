---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 0e63f8e5f427a251db13c76f915dc615f259defc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073564"
---
# <span data-ttu-id="e3282-101">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="e3282-101">Get-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="e3282-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e3282-102">SYNOPSIS</span></span>
<span data-ttu-id="e3282-103">Возвращает расписание исправлений.</span><span class="sxs-lookup"><span data-stu-id="e3282-103">Gets a patch schedule.</span></span>

## <span data-ttu-id="e3282-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e3282-104">SYNTAX</span></span>

```
Get-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3282-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3282-105">DESCRIPTION</span></span>
<span data-ttu-id="e3282-106">Командлет **Get-AzRedisCachePatchSchedule** получает расписание исправлений кэша в Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="e3282-106">The **Get-AzRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="e3282-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e3282-107">EXAMPLES</span></span>

### <span data-ttu-id="e3282-108">Пример 1: получение расписания исправлений</span><span class="sxs-lookup"><span data-stu-id="e3282-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="e3282-109">Эта команда получает расписание исправлений из кэша с именем RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="e3282-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="e3282-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e3282-110">PARAMETERS</span></span>

### <span data-ttu-id="e3282-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3282-111">-DefaultProfile</span></span>
<span data-ttu-id="e3282-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e3282-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3282-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e3282-113">-Name</span></span>
<span data-ttu-id="e3282-114">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="e3282-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="e3282-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3282-115">-ResourceGroupName</span></span>
<span data-ttu-id="e3282-116">Указывает имя группы ресурсов, содержащей кэш.</span><span class="sxs-lookup"><span data-stu-id="e3282-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="e3282-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3282-117">CommonParameters</span></span>
<span data-ttu-id="e3282-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e3282-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3282-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3282-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3282-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e3282-120">INPUTS</span></span>

### <span data-ttu-id="e3282-121">System. String</span><span class="sxs-lookup"><span data-stu-id="e3282-121">System.String</span></span>

## <span data-ttu-id="e3282-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3282-122">OUTPUTS</span></span>

### <span data-ttu-id="e3282-123">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="e3282-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="e3282-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="e3282-124">NOTES</span></span>
* <span data-ttu-id="e3282-125">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Redis, кэш, Интернет, webapp, веб-сайт</span><span class="sxs-lookup"><span data-stu-id="e3282-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="e3282-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3282-126">RELATED LINKS</span></span>

[<span data-ttu-id="e3282-127">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="e3282-127">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="e3282-128">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="e3282-128">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="e3282-129">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="e3282-129">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


