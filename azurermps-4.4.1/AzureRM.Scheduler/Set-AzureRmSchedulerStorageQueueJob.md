---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 75AF57EE-C7C3-42DE-AFD7-4B5150EEDBB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
ms.openlocfilehash: c752b4fd96ec001467e051fc01be24f592241182
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734523"
---
# <span data-ttu-id="d559e-101">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="d559e-101">Set-AzureRmSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="d559e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d559e-102">SYNOPSIS</span></span>
<span data-ttu-id="d559e-103">Изменение задания в очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="d559e-103">Modifies a storage queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d559e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d559e-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerStorageQueueJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-StorageSASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d559e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d559e-105">DESCRIPTION</span></span>
<span data-ttu-id="d559e-106">Командлет **Set-AzureRmSchedulerStorageQueueJob** изменяет задание очереди хранилища в планировщике Azure.</span><span class="sxs-lookup"><span data-stu-id="d559e-106">The **Set-AzureRmSchedulerStorageQueueJob** cmdlet modifies a storage queue job in Azure Scheduler.</span></span>

<span data-ttu-id="d559e-107">Этот командлет поддерживает динамические параметры, основанные на параметре *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="d559e-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="d559e-108">Динамические параметры становятся доступны в соответствии с другими значениями параметров.</span><span class="sxs-lookup"><span data-stu-id="d559e-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="d559e-109">Чтобы найти имена динамических параметров после указания других параметров, введите дефис (-), а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="d559e-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d559e-110">Если вы не пропустите требуемый параметр, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="d559e-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d559e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d559e-111">EXAMPLES</span></span>

## <span data-ttu-id="d559e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d559e-112">PARAMETERS</span></span>

### <span data-ttu-id="d559e-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="d559e-113">-EndTime</span></span>
<span data-ttu-id="d559e-114">Задает время окончания для задания в виде объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="d559e-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="d559e-115">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="d559e-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="d559e-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="d559e-116">-ErrorActionType</span></span>
<span data-ttu-id="d559e-117">Задает параметр действия при ошибке для задания.</span><span class="sxs-lookup"><span data-stu-id="d559e-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="d559e-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d559e-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d559e-119">Через</span><span class="sxs-lookup"><span data-stu-id="d559e-119">Http</span></span> 
- <span data-ttu-id="d559e-120">Протокол</span><span class="sxs-lookup"><span data-stu-id="d559e-120">Https</span></span> 
- <span data-ttu-id="d559e-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="d559e-121">StorageQueue</span></span> 
- <span data-ttu-id="d559e-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="d559e-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="d559e-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="d559e-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="d559e-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="d559e-124">-ExecutionCount</span></span>
<span data-ttu-id="d559e-125">Задает количество выполняемых заданий.</span><span class="sxs-lookup"><span data-stu-id="d559e-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="d559e-126">По умолчанию задание повторяется неопределенное время.</span><span class="sxs-lookup"><span data-stu-id="d559e-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="d559e-127">-Частота</span><span class="sxs-lookup"><span data-stu-id="d559e-127">-Frequency</span></span>
<span data-ttu-id="d559e-128">Указывает частоту для задания.</span><span class="sxs-lookup"><span data-stu-id="d559e-128">Specifies a frequency for the job.</span></span>
<span data-ttu-id="d559e-129">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d559e-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d559e-130">До</span><span class="sxs-lookup"><span data-stu-id="d559e-130">Minute</span></span> 
- <span data-ttu-id="d559e-131">Часовой</span><span class="sxs-lookup"><span data-stu-id="d559e-131">Hour</span></span> 
- <span data-ttu-id="d559e-132">Дневных</span><span class="sxs-lookup"><span data-stu-id="d559e-132">Day</span></span> 
- <span data-ttu-id="d559e-133">Недели</span><span class="sxs-lookup"><span data-stu-id="d559e-133">Week</span></span> 
- <span data-ttu-id="d559e-134">Перехода</span><span class="sxs-lookup"><span data-stu-id="d559e-134">Month</span></span>

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

