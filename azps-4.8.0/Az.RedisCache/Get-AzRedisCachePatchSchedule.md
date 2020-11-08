---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 0e63f8e5f427a251db13c76f915dc615f259defc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242904"
---
# <span data-ttu-id="1fb70-101">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="1fb70-101">Get-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="1fb70-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1fb70-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb70-103">Возвращает расписание исправлений.</span><span class="sxs-lookup"><span data-stu-id="1fb70-103">Gets a patch schedule.</span></span>

## <span data-ttu-id="1fb70-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1fb70-104">SYNTAX</span></span>

```
Get-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fb70-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fb70-105">DESCRIPTION</span></span>
<span data-ttu-id="1fb70-106">Командлет **Get-AzRedisCachePatchSchedule** получает расписание исправлений кэша в Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="1fb70-106">The **Get-AzRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="1fb70-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1fb70-107">EXAMPLES</span></span>

### <span data-ttu-id="1fb70-108">Пример 1: получение расписания исправлений</span><span class="sxs-lookup"><span data-stu-id="1fb70-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="1fb70-109">Эта команда получает расписание исправлений из кэша с именем RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="1fb70-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="1fb70-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1fb70-110">PARAMETERS</span></span>

### <span data-ttu-id="1fb70-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb70-111">-DefaultProfile</span></span>
<span data-ttu-id="1fb70-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1fb70-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fb70-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1fb70-113">-Name</span></span>
<span data-ttu-id="1fb70-114">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="1fb70-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="1fb70-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fb70-115">-ResourceGroupName</span></span>
<span data-ttu-id="1fb70-116">Указывает имя группы ресурсов, содержащей кэш.</span><span class="sxs-lookup"><span data-stu-id="1fb70-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="1fb70-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb70-117">CommonParameters</span></span>
<span data-ttu-id="1fb70-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1fb70-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fb70-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fb70-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb70-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1fb70-120">INPUTS</span></span>

### <span data-ttu-id="1fb70-121">System. String</span><span class="sxs-lookup"><span data-stu-id="1fb70-121">System.String</span></span>

## <span data-ttu-id="1fb70-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fb70-122">OUTPUTS</span></span>

### <span data-ttu-id="1fb70-123">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="1fb70-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="1fb70-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="1fb70-124">NOTES</span></span>
* <span data-ttu-id="1fb70-125">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Redis, кэш, Интернет, webapp, веб-сайт</span><span class="sxs-lookup"><span data-stu-id="1fb70-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="1fb70-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1fb70-126">RELATED LINKS</span></span>

[<span data-ttu-id="1fb70-127">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="1fb70-127">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="1fb70-128">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="1fb70-128">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="1fb70-129">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="1fb70-129">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


