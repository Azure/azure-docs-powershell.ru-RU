---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
ms.openlocfilehash: 6200ee0d929aaadccb8e2be0e8fb646929907d73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567670"
---
# <span data-ttu-id="58d94-101">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="58d94-101">Remove-AzureBatchTask</span></span>

## <span data-ttu-id="58d94-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="58d94-102">SYNOPSIS</span></span>
<span data-ttu-id="58d94-103">Удаляет пакетную задачу.</span><span class="sxs-lookup"><span data-stu-id="58d94-103">Deletes a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58d94-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="58d94-104">SYNTAX</span></span>

### <span data-ttu-id="58d94-105">Номер</span><span class="sxs-lookup"><span data-stu-id="58d94-105">Id</span></span>
```
Remove-AzureBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58d94-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="58d94-106">InputObject</span></span>
```
Remove-AzureBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58d94-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58d94-107">DESCRIPTION</span></span>
<span data-ttu-id="58d94-108">Командлет **Remove-AzureBatchTask** удаляет пакетную задачу Azure.</span><span class="sxs-lookup"><span data-stu-id="58d94-108">The **Remove-AzureBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="58d94-109">Этот командлет запрашивает подтверждение, если не указан параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="58d94-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="58d94-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="58d94-110">EXAMPLES</span></span>

### <span data-ttu-id="58d94-111">Пример 1: удаление пакетной задачи по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="58d94-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="58d94-112">Эта команда удаляет задачу с ИДЕНТИФИКАТОРом Task23 под заданием с ИД задания 000001.</span><span class="sxs-lookup"><span data-stu-id="58d94-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="58d94-113">В командной строке появится запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="58d94-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="58d94-114">Используйте командлет **Get-AzureRmBatchAccountKeys** , чтобы назначить контекст переменной $context.</span><span class="sxs-lookup"><span data-stu-id="58d94-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="58d94-115">Пример 2: удаление пакетной задачи с помощью конвейера без подтверждения</span><span class="sxs-lookup"><span data-stu-id="58d94-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzureBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="58d94-116">Эта команда получает пакетную задачу с ИДЕНТИФИКАТОРом Task26 в задании с ИД задания 000001 с помощью командлета **Get-AzureBatchTask** .</span><span class="sxs-lookup"><span data-stu-id="58d94-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzureBatchTask** cmdlet.</span></span>
<span data-ttu-id="58d94-117">Команда передает эту задачу текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="58d94-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="58d94-118">Команда удаляет эту задачу.</span><span class="sxs-lookup"><span data-stu-id="58d94-118">The command deletes that task.</span></span>
<span data-ttu-id="58d94-119">Эта команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="58d94-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="58d94-120">Таким образом, команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="58d94-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="58d94-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="58d94-121">PARAMETERS</span></span>

### <span data-ttu-id="58d94-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="58d94-122">-BatchContext</span></span>
<span data-ttu-id="58d94-123">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="58d94-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="58d94-124">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="58d94-124">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="58d94-125">-Force</span><span class="sxs-lookup"><span data-stu-id="58d94-125">-Force</span></span>
<span data-ttu-id="58d94-126">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="58d94-126">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58d94-127">-ID</span><span class="sxs-lookup"><span data-stu-id="58d94-127">-Id</span></span>
<span data-ttu-id="58d94-128">Указывает идентификатор задачи, которую этот командлет удаляет.</span><span class="sxs-lookup"><span data-stu-id="58d94-128">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="58d94-129">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="58d94-129">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="58d94-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58d94-130">-InputObject</span></span>
<span data-ttu-id="58d94-131">Указывает задачу, которую этот командлет удаляет.</span><span class="sxs-lookup"><span data-stu-id="58d94-131">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="58d94-132">Чтобы получить объект **PSCloudTask** , используйте командлет Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="58d94-132">To obtain a **PSCloudTask** object, use  the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="58d94-133">-JobId</span><span class="sxs-lookup"><span data-stu-id="58d94-133">-JobId</span></span>
<span data-ttu-id="58d94-134">Указывает идентификатор задания, содержащего задачу.</span><span class="sxs-lookup"><span data-stu-id="58d94-134">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="58d94-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58d94-135">-Confirm</span></span>
<span data-ttu-id="58d94-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="58d94-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58d94-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58d94-137">-WhatIf</span></span>
<span data-ttu-id="58d94-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="58d94-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58d94-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="58d94-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58d94-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58d94-140">-DefaultProfile</span></span>
<span data-ttu-id="58d94-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="58d94-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58d94-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58d94-142">CommonParameters</span></span>
<span data-ttu-id="58d94-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="58d94-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58d94-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58d94-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58d94-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="58d94-145">INPUTS</span></span>

### <span data-ttu-id="58d94-146">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="58d94-146">BatchAccountContext</span></span>
<span data-ttu-id="58d94-147">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="58d94-147">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="58d94-148">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="58d94-148">PSCloudTask</span></span>
<span data-ttu-id="58d94-149">Параметр "InputObject" принимает значение типа "PSCloudTask" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="58d94-149">Parameter 'InputObject' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="58d94-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="58d94-150">OUTPUTS</span></span>

## <span data-ttu-id="58d94-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="58d94-151">NOTES</span></span>

## <span data-ttu-id="58d94-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58d94-152">RELATED LINKS</span></span>

[<span data-ttu-id="58d94-153">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="58d94-153">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="58d94-154">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="58d94-154">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="58d94-155">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="58d94-155">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="58d94-156">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="58d94-156">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="58d94-157">Остановить-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="58d94-157">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="58d94-158">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="58d94-158">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


