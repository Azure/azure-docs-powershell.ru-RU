---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzLog.md
ms.openlocfilehash: f6000574313942c774c9243d9a4d4a42caa28820
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910247"
---
# <span data-ttu-id="b2a35-101">Get-AzLog</span><span class="sxs-lookup"><span data-stu-id="b2a35-101">Get-AzLog</span></span>

## <span data-ttu-id="b2a35-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b2a35-102">SYNOPSIS</span></span>
<span data-ttu-id="b2a35-103">Получение событий журнала активности.</span><span class="sxs-lookup"><span data-stu-id="b2a35-103">Retrieve Activity Log events.</span></span>

## <span data-ttu-id="b2a35-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b2a35-104">SYNTAX</span></span>

### <span data-ttu-id="b2a35-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="b2a35-105">GetByCorrelationId</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2a35-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b2a35-106">GetByResourceId</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2a35-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b2a35-107">GetByResourceGroup</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceGroupName] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2a35-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="b2a35-108">GetByResourceProvider</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2a35-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="b2a35-109">GetBySubscription</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2a35-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2a35-110">DESCRIPTION</span></span>
<span data-ttu-id="b2a35-111">Командлет **Get-AzLog** извлекает события журнала активности.</span><span class="sxs-lookup"><span data-stu-id="b2a35-111">The **Get-AzLog** cmdlet retrieve Activity Log events.</span></span>
<span data-ttu-id="b2a35-112">События могут быть связаны с текущим ИДЕНТИФИКАТОРом подписки, ИДЕНТИФИКАТОРом корреляции, группой ресурсов, ИДЕНТИФИКАТОРом ресурса или поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b2a35-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="b2a35-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b2a35-113">EXAMPLES</span></span>

### <span data-ttu-id="b2a35-114">Пример 1: получение журнала событий по ИДЕНТИФИКАТОРу подписки</span><span class="sxs-lookup"><span data-stu-id="b2a35-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-AzLog
```

<span data-ttu-id="b2a35-115">Эта команда перечисляет максимум 1000 событий, связанных с ИДЕНТИФИКАТОРом подписки пользователя, который занял 7 дней от текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="b2a35-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="b2a35-116">Пример 2: получение журнала событий по коду подписки с максимальным количеством событий</span><span class="sxs-lookup"><span data-stu-id="b2a35-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -MaxRecord 100
```

<span data-ttu-id="b2a35-117">Эта команда перечисляет максимум 100 событий, связанных с ИДЕНТИФИКАТОРом подписки пользователя, который занял 7 дней от текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="b2a35-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="b2a35-118">Пример 3: получение журнала событий по коду подписки с начальным временем.</span><span class="sxs-lookup"><span data-stu-id="b2a35-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="b2a35-119">Эта команда выводит максимум 1000 событий, связанных с ИДЕНТИФИКАТОРом подписки пользователя, который выполнялся до или после 2017 г., 01T10:30 местного времени, если дата и время не старше, чем 90 дней от текущих даты и времени.</span><span class="sxs-lookup"><span data-stu-id="b2a35-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="b2a35-120">Пример 4: получение журнала событий по ИДЕНТИФИКАТОРу подписки с начальным и конечным временем.</span><span class="sxs-lookup"><span data-stu-id="b2a35-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="b2a35-121">Эта команда выводит максимум 1000 событий, связанных с ИДЕНТИФИКАТОРом подписки пользователя, который выполнялся до или после 2017 г. 01T10:30 местного времени и до 2017 – 04-14T11:30 Местное время, если весь диапазон даты и времени не старше 90 дней с текущей даты и времени, например: срок хранения.</span><span class="sxs-lookup"><span data-stu-id="b2a35-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="b2a35-122">Пример 5: получение журнала событий по ИДЕНТИФИКАТОРу корреляции</span><span class="sxs-lookup"><span data-stu-id="b2a35-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="b2a35-123">Эта команда перечисляет не более 1000 событий, связанных с указанным ИДЕНТИФИКАТОРом корреляции, в котором в течение 7 дней с текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="b2a35-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="b2a35-124">**Примечание**. обычно это одно событие.</span><span class="sxs-lookup"><span data-stu-id="b2a35-124">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="b2a35-125">Пример 6: получение журнала событий по коду корреляции с максимальным количеством событий</span><span class="sxs-lookup"><span data-stu-id="b2a35-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

