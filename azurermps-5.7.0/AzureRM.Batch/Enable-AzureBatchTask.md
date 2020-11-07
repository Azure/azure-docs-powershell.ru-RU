---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
ms.openlocfilehash: 09e2c8dd4ce1eab68eb2a4237e022034696f9769
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734036"
---
# <span data-ttu-id="a6ba0-101">Enable-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a6ba0-101">Enable-AzureBatchTask</span></span>

## <span data-ttu-id="a6ba0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6ba0-102">SYNOPSIS</span></span>
<span data-ttu-id="a6ba0-103">Повторная активация задачи.</span><span class="sxs-lookup"><span data-stu-id="a6ba0-103">Reactivates a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6ba0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6ba0-104">SYNTAX</span></span>

### <span data-ttu-id="a6ba0-105">Номер</span><span class="sxs-lookup"><span data-stu-id="a6ba0-105">Id</span></span>
```
Enable-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6ba0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a6ba0-106">InputObject</span></span>
```
Enable-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6ba0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6ba0-107">DESCRIPTION</span></span>
<span data-ttu-id="a6ba0-108">Командлет **Enable-AzureBatchTask** повторно активирует задачу.</span><span class="sxs-lookup"><span data-stu-id="a6ba0-108">The **Enable-AzureBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="a6ba0-109">Если в задаче исчерпано количество повторных попыток, этот командлет, тем не менее, позволяет ему выполняться.</span><span class="sxs-lookup"><span data-stu-id="a6ba0-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="a6ba0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6ba0-110">EXAMPLES</span></span>

### <span data-ttu-id="a6ba0-111">Пример 1: повторная активация задачи</span><span class="sxs-lookup"><span data-stu-id="a6ba0-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzureBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="a6ba0-112">Эта команда повторно активирует Task2 задачи в задании Job7.</span><span class="sxs-lookup"><span data-stu-id="a6ba0-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="a6ba0-113">Пример 2: повторная активация задачи с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="a6ba0-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="a6ba0-114">Эта команда возвращает пакетную задачу с ИДЕНТИФИКАТОРом Task3 в задании с ИД Job8 с помощью командлета Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="a6ba0-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="a6ba0-115">Команда передает эту задачу текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="a6ba0-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a6ba0-116">Эта команда активирует эту задачу повторно.</span><span class="sxs-lookup"><span data-stu-id="a6ba0-116">The command reactivates that task.</span></span>

## <span data-ttu-id="a6ba0-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6ba0-117">PARAMETERS</span></span>

### <span data-ttu-id="a6ba0-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a6ba0-118">-BatchContext</span></span>
<span data-ttu-id="a6ba0-119">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="a6ba0-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a6ba0-120">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="a6ba0-120">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a6ba0-121">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="a6ba0-121">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a6ba0-122">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="a6ba0-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a6ba0-123">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a6ba0-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6ba0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6ba0-124">-DefaultProfile</span></span>
<span data-ttu-id="a6ba0-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6ba0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6ba0-126">-ID</span><span class="sxs-lookup"><span data-stu-id="a6ba0-126">-Id</span></span>
<span data-ttu-id="a6ba0-127">Указывает идентификатор задачи, которую нужно повторно активировать.</span><span class="sxs-lookup"><span data-stu-id="a6ba0-127">Specifies the ID of the task to reactivate.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6ba0-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="a6ba0-128">-JobId</span></span>
<span data-ttu-id="a6ba0-129">Указывает идентификатор задания, содержащего задачу.</span><span class="sxs-lookup"><span data-stu-id="a6ba0-129">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6ba0-130">-Задача</span><span class="sxs-lookup"><span data-stu-id="a6ba0-130">-Task</span></span>
<span data-ttu-id="a6ba0-131">Указывает задачу, которую повторно активировал этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a6ba0-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="a6ba0-132">Чтобы получить объект **PSCloudTask** , используйте командлет Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="a6ba0-132">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6ba0-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6ba0-133">-Confirm</span></span>
<span data-ttu-id="a6ba0-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a6ba0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6ba0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6ba0-135">-WhatIf</span></span>
<span data-ttu-id="a6ba0-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a6ba0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6ba0-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a6ba0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6ba0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6ba0-138">CommonParameters</span></span>
<span data-ttu-id="a6ba0-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a6ba0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6ba0-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6ba0-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6ba0-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6ba0-141">INPUTS</span></span>

### <span data-ttu-id="a6ba0-142">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a6ba0-142">BatchAccountContext</span></span>
<span data-ttu-id="a6ba0-143">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a6ba0-143">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="a6ba0-144">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="a6ba0-144">PSCloudTask</span></span>
<span data-ttu-id="a6ba0-145">Параметр "задача" принимает значение типа "PSCloudTask" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a6ba0-145">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="a6ba0-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6ba0-146">OUTPUTS</span></span>

## <span data-ttu-id="a6ba0-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6ba0-147">NOTES</span></span>

## <span data-ttu-id="a6ba0-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6ba0-148">RELATED LINKS</span></span>

[<span data-ttu-id="a6ba0-149">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a6ba0-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a6ba0-150">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a6ba0-150">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="a6ba0-151">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a6ba0-151">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="a6ba0-152">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a6ba0-152">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="a6ba0-153">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a6ba0-153">Set-AzureBatchTask</span></span>](./Set-AzureBatchTask.md)

[<span data-ttu-id="a6ba0-154">Остановить-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a6ba0-154">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)


