---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: E00D42D6-707A-479E-9964-C5B80D3DAA6A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerhttpjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: a3fdbb3732def98bbf885cb58bf6f00dcb61eb4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558836"
---
# <span data-ttu-id="45bf0-101">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="45bf0-101">New-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="45bf0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="45bf0-102">SYNOPSIS</span></span>
<span data-ttu-id="45bf0-103">Создание HTTP-задания.</span><span class="sxs-lookup"><span data-stu-id="45bf0-103">Creates an HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45bf0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="45bf0-104">SYNTAX</span></span>

```
New-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -Method <String> -Uri <Uri> [-RequestBody <String>] [-Headers <Hashtable>] [-HttpAuthenticationType <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45bf0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45bf0-105">DESCRIPTION</span></span>
<span data-ttu-id="45bf0-106">Командлет **New-AzureRmSchedulerHttpJob** создает задание HTTP в планировщике Azure.</span><span class="sxs-lookup"><span data-stu-id="45bf0-106">The **New-AzureRmSchedulerHttpJob** cmdlet creates an HTTP job in Azure Scheduler.</span></span>

<span data-ttu-id="45bf0-107">Этот командлет поддерживает динамические параметры, основанные на параметрах *ErrorActionType* и *HttpAuthenticationType* .</span><span class="sxs-lookup"><span data-stu-id="45bf0-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="45bf0-108">Динамические параметры становятся доступны в соответствии с другими значениями параметров.</span><span class="sxs-lookup"><span data-stu-id="45bf0-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="45bf0-109">Чтобы найти имена динамических параметров после указания других параметров, введите дефис (-), а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="45bf0-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="45bf0-110">Если вы не пропустите требуемый параметр, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="45bf0-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="45bf0-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="45bf0-111">EXAMPLES</span></span>

## <span data-ttu-id="45bf0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="45bf0-112">PARAMETERS</span></span>

### <span data-ttu-id="45bf0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45bf0-113">-DefaultProfile</span></span>
<span data-ttu-id="45bf0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45bf0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45bf0-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="45bf0-115">-EndTime</span></span>
<span data-ttu-id="45bf0-116">Задает время окончания для задания в виде объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="45bf0-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="45bf0-117">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="45bf0-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="45bf0-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="45bf0-118">-ErrorActionType</span></span>
<span data-ttu-id="45bf0-119">Задает параметр действия при ошибке для задания.</span><span class="sxs-lookup"><span data-stu-id="45bf0-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="45bf0-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="45bf0-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="45bf0-121">Через</span><span class="sxs-lookup"><span data-stu-id="45bf0-121">Http</span></span> 
- <span data-ttu-id="45bf0-122">Протокол</span><span class="sxs-lookup"><span data-stu-id="45bf0-122">Https</span></span> 
- <span data-ttu-id="45bf0-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="45bf0-123">StorageQueue</span></span> 
- <span data-ttu-id="45bf0-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="45bf0-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="45bf0-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="45bf0-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="45bf0-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="45bf0-126">-ExecutionCount</span></span>
<span data-ttu-id="45bf0-127">Задает количество выполняемых заданий.</span><span class="sxs-lookup"><span data-stu-id="45bf0-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="45bf0-128">По умолчанию задание повторяется неопределенное время.</span><span class="sxs-lookup"><span data-stu-id="45bf0-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="45bf0-129">-Частота</span><span class="sxs-lookup"><span data-stu-id="45bf0-129">-Frequency</span></span>
<span data-ttu-id="45bf0-130">Задает максимальную частоту для задания.</span><span class="sxs-lookup"><span data-stu-id="45bf0-130">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="45bf0-131">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="45bf0-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="45bf0-132">До</span><span class="sxs-lookup"><span data-stu-id="45bf0-132">Minute</span></span> 
- <span data-ttu-id="45bf0-133">Часовой</span><span class="sxs-lookup"><span data-stu-id="45bf0-133">Hour</span></span> 
- <span data-ttu-id="45bf0-134">Дневных</span><span class="sxs-lookup"><span data-stu-id="45bf0-134">Day</span></span> 
- <span data-ttu-id="45bf0-135">Недели</span><span class="sxs-lookup"><span data-stu-id="45bf0-135">Week</span></span> 
- <span data-ttu-id="45bf0-136">Перехода</span><span class="sxs-lookup"><span data-stu-id="45bf0-136">Month</span></span>

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

### <span data-ttu-id="45bf0-137">-Заголовки</span><span class="sxs-lookup"><span data-stu-id="45bf0-137">-Headers</span></span>
<span data-ttu-id="45bf0-138">Указывает хэш-таблицу, содержащую заголовки.</span><span class="sxs-lookup"><span data-stu-id="45bf0-138">Specifies a hash table that contains headers.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45bf0-139">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="45bf0-139">-HttpAuthenticationType</span></span>
<span data-ttu-id="45bf0-140">Указывает тип проверки подлинности HTTP.</span><span class="sxs-lookup"><span data-stu-id="45bf0-140">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="45bf0-141">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="45bf0-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="45bf0-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="45bf0-142">None</span></span> 
- <span data-ttu-id="45bf0-143">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="45bf0-143">ClientCertificate</span></span> 
- <span data-ttu-id="45bf0-144">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="45bf0-144">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="45bf0-145">Базового</span><span class="sxs-lookup"><span data-stu-id="45bf0-145">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, ClientCertificate, ActiveDirectoryOAuth, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45bf0-146">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="45bf0-146">-Interval</span></span>
<span data-ttu-id="45bf0-147">Указывает интервал повторения для задания.</span><span class="sxs-lookup"><span data-stu-id="45bf0-147">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="45bf0-148">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="45bf0-148">-JobCollectionName</span></span>
<span data-ttu-id="45bf0-149">Указывает имя коллекции заданий, к которой относится задание.</span><span class="sxs-lookup"><span data-stu-id="45bf0-149">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="45bf0-150">-JobName</span><span class="sxs-lookup"><span data-stu-id="45bf0-150">-JobName</span></span>
<span data-ttu-id="45bf0-151">Задает имя задания.</span><span class="sxs-lookup"><span data-stu-id="45bf0-151">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="45bf0-152">-JobState</span><span class="sxs-lookup"><span data-stu-id="45bf0-152">-JobState</span></span>
<span data-ttu-id="45bf0-153">Указывает состояние задания.</span><span class="sxs-lookup"><span data-stu-id="45bf0-153">Specifies the state of the job.</span></span>
<span data-ttu-id="45bf0-154">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="45bf0-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="45bf0-155">Включаем</span><span class="sxs-lookup"><span data-stu-id="45bf0-155">Enabled</span></span> 
- <span data-ttu-id="45bf0-156">Отключает</span><span class="sxs-lookup"><span data-stu-id="45bf0-156">Disabled</span></span>

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

### <span data-ttu-id="45bf0-157">-Method</span><span class="sxs-lookup"><span data-stu-id="45bf0-157">-Method</span></span>
<span data-ttu-id="45bf0-158">Указывает метод для типов действий для задания.</span><span class="sxs-lookup"><span data-stu-id="45bf0-158">Specifies the method for the action types for the job.</span></span>
<span data-ttu-id="45bf0-159">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="45bf0-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="45bf0-160">Получить</span><span class="sxs-lookup"><span data-stu-id="45bf0-160">GET</span></span> 
- <span data-ttu-id="45bf0-161">Установка</span><span class="sxs-lookup"><span data-stu-id="45bf0-161">PUT</span></span> 
- <span data-ttu-id="45bf0-162">Поместить</span><span class="sxs-lookup"><span data-stu-id="45bf0-162">POST</span></span> 
- <span data-ttu-id="45bf0-163">Удаление</span><span class="sxs-lookup"><span data-stu-id="45bf0-163">DELETE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: GET, PUT, POST, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45bf0-164">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="45bf0-164">-RequestBody</span></span>
<span data-ttu-id="45bf0-165">Указывает значение тела для действий помещения и публикации.</span><span class="sxs-lookup"><span data-stu-id="45bf0-165">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="45bf0-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45bf0-166">-ResourceGroupName</span></span>
<span data-ttu-id="45bf0-167">Указывает группу ресурсов, к которой относится задание.</span><span class="sxs-lookup"><span data-stu-id="45bf0-167">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="45bf0-168">-StartTime</span><span class="sxs-lookup"><span data-stu-id="45bf0-168">-StartTime</span></span>
<span data-ttu-id="45bf0-169">Задает время начала в виде объекта **DateTime** для задания.</span><span class="sxs-lookup"><span data-stu-id="45bf0-169">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="45bf0-170">-URI</span><span class="sxs-lookup"><span data-stu-id="45bf0-170">-Uri</span></span>
<span data-ttu-id="45bf0-171">Задает универсальный код ресурса (URI) для действия задания.</span><span class="sxs-lookup"><span data-stu-id="45bf0-171">Specifies a URI for the job action.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45bf0-172">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45bf0-172">-Confirm</span></span>
<span data-ttu-id="45bf0-173">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="45bf0-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45bf0-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45bf0-174">-WhatIf</span></span>
<span data-ttu-id="45bf0-175">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="45bf0-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45bf0-176">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="45bf0-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45bf0-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45bf0-177">CommonParameters</span></span>
<span data-ttu-id="45bf0-178">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="45bf0-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45bf0-179">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45bf0-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45bf0-180">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="45bf0-180">INPUTS</span></span>

### <span data-ttu-id="45bf0-181">Ничего</span><span class="sxs-lookup"><span data-stu-id="45bf0-181">None</span></span>
<span data-ttu-id="45bf0-182">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="45bf0-182">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="45bf0-183">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="45bf0-183">OUTPUTS</span></span>

### <span data-ttu-id="45bf0-184">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="45bf0-184">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="45bf0-185">Пуск</span><span class="sxs-lookup"><span data-stu-id="45bf0-185">NOTES</span></span>

## <span data-ttu-id="45bf0-186">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45bf0-186">RELATED LINKS</span></span>

[<span data-ttu-id="45bf0-187">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="45bf0-187">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="45bf0-188">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="45bf0-188">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="45bf0-189">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="45bf0-189">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="45bf0-190">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="45bf0-190">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="45bf0-191">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="45bf0-191">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="45bf0-192">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="45bf0-192">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="45bf0-193">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="45bf0-193">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="45bf0-194">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="45bf0-194">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="45bf0-195">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="45bf0-195">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


