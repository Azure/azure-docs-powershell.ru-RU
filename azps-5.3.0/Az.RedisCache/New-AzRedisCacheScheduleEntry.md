---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
ms.openlocfilehash: e3976c1008388c85a04715541d0d88e164a422e9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505383"
---
# <span data-ttu-id="03927-101">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="03927-101">New-AzRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="03927-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03927-102">SYNOPSIS</span></span>
<span data-ttu-id="03927-103">Создает запись расписания.</span><span class="sxs-lookup"><span data-stu-id="03927-103">Creates a schedule entry.</span></span>

## <span data-ttu-id="03927-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="03927-104">SYNTAX</span></span>

```
New-AzRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03927-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="03927-105">DESCRIPTION</span></span>
<span data-ttu-id="03927-106">С **новыми azRedisCacheScheduleEntry создается** объект **PSScheduleEntry.**</span><span class="sxs-lookup"><span data-stu-id="03927-106">The **New-AzRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="03927-107">Для работы с исправлениями в кэше Azure Redis, например с New-AzRedisCachePatchSchedule, требуются объекты для ввода исправлений.</span><span class="sxs-lookup"><span data-stu-id="03927-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="03927-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="03927-108">EXAMPLES</span></span>

### <span data-ttu-id="03927-109">Пример 1. Создание записи расписания для выходных</span><span class="sxs-lookup"><span data-stu-id="03927-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="03927-110">Эта команда создает объект **PSScheduleEntry,** который представляет расписание на выходные с указанным временем начала и окном.</span><span class="sxs-lookup"><span data-stu-id="03927-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="03927-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03927-111">PARAMETERS</span></span>

### <span data-ttu-id="03927-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="03927-112">-DayOfWeek</span></span>
<span data-ttu-id="03927-113">Определяет день недели в записи расписания.</span><span class="sxs-lookup"><span data-stu-id="03927-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="03927-114">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="03927-114">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="03927-115">Каждый день</span><span class="sxs-lookup"><span data-stu-id="03927-115">Everyday</span></span> 
- <span data-ttu-id="03927-116">Выходной</span><span class="sxs-lookup"><span data-stu-id="03927-116">Weekend</span></span> 
- <span data-ttu-id="03927-117">Понедельник</span><span class="sxs-lookup"><span data-stu-id="03927-117">Monday</span></span> 
- <span data-ttu-id="03927-118">Вторник</span><span class="sxs-lookup"><span data-stu-id="03927-118">Tuesday</span></span> 
- <span data-ttu-id="03927-119">Среда</span><span class="sxs-lookup"><span data-stu-id="03927-119">Wednesday</span></span> 
- <span data-ttu-id="03927-120">Четверг</span><span class="sxs-lookup"><span data-stu-id="03927-120">Thursday</span></span> 
- <span data-ttu-id="03927-121">Пятница</span><span class="sxs-lookup"><span data-stu-id="03927-121">Friday</span></span> 
- <span data-ttu-id="03927-122">Суббота</span><span class="sxs-lookup"><span data-stu-id="03927-122">Saturday</span></span> 
- <span data-ttu-id="03927-123">Воскресенье</span><span class="sxs-lookup"><span data-stu-id="03927-123">Sunday</span></span>

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

### <span data-ttu-id="03927-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03927-124">-DefaultProfile</span></span>
<span data-ttu-id="03927-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="03927-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03927-126">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="03927-126">-MaintenanceWindow</span></span>
<span data-ttu-id="03927-127">Определяет время, в течение времени, заданное для обновления.</span><span class="sxs-lookup"><span data-stu-id="03927-127">Specifies the amount of time window allowed for updates.</span></span>

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

### <span data-ttu-id="03927-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="03927-128">-StartHourUtc</span></span>
<span data-ttu-id="03927-129">Определяет час, в который день начинается расписание.</span><span class="sxs-lookup"><span data-stu-id="03927-129">Specifies an hour of the day when the schedule starts.</span></span>

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

### <span data-ttu-id="03927-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03927-130">CommonParameters</span></span>
<span data-ttu-id="03927-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03927-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03927-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03927-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03927-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03927-133">INPUTS</span></span>

### <span data-ttu-id="03927-134">System.String</span><span class="sxs-lookup"><span data-stu-id="03927-134">System.String</span></span>

### <span data-ttu-id="03927-135">System.Int32</span><span class="sxs-lookup"><span data-stu-id="03927-135">System.Int32</span></span>

### <span data-ttu-id="03927-136">System.Nullable'1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="03927-136">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="03927-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="03927-137">OUTPUTS</span></span>

### <span data-ttu-id="03927-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="03927-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="03927-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="03927-139">NOTES</span></span>
* <span data-ttu-id="03927-140">Ключевые слова: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="03927-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="03927-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="03927-141">RELATED LINKS</span></span>

[<span data-ttu-id="03927-142">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="03927-142">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="03927-143">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="03927-143">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="03927-144">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="03927-144">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


