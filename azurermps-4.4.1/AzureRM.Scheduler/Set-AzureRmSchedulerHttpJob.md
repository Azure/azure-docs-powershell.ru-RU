---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D9FA686C-48BB-48A1-926C-56B8151F8F82
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 2debabbcd4ae9b5418436e7846e8490926f37b1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565154"
---
# <span data-ttu-id="ced23-101">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="ced23-101">Set-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="ced23-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ced23-102">SYNOPSIS</span></span>
<span data-ttu-id="ced23-103">Изменяет HTTP-задание планировщика.</span><span class="sxs-lookup"><span data-stu-id="ced23-103">Modifies a Scheduler HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ced23-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ced23-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-Method <String>] [-Uri <Uri>] [-RequestBody <String>] [-Headers <Hashtable>]
 [-HttpAuthenticationType <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ced23-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ced23-105">DESCRIPTION</span></span>
<span data-ttu-id="ced23-106">Командлет **Set-AzureRmSchedulerHttpJob** изменяет задание HTTP в планировщике Azure.</span><span class="sxs-lookup"><span data-stu-id="ced23-106">The **Set-AzureRmSchedulerHttpJob** cmdlet modifies an HTTP job in Azure Scheduler.</span></span>

<span data-ttu-id="ced23-107">Этот командлет поддерживает динамические параметры, основанные на параметрах *ErrorActionType* и *HttpAuthenticationType* .</span><span class="sxs-lookup"><span data-stu-id="ced23-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="ced23-108">Динамические параметры становятся доступны в соответствии с другими значениями параметров.</span><span class="sxs-lookup"><span data-stu-id="ced23-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="ced23-109">Чтобы найти имена динамических параметров после указания других параметров, введите дефис (-), а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="ced23-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ced23-110">Если вы не пропустите требуемый параметр, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="ced23-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ced23-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ced23-111">EXAMPLES</span></span>

## <span data-ttu-id="ced23-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ced23-112">PARAMETERS</span></span>

### <span data-ttu-id="ced23-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="ced23-113">-EndTime</span></span>
<span data-ttu-id="ced23-114">Задает время окончания для задания в виде объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="ced23-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="ced23-115">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="ced23-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="ced23-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="ced23-116">-ErrorActionType</span></span>
<span data-ttu-id="ced23-117">Задает параметр действия при ошибке для задания.</span><span class="sxs-lookup"><span data-stu-id="ced23-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="ced23-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ced23-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ced23-119">Через</span><span class="sxs-lookup"><span data-stu-id="ced23-119">Http</span></span> 
- <span data-ttu-id="ced23-120">Протокол</span><span class="sxs-lookup"><span data-stu-id="ced23-120">Https</span></span> 
- <span data-ttu-id="ced23-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="ced23-121">StorageQueue</span></span> 
- <span data-ttu-id="ced23-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="ced23-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="ced23-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="ced23-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="ced23-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="ced23-124">-ExecutionCount</span></span>
<span data-ttu-id="ced23-125">Задает количество выполняемых заданий.</span><span class="sxs-lookup"><span data-stu-id="ced23-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="ced23-126">По умолчанию задание повторяется неопределенное время.</span><span class="sxs-lookup"><span data-stu-id="ced23-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="ced23-127">-Частота</span><span class="sxs-lookup"><span data-stu-id="ced23-127">-Frequency</span></span>
<span data-ttu-id="ced23-128">Указывает максимальную частоту для задания.</span><span class="sxs-lookup"><span data-stu-id="ced23-128">Specifies the maximum frequency for the job.</span></span>
<span data-ttu-id="ced23-129">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ced23-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ced23-130">До</span><span class="sxs-lookup"><span data-stu-id="ced23-130">Minute</span></span> 
- <span data-ttu-id="ced23-131">Часовой</span><span class="sxs-lookup"><span data-stu-id="ced23-131">Hour</span></span> 
- <span data-ttu-id="ced23-132">Дневных</span><span class="sxs-lookup"><span data-stu-id="ced23-132">Day</span></span> 
- <span data-ttu-id="ced23-133">Недели</span><span class="sxs-lookup"><span data-stu-id="ced23-133">Week</span></span> 
- <span data-ttu-id="ced23-134">Перехода</span><span class="sxs-lookup"><span data-stu-id="ced23-134">Month</span></span>

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

### <span data-ttu-id="ced23-135">-Заголовки</span><span class="sxs-lookup"><span data-stu-id="ced23-135">-Headers</span></span>
<span data-ttu-id="ced23-136">Указывает хэш-таблицу, содержащую заголовки.</span><span class="sxs-lookup"><span data-stu-id="ced23-136">Specifies a hash table that contains headers.</span></span>

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

### <span data-ttu-id="ced23-137">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="ced23-137">-HttpAuthenticationType</span></span>
<span data-ttu-id="ced23-138">Указывает тип проверки подлинности HTTP.</span><span class="sxs-lookup"><span data-stu-id="ced23-138">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="ced23-139">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ced23-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ced23-140">Ничего</span><span class="sxs-lookup"><span data-stu-id="ced23-140">None</span></span> 
- <span data-ttu-id="ced23-141">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ced23-141">ClientCertificate</span></span> 
- <span data-ttu-id="ced23-142">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="ced23-142">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="ced23-143">Базового</span><span class="sxs-lookup"><span data-stu-id="ced23-143">Basic</span></span>

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

### <span data-ttu-id="ced23-144">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="ced23-144">-Interval</span></span>
<span data-ttu-id="ced23-145">Указывает интервал повторения для задания.</span><span class="sxs-lookup"><span data-stu-id="ced23-145">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="ced23-146">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="ced23-146">-JobCollectionName</span></span>
<span data-ttu-id="ced23-147">Указывает имя коллекции заданий, к которой относится задание.</span><span class="sxs-lookup"><span data-stu-id="ced23-147">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="ced23-148">-JobName</span><span class="sxs-lookup"><span data-stu-id="ced23-148">-JobName</span></span>
<span data-ttu-id="ced23-149">Указывает имя задания, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ced23-149">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ced23-150">-JobState</span><span class="sxs-lookup"><span data-stu-id="ced23-150">-JobState</span></span>
<span data-ttu-id="ced23-151">Указывает состояние задания.</span><span class="sxs-lookup"><span data-stu-id="ced23-151">Specifies the state of the job.</span></span>
<span data-ttu-id="ced23-152">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ced23-152">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ced23-153">Включаем</span><span class="sxs-lookup"><span data-stu-id="ced23-153">Enabled</span></span> 
- <span data-ttu-id="ced23-154">Отключает</span><span class="sxs-lookup"><span data-stu-id="ced23-154">Disabled</span></span>

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

### <span data-ttu-id="ced23-155">-Method</span><span class="sxs-lookup"><span data-stu-id="ced23-155">-Method</span></span>
<span data-ttu-id="ced23-156">Указывает метод для типов действий для этого задания.</span><span class="sxs-lookup"><span data-stu-id="ced23-156">Specifies the method for the action types for this job.</span></span>
<span data-ttu-id="ced23-157">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ced23-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ced23-158">Получить</span><span class="sxs-lookup"><span data-stu-id="ced23-158">GET</span></span> 
- <span data-ttu-id="ced23-159">Установка</span><span class="sxs-lookup"><span data-stu-id="ced23-159">PUT</span></span> 
- <span data-ttu-id="ced23-160">Поместить</span><span class="sxs-lookup"><span data-stu-id="ced23-160">POST</span></span> 
- <span data-ttu-id="ced23-161">Удаление</span><span class="sxs-lookup"><span data-stu-id="ced23-161">DELETE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: GET, PUT, POST, DELETE

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ced23-162">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="ced23-162">-RequestBody</span></span>
<span data-ttu-id="ced23-163">Указывает значение тела для действий помещения и публикации.</span><span class="sxs-lookup"><span data-stu-id="ced23-163">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="ced23-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ced23-164">-ResourceGroupName</span></span>
<span data-ttu-id="ced23-165">Указывает группу ресурсов, к которой относится задание.</span><span class="sxs-lookup"><span data-stu-id="ced23-165">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="ced23-166">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ced23-166">-StartTime</span></span>
<span data-ttu-id="ced23-167">Задает время начала в виде объекта **DateTime** для задания.</span><span class="sxs-lookup"><span data-stu-id="ced23-167">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="ced23-168">-URI</span><span class="sxs-lookup"><span data-stu-id="ced23-168">-Uri</span></span>
<span data-ttu-id="ced23-169">Задает универсальный код ресурса (URI) для действия задания.</span><span class="sxs-lookup"><span data-stu-id="ced23-169">Specifies a URI for the job action.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ced23-170">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ced23-170">-Confirm</span></span>
<span data-ttu-id="ced23-171">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ced23-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ced23-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ced23-172">-WhatIf</span></span>
<span data-ttu-id="ced23-173">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ced23-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ced23-174">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ced23-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ced23-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ced23-175">-DefaultProfile</span></span>
<span data-ttu-id="ced23-176">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ced23-176">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ced23-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ced23-177">CommonParameters</span></span>
<span data-ttu-id="ced23-178">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ced23-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ced23-179">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ced23-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ced23-180">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ced23-180">INPUTS</span></span>

## <span data-ttu-id="ced23-181">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ced23-181">OUTPUTS</span></span>

### <span data-ttu-id="ced23-182">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ced23-182">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="ced23-183">Пуск</span><span class="sxs-lookup"><span data-stu-id="ced23-183">NOTES</span></span>

## <span data-ttu-id="ced23-184">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ced23-184">RELATED LINKS</span></span>

[<span data-ttu-id="ced23-185">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="ced23-185">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="ced23-186">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ced23-186">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ced23-187">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="ced23-187">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="ced23-188">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="ced23-188">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="ced23-189">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="ced23-189">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="ced23-190">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ced23-190">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ced23-191">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="ced23-191">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="ced23-192">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="ced23-192">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="ced23-193">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="ced23-193">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


