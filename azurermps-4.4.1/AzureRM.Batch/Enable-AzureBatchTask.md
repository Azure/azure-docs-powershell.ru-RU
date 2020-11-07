---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
ms.openlocfilehash: 8e7636d83b953997ac1f9269e45fbf3c2278612f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734903"
---
# <span data-ttu-id="5b283-101">Enable-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="5b283-101">Enable-AzureBatchTask</span></span>

## <span data-ttu-id="5b283-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5b283-102">SYNOPSIS</span></span>
<span data-ttu-id="5b283-103">Повторная активация задачи.</span><span class="sxs-lookup"><span data-stu-id="5b283-103">Reactivates a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b283-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5b283-104">SYNTAX</span></span>

### <span data-ttu-id="5b283-105">Номер</span><span class="sxs-lookup"><span data-stu-id="5b283-105">Id</span></span>
```
Enable-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b283-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5b283-106">InputObject</span></span>
```
Enable-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b283-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b283-107">DESCRIPTION</span></span>
<span data-ttu-id="5b283-108">Командлет **Enable-AzureBatchTask** повторно активирует задачу.</span><span class="sxs-lookup"><span data-stu-id="5b283-108">The **Enable-AzureBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="5b283-109">Если в задаче исчерпано количество повторных попыток, этот командлет, тем не менее, позволяет ему выполняться.</span><span class="sxs-lookup"><span data-stu-id="5b283-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="5b283-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5b283-110">EXAMPLES</span></span>

### <span data-ttu-id="5b283-111">Пример 1: повторная активация задачи</span><span class="sxs-lookup"><span data-stu-id="5b283-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzureBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="5b283-112">Эта команда повторно активирует Task2 задачи в задании Job7.</span><span class="sxs-lookup"><span data-stu-id="5b283-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="5b283-113">Пример 2: повторная активация задачи с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="5b283-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="5b283-114">Эта команда возвращает пакетную задачу с ИДЕНТИФИКАТОРом Task3 в задании с ИД Job8 с помощью командлета Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="5b283-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="5b283-115">Команда передает эту задачу текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="5b283-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5b283-116">Эта команда активирует эту задачу повторно.</span><span class="sxs-lookup"><span data-stu-id="5b283-116">The command reactivates that task.</span></span>

## <span data-ttu-id="5b283-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5b283-117">PARAMETERS</span></span>

### <span data-ttu-id="5b283-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5b283-118">-BatchContext</span></span>
<span data-ttu-id="5b283-119">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="5b283-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5b283-120">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="5b283-120">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b283-121">-ID</span><span class="sxs-lookup"><span data-stu-id="5b283-121">-Id</span></span>
<span data-ttu-id="5b283-122">Указывает идентификатор задачи, которую нужно повторно активировать.</span><span class="sxs-lookup"><span data-stu-id="5b283-122">Specifies the ID of the task to reactivate.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b283-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="5b283-123">-JobId</span></span>
<span data-ttu-id="5b283-124">Указывает идентификатор задания, содержащего задачу.</span><span class="sxs-lookup"><span data-stu-id="5b283-124">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b283-125">-Задача</span><span class="sxs-lookup"><span data-stu-id="5b283-125">-Task</span></span>
<span data-ttu-id="5b283-126">Указывает задачу, которую повторно активировал этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5b283-126">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="5b283-127">Чтобы получить объект **PSCloudTask** , используйте командлет Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="5b283-127">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b283-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b283-128">-Confirm</span></span>
<span data-ttu-id="5b283-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5b283-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b283-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b283-130">-WhatIf</span></span>
<span data-ttu-id="5b283-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5b283-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b283-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5b283-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b283-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b283-133">-DefaultProfile</span></span>
<span data-ttu-id="5b283-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b283-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b283-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b283-135">CommonParameters</span></span>
<span data-ttu-id="5b283-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5b283-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b283-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b283-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b283-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5b283-138">INPUTS</span></span>

### <span data-ttu-id="5b283-139">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5b283-139">BatchAccountContext</span></span>
<span data-ttu-id="5b283-140">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="5b283-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="5b283-141">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="5b283-141">PSCloudTask</span></span>
<span data-ttu-id="5b283-142">Параметр "задача" принимает значение типа "PSCloudTask" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="5b283-142">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="5b283-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b283-143">OUTPUTS</span></span>

## <span data-ttu-id="5b283-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="5b283-144">NOTES</span></span>

## <span data-ttu-id="5b283-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b283-145">RELATED LINKS</span></span>

[<span data-ttu-id="5b283-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5b283-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="5b283-147">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="5b283-147">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="5b283-148">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="5b283-148">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="5b283-149">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="5b283-149">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="5b283-150">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="5b283-150">Set-AzureBatchTask</span></span>](./Set-AzureBatchTask.md)

[<span data-ttu-id="5b283-151">Остановить-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="5b283-151">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)