<span data-ttu-id="b2a35-126">Эта команда перечисляет не более 100 событий, связанных с указанным ИДЕНТИФИКАТОРом корреляции, в котором в течение 7 дней с текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="b2a35-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="b2a35-127">**Примечание**. обычно это одно событие.</span><span class="sxs-lookup"><span data-stu-id="b2a35-127">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="b2a35-128">Пример 7: получение журнала событий по коду корреляции и времени начала</span><span class="sxs-lookup"><span data-stu-id="b2a35-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="b2a35-129">Эта команда перечисляет не более 1000 событий, связанных с указанным ИДЕНТИФИКАТОРом корреляции, который выполнялся в течение или после 2017 г., 22T04:30:00 местного времени, если время начала не более 90 дня от текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="b2a35-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="b2a35-130">**Примечание**. обычно это одно событие.</span><span class="sxs-lookup"><span data-stu-id="b2a35-130">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="b2a35-131">Пример 8: получение журнала событий по ИДЕНТИФИКАТОРу корреляции с начальным и конечным временем</span><span class="sxs-lookup"><span data-stu-id="b2a35-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="b2a35-132">Эта команда перечисляет максимум 1000 событий, связанных с указанным ИДЕНТИФИКАТОРом корреляции, который выполнялся в течение или после 2017 г. 15T04:30 местного времени, но до 2017 – 04-25T12:30 Местное время, если весь диапазон даты и времени не старше 90 дней с текущей даты и времени, т.е.: срок хранения.</span><span class="sxs-lookup"><span data-stu-id="b2a35-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="b2a35-133">Пример 9: получение журнала событий для группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b2a35-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="b2a35-134">В этой команде перечислены не более 1000 событий, связанных с указанной группой ресурсов, для которых на текущий момент Дата и время проходило 7 дней.</span><span class="sxs-lookup"><span data-stu-id="b2a35-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="b2a35-135">Пример 10: получение журнала событий для группы ресурсов с максимальным количеством событий</span><span class="sxs-lookup"><span data-stu-id="b2a35-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

<span data-ttu-id="b2a35-136">Эта команда включает в себя максимум 100 событий, связанных с указанной группой ресурсов, в которой в течение 7 дней с текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="b2a35-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="b2a35-137">Пример 11: получение журнала событий для группы ресурсов по времени начала</span><span class="sxs-lookup"><span data-stu-id="b2a35-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="b2a35-138">Эта команда выводит максимум 1000 событий, связанных с указанной группой ресурсов, которая выполнялась в течение или после 2017 г., в 22T04:30:00. местного времени, если время начала не более 90 дня от текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="b2a35-138">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="b2a35-139">Пример 12: получение журнала событий для группы ресурсов с временем начала и окончания</span><span class="sxs-lookup"><span data-stu-id="b2a35-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="b2a35-140">Эта команда перечисляет максимум 1000 событий, связанных с указанной группой ресурсов, которая выполнялась в течение или после 2017 г. 15T04:30 местного времени, но до 2017 – 04-25T12:30 Местное время, если весь диапазон даты и времени не старше 90 дней с текущей даты и времени, например: срок хранения.</span><span class="sxs-lookup"><span data-stu-id="b2a35-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="b2a35-141">Пример 13: получение журнала событий по ИДЕНТИФИКАТОРу ресурса</span><span class="sxs-lookup"><span data-stu-id="b2a35-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="b2a35-142">Эта команда перечисляет не более 1000 событий, связанных с указанным ИДЕНТИФИКАТОРом ресурса, в течение 7 дней с текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="b2a35-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="b2a35-143">Пример 14: получение журнала событий по ИДЕНТИФИКАТОРу ресурса с максимальным количеством событий</span><span class="sxs-lookup"><span data-stu-id="b2a35-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

