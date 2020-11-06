---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
ms.openlocfilehash: 8364a3a8b9d88bfd3ce34f2e70f8fcae80e9b612
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567250"
---
# <span data-ttu-id="0027c-101">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="0027c-101">New-AzureRmRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="0027c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0027c-102">SYNOPSIS</span></span>
<span data-ttu-id="0027c-103">Создание записи расписания.</span><span class="sxs-lookup"><span data-stu-id="0027c-103">Creates a schedule entry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0027c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0027c-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0027c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0027c-105">DESCRIPTION</span></span>
<span data-ttu-id="0027c-106">Командлет **New-AzureRmRedisCacheScheduleEntry** создает объект **PSScheduleEntry** .</span><span class="sxs-lookup"><span data-stu-id="0027c-106">The **New-AzureRmRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="0027c-107">Командлеты расписания Redis Azure Cache, например командлет New-AzureRmRedisCachePatchSchedule, требуют объектов записи расписания.</span><span class="sxs-lookup"><span data-stu-id="0027c-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzureRmRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="0027c-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0027c-108">EXAMPLES</span></span>

### <span data-ttu-id="0027c-109">Пример 1: создание записи расписания для выходных дней</span><span class="sxs-lookup"><span data-stu-id="0027c-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="0027c-110">Эта команда создает объект **PSScheduleEntry** , представляющий расписание выходных дней с указанными временем начала и окном.</span><span class="sxs-lookup"><span data-stu-id="0027c-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="0027c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0027c-111">PARAMETERS</span></span>

### <span data-ttu-id="0027c-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="0027c-112">-DayOfWeek</span></span>
<span data-ttu-id="0027c-113">Задает день недели для записи расписания.</span><span class="sxs-lookup"><span data-stu-id="0027c-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="0027c-114">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0027c-114">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0027c-115">Жизни</span><span class="sxs-lookup"><span data-stu-id="0027c-115">Everyday</span></span> 
- <span data-ttu-id="0027c-116">Выходные</span><span class="sxs-lookup"><span data-stu-id="0027c-116">Weekend</span></span> 
- <span data-ttu-id="0027c-117">Вторник</span><span class="sxs-lookup"><span data-stu-id="0027c-117">Monday</span></span> 
- <span data-ttu-id="0027c-118">Вторник</span><span class="sxs-lookup"><span data-stu-id="0027c-118">Tuesday</span></span> 
- <span data-ttu-id="0027c-119">Четверг</span><span class="sxs-lookup"><span data-stu-id="0027c-119">Wednesday</span></span> 
- <span data-ttu-id="0027c-120">Вторник</span><span class="sxs-lookup"><span data-stu-id="0027c-120">Thursday</span></span> 
- <span data-ttu-id="0027c-121">Пт</span><span class="sxs-lookup"><span data-stu-id="0027c-121">Friday</span></span> 
- <span data-ttu-id="0027c-122">Субботам</span><span class="sxs-lookup"><span data-stu-id="0027c-122">Saturday</span></span> 
- <span data-ttu-id="0027c-123">Воскресеньям</span><span class="sxs-lookup"><span data-stu-id="0027c-123">Sunday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Everyday, Weekend, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0027c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0027c-124">-DefaultProfile</span></span>
<span data-ttu-id="0027c-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0027c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0027c-126">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="0027c-126">-MaintenanceWindow</span></span>
<span data-ttu-id="0027c-127">Указывает количество времени, в течение которого разрешено обновление.</span><span class="sxs-lookup"><span data-stu-id="0027c-127">Specifies the amount of time window allowed for updates.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0027c-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="0027c-128">-StartHourUtc</span></span>
<span data-ttu-id="0027c-129">Задает час дня начала расписания.</span><span class="sxs-lookup"><span data-stu-id="0027c-129">Specifies an hour of the day when the schedule starts.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0027c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0027c-130">CommonParameters</span></span>
<span data-ttu-id="0027c-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0027c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0027c-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0027c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0027c-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0027c-133">INPUTS</span></span>

### <span data-ttu-id="0027c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0027c-134">System.String</span></span>

### <span data-ttu-id="0027c-135">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0027c-135">System.Int32</span></span>

### <span data-ttu-id="0027c-136">System. Nullable "1 [[System. TimeSpan, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0027c-136">System.Nullable\`1[[System.TimeSpan, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="0027c-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0027c-137">OUTPUTS</span></span>

### <span data-ttu-id="0027c-138">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="0027c-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="0027c-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="0027c-139">NOTES</span></span>
* <span data-ttu-id="0027c-140">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Redis, кэш, Интернет, webapp, веб-сайт</span><span class="sxs-lookup"><span data-stu-id="0027c-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="0027c-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0027c-141">RELATED LINKS</span></span>

[<span data-ttu-id="0027c-142">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0027c-142">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="0027c-143">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0027c-143">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="0027c-144">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0027c-144">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


