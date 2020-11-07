---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: E00D42D6-707A-479E-9964-C5B80D3DAA6A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 5fc591ff5d24211b8af464dab46bfb81360f83e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733625"
---
# <span data-ttu-id="64947-101">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="64947-101">New-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="64947-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="64947-102">SYNOPSIS</span></span>
<span data-ttu-id="64947-103">Создание HTTP-задания.</span><span class="sxs-lookup"><span data-stu-id="64947-103">Creates an HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64947-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="64947-104">SYNTAX</span></span>

```
New-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -Method <String> -Uri <Uri> [-RequestBody <String>] [-Headers <Hashtable>] [-HttpAuthenticationType <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64947-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64947-105">DESCRIPTION</span></span>
<span data-ttu-id="64947-106">Командлет **New-AzureRmSchedulerHttpJob** создает задание HTTP в планировщике Azure.</span><span class="sxs-lookup"><span data-stu-id="64947-106">The **New-AzureRmSchedulerHttpJob** cmdlet creates an HTTP job in Azure Scheduler.</span></span>

<span data-ttu-id="64947-107">Этот командлет поддерживает динамические параметры, основанные на параметрах *ErrorActionType* и *HttpAuthenticationType* .</span><span class="sxs-lookup"><span data-stu-id="64947-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="64947-108">Динамические параметры становятся доступны в соответствии с другими значениями параметров.</span><span class="sxs-lookup"><span data-stu-id="64947-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="64947-109">Чтобы найти имена динамических параметров после указания других параметров, введите дефис (-), а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="64947-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="64947-110">Если вы не пропустите требуемый параметр, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="64947-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="64947-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="64947-111">EXAMPLES</span></span>

## <span data-ttu-id="64947-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="64947-112">PARAMETERS</span></span>

### <span data-ttu-id="64947-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="64947-113">-EndTime</span></span>
<span data-ttu-id="64947-114">Задает время окончания для задания в виде объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="64947-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="64947-115">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="64947-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="64947-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="64947-116">-ErrorActionType</span></span>
<span data-ttu-id="64947-117">Задает параметр действия при ошибке для задания.</span><span class="sxs-lookup"><span data-stu-id="64947-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="64947-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="64947-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64947-119">Через</span><span class="sxs-lookup"><span data-stu-id="64947-119">Http</span></span> 
- <span data-ttu-id="64947-120">Протокол</span><span class="sxs-lookup"><span data-stu-id="64947-120">Https</span></span> 
- <span data-ttu-id="64947-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="64947-121">StorageQueue</span></span> 
- <span data-ttu-id="64947-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="64947-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="64947-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="64947-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="64947-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="64947-124">-ExecutionCount</span></span>
<span data-ttu-id="64947-125">Задает количество выполняемых заданий.</span><span class="sxs-lookup"><span data-stu-id="64947-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="64947-126">По умолчанию задание повторяется неопределенное время.</span><span class="sxs-lookup"><span data-stu-id="64947-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="64947-127">-Частота</span><span class="sxs-lookup"><span data-stu-id="64947-127">-Frequency</span></span>
<span data-ttu-id="64947-128">Задает максимальную частоту для задания.</span><span class="sxs-lookup"><span data-stu-id="64947-128">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="64947-129">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="64947-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64947-130">До</span><span class="sxs-lookup"><span data-stu-id="64947-130">Minute</span></span> 
- <span data-ttu-id="64947-131">Часовой</span><span class="sxs-lookup"><span data-stu-id="64947-131">Hour</span></span> 
- <span data-ttu-id="64947-132">Дневных</span><span class="sxs-lookup"><span data-stu-id="64947-132">Day</span></span> 
- <span data-ttu-id="64947-133">Недели</span><span class="sxs-lookup"><span data-stu-id="64947-133">Week</span></span> 
- <span data-ttu-id="64947-134">Перехода</span><span class="sxs-lookup"><span data-stu-id="64947-134">Month</span></span>

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

### <span data-ttu-id="64947-135">-Заголовки</span><span class="sxs-lookup"><span data-stu-id="64947-135">-Headers</span></span>
<span data-ttu-id="64947-136">Указывает хэш-таблицу, содержащую заголовки.</span><span class="sxs-lookup"><span data-stu-id="64947-136">Specifies a hash table that contains headers.</span></span>

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

### <span data-ttu-id="64947-137">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="64947-137">-HttpAuthenticationType</span></span>
<span data-ttu-id="64947-138">Указывает тип проверки подлинности HTTP.</span><span class="sxs-lookup"><span data-stu-id="64947-138">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="64947-139">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="64947-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64947-140">Ничего</span><span class="sxs-lookup"><span data-stu-id="64947-140">None</span></span> 
- <span data-ttu-id="64947-141">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="64947-141">ClientCertificate</span></span> 
- <span data-ttu-id="64947-142">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="64947-142">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="64947-143">Базового</span><span class="sxs-lookup"><span data-stu-id="64947-143">Basic</span></span>

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

### <span data-ttu-id="64947-144">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="64947-144">-Interval</span></span>
<span data-ttu-id="64947-145">Указывает интервал повторения для задания.</span><span class="sxs-lookup"><span data-stu-id="64947-145">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="64947-146">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="64947-146">-JobCollectionName</span></span>
<span data-ttu-id="64947-147">Указывает имя коллекции заданий, к которой относится задание.</span><span class="sxs-lookup"><span data-stu-id="64947-147">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="64947-148">-JobName</span><span class="sxs-lookup"><span data-stu-id="64947-148">-JobName</span></span>
<span data-ttu-id="64947-149">Задает имя задания.</span><span class="sxs-lookup"><span data-stu-id="64947-149">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="64947-150">-JobState</span><span class="sxs-lookup"><span data-stu-id="64947-150">-JobState</span></span>
<span data-ttu-id="64947-151">Указывает состояние задания.</span><span class="sxs-lookup"><span data-stu-id="64947-151">Specifies the state of the job.</span></span>
<span data-ttu-id="64947-152">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="64947-152">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64947-153">Включаем</span><span class="sxs-lookup"><span data-stu-id="64947-153">Enabled</span></span> 
- <span data-ttu-id="64947-154">Отключает</span><span class="sxs-lookup"><span data-stu-id="64947-154">Disabled</span></span>

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

### <span data-ttu-id="64947-155">-Method</span><span class="sxs-lookup"><span data-stu-id="64947-155">-Method</span></span>
<span data-ttu-id="64947-156">Указывает метод для типов действий для задания.</span><span class="sxs-lookup"><span data-stu-id="64947-156">Specifies the method for the action types for the job.</span></span>
<span data-ttu-id="64947-157">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="64947-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64947-158">Получить</span><span class="sxs-lookup"><span data-stu-id="64947-158">GET</span></span> 
- <span data-ttu-id="64947-159">Установка</span><span class="sxs-lookup"><span data-stu-id="64947-159">PUT</span></span> 
- <span data-ttu-id="64947-160">Поместить</span><span class="sxs-lookup"><span data-stu-id="64947-160">POST</span></span> 
- <span data-ttu-id="64947-161">Удаление</span><span class="sxs-lookup"><span data-stu-id="64947-161">DELETE</span></span>

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

### <span data-ttu-id="64947-162">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="64947-162">-RequestBody</span></span>
<span data-ttu-id="64947-163">Указывает значение тела для действий помещения и публикации.</span><span class="sxs-lookup"><span data-stu-id="64947-163">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="64947-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64947-164">-ResourceGroupName</span></span>
<span data-ttu-id="64947-165">Указывает группу ресурсов, к которой относится задание.</span><span class="sxs-lookup"><span data-stu-id="64947-165">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="64947-166">-StartTime</span><span class="sxs-lookup"><span data-stu-id="64947-166">-StartTime</span></span>
<span data-ttu-id="64947-167">Задает время начала в виде объекта **DateTime** для задания.</span><span class="sxs-lookup"><span data-stu-id="64947-167">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="64947-168">-URI</span><span class="sxs-lookup"><span data-stu-id="64947-168">-Uri</span></span>
<span data-ttu-id="64947-169">Задает универсальный код ресурса (URI) для действия задания.</span><span class="sxs-lookup"><span data-stu-id="64947-169">Specifies a URI for the job action.</span></span>

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

### <span data-ttu-id="64947-170">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64947-170">-Confirm</span></span>
<span data-ttu-id="64947-171">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="64947-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64947-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64947-172">-WhatIf</span></span>
<span data-ttu-id="64947-173">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="64947-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64947-174">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="64947-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64947-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64947-175">-DefaultProfile</span></span>
<span data-ttu-id="64947-176">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="64947-176">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64947-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64947-177">CommonParameters</span></span>
<span data-ttu-id="64947-178">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="64947-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64947-179">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64947-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64947-180">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="64947-180">INPUTS</span></span>

## <span data-ttu-id="64947-181">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="64947-181">OUTPUTS</span></span>

### <span data-ttu-id="64947-182">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="64947-182">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="64947-183">Пуск</span><span class="sxs-lookup"><span data-stu-id="64947-183">NOTES</span></span>

## <span data-ttu-id="64947-184">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64947-184">RELATED LINKS</span></span>

[<span data-ttu-id="64947-185">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="64947-185">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="64947-186">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="64947-186">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="64947-187">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="64947-187">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="64947-188">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="64947-188">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="64947-189">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="64947-189">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="64947-190">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="64947-190">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="64947-191">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="64947-191">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="64947-192">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="64947-192">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="64947-193">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="64947-193">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


