---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 75AF57EE-C7C3-42DE-AFD7-4B5150EEDBB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerstoragequeuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
ms.openlocfilehash: 68747f616971927ab719ec9ccc8eaf8bd9efc370
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566767"
---
# <span data-ttu-id="0e3df-101">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="0e3df-101">Set-AzureRmSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="0e3df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0e3df-102">SYNOPSIS</span></span>
<span data-ttu-id="0e3df-103">Изменение задания в очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="0e3df-103">Modifies a storage queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e3df-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0e3df-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerStorageQueueJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-StorageSASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e3df-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e3df-105">DESCRIPTION</span></span>
<span data-ttu-id="0e3df-106">Командлет **Set-AzureRmSchedulerStorageQueueJob** изменяет задание очереди хранилища в планировщике Azure.</span><span class="sxs-lookup"><span data-stu-id="0e3df-106">The **Set-AzureRmSchedulerStorageQueueJob** cmdlet modifies a storage queue job in Azure Scheduler.</span></span>
<span data-ttu-id="0e3df-107">Этот командлет поддерживает динамические параметры, основанные на параметре *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="0e3df-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="0e3df-108">Динамические параметры становятся доступны в соответствии с другими значениями параметров.</span><span class="sxs-lookup"><span data-stu-id="0e3df-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="0e3df-109">Чтобы найти имена динамических параметров после указания других параметров, введите дефис (-), а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="0e3df-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0e3df-110">Если вы не пропустите требуемый параметр, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="0e3df-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0e3df-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0e3df-111">EXAMPLES</span></span>

## <span data-ttu-id="0e3df-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0e3df-112">PARAMETERS</span></span>

### <span data-ttu-id="0e3df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e3df-113">-DefaultProfile</span></span>
<span data-ttu-id="0e3df-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0e3df-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e3df-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="0e3df-115">-EndTime</span></span>
<span data-ttu-id="0e3df-116">Задает время окончания для задания в виде объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="0e3df-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="0e3df-117">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="0e3df-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="0e3df-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="0e3df-118">-ErrorActionType</span></span>
<span data-ttu-id="0e3df-119">Задает параметр действия при ошибке для задания.</span><span class="sxs-lookup"><span data-stu-id="0e3df-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="0e3df-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0e3df-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0e3df-121">Через</span><span class="sxs-lookup"><span data-stu-id="0e3df-121">Http</span></span> 
- <span data-ttu-id="0e3df-122">Протокол</span><span class="sxs-lookup"><span data-stu-id="0e3df-122">Https</span></span> 
- <span data-ttu-id="0e3df-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="0e3df-123">StorageQueue</span></span> 
- <span data-ttu-id="0e3df-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="0e3df-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="0e3df-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="0e3df-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="0e3df-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="0e3df-126">-ExecutionCount</span></span>
<span data-ttu-id="0e3df-127">Задает количество выполняемых заданий.</span><span class="sxs-lookup"><span data-stu-id="0e3df-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="0e3df-128">По умолчанию задание повторяется неопределенное время.</span><span class="sxs-lookup"><span data-stu-id="0e3df-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="0e3df-129">-Частота</span><span class="sxs-lookup"><span data-stu-id="0e3df-129">-Frequency</span></span>
<span data-ttu-id="0e3df-130">Указывает частоту для задания.</span><span class="sxs-lookup"><span data-stu-id="0e3df-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="0e3df-131">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0e3df-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0e3df-132">До</span><span class="sxs-lookup"><span data-stu-id="0e3df-132">Minute</span></span> 
- <span data-ttu-id="0e3df-133">Часовой</span><span class="sxs-lookup"><span data-stu-id="0e3df-133">Hour</span></span> 
- <span data-ttu-id="0e3df-134">Дневных</span><span class="sxs-lookup"><span data-stu-id="0e3df-134">Day</span></span> 
- <span data-ttu-id="0e3df-135">Недели</span><span class="sxs-lookup"><span data-stu-id="0e3df-135">Week</span></span> 
- <span data-ttu-id="0e3df-136">Перехода</span><span class="sxs-lookup"><span data-stu-id="0e3df-136">Month</span></span>

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

