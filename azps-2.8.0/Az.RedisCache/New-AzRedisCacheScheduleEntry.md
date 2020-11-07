---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
ms.openlocfilehash: 7f877b929cb5ccd171b76cd9131f33693a5f0906
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905730"
---
# <span data-ttu-id="9939e-101">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="9939e-101">New-AzRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="9939e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9939e-102">SYNOPSIS</span></span>
<span data-ttu-id="9939e-103">Создание записи расписания.</span><span class="sxs-lookup"><span data-stu-id="9939e-103">Creates a schedule entry.</span></span>

## <span data-ttu-id="9939e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9939e-104">SYNTAX</span></span>

```
New-AzRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9939e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9939e-105">DESCRIPTION</span></span>
<span data-ttu-id="9939e-106">Командлет **New-AzRedisCacheScheduleEntry** создает объект **PSScheduleEntry** .</span><span class="sxs-lookup"><span data-stu-id="9939e-106">The **New-AzRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="9939e-107">Командлеты расписания Redis Azure Cache, например командлет New-AzRedisCachePatchSchedule, требуют объектов записи расписания.</span><span class="sxs-lookup"><span data-stu-id="9939e-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="9939e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9939e-108">EXAMPLES</span></span>

### <span data-ttu-id="9939e-109">Пример 1: создание записи расписания для выходных дней</span><span class="sxs-lookup"><span data-stu-id="9939e-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="9939e-110">Эта команда создает объект **PSScheduleEntry** , представляющий расписание выходных дней с указанными временем начала и окном.</span><span class="sxs-lookup"><span data-stu-id="9939e-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="9939e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9939e-111">PARAMETERS</span></span>

### <span data-ttu-id="9939e-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="9939e-112">-DayOfWeek</span></span>
<span data-ttu-id="9939e-113">Задает день недели для записи расписания.</span><span class="sxs-lookup"><span data-stu-id="9939e-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="9939e-114">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9939e-114">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9939e-115">Жизни</span><span class="sxs-lookup"><span data-stu-id="9939e-115">Everyday</span></span> 
- <span data-ttu-id="9939e-116">Выходные</span><span class="sxs-lookup"><span data-stu-id="9939e-116">Weekend</span></span> 
- <span data-ttu-id="9939e-117">Вторник</span><span class="sxs-lookup"><span data-stu-id="9939e-117">Monday</span></span> 
- <span data-ttu-id="9939e-118">Вторник</span><span class="sxs-lookup"><span data-stu-id="9939e-118">Tuesday</span></span> 
- <span data-ttu-id="9939e-119">Четверг</span><span class="sxs-lookup"><span data-stu-id="9939e-119">Wednesday</span></span> 
- <span data-ttu-id="9939e-120">Вторник</span><span class="sxs-lookup"><span data-stu-id="9939e-120">Thursday</span></span> 
- <span data-ttu-id="9939e-121">Пт</span><span class="sxs-lookup"><span data-stu-id="9939e-121">Friday</span></span> 
- <span data-ttu-id="9939e-122">Субботам</span><span class="sxs-lookup"><span data-stu-id="9939e-122">Saturday</span></span> 
- <span data-ttu-id="9939e-123">Воскресеньям</span><span class="sxs-lookup"><span data-stu-id="9939e-123">Sunday</span></span>

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

### <span data-ttu-id="9939e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9939e-124">-DefaultProfile</span></span>
<span data-ttu-id="9939e-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9939e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9939e-126">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="9939e-126">-MaintenanceWindow</span></span>
<span data-ttu-id="9939e-127">Указывает количество времени, в течение которого разрешено обновление.</span><span class="sxs-lookup"><span data-stu-id="9939e-127">Specifies the amount of time window allowed for updates.</span></span>

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

### <span data-ttu-id="9939e-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="9939e-128">-StartHourUtc</span></span>
<span data-ttu-id="9939e-129">Задает час дня начала расписания.</span><span class="sxs-lookup"><span data-stu-id="9939e-129">Specifies an hour of the day when the schedule starts.</span></span>

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

### <span data-ttu-id="9939e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9939e-130">CommonParameters</span></span>
<span data-ttu-id="9939e-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9939e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9939e-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9939e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9939e-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9939e-133">INPUTS</span></span>

### <span data-ttu-id="9939e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9939e-134">System.String</span></span>

### <span data-ttu-id="9939e-135">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9939e-135">System.Int32</span></span>

### <span data-ttu-id="9939e-136">System. Nullable "1 [[System. TimeSpan, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9939e-136">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9939e-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9939e-137">OUTPUTS</span></span>

### <span data-ttu-id="9939e-138">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="9939e-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="9939e-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="9939e-139">NOTES</span></span>
* <span data-ttu-id="9939e-140">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Redis, кэш, Интернет, webapp, веб-сайт</span><span class="sxs-lookup"><span data-stu-id="9939e-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="9939e-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9939e-141">RELATED LINKS</span></span>

[<span data-ttu-id="9939e-142">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="9939e-142">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="9939e-143">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="9939e-143">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="9939e-144">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="9939e-144">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


