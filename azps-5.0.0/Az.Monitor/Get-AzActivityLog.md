---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: 9b57d7584ee7720ec73aa57ddec070ad26ddff9f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248612"
---
# <span data-ttu-id="f585f-101">Get-AzActivityLog</span><span class="sxs-lookup"><span data-stu-id="f585f-101">Get-AzActivityLog</span></span>

## <span data-ttu-id="f585f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f585f-102">SYNOPSIS</span></span>
<span data-ttu-id="f585f-103">Получение событий журнала активности.</span><span class="sxs-lookup"><span data-stu-id="f585f-103">Retrieve Activity Log events.</span></span>

## <span data-ttu-id="f585f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f585f-104">SYNTAX</span></span>

### <span data-ttu-id="f585f-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="f585f-105">GetByCorrelationId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f585f-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f585f-106">GetByResourceId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f585f-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f585f-107">GetByResourceGroup</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f585f-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="f585f-108">GetByResourceProvider</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f585f-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="f585f-109">GetBySubscription</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f585f-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f585f-110">DESCRIPTION</span></span>
<span data-ttu-id="f585f-111">Командлет Get-AzActivityLog извлекает события журнала активности.</span><span class="sxs-lookup"><span data-stu-id="f585f-111">The Get-AzActivityLog cmdlet retrieve Activity Log events.</span></span> <span data-ttu-id="f585f-112">События могут быть связаны с текущим ИДЕНТИФИКАТОРом подписки, ИДЕНТИФИКАТОРом корреляции, группой ресурсов, ИДЕНТИФИКАТОРом ресурса или поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f585f-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="f585f-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f585f-113">EXAMPLES</span></span>