### <span data-ttu-id="d559e-135">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="d559e-135">-Interval</span></span>
<span data-ttu-id="d559e-136">Указывает интервал повторения для задания.</span><span class="sxs-lookup"><span data-stu-id="d559e-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="d559e-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="d559e-137">-JobCollectionName</span></span>
<span data-ttu-id="d559e-138">Указывает имя коллекции заданий, к которой относится задание.</span><span class="sxs-lookup"><span data-stu-id="d559e-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="d559e-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="d559e-139">-JobName</span></span>
<span data-ttu-id="d559e-140">Указывает имя задания, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d559e-140">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d559e-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="d559e-141">-JobState</span></span>
<span data-ttu-id="d559e-142">Указывает состояние задания.</span><span class="sxs-lookup"><span data-stu-id="d559e-142">Specifies the state of the job.</span></span>
<span data-ttu-id="d559e-143">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d559e-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d559e-144">Включаем</span><span class="sxs-lookup"><span data-stu-id="d559e-144">Enabled</span></span> 
- <span data-ttu-id="d559e-145">Отключает</span><span class="sxs-lookup"><span data-stu-id="d559e-145">Disabled</span></span>

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

### <span data-ttu-id="d559e-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d559e-146">-ResourceGroupName</span></span>
<span data-ttu-id="d559e-147">Указывает группу ресурсов, к которой относится задание.</span><span class="sxs-lookup"><span data-stu-id="d559e-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="d559e-148">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d559e-148">-StartTime</span></span>
<span data-ttu-id="d559e-149">Задает время начала в виде объекта **DateTime** для задания.</span><span class="sxs-lookup"><span data-stu-id="d559e-149">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="d559e-150">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="d559e-150">-StorageQueueAccount</span></span>
<span data-ttu-id="d559e-151">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d559e-151">Specifies a storage account name.</span></span>

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

### <span data-ttu-id="d559e-152">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="d559e-152">-StorageQueueMessage</span></span>
<span data-ttu-id="d559e-153">Указывает сообщение очереди для задания хранилища.</span><span class="sxs-lookup"><span data-stu-id="d559e-153">Specifies a queue message for storage job.</span></span>

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

### <span data-ttu-id="d559e-154">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="d559e-154">-StorageQueueName</span></span>
<span data-ttu-id="d559e-155">Указывает имя очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="d559e-155">Specifies a storage queue name.</span></span>

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

### <span data-ttu-id="d559e-156">-StorageSASToken</span><span class="sxs-lookup"><span data-stu-id="d559e-156">-StorageSASToken</span></span>
<span data-ttu-id="d559e-157">Задает маркер подписи общего доступа для очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="d559e-157">Specifies a shared access signature token for a storage queue.</span></span>

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

### <span data-ttu-id="d559e-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d559e-158">-Confirm</span></span>
<span data-ttu-id="d559e-159">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d559e-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d559e-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d559e-160">-WhatIf</span></span>
<span data-ttu-id="d559e-161">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d559e-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d559e-162">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d559e-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d559e-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d559e-163">-DefaultProfile</span></span>
<span data-ttu-id="d559e-164">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d559e-164">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d559e-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d559e-165">CommonParameters</span></span>
<span data-ttu-id="d559e-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d559e-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d559e-167">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d559e-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d559e-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d559e-168">INPUTS</span></span>

## <span data-ttu-id="d559e-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d559e-169">OUTPUTS</span></span>

### <span data-ttu-id="d559e-170">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d559e-170">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="d559e-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="d559e-171">NOTES</span></span>

## <span data-ttu-id="d559e-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d559e-172">RELATED LINKS</span></span>

[<span data-ttu-id="d559e-173">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="d559e-173">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="d559e-174">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d559e-174">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d559e-175">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="d559e-175">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="d559e-176">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="d559e-176">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="d559e-177">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="d559e-177">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="d559e-178">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="d559e-178">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="d559e-179">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d559e-179">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d559e-180">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="d559e-180">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="d559e-181">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="d559e-181">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)


