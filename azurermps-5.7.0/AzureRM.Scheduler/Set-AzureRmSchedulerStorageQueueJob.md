---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 75AF57EE-C7C3-42DE-AFD7-4B5150EEDBB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerstoragequeuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
ms.openlocfilehash: d93ceb91ded5161dc962f902434cefe0f2070ae5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732141"
---
# <span data-ttu-id="a0cc5-101">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="a0cc5-101">Set-AzureRmSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="a0cc5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a0cc5-102">SYNOPSIS</span></span>
<span data-ttu-id="a0cc5-103">Изменение задания в очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-103">Modifies a storage queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0cc5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a0cc5-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerStorageQueueJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-StorageSASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0cc5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0cc5-105">DESCRIPTION</span></span>
<span data-ttu-id="a0cc5-106">Командлет **Set-AzureRmSchedulerStorageQueueJob** изменяет задание очереди хранилища в планировщике Azure.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-106">The **Set-AzureRmSchedulerStorageQueueJob** cmdlet modifies a storage queue job in Azure Scheduler.</span></span>

<span data-ttu-id="a0cc5-107">Этот командлет поддерживает динамические параметры, основанные на параметре *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="a0cc5-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="a0cc5-108">Динамические параметры становятся доступны в соответствии с другими значениями параметров.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="a0cc5-109">Чтобы найти имена динамических параметров после указания других параметров, введите дефис (-), а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a0cc5-110">Если вы не пропустите требуемый параметр, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a0cc5-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a0cc5-111">EXAMPLES</span></span>

## <span data-ttu-id="a0cc5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a0cc5-112">PARAMETERS</span></span>

### <span data-ttu-id="a0cc5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0cc5-113">-DefaultProfile</span></span>
<span data-ttu-id="a0cc5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0cc5-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="a0cc5-115">-EndTime</span></span>
<span data-ttu-id="a0cc5-116">Задает время окончания для задания в виде объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="a0cc5-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="a0cc5-117">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="a0cc5-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="a0cc5-118">-ErrorActionType</span></span>
<span data-ttu-id="a0cc5-119">Задает параметр действия при ошибке для задания.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="a0cc5-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a0cc5-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a0cc5-121">Через</span><span class="sxs-lookup"><span data-stu-id="a0cc5-121">Http</span></span> 
- <span data-ttu-id="a0cc5-122">Протокол</span><span class="sxs-lookup"><span data-stu-id="a0cc5-122">Https</span></span> 
- <span data-ttu-id="a0cc5-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="a0cc5-123">StorageQueue</span></span> 
- <span data-ttu-id="a0cc5-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="a0cc5-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="a0cc5-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="a0cc5-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="a0cc5-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="a0cc5-126">-ExecutionCount</span></span>
<span data-ttu-id="a0cc5-127">Задает количество выполняемых заданий.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="a0cc5-128">По умолчанию задание повторяется неопределенное время.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="a0cc5-129">-Частота</span><span class="sxs-lookup"><span data-stu-id="a0cc5-129">-Frequency</span></span>
<span data-ttu-id="a0cc5-130">Указывает частоту для задания.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="a0cc5-131">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a0cc5-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a0cc5-132">До</span><span class="sxs-lookup"><span data-stu-id="a0cc5-132">Minute</span></span> 
- <span data-ttu-id="a0cc5-133">Часовой</span><span class="sxs-lookup"><span data-stu-id="a0cc5-133">Hour</span></span> 
- <span data-ttu-id="a0cc5-134">Дневных</span><span class="sxs-lookup"><span data-stu-id="a0cc5-134">Day</span></span> 
- <span data-ttu-id="a0cc5-135">Недели</span><span class="sxs-lookup"><span data-stu-id="a0cc5-135">Week</span></span> 
- <span data-ttu-id="a0cc5-136">Перехода</span><span class="sxs-lookup"><span data-stu-id="a0cc5-136">Month</span></span>

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

### <span data-ttu-id="a0cc5-137">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="a0cc5-137">-Interval</span></span>
<span data-ttu-id="a0cc5-138">Указывает интервал повторения для задания.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="a0cc5-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="a0cc5-139">-JobCollectionName</span></span>
<span data-ttu-id="a0cc5-140">Указывает имя коллекции заданий, к которой относится задание.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="a0cc5-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="a0cc5-141">-JobName</span></span>
<span data-ttu-id="a0cc5-142">Указывает имя задания, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-142">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a0cc5-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="a0cc5-143">-JobState</span></span>
<span data-ttu-id="a0cc5-144">Указывает состояние задания.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-144">Specifies the state of the job.</span></span>
<span data-ttu-id="a0cc5-145">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a0cc5-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a0cc5-146">Включаем</span><span class="sxs-lookup"><span data-stu-id="a0cc5-146">Enabled</span></span> 
- <span data-ttu-id="a0cc5-147">Отключает</span><span class="sxs-lookup"><span data-stu-id="a0cc5-147">Disabled</span></span>

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

### <span data-ttu-id="a0cc5-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0cc5-148">-ResourceGroupName</span></span>
<span data-ttu-id="a0cc5-149">Указывает группу ресурсов, к которой относится задание.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="a0cc5-150">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a0cc5-150">-StartTime</span></span>
<span data-ttu-id="a0cc5-151">Задает время начала в виде объекта **DateTime** для задания.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-151">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="a0cc5-152">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="a0cc5-152">-StorageQueueAccount</span></span>
<span data-ttu-id="a0cc5-153">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-153">Specifies a storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0cc5-154">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="a0cc5-154">-StorageQueueMessage</span></span>
<span data-ttu-id="a0cc5-155">Указывает сообщение очереди для задания хранилища.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-155">Specifies a queue message for storage job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0cc5-156">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="a0cc5-156">-StorageQueueName</span></span>
<span data-ttu-id="a0cc5-157">Указывает имя очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-157">Specifies a storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0cc5-158">-StorageSASToken</span><span class="sxs-lookup"><span data-stu-id="a0cc5-158">-StorageSASToken</span></span>
<span data-ttu-id="a0cc5-159">Задает маркер подписи общего доступа для очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-159">Specifies a shared access signature token for a storage queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0cc5-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0cc5-160">-Confirm</span></span>
<span data-ttu-id="a0cc5-161">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0cc5-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0cc5-162">-WhatIf</span></span>
<span data-ttu-id="a0cc5-163">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0cc5-164">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0cc5-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0cc5-165">CommonParameters</span></span>
<span data-ttu-id="a0cc5-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0cc5-167">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0cc5-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0cc5-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a0cc5-168">INPUTS</span></span>

### <span data-ttu-id="a0cc5-169">Ничего</span><span class="sxs-lookup"><span data-stu-id="a0cc5-169">None</span></span>
<span data-ttu-id="a0cc5-170">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a0cc5-170">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a0cc5-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0cc5-171">OUTPUTS</span></span>

### <span data-ttu-id="a0cc5-172">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a0cc5-172">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="a0cc5-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="a0cc5-173">NOTES</span></span>

## <span data-ttu-id="a0cc5-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0cc5-174">RELATED LINKS</span></span>

[<span data-ttu-id="a0cc5-175">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="a0cc5-175">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="a0cc5-176">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a0cc5-176">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="a0cc5-177">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="a0cc5-177">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="a0cc5-178">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="a0cc5-178">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="a0cc5-179">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="a0cc5-179">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="a0cc5-180">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="a0cc5-180">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="a0cc5-181">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a0cc5-181">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="a0cc5-182">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="a0cc5-182">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="a0cc5-183">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="a0cc5-183">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)


