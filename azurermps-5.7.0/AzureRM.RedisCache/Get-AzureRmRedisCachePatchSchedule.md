---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 091d3d52da1319842d221881f03fca2b21353fa9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732146"
---
# <span data-ttu-id="29f94-101">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="29f94-101">Get-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="29f94-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="29f94-102">SYNOPSIS</span></span>
<span data-ttu-id="29f94-103">Возвращает расписание исправлений.</span><span class="sxs-lookup"><span data-stu-id="29f94-103">Gets a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29f94-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="29f94-104">SYNTAX</span></span>

```
Get-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29f94-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29f94-105">DESCRIPTION</span></span>
<span data-ttu-id="29f94-106">Командлет **Get-AzureRmRedisCachePatchSchedule** получает расписание исправлений кэша в Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="29f94-106">The **Get-AzureRmRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="29f94-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="29f94-107">EXAMPLES</span></span>

### <span data-ttu-id="29f94-108">Пример 1: получение расписания исправлений</span><span class="sxs-lookup"><span data-stu-id="29f94-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="29f94-109">Эта команда получает расписание исправлений из кэша с именем RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="29f94-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="29f94-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="29f94-110">PARAMETERS</span></span>

### <span data-ttu-id="29f94-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29f94-111">-DefaultProfile</span></span>
<span data-ttu-id="29f94-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="29f94-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f94-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="29f94-113">-Name</span></span>
<span data-ttu-id="29f94-114">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="29f94-114">Specifies the name of a cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29f94-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29f94-115">-ResourceGroupName</span></span>
<span data-ttu-id="29f94-116">Указывает имя группы ресурсов, содержащей кэш.</span><span class="sxs-lookup"><span data-stu-id="29f94-116">Specifies the name of the resource group which contains the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29f94-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29f94-117">CommonParameters</span></span>
<span data-ttu-id="29f94-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="29f94-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29f94-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29f94-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29f94-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="29f94-120">INPUTS</span></span>

### <span data-ttu-id="29f94-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="29f94-121">None</span></span>
<span data-ttu-id="29f94-122">Вы можете передавать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="29f94-122">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="29f94-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="29f94-123">OUTPUTS</span></span>

### <span data-ttu-id="29f94-124">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="29f94-124">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="29f94-125">Этот командлет возвращает записи расписания исправлений, заданные в кэше.</span><span class="sxs-lookup"><span data-stu-id="29f94-125">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="29f94-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="29f94-126">NOTES</span></span>
* <span data-ttu-id="29f94-127">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Redis, кэш, Интернет, webapp, веб-сайт</span><span class="sxs-lookup"><span data-stu-id="29f94-127">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="29f94-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29f94-128">RELATED LINKS</span></span>

[<span data-ttu-id="29f94-129">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="29f94-129">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="29f94-130">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="29f94-130">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="29f94-131">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="29f94-131">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


