---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
ms.openlocfilehash: 2f43cfa1e10fe115f8bf5fc94404f532f04f6573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732012"
---
# <span data-ttu-id="a4b57-101">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="a4b57-101">New-AzureRmRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="a4b57-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4b57-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b57-103">Создание записи расписания.</span><span class="sxs-lookup"><span data-stu-id="a4b57-103">Creates a schedule entry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4b57-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4b57-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4b57-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4b57-105">DESCRIPTION</span></span>
<span data-ttu-id="a4b57-106">Командлет **New-AzureRmRedisCacheScheduleEntry** создает объект **PSScheduleEntry** .</span><span class="sxs-lookup"><span data-stu-id="a4b57-106">The **New-AzureRmRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="a4b57-107">Командлеты расписания Redis Azure Cache, например командлет New-AzureRmRedisCachePatchSchedule, требуют объектов записи расписания.</span><span class="sxs-lookup"><span data-stu-id="a4b57-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzureRmRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="a4b57-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4b57-108">EXAMPLES</span></span>

### <span data-ttu-id="a4b57-109">Пример 1: создание записи расписания для выходных дней</span><span class="sxs-lookup"><span data-stu-id="a4b57-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="a4b57-110">Эта команда создает объект **PSScheduleEntry** , представляющий расписание выходных дней с указанными временем начала и окном.</span><span class="sxs-lookup"><span data-stu-id="a4b57-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="a4b57-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4b57-111">PARAMETERS</span></span>

### <span data-ttu-id="a4b57-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="a4b57-112">-DayOfWeek</span></span>
<span data-ttu-id="a4b57-113">Задает день недели для записи расписания.</span><span class="sxs-lookup"><span data-stu-id="a4b57-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="a4b57-114">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a4b57-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a4b57-115">Жизни</span><span class="sxs-lookup"><span data-stu-id="a4b57-115">Everyday</span></span> 
- <span data-ttu-id="a4b57-116">Выходные</span><span class="sxs-lookup"><span data-stu-id="a4b57-116">Weekend</span></span> 
- <span data-ttu-id="a4b57-117">Вторник</span><span class="sxs-lookup"><span data-stu-id="a4b57-117">Monday</span></span> 
- <span data-ttu-id="a4b57-118">Вторник</span><span class="sxs-lookup"><span data-stu-id="a4b57-118">Tuesday</span></span> 
- <span data-ttu-id="a4b57-119">Четверг</span><span class="sxs-lookup"><span data-stu-id="a4b57-119">Wednesday</span></span> 
- <span data-ttu-id="a4b57-120">Вторник</span><span class="sxs-lookup"><span data-stu-id="a4b57-120">Thursday</span></span> 
- <span data-ttu-id="a4b57-121">Пт</span><span class="sxs-lookup"><span data-stu-id="a4b57-121">Friday</span></span> 
- <span data-ttu-id="a4b57-122">Субботам</span><span class="sxs-lookup"><span data-stu-id="a4b57-122">Saturday</span></span> 
- <span data-ttu-id="a4b57-123">Воскресеньям</span><span class="sxs-lookup"><span data-stu-id="a4b57-123">Sunday</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Everyday, Weekend, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b57-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b57-124">-DefaultProfile</span></span>
<span data-ttu-id="a4b57-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4b57-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4b57-126">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="a4b57-126">-MaintenanceWindow</span></span>
<span data-ttu-id="a4b57-127">Указывает количество времени, в течение которого разрешено обновление.</span><span class="sxs-lookup"><span data-stu-id="a4b57-127">Specifies the amount of time window allowed for updates.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b57-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="a4b57-128">-StartHourUtc</span></span>
<span data-ttu-id="a4b57-129">Задает час дня начала расписания.</span><span class="sxs-lookup"><span data-stu-id="a4b57-129">Specifies an hour of the day when the schedule starts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b57-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b57-130">CommonParameters</span></span>
<span data-ttu-id="a4b57-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4b57-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b57-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4b57-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b57-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4b57-133">INPUTS</span></span>

### <span data-ttu-id="a4b57-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="a4b57-134">None</span></span>
<span data-ttu-id="a4b57-135">Вы можете передавать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="a4b57-135">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="a4b57-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4b57-136">OUTPUTS</span></span>

### <span data-ttu-id="a4b57-137">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="a4b57-137">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="a4b57-138">Этот командлет возвращает объект для записи расписания.</span><span class="sxs-lookup"><span data-stu-id="a4b57-138">This cmdlet returns a schedule entry object.</span></span>

## <span data-ttu-id="a4b57-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4b57-139">NOTES</span></span>
* <span data-ttu-id="a4b57-140">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Redis, кэш, Интернет, webapp, веб-сайт</span><span class="sxs-lookup"><span data-stu-id="a4b57-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="a4b57-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4b57-141">RELATED LINKS</span></span>

[<span data-ttu-id="a4b57-142">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a4b57-142">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="a4b57-143">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a4b57-143">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="a4b57-144">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a4b57-144">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