<span data-ttu-id="b2a35-144">Эта команда перечисляет не более 100 событий, связанных с указанным ИДЕНТИФИКАТОРом ресурса, в течение 7 дней с текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="b2a35-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="b2a35-145">Пример 15: получение журнала событий по ИДЕНТИФИКАТОРу ресурса с начальным временем</span><span class="sxs-lookup"><span data-stu-id="b2a35-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="b2a35-146">Эта команда выводит максимум 1000 событий, связанных с указанным ИДЕНТИФИКАТОРом ресурса, который выполнялся в течение или после 2017 г., в 22T04:30:00. Местное время, если время начала не более 90 дня от текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="b2a35-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="b2a35-147">Пример 16: получение журнала событий по ИДЕНТИФИКАТОРу ресурса с начальным и конечным временем</span><span class="sxs-lookup"><span data-stu-id="b2a35-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="b2a35-148">Эта команда выводит максимум 1000 событий, связанных с указанным ИДЕНТИФИКАТОРом ресурса, который выполнялся или после 2017 – 04-15T04:30 местного времени, но до 2017 – 04-25T12:30 Местное время, если весь диапазон даты и времени не старше 90 дней с текущей даты и времени, т.е.: срок хранения.</span><span class="sxs-lookup"><span data-stu-id="b2a35-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="b2a35-149">Пример 17: получение журнала событий по поставщику ресурсов</span><span class="sxs-lookup"><span data-stu-id="b2a35-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="b2a35-150">Эта команда выводит не более 1000 событий, связанных с указанным поставщиком ресурсов, для которых на текущий момент Дата и время проходило 7 дней.</span><span class="sxs-lookup"><span data-stu-id="b2a35-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="b2a35-151">Пример 18: получение журнала событий поставщиком ресурсов с максимальным количеством событий</span><span class="sxs-lookup"><span data-stu-id="b2a35-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

<span data-ttu-id="b2a35-152">Эта команда выводит не более 100 событий, связанных с указанным поставщиком ресурсов, для которых на текущий момент Дата и время проходило 7 дней.</span><span class="sxs-lookup"><span data-stu-id="b2a35-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="b2a35-153">Пример 19: получение журнала событий по поставщику ресурсов с начальным временем</span><span class="sxs-lookup"><span data-stu-id="b2a35-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="b2a35-154">Эта команда выводит максимум 1000 событий, связанных с указанным поставщиком ресурсов, который выполнялся в течение или после 2017 г., 22T04:30:00. Местное время, если время начала не более 90 дня от текущей даты и времени.</span><span class="sxs-lookup"><span data-stu-id="b2a35-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="b2a35-155">Пример 20: получение журнала событий по поставщику ресурсов с начальным и конечным временем</span><span class="sxs-lookup"><span data-stu-id="b2a35-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="b2a35-156">Эта команда перечисляет максимум 1000 событий, связанных с указанным поставщиком ресурсов, который выполнялся в течение или после 2017 г. 15T04:30 местного времени, но до 2017 – 04-25T12:30 Местное время, если весь диапазон даты и времени не старше 90 дней с текущей даты и времени, т.е.: срок хранения.</span><span class="sxs-lookup"><span data-stu-id="b2a35-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="b2a35-157">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b2a35-157">PARAMETERS</span></span>

### <span data-ttu-id="b2a35-158">-Вызывающий абонент</span><span class="sxs-lookup"><span data-stu-id="b2a35-158">-Caller</span></span>
<span data-ttu-id="b2a35-159">Задает вызывающий абонент.</span><span class="sxs-lookup"><span data-stu-id="b2a35-159">Specifies a caller.</span></span>

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

### <span data-ttu-id="b2a35-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="b2a35-160">-CorrelationId</span></span>
<span data-ttu-id="b2a35-161">Указывает идентификатор корреляции.</span><span class="sxs-lookup"><span data-stu-id="b2a35-161">Specifies the correlation ID.</span></span>
<span data-ttu-id="b2a35-162">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="b2a35-162">This parameter is required.</span></span>

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

