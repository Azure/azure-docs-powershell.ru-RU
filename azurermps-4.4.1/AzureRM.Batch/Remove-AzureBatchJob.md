---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
ms.openlocfilehash: 0d210056670baa974c7bf11e9c44142c11f2721e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567671"
---
# <span data-ttu-id="8e9ed-101">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8e9ed-101">Remove-AzureBatchJob</span></span>

## <span data-ttu-id="8e9ed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e9ed-102">SYNOPSIS</span></span>
<span data-ttu-id="8e9ed-103">Удаляет пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="8e9ed-103">Deletes a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e9ed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e9ed-104">SYNTAX</span></span>

```
Remove-AzureBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e9ed-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e9ed-105">DESCRIPTION</span></span>
<span data-ttu-id="8e9ed-106">Командлет **Remove-AzureBatchJob** удаляет пакетное задание Azure.</span><span class="sxs-lookup"><span data-stu-id="8e9ed-106">The **Remove-AzureBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="8e9ed-107">Этот командлет запрашивает подтверждение перед удалением задания, если не указан параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="8e9ed-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="8e9ed-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e9ed-108">EXAMPLES</span></span>

### <span data-ttu-id="8e9ed-109">Пример 1: Удаление пакетного задания</span><span class="sxs-lookup"><span data-stu-id="8e9ed-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="8e9ed-110">Эта команда удаляет задание с ИД задания-000001.</span><span class="sxs-lookup"><span data-stu-id="8e9ed-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="8e9ed-111">Команда запрашивает подтверждение перед удалением задания.</span><span class="sxs-lookup"><span data-stu-id="8e9ed-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="8e9ed-112">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="8e9ed-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="8e9ed-113">Пример 2: Удаление пакетного задания без подтверждения с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="8e9ed-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzureBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="8e9ed-114">Эта команда получает задание с ИДЕНТИФИКАТОРом Job 000002 с помощью командлета Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="8e9ed-114">This command gets the job that has the ID Job-000002 by using the Get-AzureBatchJob cmdlet.</span></span>
<span data-ttu-id="8e9ed-115">Команда передает это задание текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="8e9ed-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8e9ed-116">Команда удаляет это задание.</span><span class="sxs-lookup"><span data-stu-id="8e9ed-116">The command deletes that job.</span></span>
<span data-ttu-id="8e9ed-117">Так как команда включает параметр *Force* , она не предлагает подтверждения.</span><span class="sxs-lookup"><span data-stu-id="8e9ed-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8e9ed-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e9ed-118">PARAMETERS</span></span>

### <span data-ttu-id="8e9ed-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8e9ed-119">-BatchContext</span></span>
<span data-ttu-id="8e9ed-120">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="8e9ed-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8e9ed-121">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="8e9ed-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="8e9ed-122">-Force</span><span class="sxs-lookup"><span data-stu-id="8e9ed-122">-Force</span></span>
<span data-ttu-id="8e9ed-123">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8e9ed-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8e9ed-124">-ID</span><span class="sxs-lookup"><span data-stu-id="8e9ed-124">-Id</span></span>
<span data-ttu-id="8e9ed-125">Указывает идентификатор задания, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8e9ed-125">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="8e9ed-126">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="8e9ed-126">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e9ed-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e9ed-127">-Confirm</span></span>
<span data-ttu-id="8e9ed-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8e9ed-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e9ed-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e9ed-129">-WhatIf</span></span>
<span data-ttu-id="8e9ed-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8e9ed-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e9ed-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8e9ed-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e9ed-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e9ed-132">-DefaultProfile</span></span>
<span data-ttu-id="8e9ed-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e9ed-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e9ed-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e9ed-134">CommonParameters</span></span>
<span data-ttu-id="8e9ed-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e9ed-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e9ed-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e9ed-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e9ed-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e9ed-137">INPUTS</span></span>

### <span data-ttu-id="8e9ed-138">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8e9ed-138">BatchAccountContext</span></span>
<span data-ttu-id="8e9ed-139">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="8e9ed-139">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="8e9ed-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e9ed-140">OUTPUTS</span></span>

## <span data-ttu-id="8e9ed-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e9ed-141">NOTES</span></span>

## <span data-ttu-id="8e9ed-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e9ed-142">RELATED LINKS</span></span>

[<span data-ttu-id="8e9ed-143">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8e9ed-143">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="8e9ed-144">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8e9ed-144">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="8e9ed-145">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8e9ed-145">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="8e9ed-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8e9ed-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="8e9ed-147">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8e9ed-147">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="8e9ed-148">Остановить-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8e9ed-148">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="8e9ed-149">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="8e9ed-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


