---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: E00D42D6-707A-479E-9964-C5B80D3DAA6A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerhttpjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 1d0c66d3442d6db03897140849f5713d3107f8d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568385"
---
# <span data-ttu-id="d411c-101">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="d411c-101">New-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="d411c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d411c-102">SYNOPSIS</span></span>
<span data-ttu-id="d411c-103">Создание HTTP-задания.</span><span class="sxs-lookup"><span data-stu-id="d411c-103">Creates an HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d411c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d411c-104">SYNTAX</span></span>

```
New-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -Method <String> -Uri <Uri> [-RequestBody <String>] [-Headers <Hashtable>] [-HttpAuthenticationType <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d411c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d411c-105">DESCRIPTION</span></span>
<span data-ttu-id="d411c-106">Командлет **New-AzureRmSchedulerHttpJob** создает задание HTTP в планировщике Azure.</span><span class="sxs-lookup"><span data-stu-id="d411c-106">The **New-AzureRmSchedulerHttpJob** cmdlet creates an HTTP job in Azure Scheduler.</span></span>
<span data-ttu-id="d411c-107">Этот командлет поддерживает динамические параметры, основанные на параметрах *ErrorActionType* и *HttpAuthenticationType* .</span><span class="sxs-lookup"><span data-stu-id="d411c-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="d411c-108">Динамические параметры становятся доступны в соответствии с другими значениями параметров.</span><span class="sxs-lookup"><span data-stu-id="d411c-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="d411c-109">Чтобы найти имена динамических параметров после указания других параметров, введите дефис (-), а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="d411c-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d411c-110">Если вы не пропустите требуемый параметр, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="d411c-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d411c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d411c-111">EXAMPLES</span></span>

## <span data-ttu-id="d411c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d411c-112">PARAMETERS</span></span>

### <span data-ttu-id="d411c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d411c-113">-DefaultProfile</span></span>
<span data-ttu-id="d411c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d411c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d411c-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="d411c-115">-EndTime</span></span>
<span data-ttu-id="d411c-116">Задает время окончания для задания в виде объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="d411c-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="d411c-117">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="d411c-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="d411c-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="d411c-118">-ErrorActionType</span></span>
<span data-ttu-id="d411c-119">Задает параметр действия при ошибке для задания.</span><span class="sxs-lookup"><span data-stu-id="d411c-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="d411c-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d411c-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d411c-121">Через</span><span class="sxs-lookup"><span data-stu-id="d411c-121">Http</span></span> 
- <span data-ttu-id="d411c-122">Протокол</span><span class="sxs-lookup"><span data-stu-id="d411c-122">Https</span></span> 
- <span data-ttu-id="d411c-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="d411c-123">StorageQueue</span></span> 
- <span data-ttu-id="d411c-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="d411c-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="d411c-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="d411c-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="d411c-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="d411c-126">-ExecutionCount</span></span>
<span data-ttu-id="d411c-127">Задает количество выполняемых заданий.</span><span class="sxs-lookup"><span data-stu-id="d411c-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="d411c-128">По умолчанию задание повторяется неопределенное время.</span><span class="sxs-lookup"><span data-stu-id="d411c-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="d411c-129">-Частота</span><span class="sxs-lookup"><span data-stu-id="d411c-129">-Frequency</span></span>
<span data-ttu-id="d411c-130">Задает максимальную частоту для задания.</span><span class="sxs-lookup"><span data-stu-id="d411c-130">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="d411c-131">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d411c-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d411c-132">До</span><span class="sxs-lookup"><span data-stu-id="d411c-132">Minute</span></span> 
- <span data-ttu-id="d411c-133">Часовой</span><span class="sxs-lookup"><span data-stu-id="d411c-133">Hour</span></span> 
- <span data-ttu-id="d411c-134">Дневных</span><span class="sxs-lookup"><span data-stu-id="d411c-134">Day</span></span> 
- <span data-ttu-id="d411c-135">Недели</span><span class="sxs-lookup"><span data-stu-id="d411c-135">Week</span></span> 
- <span data-ttu-id="d411c-136">Перехода</span><span class="sxs-lookup"><span data-stu-id="d411c-136">Month</span></span>

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

### <span data-ttu-id="d411c-137">-Заголовки</span><span class="sxs-lookup"><span data-stu-id="d411c-137">-Headers</span></span>
<span data-ttu-id="d411c-138">Указывает хэш-таблицу, содержащую заголовки.</span><span class="sxs-lookup"><span data-stu-id="d411c-138">Specifies a hash table that contains headers.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d411c-139">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="d411c-139">-HttpAuthenticationType</span></span>
<span data-ttu-id="d411c-140">Указывает тип проверки подлинности HTTP.</span><span class="sxs-lookup"><span data-stu-id="d411c-140">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="d411c-141">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d411c-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d411c-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="d411c-142">None</span></span> 
- <span data-ttu-id="d411c-143">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="d411c-143">ClientCertificate</span></span> 
- <span data-ttu-id="d411c-144">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="d411c-144">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="d411c-145">Базового</span><span class="sxs-lookup"><span data-stu-id="d411c-145">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, ClientCertificate, ActiveDirectoryOAuth, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d411c-146">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="d411c-146">-Interval</span></span>
<span data-ttu-id="d411c-147">Указывает интервал повторения для задания.</span><span class="sxs-lookup"><span data-stu-id="d411c-147">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="d411c-148">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="d411c-148">-JobCollectionName</span></span>
<span data-ttu-id="d411c-149">Указывает имя коллекции заданий, к которой относится задание.</span><span class="sxs-lookup"><span data-stu-id="d411c-149">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="d411c-150">-JobName</span><span class="sxs-lookup"><span data-stu-id="d411c-150">-JobName</span></span>
<span data-ttu-id="d411c-151">Задает имя задания.</span><span class="sxs-lookup"><span data-stu-id="d411c-151">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="d411c-152">-JobState</span><span class="sxs-lookup"><span data-stu-id="d411c-152">-JobState</span></span>
<span data-ttu-id="d411c-153">Указывает состояние задания.</span><span class="sxs-lookup"><span data-stu-id="d411c-153">Specifies the state of the job.</span></span>
<span data-ttu-id="d411c-154">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d411c-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d411c-155">Включаем</span><span class="sxs-lookup"><span data-stu-id="d411c-155">Enabled</span></span> 
- <span data-ttu-id="d411c-156">Отключает</span><span class="sxs-lookup"><span data-stu-id="d411c-156">Disabled</span></span>

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

### <span data-ttu-id="d411c-157">-Method</span><span class="sxs-lookup"><span data-stu-id="d411c-157">-Method</span></span>
<span data-ttu-id="d411c-158">Указывает метод для типов действий для задания.</span><span class="sxs-lookup"><span data-stu-id="d411c-158">Specifies the method for the action types for the job.</span></span>
<span data-ttu-id="d411c-159">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d411c-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d411c-160">Получить</span><span class="sxs-lookup"><span data-stu-id="d411c-160">GET</span></span> 
- <span data-ttu-id="d411c-161">Установка</span><span class="sxs-lookup"><span data-stu-id="d411c-161">PUT</span></span> 
- <span data-ttu-id="d411c-162">Поместить</span><span class="sxs-lookup"><span data-stu-id="d411c-162">POST</span></span> 
- <span data-ttu-id="d411c-163">Удаление</span><span class="sxs-lookup"><span data-stu-id="d411c-163">DELETE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GET, PUT, POST, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d411c-164">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="d411c-164">-RequestBody</span></span>
<span data-ttu-id="d411c-165">Указывает значение тела для действий помещения и публикации.</span><span class="sxs-lookup"><span data-stu-id="d411c-165">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="d411c-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d411c-166">-ResourceGroupName</span></span>
<span data-ttu-id="d411c-167">Указывает группу ресурсов, к которой относится задание.</span><span class="sxs-lookup"><span data-stu-id="d411c-167">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="d411c-168">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d411c-168">-StartTime</span></span>
<span data-ttu-id="d411c-169">Задает время начала в виде объекта **DateTime** для задания.</span><span class="sxs-lookup"><span data-stu-id="d411c-169">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="d411c-170">-URI</span><span class="sxs-lookup"><span data-stu-id="d411c-170">-Uri</span></span>
<span data-ttu-id="d411c-171">Задает универсальный код ресурса (URI) для действия задания.</span><span class="sxs-lookup"><span data-stu-id="d411c-171">Specifies a URI for the job action.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d411c-172">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d411c-172">-Confirm</span></span>
<span data-ttu-id="d411c-173">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d411c-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d411c-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d411c-174">-WhatIf</span></span>
<span data-ttu-id="d411c-175">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d411c-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d411c-176">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d411c-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d411c-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d411c-177">CommonParameters</span></span>
<span data-ttu-id="d411c-178">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d411c-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d411c-179">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d411c-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d411c-180">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d411c-180">INPUTS</span></span>

### <span data-ttu-id="d411c-181">System. String</span><span class="sxs-lookup"><span data-stu-id="d411c-181">System.String</span></span>

### <span data-ttu-id="d411c-182">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d411c-182">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d411c-183">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d411c-183">OUTPUTS</span></span>

### <span data-ttu-id="d411c-184">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d411c-184">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="d411c-185">Пуск</span><span class="sxs-lookup"><span data-stu-id="d411c-185">NOTES</span></span>

## <span data-ttu-id="d411c-186">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d411c-186">RELATED LINKS</span></span>

[<span data-ttu-id="d411c-187">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d411c-187">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d411c-188">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="d411c-188">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="d411c-189">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="d411c-189">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="d411c-190">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="d411c-190">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="d411c-191">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="d411c-191">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="d411c-192">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d411c-192">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d411c-193">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="d411c-193">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="d411c-194">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="d411c-194">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="d411c-195">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="d411c-195">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


