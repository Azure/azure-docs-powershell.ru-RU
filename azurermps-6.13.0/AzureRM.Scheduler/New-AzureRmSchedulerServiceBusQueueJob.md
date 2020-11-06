---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 52987702-D101-4D5D-852D-2809374292F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerservicebusqueuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
ms.openlocfilehash: 0382362c16ba65aa194029677cf8ca846e93db54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558292"
---
# <span data-ttu-id="77fe5-101">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="77fe5-101">New-AzureRmSchedulerServiceBusQueueJob</span></span>

## <span data-ttu-id="77fe5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="77fe5-103">Создание задания очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="77fe5-103">Creates a service bus queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77fe5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77fe5-104">SYNTAX</span></span>

```
New-AzureRmSchedulerServiceBusQueueJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusQueueName <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77fe5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77fe5-105">DESCRIPTION</span></span>
<span data-ttu-id="77fe5-106">Командлет **New-AzureRmSchedulerServiceBusQueueJob** создает задание в очереди служебной шины в планировщике Azure.</span><span class="sxs-lookup"><span data-stu-id="77fe5-106">The **New-AzureRmSchedulerServiceBusQueueJob** cmdlet creates a service bus queue job in Azure Scheduler.</span></span>
<span data-ttu-id="77fe5-107">Этот командлет поддерживает динамические параметры, основанные на параметре *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="77fe5-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="77fe5-108">Динамические параметры становятся доступны в соответствии с другими значениями параметров.</span><span class="sxs-lookup"><span data-stu-id="77fe5-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="77fe5-109">Чтобы найти имена динамических параметров после указания других параметров, введите дефис (-), а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="77fe5-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="77fe5-110">Если вы не пропустите требуемый параметр, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="77fe5-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="77fe5-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77fe5-111">EXAMPLES</span></span>

## <span data-ttu-id="77fe5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77fe5-112">PARAMETERS</span></span>

### <span data-ttu-id="77fe5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77fe5-113">-DefaultProfile</span></span>
<span data-ttu-id="77fe5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="77fe5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77fe5-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="77fe5-115">-EndTime</span></span>
<span data-ttu-id="77fe5-116">Задает время окончания для задания в виде объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="77fe5-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="77fe5-117">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="77fe5-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77fe5-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="77fe5-118">-ErrorActionType</span></span>
<span data-ttu-id="77fe5-119">Задает параметр действия при ошибке для задания.</span><span class="sxs-lookup"><span data-stu-id="77fe5-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="77fe5-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="77fe5-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="77fe5-121">Через</span><span class="sxs-lookup"><span data-stu-id="77fe5-121">Http</span></span> 
- <span data-ttu-id="77fe5-122">Протокол</span><span class="sxs-lookup"><span data-stu-id="77fe5-122">Https</span></span> 
- <span data-ttu-id="77fe5-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="77fe5-123">StorageQueue</span></span> 
- <span data-ttu-id="77fe5-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="77fe5-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="77fe5-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="77fe5-125">ServiceBusTopic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https, StorageQueue, ServiceBusQueue, ServiceBusTopic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77fe5-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="77fe5-126">-ExecutionCount</span></span>
<span data-ttu-id="77fe5-127">Задает количество выполняемых заданий.</span><span class="sxs-lookup"><span data-stu-id="77fe5-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="77fe5-128">По умолчанию задание повторяется неопределенное время.</span><span class="sxs-lookup"><span data-stu-id="77fe5-128">By default, a job recurs indefinitely.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77fe5-129">-Частота</span><span class="sxs-lookup"><span data-stu-id="77fe5-129">-Frequency</span></span>
<span data-ttu-id="77fe5-130">Указывает частоту для задания.</span><span class="sxs-lookup"><span data-stu-id="77fe5-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="77fe5-131">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="77fe5-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="77fe5-132">До</span><span class="sxs-lookup"><span data-stu-id="77fe5-132">Minute</span></span> 
- <span data-ttu-id="77fe5-133">Часовой</span><span class="sxs-lookup"><span data-stu-id="77fe5-133">Hour</span></span> 
- <span data-ttu-id="77fe5-134">Дневных</span><span class="sxs-lookup"><span data-stu-id="77fe5-134">Day</span></span> 
- <span data-ttu-id="77fe5-135">Недели</span><span class="sxs-lookup"><span data-stu-id="77fe5-135">Week</span></span> 
- <span data-ttu-id="77fe5-136">Перехода</span><span class="sxs-lookup"><span data-stu-id="77fe5-136">Month</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77fe5-137">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="77fe5-137">-Interval</span></span>
<span data-ttu-id="77fe5-138">Указывает интервал повторения для задания.</span><span class="sxs-lookup"><span data-stu-id="77fe5-138">Specifies an interval of recurrence for the job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77fe5-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="77fe5-139">-JobCollectionName</span></span>
<span data-ttu-id="77fe5-140">Указывает имя коллекции заданий, к которой относится задание.</span><span class="sxs-lookup"><span data-stu-id="77fe5-140">Specifies the name of the job collection to which the job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77fe5-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="77fe5-141">-JobName</span></span>
<span data-ttu-id="77fe5-142">Задает имя задания.</span><span class="sxs-lookup"><span data-stu-id="77fe5-142">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="77fe5-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="77fe5-143">-JobState</span></span>
<span data-ttu-id="77fe5-144">Указывает состояние задания.</span><span class="sxs-lookup"><span data-stu-id="77fe5-144">Specifies the state of the job.</span></span>
<span data-ttu-id="77fe5-145">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="77fe5-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="77fe5-146">Включаем</span><span class="sxs-lookup"><span data-stu-id="77fe5-146">Enabled</span></span> 
- <span data-ttu-id="77fe5-147">Отключает</span><span class="sxs-lookup"><span data-stu-id="77fe5-147">Disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77fe5-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77fe5-148">-ResourceGroupName</span></span>
<span data-ttu-id="77fe5-149">Указывает группу ресурсов, к которой относится задание.</span><span class="sxs-lookup"><span data-stu-id="77fe5-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="77fe5-150">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="77fe5-150">-ServiceBusMessage</span></span>
<span data-ttu-id="77fe5-151">Указывает сообщение очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="77fe5-151">Specifies a service bus queue message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77fe5-152">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="77fe5-152">-ServiceBusNamespace</span></span>
<span data-ttu-id="77fe5-153">Задает пространство имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="77fe5-153">Specifies a service bus namespace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77fe5-154">-ServiceBusQueueName</span><span class="sxs-lookup"><span data-stu-id="77fe5-154">-ServiceBusQueueName</span></span>
<span data-ttu-id="77fe5-155">Указывает имя очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="77fe5-155">Specifies a service bus queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77fe5-156">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="77fe5-156">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="77fe5-157">Задает имя ключа подписи для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="77fe5-157">Specifies a shared access signature key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77fe5-158">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="77fe5-158">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="77fe5-159">Задает значение ключа подписи для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="77fe5-159">Specifies a shared access signature key value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77fe5-160">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="77fe5-160">-ServiceBusTransportType</span></span>
<span data-ttu-id="77fe5-161">Указывает тип транспорта служебной шины.</span><span class="sxs-lookup"><span data-stu-id="77fe5-161">Specifies a service bus transport type.</span></span>
<span data-ttu-id="77fe5-162">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="77fe5-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="77fe5-163">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="77fe5-163">NetMessaging</span></span> 
- <span data-ttu-id="77fe5-164">AMQP</span><span class="sxs-lookup"><span data-stu-id="77fe5-164">AMQP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NetMessaging, AMQP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77fe5-165">-StartTime</span><span class="sxs-lookup"><span data-stu-id="77fe5-165">-StartTime</span></span>
<span data-ttu-id="77fe5-166">Задает время начала в виде объекта **DateTime** для задания.</span><span class="sxs-lookup"><span data-stu-id="77fe5-166">Specifies the start time, as a **DateTime** object, for the job.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77fe5-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77fe5-167">-Confirm</span></span>
<span data-ttu-id="77fe5-168">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="77fe5-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77fe5-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77fe5-169">-WhatIf</span></span>
<span data-ttu-id="77fe5-170">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="77fe5-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77fe5-171">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="77fe5-171">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77fe5-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77fe5-172">CommonParameters</span></span>
<span data-ttu-id="77fe5-173">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77fe5-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77fe5-174">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77fe5-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77fe5-175">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77fe5-175">INPUTS</span></span>

### <span data-ttu-id="77fe5-176">System. String</span><span class="sxs-lookup"><span data-stu-id="77fe5-176">System.String</span></span>

## <span data-ttu-id="77fe5-177">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77fe5-177">OUTPUTS</span></span>

### <span data-ttu-id="77fe5-178">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="77fe5-178">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="77fe5-179">Пуск</span><span class="sxs-lookup"><span data-stu-id="77fe5-179">NOTES</span></span>

## <span data-ttu-id="77fe5-180">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77fe5-180">RELATED LINKS</span></span>

[<span data-ttu-id="77fe5-181">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="77fe5-181">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="77fe5-182">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="77fe5-182">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="77fe5-183">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="77fe5-183">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="77fe5-184">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="77fe5-184">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="77fe5-185">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="77fe5-185">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="77fe5-186">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="77fe5-186">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="77fe5-187">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="77fe5-187">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="77fe5-188">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="77fe5-188">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="77fe5-189">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="77fe5-189">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


