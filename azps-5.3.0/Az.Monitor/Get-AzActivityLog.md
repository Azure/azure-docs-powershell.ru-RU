---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: 9b57d7584ee7720ec73aa57ddec070ad26ddff9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508182"
---
# <span data-ttu-id="5e144-101">Get-AzActivityLog</span><span class="sxs-lookup"><span data-stu-id="5e144-101">Get-AzActivityLog</span></span>

## <span data-ttu-id="5e144-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e144-102">SYNOPSIS</span></span>
<span data-ttu-id="5e144-103">Получить события журнала действий.</span><span class="sxs-lookup"><span data-stu-id="5e144-103">Retrieve Activity Log events.</span></span>

## <span data-ttu-id="5e144-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5e144-104">SYNTAX</span></span>

### <span data-ttu-id="5e144-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="5e144-105">GetByCorrelationId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e144-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5e144-106">GetByResourceId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e144-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5e144-107">GetByResourceGroup</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e144-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5e144-108">GetByResourceProvider</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e144-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="5e144-109">GetBySubscription</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e144-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e144-110">DESCRIPTION</span></span>
<span data-ttu-id="5e144-111">Он Get-AzActivityLog получить события журнала действий.</span><span class="sxs-lookup"><span data-stu-id="5e144-111">The Get-AzActivityLog cmdlet retrieve Activity Log events.</span></span> <span data-ttu-id="5e144-112">События могут быть связаны с текущим ИД подписки, корреляцией, группой ресурсов, ИД ресурса или поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5e144-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="5e144-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5e144-113">EXAMPLES</span></span>

