---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2B9FEEDB-09AA-40B6-B42C-F9090F54EB3B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerservicebustopicjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusTopicJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusTopicJob.md
ms.openlocfilehash: ecd801cff6a6cc67a4187e7f89b26e8b5edb3784
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566121"
---
# <span data-ttu-id="c3969-101">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="c3969-101">New-AzureRmSchedulerServiceBusTopicJob</span></span>

## <span data-ttu-id="c3969-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c3969-102">SYNOPSIS</span></span>
<span data-ttu-id="c3969-103">Создание раздела служебной шины.</span><span class="sxs-lookup"><span data-stu-id="c3969-103">Creates a service bus topic job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3969-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c3969-104">SYNTAX</span></span>

```
New-AzureRmSchedulerServiceBusTopicJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusTopicPath <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3969-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3969-105">DESCRIPTION</span></span>
<span data-ttu-id="c3969-106">Командлет **New-AzureRmSchedulerServiceBusTopicJob** создает раздел служебной шины в планировщике Azure.</span><span class="sxs-lookup"><span data-stu-id="c3969-106">The **New-AzureRmSchedulerServiceBusTopicJob** cmdlet creates a service bus topic job in Azure Scheduler.</span></span>

<span data-ttu-id="c3969-107">Этот командлет поддерживает динамические параметры, основанные на параметре *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="c3969-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="c3969-108">Динамические параметры становятся доступны в соответствии с другими значениями параметров.</span><span class="sxs-lookup"><span data-stu-id="c3969-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="c3969-109">Чтобы найти имена динамических параметров после указания других параметров, введите дефис (-), а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="c3969-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c3969-110">Если вы не пропустите требуемый параметр, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="c3969-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c3969-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c3969-111">EXAMPLES</span></span>

## <span data-ttu-id="c3969-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c3969-112">PARAMETERS</span></span>

### <span data-ttu-id="c3969-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3969-113">-DefaultProfile</span></span>
<span data-ttu-id="c3969-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c3969-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3969-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c3969-115">-EndTime</span></span>
<span data-ttu-id="c3969-116">Задает время окончания для задания в виде объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="c3969-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="c3969-117">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="c3969-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3969-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="c3969-118">-ErrorActionType</span></span>
<span data-ttu-id="c3969-119">Задает параметр действия при ошибке для задания.</span><span class="sxs-lookup"><span data-stu-id="c3969-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="c3969-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c3969-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c3969-121">Через</span><span class="sxs-lookup"><span data-stu-id="c3969-121">Http</span></span> 
- <span data-ttu-id="c3969-122">Протокол</span><span class="sxs-lookup"><span data-stu-id="c3969-122">Https</span></span> 
- <span data-ttu-id="c3969-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="c3969-123">StorageQueue</span></span> 
- <span data-ttu-id="c3969-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="c3969-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="c3969-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="c3969-125">ServiceBusTopic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https, StorageQueue, ServiceBusQueue, ServiceBusTopic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3969-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="c3969-126">-ExecutionCount</span></span>
<span data-ttu-id="c3969-127">Задает количество выполняемых заданий.</span><span class="sxs-lookup"><span data-stu-id="c3969-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="c3969-128">По умолчанию задание повторяется неопределенное время.</span><span class="sxs-lookup"><span data-stu-id="c3969-128">By default, a job recurs indefinitely.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3969-129">-Частота</span><span class="sxs-lookup"><span data-stu-id="c3969-129">-Frequency</span></span>
<span data-ttu-id="c3969-130">Задает максимальную частоту для задания.</span><span class="sxs-lookup"><span data-stu-id="c3969-130">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="c3969-131">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c3969-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c3969-132">До</span><span class="sxs-lookup"><span data-stu-id="c3969-132">Minute</span></span> 
- <span data-ttu-id="c3969-133">Часовой</span><span class="sxs-lookup"><span data-stu-id="c3969-133">Hour</span></span> 
- <span data-ttu-id="c3969-134">Дневных</span><span class="sxs-lookup"><span data-stu-id="c3969-134">Day</span></span> 
- <span data-ttu-id="c3969-135">Недели</span><span class="sxs-lookup"><span data-stu-id="c3969-135">Week</span></span> 
- <span data-ttu-id="c3969-136">Перехода</span><span class="sxs-lookup"><span data-stu-id="c3969-136">Month</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3969-137">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="c3969-137">-Interval</span></span>
<span data-ttu-id="c3969-138">Указывает интервал повторения для задания.</span><span class="sxs-lookup"><span data-stu-id="c3969-138">Specifies an interval of recurrence for the job.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3969-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="c3969-139">-JobCollectionName</span></span>
<span data-ttu-id="c3969-140">Указывает имя коллекции заданий, к которой относится задание.</span><span class="sxs-lookup"><span data-stu-id="c3969-140">Specifies the name of the job collection to which the job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3969-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="c3969-141">-JobName</span></span>
<span data-ttu-id="c3969-142">Задает имя задания.</span><span class="sxs-lookup"><span data-stu-id="c3969-142">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="c3969-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="c3969-143">-JobState</span></span>
<span data-ttu-id="c3969-144">Указывает состояние задания.</span><span class="sxs-lookup"><span data-stu-id="c3969-144">Specifies the state of the job.</span></span>
<span data-ttu-id="c3969-145">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c3969-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c3969-146">Включаем</span><span class="sxs-lookup"><span data-stu-id="c3969-146">Enabled</span></span> 
- <span data-ttu-id="c3969-147">Отключает</span><span class="sxs-lookup"><span data-stu-id="c3969-147">Disabled</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3969-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3969-148">-ResourceGroupName</span></span>
<span data-ttu-id="c3969-149">Указывает группу ресурсов, к которой относится задание.</span><span class="sxs-lookup"><span data-stu-id="c3969-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="c3969-150">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="c3969-150">-ServiceBusMessage</span></span>
<span data-ttu-id="c3969-151">Указывает сообщение о теме служебной шины.</span><span class="sxs-lookup"><span data-stu-id="c3969-151">Specifies a service bus topic message.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3969-152">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="c3969-152">-ServiceBusNamespace</span></span>
<span data-ttu-id="c3969-153">Задает пространство имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="c3969-153">Specifies a service bus namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3969-154">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="c3969-154">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="c3969-155">Задает имя ключа подписи для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="c3969-155">Specifies a shared access signature key name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3969-156">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="c3969-156">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="c3969-157">Задает значение ключа подписи для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="c3969-157">Specifies a shared access signature key value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3969-158">-ServiceBusTopicPath</span><span class="sxs-lookup"><span data-stu-id="c3969-158">-ServiceBusTopicPath</span></span>
<span data-ttu-id="c3969-159">Указывает путь к разделу служебной шины.</span><span class="sxs-lookup"><span data-stu-id="c3969-159">Specifies a service bus topic path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3969-160">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="c3969-160">-ServiceBusTransportType</span></span>
<span data-ttu-id="c3969-161">Указывает тип транспорта служебной шины.</span><span class="sxs-lookup"><span data-stu-id="c3969-161">Specifies a service bus transport type.</span></span>
<span data-ttu-id="c3969-162">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c3969-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c3969-163">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="c3969-163">NetMessaging</span></span>
- <span data-ttu-id="c3969-164">AMQP</span><span class="sxs-lookup"><span data-stu-id="c3969-164">AMQP</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NetMessaging, AMQP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3969-165">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c3969-165">-StartTime</span></span>
<span data-ttu-id="c3969-166">Задает время начала в виде объекта **DateTime** для задания.</span><span class="sxs-lookup"><span data-stu-id="c3969-166">Specifies the start time, as a **DateTime** object, for the job.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3969-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3969-167">-Confirm</span></span>
<span data-ttu-id="c3969-168">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c3969-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3969-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3969-169">-WhatIf</span></span>
<span data-ttu-id="c3969-170">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c3969-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3969-171">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c3969-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3969-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3969-172">CommonParameters</span></span>
<span data-ttu-id="c3969-173">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c3969-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3969-174">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3969-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3969-175">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c3969-175">INPUTS</span></span>

### <span data-ttu-id="c3969-176">Ничего</span><span class="sxs-lookup"><span data-stu-id="c3969-176">None</span></span>
<span data-ttu-id="c3969-177">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c3969-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c3969-178">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3969-178">OUTPUTS</span></span>

### <span data-ttu-id="c3969-179">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="c3969-179">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="c3969-180">Пуск</span><span class="sxs-lookup"><span data-stu-id="c3969-180">NOTES</span></span>

## <span data-ttu-id="c3969-181">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c3969-181">RELATED LINKS</span></span>

[<span data-ttu-id="c3969-182">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="c3969-182">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="c3969-183">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c3969-183">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="c3969-184">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="c3969-184">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="c3969-185">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="c3969-185">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="c3969-186">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="c3969-186">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="c3969-187">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c3969-187">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="c3969-188">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="c3969-188">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="c3969-189">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="c3969-189">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="c3969-190">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="c3969-190">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