### <span data-ttu-id="f585f-114">Пример 1: получение журнала событий по ИДЕНТИФИКАТОРу подписки</span><span class="sxs-lookup"><span data-stu-id="f585f-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-ActivityAzLog
```

<span data-ttu-id="f585f-115">Эта команда перечисляет максимум 1000 событий, связанных с ИДЕНТИФИКАТОРом подписки пользователя, который занял 7 дней от текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="f585f-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="f585f-116">Пример 2: получение журнала событий по коду подписки с максимальным количеством событий</span><span class="sxs-lookup"><span data-stu-id="f585f-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

<span data-ttu-id="f585f-117">Эта команда перечисляет максимум 100 событий, связанных с ИДЕНТИФИКАТОРом подписки пользователя, который занял 7 дней от текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="f585f-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="f585f-118">Пример 3: получение журнала событий по коду подписки с начальным временем.</span><span class="sxs-lookup"><span data-stu-id="f585f-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="f585f-119">Эта команда выводит максимум 1000 событий, связанных с ИДЕНТИФИКАТОРом подписки пользователя, который выполнялся до или после 2017 г., 01T10:30 местного времени, если дата и время не старше, чем 90 дней от текущих даты и времени.</span><span class="sxs-lookup"><span data-stu-id="f585f-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="f585f-120">Пример 4: получение журнала событий по ИДЕНТИФИКАТОРу подписки с начальным и конечным временем.</span><span class="sxs-lookup"><span data-stu-id="f585f-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="f585f-121">Эта команда выводит максимум 1000 событий, связанных с ИДЕНТИФИКАТОРом подписки пользователя, который выполнялся до или после 2017 г. 01T10:30 местного времени и до 2017 – 04-14T11:30 Местное время, если весь диапазон даты и времени не старше 90 дней с текущей даты и времени, например: срок хранения.</span><span class="sxs-lookup"><span data-stu-id="f585f-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="f585f-122">Пример 5: получение журнала событий по ИДЕНТИФИКАТОРу корреляции</span><span class="sxs-lookup"><span data-stu-id="f585f-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="f585f-123">Эта команда перечисляет не более 1000 событий, связанных с указанным ИДЕНТИФИКАТОРом корреляции, в котором в течение 7 дней с текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="f585f-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="f585f-124">**Примечание**. обычно это одно событие.</span><span class="sxs-lookup"><span data-stu-id="f585f-124">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="f585f-125">Пример 6: получение журнала событий по коду корреляции с максимальным количеством событий</span><span class="sxs-lookup"><span data-stu-id="f585f-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

<span data-ttu-id="f585f-126">Эта команда перечисляет не более 100 событий, связанных с указанным ИДЕНТИФИКАТОРом корреляции, в котором в течение 7 дней с текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="f585f-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="f585f-127">**Примечание**. обычно это одно событие.</span><span class="sxs-lookup"><span data-stu-id="f585f-127">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="f585f-128">Пример 7: получение журнала событий по коду корреляции и времени начала</span><span class="sxs-lookup"><span data-stu-id="f585f-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="f585f-129">Эта команда перечисляет не более 1000 событий, связанных с указанным ИДЕНТИФИКАТОРом корреляции, который выполнялся в течение или после 2017 г., 22T04:30:00 местного времени, если время начала не более 90 дня от текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="f585f-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="f585f-130">**Примечание**. обычно это одно событие.</span><span class="sxs-lookup"><span data-stu-id="f585f-130">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="f585f-131">Пример 8: получение журнала событий по ИДЕНТИФИКАТОРу корреляции с начальным и конечным временем</span><span class="sxs-lookup"><span data-stu-id="f585f-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="f585f-132">Эта команда перечисляет максимум 1000 событий, связанных с указанным ИДЕНТИФИКАТОРом корреляции, который выполнялся в течение или после 2017 г. 15T04:30 местного времени, но до 2017 – 04-25T12:30 Местное время, если весь диапазон даты и времени не старше 90 дней с текущей даты и времени, т.е.: срок хранения.</span><span class="sxs-lookup"><span data-stu-id="f585f-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="f585f-133">Пример 9: получение журнала событий для группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f585f-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="f585f-134">В этой команде перечислены не более 1000 событий, связанных с указанной группой ресурсов, для которых на текущий момент Дата и время проходило 7 дней.</span><span class="sxs-lookup"><span data-stu-id="f585f-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="f585f-135">Пример 10: получение журнала событий для группы ресурсов с максимальным количеством событий</span><span class="sxs-lookup"><span data-stu-id="f585f-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

<span data-ttu-id="f585f-136">Эта команда включает в себя максимум 100 событий, связанных с указанной группой ресурсов, в которой в течение 7 дней с текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="f585f-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="f585f-137">Пример 11: получение журнала событий для группы ресурсов по времени начала</span><span class="sxs-lookup"><span data-stu-id="f585f-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="f585f-138">Эта команда выводит максимум 1000 событий, связанных с указанной группой ресурсов, которая выполнялась в течение или после 2017 г., в 22T04:30:00. местного времени, если время начала не более 90 дня от текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="f585f-138">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="f585f-139">Пример 12: получение журнала событий для группы ресурсов с временем начала и окончания</span><span class="sxs-lookup"><span data-stu-id="f585f-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="f585f-140">Эта команда перечисляет максимум 1000 событий, связанных с указанной группой ресурсов, которая выполнялась в течение или после 2017 г. 15T04:30 местного времени, но до 2017 – 04-25T12:30 Местное время, если весь диапазон даты и времени не старше 90 дней с текущей даты и времени, например: срок хранения.</span><span class="sxs-lookup"><span data-stu-id="f585f-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="f585f-141">Пример 13: получение журнала событий по ИДЕНТИФИКАТОРу ресурса</span><span class="sxs-lookup"><span data-stu-id="f585f-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="f585f-142">Эта команда перечисляет не более 1000 событий, связанных с указанным ИДЕНТИФИКАТОРом ресурса, в течение 7 дней с текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="f585f-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="f585f-143">Пример 14: получение журнала событий по ИДЕНТИФИКАТОРу ресурса с максимальным количеством событий</span><span class="sxs-lookup"><span data-stu-id="f585f-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

<span data-ttu-id="f585f-144">Эта команда перечисляет не более 100 событий, связанных с указанным ИДЕНТИФИКАТОРом ресурса, в течение 7 дней с текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="f585f-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="f585f-145">Пример 15: получение журнала событий по ИДЕНТИФИКАТОРу ресурса с начальным временем</span><span class="sxs-lookup"><span data-stu-id="f585f-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="f585f-146">Эта команда выводит максимум 1000 событий, связанных с указанным ИДЕНТИФИКАТОРом ресурса, который выполнялся в течение или после 2017 г., в 22T04:30:00. Местное время, если время начала не более 90 дня от текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="f585f-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="f585f-147">Пример 16: получение журнала событий по ИДЕНТИФИКАТОРу ресурса с начальным и конечным временем</span><span class="sxs-lookup"><span data-stu-id="f585f-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="f585f-148">Эта команда выводит максимум 1000 событий, связанных с указанным ИДЕНТИФИКАТОРом ресурса, который выполнялся или после 2017 – 04-15T04:30 местного времени, но до 2017 – 04-25T12:30 Местное время, если весь диапазон даты и времени не старше 90 дней с текущей даты и времени, т.е.: срок хранения.</span><span class="sxs-lookup"><span data-stu-id="f585f-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="f585f-149">Пример 17: получение журнала событий по поставщику ресурсов</span><span class="sxs-lookup"><span data-stu-id="f585f-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="f585f-150">Эта команда выводит не более 1000 событий, связанных с указанным поставщиком ресурсов, для которых на текущий момент Дата и время проходило 7 дней.</span><span class="sxs-lookup"><span data-stu-id="f585f-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="f585f-151">Пример 18: получение журнала событий поставщиком ресурсов с максимальным количеством событий</span><span class="sxs-lookup"><span data-stu-id="f585f-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

<span data-ttu-id="f585f-152">Эта команда выводит не более 100 событий, связанных с указанным поставщиком ресурсов, для которых на текущий момент Дата и время проходило 7 дней.</span><span class="sxs-lookup"><span data-stu-id="f585f-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="f585f-153">Пример 19: получение журнала событий по поставщику ресурсов с начальным временем</span><span class="sxs-lookup"><span data-stu-id="f585f-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="f585f-154">Эта команда выводит максимум 1000 событий, связанных с указанным поставщиком ресурсов, который выполнялся в течение или после 2017 г., 22T04:30:00. Местное время, если время начала не более 90 дня от текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="f585f-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="f585f-155">Пример 20: получение журнала событий по поставщику ресурсов с начальным и конечным временем</span><span class="sxs-lookup"><span data-stu-id="f585f-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="f585f-156">Эта команда перечисляет максимум 1000 событий, связанных с указанным поставщиком ресурсов, который выполнялся в течение или после 2017 г. 15T04:30 местного времени, но до 2017 – 04-25T12:30 Местное время, если весь диапазон даты и времени не старше 90 дней с текущей даты и времени, т.е.: срок хранения.</span><span class="sxs-lookup"><span data-stu-id="f585f-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="f585f-157">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f585f-157">PARAMETERS</span></span>

### <span data-ttu-id="f585f-158">-Вызывающий абонент</span><span class="sxs-lookup"><span data-stu-id="f585f-158">-Caller</span></span>
<span data-ttu-id="f585f-159">Вызывающий объект события для получения</span><span class="sxs-lookup"><span data-stu-id="f585f-159">The caller of the events to fetch</span></span>

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

### <span data-ttu-id="f585f-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="f585f-160">-CorrelationId</span></span>
<span data-ttu-id="f585f-161">Значение CorrelationId</span><span class="sxs-lookup"><span data-stu-id="f585f-161">The CorrelationId</span></span>

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

### <span data-ttu-id="f585f-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f585f-162">-DefaultProfile</span></span>
<span data-ttu-id="f585f-163">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f585f-163">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f585f-164">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="f585f-164">-DetailedOutput</span></span>
<span data-ttu-id="f585f-165">Возвращает объект со всеми подробностями событий (значение по умолчанию — возврат только некоторых атрибутов, т. е. не подробных данных).</span><span class="sxs-lookup"><span data-stu-id="f585f-165">Return object with all the details of the events (the default is to return only some attributes, i.e. no detail)</span></span>

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

### <span data-ttu-id="f585f-166">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f585f-166">-EndTime</span></span>
<span data-ttu-id="f585f-167">Значение endTime запроса</span><span class="sxs-lookup"><span data-stu-id="f585f-167">The endTime of the query</span></span>

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

### <span data-ttu-id="f585f-168">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="f585f-168">-MaxRecord</span></span>
<span data-ttu-id="f585f-169">Максимальное количество записей, которые нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="f585f-169">The maximum number of records to fetch.</span></span>
<span data-ttu-id="f585f-170">Alias (псевдоним): MaxRecords; MaxEvents</span><span class="sxs-lookup"><span data-stu-id="f585f-170">Alias: MaxRecords, MaxEvents</span></span>

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

### <span data-ttu-id="f585f-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f585f-171">-ResourceGroupName</span></span>
<span data-ttu-id="f585f-172">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f585f-172">The resource group name</span></span>

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

### <span data-ttu-id="f585f-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f585f-173">-ResourceId</span></span>
<span data-ttu-id="f585f-174">ResourceId (ИД ресурса)</span><span class="sxs-lookup"><span data-stu-id="f585f-174">The ResourceId</span></span>

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

### <span data-ttu-id="f585f-175">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="f585f-175">-ResourceProvider</span></span>
<span data-ttu-id="f585f-176">Имя ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="f585f-176">The ResourceProvider name</span></span>

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

### <span data-ttu-id="f585f-177">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f585f-177">-StartTime</span></span>
<span data-ttu-id="f585f-178">Значение correlationId запроса</span><span class="sxs-lookup"><span data-stu-id="f585f-178">The correlationId of the query</span></span>

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

### <span data-ttu-id="f585f-179">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="f585f-179">-Status</span></span>
<span data-ttu-id="f585f-180">Состояние событий для выборки</span><span class="sxs-lookup"><span data-stu-id="f585f-180">The status of the events to fetch</span></span>

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

### <span data-ttu-id="f585f-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f585f-181">CommonParameters</span></span>
<span data-ttu-id="f585f-182">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f585f-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f585f-183">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f585f-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f585f-184">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f585f-184">INPUTS</span></span>

### <span data-ttu-id="f585f-185">System. Nullable "1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f585f-185">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f585f-186">System. String</span><span class="sxs-lookup"><span data-stu-id="f585f-186">System.String</span></span>

### <span data-ttu-id="f585f-187">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f585f-187">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f585f-188">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f585f-188">System.Int32</span></span>

## <span data-ttu-id="f585f-189">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f585f-189">OUTPUTS</span></span>

### <span data-ttu-id="f585f-190">Microsoft. Azure. Commands. Insights. OutputClasses. PSEventData</span><span class="sxs-lookup"><span data-stu-id="f585f-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="f585f-191">Пуск</span><span class="sxs-lookup"><span data-stu-id="f585f-191">NOTES</span></span>

## <span data-ttu-id="f585f-192">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f585f-192">RELATED LINKS</span></span>