### <span data-ttu-id="5e144-114">Пример 1. Получить журнал событий по ИД подписки</span><span class="sxs-lookup"><span data-stu-id="5e144-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-ActivityAzLog
```

<span data-ttu-id="5e144-115">Эта команда содержит не более 1000 событий, связанных с ИД подписки пользователя, которые были за 7 дней от текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="5e144-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="5e144-116">Пример 2. Получите журнал событий по ИД подписки с максимальным количеством событий</span><span class="sxs-lookup"><span data-stu-id="5e144-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

<span data-ttu-id="5e144-117">Эта команда содержит не более 100 событий, связанных с ИД подписки пользователя, которые были за 7 дней от текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="5e144-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="5e144-118">Пример 3. Получите журнал событий по ИД подписки с временем начала.</span><span class="sxs-lookup"><span data-stu-id="5e144-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="5e144-119">Эта команда содержит не более 1000 событий, связанных с ИД подписки пользователя, который прошел в 2017-06-01T10:30 локального времени или после него, если дата и время не старше 90 дней с текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="5e144-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="5e144-120">Пример 4. Получите журнал событий по ИД подписки с временем начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="5e144-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="5e144-121">Эта команда содержит не более 1000 событий, связанных с ИД подписки пользователя, которые произошли в 2017-04-01T10:30 по местному времени и до 2017-04-14T11:30 локального времени, если весь диапазон дат и времени не был старше 90 дней с текущей даты/времени, то есть период хранения.</span><span class="sxs-lookup"><span data-stu-id="5e144-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="5e144-122">Пример 5. Получить журнал событий по корреляции</span><span class="sxs-lookup"><span data-stu-id="5e144-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="5e144-123">Эта команда содержит не более 1000 событий, связанных с указанным ид корреляции, которые произошли за 7 дней от текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="5e144-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="5e144-124">**ПРИМЕЧАНИЕ.** Обычно это только одно событие.</span><span class="sxs-lookup"><span data-stu-id="5e144-124">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="5e144-125">Пример 6. Получите журнал событий по ид корреляции с максимальным количеством событий</span><span class="sxs-lookup"><span data-stu-id="5e144-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

<span data-ttu-id="5e144-126">Эта команда содержит не более 100 событий, связанных с указанным ид корреляции, которые были заданы за 7 дней от текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="5e144-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="5e144-127">**ПРИМЕЧАНИЕ.** Обычно это только одно событие.</span><span class="sxs-lookup"><span data-stu-id="5e144-127">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="5e144-128">Пример 7. Получите журнал событий по корреляции и времени начала</span><span class="sxs-lookup"><span data-stu-id="5e144-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="5e144-129">Эта команда содержит не более 1000 событий, связанных с указанным id корреляции, которые произошли в 2017-05-22T04:30:00 локального времени, если время начала не прошло более 90 дней с текущей даты/времени.</span><span class="sxs-lookup"><span data-stu-id="5e144-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="5e144-130">**ПРИМЕЧАНИЕ.** Обычно это только одно событие.</span><span class="sxs-lookup"><span data-stu-id="5e144-130">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="5e144-131">Пример 8. Получите журнал событий по ид корреляции со временем начала и окончания</span><span class="sxs-lookup"><span data-stu-id="5e144-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="5e144-132">Эта команда содержит не более 1000 событий, связанных с указанным ид корреляции, которые произошли в 2017-04-15T04:30 локального времени, но до 2017-04-25T12:30 локального времени, если весь диапазон дат и времени не был старше 90 дней с текущей даты/времени, то есть период хранения.</span><span class="sxs-lookup"><span data-stu-id="5e144-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="5e144-133">Пример 9. Получить журнал событий для группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5e144-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="5e144-134">Эта команда содержит не более 1000 событий, связанных с указанной группой ресурсов, которые были заданы на 7 дней от текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="5e144-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="5e144-135">Пример 10. Получите журнал событий для группы ресурсов с максимальным количеством событий</span><span class="sxs-lookup"><span data-stu-id="5e144-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

<span data-ttu-id="5e144-136">Эта команда содержит не более 100 событий, связанных с указанной группой ресурсов, которые были заданы на 7 дней от текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="5e144-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="5e144-137">Пример 11. Получить журнал событий для группы ресурсов по времени начала</span><span class="sxs-lookup"><span data-stu-id="5e144-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="5e144-138">Эта команда содержит не более 1000 событий, связанных с указанной группой ресурсов, которые произошли в 2017-05-22T04:30:00 по локальному времени, если время начала не старше 90 дней с текущей даты/времени.</span><span class="sxs-lookup"><span data-stu-id="5e144-138">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="5e144-139">Пример 12. Получить журнал событий для группы ресурсов с временем начала и окончания</span><span class="sxs-lookup"><span data-stu-id="5e144-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="5e144-140">Эта команда содержит не более 1000 событий, связанных с указанной группой ресурсов, которые произошли в 2017-04-15T04:30 локального времени, но до 2017-04-25T12:30 локального времени, если весь диапазон дат и времени не превышает 90 дней с текущей даты/времени, то есть период хранения.</span><span class="sxs-lookup"><span data-stu-id="5e144-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="5e144-141">Пример 13. Получить журнал событий по ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="5e144-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="5e144-142">Эта команда содержит не более 1000 событий, связанных с указанным ИД ресурса, которые были заданы за 7 дней от текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="5e144-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="5e144-143">Пример 14. Получите журнал событий по ИД ресурса с максимальным количеством событий</span><span class="sxs-lookup"><span data-stu-id="5e144-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

<span data-ttu-id="5e144-144">Эта команда содержит не более 100 событий, связанных с указанным ИД ресурса, которые были заданы на 7 дней от текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="5e144-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="5e144-145">Пример 15. Получить журнал событий по ИД ресурса с временем начала</span><span class="sxs-lookup"><span data-stu-id="5e144-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="5e144-146">Эта команда содержит не более 1000 событий, связанных с указанным ИД ресурса, которые произошли в 2017-05-22T04:30:00 локального времени, если время начала не превышает 90 дней с текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="5e144-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="5e144-147">Пример 16. Получите журнал событий по ИД ресурса с временем начала и окончания</span><span class="sxs-lookup"><span data-stu-id="5e144-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="5e144-148">Эта команда содержит не более 1000 событий, связанных с указанным ИД ресурса, которые произошли в 2017-04-15T04:30 локального времени, но до 2017-04-25T12:30 локального времени, если весь диапазон дат и времени не превышает 90 дней с текущей даты/времени, то есть период хранения.</span><span class="sxs-lookup"><span data-stu-id="5e144-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="5e144-149">Пример 17. Получить журнал событий от поставщика ресурсов</span><span class="sxs-lookup"><span data-stu-id="5e144-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="5e144-150">Эта команда содержит не более 1000 событий, связанных с указанным поставщиком ресурсов, которые прошли 7 дней с текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="5e144-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="5e144-151">Пример 18. Получите журнал событий от поставщика ресурсов с максимальным количеством событий</span><span class="sxs-lookup"><span data-stu-id="5e144-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

<span data-ttu-id="5e144-152">Эта команда содержит не более 100 событий, связанных с указанным поставщиком ресурсов, которые были заданы на 7 дней от текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="5e144-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="5e144-153">Пример 19. Получить журнал событий от поставщика ресурсов с временем начала</span><span class="sxs-lookup"><span data-stu-id="5e144-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="5e144-154">Эта команда содержит не более 1000 событий, связанных с указанным поставщиком ресурсов, которые произошли в 2017-05-22T04:30:00 по локальному времени, если время начала не превышает 90 дней с текущей даты или времени.</span><span class="sxs-lookup"><span data-stu-id="5e144-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="5e144-155">Пример 20. Получить журнал событий от поставщика ресурсов с временем начала и окончания</span><span class="sxs-lookup"><span data-stu-id="5e144-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="5e144-156">Эта команда содержит не более 1000 событий, связанных с указанным поставщиком ресурсов, которые произошли в 2017-04-15T04:30 локального времени, но до 2017-04-25T12:30 локального времени, если весь диапазон дат и времени не превышает 90 дней с текущей даты/времени, то есть период хранения.</span><span class="sxs-lookup"><span data-stu-id="5e144-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="5e144-157">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e144-157">PARAMETERS</span></span>

### <span data-ttu-id="5e144-158">-Caller</span><span class="sxs-lookup"><span data-stu-id="5e144-158">-Caller</span></span>
<span data-ttu-id="5e144-159">The caller of the events to fetch</span><span class="sxs-lookup"><span data-stu-id="5e144-159">The caller of the events to fetch</span></span>

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

### <span data-ttu-id="5e144-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="5e144-160">-CorrelationId</span></span>
<span data-ttu-id="5e144-161">The CorrelationId</span><span class="sxs-lookup"><span data-stu-id="5e144-161">The CorrelationId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByCorrelationId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e144-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e144-162">-DefaultProfile</span></span>
<span data-ttu-id="5e144-163">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5e144-163">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e144-164">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="5e144-164">-DetailedOutput</span></span>
<span data-ttu-id="5e144-165">Возврат объекта со всеми сведениями о событиях (по умолчанию возвращает только некоторые атрибуты, то есть без подробностей)</span><span class="sxs-lookup"><span data-stu-id="5e144-165">Return object with all the details of the events (the default is to return only some attributes, i.e. no detail)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e144-166">-EndTime</span><span class="sxs-lookup"><span data-stu-id="5e144-166">-EndTime</span></span>
<span data-ttu-id="5e144-167">Время окончания запроса</span><span class="sxs-lookup"><span data-stu-id="5e144-167">The endTime of the query</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e144-168">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="5e144-168">-MaxRecord</span></span>
<span data-ttu-id="5e144-169">Максимальное количество записей для выборки.</span><span class="sxs-lookup"><span data-stu-id="5e144-169">The maximum number of records to fetch.</span></span>
<span data-ttu-id="5e144-170">Псевдоним: MaxRecords, MaxEvents</span><span class="sxs-lookup"><span data-stu-id="5e144-170">Alias: MaxRecords, MaxEvents</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e144-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e144-171">-ResourceGroupName</span></span>
<span data-ttu-id="5e144-172">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5e144-172">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e144-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e144-173">-ResourceId</span></span>
<span data-ttu-id="5e144-174">The ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e144-174">The ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e144-175">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5e144-175">-ResourceProvider</span></span>
<span data-ttu-id="5e144-176">Имя ресурса</span><span class="sxs-lookup"><span data-stu-id="5e144-176">The ResourceProvider name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceProvider
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e144-177">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5e144-177">-StartTime</span></span>
<span data-ttu-id="5e144-178">CorrelationId запроса</span><span class="sxs-lookup"><span data-stu-id="5e144-178">The correlationId of the query</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e144-179">-Status</span><span class="sxs-lookup"><span data-stu-id="5e144-179">-Status</span></span>
<span data-ttu-id="5e144-180">Состояние событий, извлекаемого</span><span class="sxs-lookup"><span data-stu-id="5e144-180">The status of the events to fetch</span></span>

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

### <span data-ttu-id="5e144-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e144-181">CommonParameters</span></span>
<span data-ttu-id="5e144-182">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e144-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e144-183">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e144-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e144-184">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e144-184">INPUTS</span></span>

### <span data-ttu-id="5e144-185">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5e144-185">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5e144-186">System.String</span><span class="sxs-lookup"><span data-stu-id="5e144-186">System.String</span></span>

### <span data-ttu-id="5e144-187">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5e144-187">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5e144-188">System.Int32</span><span class="sxs-lookup"><span data-stu-id="5e144-188">System.Int32</span></span>

## <span data-ttu-id="5e144-189">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5e144-189">OUTPUTS</span></span>

### <span data-ttu-id="5e144-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span><span class="sxs-lookup"><span data-stu-id="5e144-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="5e144-191">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5e144-191">NOTES</span></span>

## <span data-ttu-id="5e144-192">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e144-192">RELATED LINKS</span></span>
