---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 52987702-D101-4D5D-852D-2809374292F4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
ms.openlocfilehash: a61d745cb748d27baf7b07b6b4389077e50aaa24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567515"
---
# <span data-ttu-id="c11dd-101">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="c11dd-101">New-AzureRmSchedulerServiceBusQueueJob</span></span>

## <span data-ttu-id="c11dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c11dd-102">SYNOPSIS</span></span>
<span data-ttu-id="c11dd-103">Создание задания очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="c11dd-103">Creates a service bus queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c11dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c11dd-104">SYNTAX</span></span>

```
New-AzureRmSchedulerServiceBusQueueJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusQueueName <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c11dd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c11dd-105">DESCRIPTION</span></span>
<span data-ttu-id="c11dd-106">Командлет **New-AzureRmSchedulerServiceBusQueueJob** создает задание в очереди служебной шины в планировщике Azure.</span><span class="sxs-lookup"><span data-stu-id="c11dd-106">The **New-AzureRmSchedulerServiceBusQueueJob** cmdlet creates a service bus queue job in Azure Scheduler.</span></span>

<span data-ttu-id="c11dd-107">Этот командлет поддерживает динамические параметры, основанные на параметре *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="c11dd-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="c11dd-108">Динамические параметры становятся доступны в соответствии с другими значениями параметров.</span><span class="sxs-lookup"><span data-stu-id="c11dd-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="c11dd-109">Чтобы найти имена динамических параметров после указания других параметров, введите дефис (-), а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="c11dd-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c11dd-110">Если вы не пропустите требуемый параметр, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="c11dd-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c11dd-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c11dd-111">EXAMPLES</span></span>

## <span data-ttu-id="c11dd-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c11dd-112">PARAMETERS</span></span>

### <span data-ttu-id="c11dd-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c11dd-113">-EndTime</span></span>
<span data-ttu-id="c11dd-114">Задает время окончания для задания в виде объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="c11dd-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="c11dd-115">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="c11dd-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="c11dd-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="c11dd-116">-ErrorActionType</span></span>
<span data-ttu-id="c11dd-117">Задает параметр действия при ошибке для задания.</span><span class="sxs-lookup"><span data-stu-id="c11dd-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="c11dd-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c11dd-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c11dd-119">Через</span><span class="sxs-lookup"><span data-stu-id="c11dd-119">Http</span></span> 
- <span data-ttu-id="c11dd-120">Протокол</span><span class="sxs-lookup"><span data-stu-id="c11dd-120">Https</span></span> 
- <span data-ttu-id="c11dd-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="c11dd-121">StorageQueue</span></span> 
- <span data-ttu-id="c11dd-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="c11dd-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="c11dd-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="c11dd-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="c11dd-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="c11dd-124">-ExecutionCount</span></span>
<span data-ttu-id="c11dd-125">Задает количество выполняемых заданий.</span><span class="sxs-lookup"><span data-stu-id="c11dd-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="c11dd-126">По умолчанию задание повторяется неопределенное время.</span><span class="sxs-lookup"><span data-stu-id="c11dd-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="c11dd-127">-Частота</span><span class="sxs-lookup"><span data-stu-id="c11dd-127">-Frequency</span></span>
<span data-ttu-id="c11dd-128">Указывает частоту для задания.</span><span class="sxs-lookup"><span data-stu-id="c11dd-128">Specifies a frequency for the job.</span></span>
<span data-ttu-id="c11dd-129">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c11dd-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c11dd-130">До</span><span class="sxs-lookup"><span data-stu-id="c11dd-130">Minute</span></span> 
- <span data-ttu-id="c11dd-131">Часовой</span><span class="sxs-lookup"><span data-stu-id="c11dd-131">Hour</span></span> 
- <span data-ttu-id="c11dd-132">Дневных</span><span class="sxs-lookup"><span data-stu-id="c11dd-132">Day</span></span> 
- <span data-ttu-id="c11dd-133">Недели</span><span class="sxs-lookup"><span data-stu-id="c11dd-133">Week</span></span> 
- <span data-ttu-id="c11dd-134">Перехода</span><span class="sxs-lookup"><span data-stu-id="c11dd-134">Month</span></span>

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

### <span data-ttu-id="c11dd-135">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="c11dd-135">-Interval</span></span>
<span data-ttu-id="c11dd-136">Указывает интервал повторения для задания.</span><span class="sxs-lookup"><span data-stu-id="c11dd-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="c11dd-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="c11dd-137">-JobCollectionName</span></span>
<span data-ttu-id="c11dd-138">Указывает имя коллекции заданий, к которой относится задание.</span><span class="sxs-lookup"><span data-stu-id="c11dd-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="c11dd-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="c11dd-139">-JobName</span></span>
<span data-ttu-id="c11dd-140">Задает имя задания.</span><span class="sxs-lookup"><span data-stu-id="c11dd-140">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="c11dd-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="c11dd-141">-JobState</span></span>
<span data-ttu-id="c11dd-142">Указывает состояние задания.</span><span class="sxs-lookup"><span data-stu-id="c11dd-142">Specifies the state of the job.</span></span>
<span data-ttu-id="c11dd-143">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c11dd-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c11dd-144">Включаем</span><span class="sxs-lookup"><span data-stu-id="c11dd-144">Enabled</span></span> 
- <span data-ttu-id="c11dd-145">Отключает</span><span class="sxs-lookup"><span data-stu-id="c11dd-145">Disabled</span></span>

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

### <span data-ttu-id="c11dd-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c11dd-146">-ResourceGroupName</span></span>
<span data-ttu-id="c11dd-147">Указывает группу ресурсов, к которой относится задание.</span><span class="sxs-lookup"><span data-stu-id="c11dd-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="c11dd-148">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="c11dd-148">-ServiceBusMessage</span></span>
<span data-ttu-id="c11dd-149">Указывает сообщение очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="c11dd-149">Specifies a service bus queue message.</span></span>

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

### <span data-ttu-id="c11dd-150">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="c11dd-150">-ServiceBusNamespace</span></span>
<span data-ttu-id="c11dd-151">Задает пространство имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="c11dd-151">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="c11dd-152">-ServiceBusQueueName</span><span class="sxs-lookup"><span data-stu-id="c11dd-152">-ServiceBusQueueName</span></span>
<span data-ttu-id="c11dd-153">Указывает имя очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="c11dd-153">Specifies a service bus queue name.</span></span>

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

### <span data-ttu-id="c11dd-154">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="c11dd-154">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="c11dd-155">Задает имя ключа подписи для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="c11dd-155">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="c11dd-156">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="c11dd-156">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="c11dd-157">Задает значение ключа подписи для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="c11dd-157">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="c11dd-158">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="c11dd-158">-ServiceBusTransportType</span></span>
<span data-ttu-id="c11dd-159">Указывает тип транспорта служебной шины.</span><span class="sxs-lookup"><span data-stu-id="c11dd-159">Specifies a service bus transport type.</span></span>
<span data-ttu-id="c11dd-160">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c11dd-160">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c11dd-161">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="c11dd-161">NetMessaging</span></span> 
- <span data-ttu-id="c11dd-162">AMQP</span><span class="sxs-lookup"><span data-stu-id="c11dd-162">AMQP</span></span>

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

### <span data-ttu-id="c11dd-163">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c11dd-163">-StartTime</span></span>
<span data-ttu-id="c11dd-164">Задает время начала в виде объекта **DateTime** для задания.</span><span class="sxs-lookup"><span data-stu-id="c11dd-164">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="c11dd-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c11dd-165">-Confirm</span></span>
<span data-ttu-id="c11dd-166">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c11dd-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c11dd-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c11dd-167">-WhatIf</span></span>
<span data-ttu-id="c11dd-168">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c11dd-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c11dd-169">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c11dd-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c11dd-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c11dd-170">-DefaultProfile</span></span>
<span data-ttu-id="c11dd-171">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c11dd-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c11dd-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c11dd-172">CommonParameters</span></span>
<span data-ttu-id="c11dd-173">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c11dd-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c11dd-174">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c11dd-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c11dd-175">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c11dd-175">INPUTS</span></span>

## <span data-ttu-id="c11dd-176">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c11dd-176">OUTPUTS</span></span>

### <span data-ttu-id="c11dd-177">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="c11dd-177">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="c11dd-178">Пуск</span><span class="sxs-lookup"><span data-stu-id="c11dd-178">NOTES</span></span>

## <span data-ttu-id="c11dd-179">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c11dd-179">RELATED LINKS</span></span>

[<span data-ttu-id="c11dd-180">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="c11dd-180">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="c11dd-181">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c11dd-181">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="c11dd-182">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="c11dd-182">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="c11dd-183">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="c11dd-183">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="c11dd-184">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="c11dd-184">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="c11dd-185">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c11dd-185">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="c11dd-186">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="c11dd-186">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="c11dd-187">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="c11dd-187">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="c11dd-188">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="c11dd-188">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