### <span data-ttu-id="0e3df-137">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="0e3df-137">-Interval</span></span>
<span data-ttu-id="0e3df-138">Указывает интервал повторения для задания.</span><span class="sxs-lookup"><span data-stu-id="0e3df-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="0e3df-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="0e3df-139">-JobCollectionName</span></span>
<span data-ttu-id="0e3df-140">Указывает имя коллекции заданий, к которой относится задание.</span><span class="sxs-lookup"><span data-stu-id="0e3df-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="0e3df-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="0e3df-141">-JobName</span></span>
<span data-ttu-id="0e3df-142">Указывает имя задания, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0e3df-142">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0e3df-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="0e3df-143">-JobState</span></span>
<span data-ttu-id="0e3df-144">Указывает состояние задания.</span><span class="sxs-lookup"><span data-stu-id="0e3df-144">Specifies the state of the job.</span></span>
<span data-ttu-id="0e3df-145">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0e3df-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0e3df-146">Включаем</span><span class="sxs-lookup"><span data-stu-id="0e3df-146">Enabled</span></span> 
- <span data-ttu-id="0e3df-147">Отключает</span><span class="sxs-lookup"><span data-stu-id="0e3df-147">Disabled</span></span>

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

### <span data-ttu-id="0e3df-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e3df-148">-ResourceGroupName</span></span>
<span data-ttu-id="0e3df-149">Указывает группу ресурсов, к которой относится задание.</span><span class="sxs-lookup"><span data-stu-id="0e3df-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="0e3df-150">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0e3df-150">-StartTime</span></span>
<span data-ttu-id="0e3df-151">Задает время начала в виде объекта **DateTime** для задания.</span><span class="sxs-lookup"><span data-stu-id="0e3df-151">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="0e3df-152">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="0e3df-152">-StorageQueueAccount</span></span>
<span data-ttu-id="0e3df-153">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0e3df-153">Specifies a storage account name.</span></span>

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

### <span data-ttu-id="0e3df-154">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="0e3df-154">-StorageQueueMessage</span></span>
<span data-ttu-id="0e3df-155">Указывает сообщение очереди для задания хранилища.</span><span class="sxs-lookup"><span data-stu-id="0e3df-155">Specifies a queue message for storage job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e3df-156">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="0e3df-156">-StorageQueueName</span></span>
<span data-ttu-id="0e3df-157">Указывает имя очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="0e3df-157">Specifies a storage queue name.</span></span>

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

### <span data-ttu-id="0e3df-158">-StorageSASToken</span><span class="sxs-lookup"><span data-stu-id="0e3df-158">-StorageSASToken</span></span>
<span data-ttu-id="0e3df-159">Задает маркер подписи общего доступа для очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="0e3df-159">Specifies a shared access signature token for a storage queue.</span></span>

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

### <span data-ttu-id="0e3df-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e3df-160">-Confirm</span></span>
<span data-ttu-id="0e3df-161">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0e3df-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e3df-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e3df-162">-WhatIf</span></span>
<span data-ttu-id="0e3df-163">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0e3df-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e3df-164">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0e3df-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e3df-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e3df-165">CommonParameters</span></span>
<span data-ttu-id="0e3df-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0e3df-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e3df-167">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e3df-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e3df-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0e3df-168">INPUTS</span></span>

### <span data-ttu-id="0e3df-169">System. String</span><span class="sxs-lookup"><span data-stu-id="0e3df-169">System.String</span></span>

## <span data-ttu-id="0e3df-170">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e3df-170">OUTPUTS</span></span>

### <span data-ttu-id="0e3df-171">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="0e3df-171">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="0e3df-172">Пуск</span><span class="sxs-lookup"><span data-stu-id="0e3df-172">NOTES</span></span>

## <span data-ttu-id="0e3df-173">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e3df-173">RELATED LINKS</span></span>

[<span data-ttu-id="0e3df-174">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="0e3df-174">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="0e3df-175">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0e3df-175">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="0e3df-176">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="0e3df-176">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="0e3df-177">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="0e3df-177">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="0e3df-178">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="0e3df-178">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="0e3df-179">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="0e3df-179">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="0e3df-180">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0e3df-180">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="0e3df-181">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="0e3df-181">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="0e3df-182">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="0e3df-182">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)