### <span data-ttu-id="b2a35-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2a35-163">-DefaultProfile</span></span>
<span data-ttu-id="b2a35-164">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b2a35-164">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2a35-165">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="b2a35-165">-DetailedOutput</span></span>
<span data-ttu-id="b2a35-166">Указывает на то, что этот командлет отображает подробный вывод.</span><span class="sxs-lookup"><span data-stu-id="b2a35-166">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="b2a35-167">По умолчанию выводятся итоги.</span><span class="sxs-lookup"><span data-stu-id="b2a35-167">By default, output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Switch not present = False, i.e. output summarized
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2a35-168">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b2a35-168">-EndTime</span></span>
<span data-ttu-id="b2a35-169">Указывает время окончания запроса в местном времени.</span><span class="sxs-lookup"><span data-stu-id="b2a35-169">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="b2a35-170">Значение по умолчанию — текущее время.</span><span class="sxs-lookup"><span data-stu-id="b2a35-170">The default value is the current time.</span></span>
<span data-ttu-id="b2a35-171">Значение должно быть позже, чем *StartTime*.</span><span class="sxs-lookup"><span data-stu-id="b2a35-171">The value must be later than *StartTime*.</span></span>
<span data-ttu-id="b2a35-172">Вы можете использовать командлет Get-Date для получения объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="b2a35-172">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Current date (time: 00:00:00 AM) + 1 day
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2a35-173">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="b2a35-173">-MaxRecord</span></span>
<span data-ttu-id="b2a35-174">Указывает общее количество записей, которые нужно получить для указанного фильтра.</span><span class="sxs-lookup"><span data-stu-id="b2a35-174">Specifies the total number of records to fetch for the specified filter.</span></span>
<span data-ttu-id="b2a35-175">Значением по умолчанию является 1000, а максимальное допустимое значение — 100000.</span><span class="sxs-lookup"><span data-stu-id="b2a35-175">The default value is 1000 and the maximum value accepted is 100000.</span></span> <span data-ttu-id="b2a35-176">Отрицательные и нулевые значения будут игнорироваться, и будет использоваться значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b2a35-176">Negative values and 0 are ignored and the default value will be used.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1000
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2a35-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2a35-177">-ResourceGroupName</span></span>
<span data-ttu-id="b2a35-178">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b2a35-178">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b2a35-179">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2a35-179">-ResourceId</span></span>
<span data-ttu-id="b2a35-180">Указывает идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="b2a35-180">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="b2a35-181">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="b2a35-181">-ResourceProvider</span></span>
<span data-ttu-id="b2a35-182">Задает фильтр по поставщику ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b2a35-182">Specifies a filter by resource provider.</span></span>

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

### <span data-ttu-id="b2a35-183">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b2a35-183">-StartTime</span></span>
<span data-ttu-id="b2a35-184">Задает время начала запроса в местном времени.</span><span class="sxs-lookup"><span data-stu-id="b2a35-184">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="b2a35-185">Значение по умолчанию — *EndTime* , минус семь дней.</span><span class="sxs-lookup"><span data-stu-id="b2a35-185">The default value is *EndTime* minus seven days.</span></span>
<span data-ttu-id="b2a35-186">Вы можете использовать командлет Get-Date для получения объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="b2a35-186">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: EndTime - 7 days
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2a35-187">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="b2a35-187">-Status</span></span>
<span data-ttu-id="b2a35-188">Указывает состояние.</span><span class="sxs-lookup"><span data-stu-id="b2a35-188">Specifies the status.</span></span>

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

### <span data-ttu-id="b2a35-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2a35-189">CommonParameters</span></span>
<span data-ttu-id="b2a35-190">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b2a35-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2a35-191">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2a35-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2a35-192">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b2a35-192">INPUTS</span></span>

### <span data-ttu-id="b2a35-193">System. Nullable "1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b2a35-193">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b2a35-194">System. String</span><span class="sxs-lookup"><span data-stu-id="b2a35-194">System.String</span></span>

### <span data-ttu-id="b2a35-195">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b2a35-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="b2a35-196">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b2a35-196">System.Int32</span></span>

## <span data-ttu-id="b2a35-197">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2a35-197">OUTPUTS</span></span>

### <span data-ttu-id="b2a35-198">Microsoft. Azure. Commands. Insights. OutputClasses. PSEventData</span><span class="sxs-lookup"><span data-stu-id="b2a35-198">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="b2a35-199">Пуск</span><span class="sxs-lookup"><span data-stu-id="b2a35-199">NOTES</span></span>

## <span data-ttu-id="b2a35-200">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2a35-200">RELATED LINKS</span></span>
