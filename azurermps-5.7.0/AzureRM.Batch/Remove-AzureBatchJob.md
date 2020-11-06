---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
ms.openlocfilehash: f6a7d03370184b45cc8066e2f17842187cbab98c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568647"
---
# <span data-ttu-id="39c3a-101">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="39c3a-101">Remove-AzureBatchJob</span></span>

## <span data-ttu-id="39c3a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="39c3a-102">SYNOPSIS</span></span>
<span data-ttu-id="39c3a-103">Удаляет пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="39c3a-103">Deletes a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39c3a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="39c3a-104">SYNTAX</span></span>

```
Remove-AzureBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39c3a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39c3a-105">DESCRIPTION</span></span>
<span data-ttu-id="39c3a-106">Командлет **Remove-AzureBatchJob** удаляет пакетное задание Azure.</span><span class="sxs-lookup"><span data-stu-id="39c3a-106">The **Remove-AzureBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="39c3a-107">Этот командлет запрашивает подтверждение перед удалением задания, если не указан параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="39c3a-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="39c3a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="39c3a-108">EXAMPLES</span></span>

### <span data-ttu-id="39c3a-109">Пример 1: Удаление пакетного задания</span><span class="sxs-lookup"><span data-stu-id="39c3a-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="39c3a-110">Эта команда удаляет задание с ИД задания-000001.</span><span class="sxs-lookup"><span data-stu-id="39c3a-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="39c3a-111">Команда запрашивает подтверждение перед удалением задания.</span><span class="sxs-lookup"><span data-stu-id="39c3a-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="39c3a-112">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="39c3a-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="39c3a-113">Пример 2: Удаление пакетного задания без подтверждения с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="39c3a-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzureBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="39c3a-114">Эта команда получает задание с ИДЕНТИФИКАТОРом Job 000002 с помощью командлета Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="39c3a-114">This command gets the job that has the ID Job-000002 by using the Get-AzureBatchJob cmdlet.</span></span>
<span data-ttu-id="39c3a-115">Команда передает это задание текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="39c3a-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="39c3a-116">Команда удаляет это задание.</span><span class="sxs-lookup"><span data-stu-id="39c3a-116">The command deletes that job.</span></span>
<span data-ttu-id="39c3a-117">Так как команда включает параметр *Force* , она не предлагает подтверждения.</span><span class="sxs-lookup"><span data-stu-id="39c3a-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="39c3a-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="39c3a-118">PARAMETERS</span></span>

### <span data-ttu-id="39c3a-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="39c3a-119">-BatchContext</span></span>
<span data-ttu-id="39c3a-120">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="39c3a-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="39c3a-121">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="39c3a-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="39c3a-122">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="39c3a-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="39c3a-123">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="39c3a-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="39c3a-124">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="39c3a-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="39c3a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39c3a-125">-DefaultProfile</span></span>
<span data-ttu-id="39c3a-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39c3a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39c3a-127">-Force</span><span class="sxs-lookup"><span data-stu-id="39c3a-127">-Force</span></span>
<span data-ttu-id="39c3a-128">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="39c3a-128">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39c3a-129">-ID</span><span class="sxs-lookup"><span data-stu-id="39c3a-129">-Id</span></span>
<span data-ttu-id="39c3a-130">Указывает идентификатор задания, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="39c3a-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="39c3a-131">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="39c3a-131">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39c3a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39c3a-132">-Confirm</span></span>
<span data-ttu-id="39c3a-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="39c3a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39c3a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39c3a-134">-WhatIf</span></span>
<span data-ttu-id="39c3a-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="39c3a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39c3a-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="39c3a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39c3a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39c3a-137">CommonParameters</span></span>
<span data-ttu-id="39c3a-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="39c3a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39c3a-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39c3a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39c3a-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="39c3a-140">INPUTS</span></span>

### <span data-ttu-id="39c3a-141">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="39c3a-141">BatchAccountContext</span></span>
<span data-ttu-id="39c3a-142">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="39c3a-142">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="39c3a-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="39c3a-143">OUTPUTS</span></span>

## <span data-ttu-id="39c3a-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="39c3a-144">NOTES</span></span>

## <span data-ttu-id="39c3a-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39c3a-145">RELATED LINKS</span></span>

[<span data-ttu-id="39c3a-146">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="39c3a-146">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="39c3a-147">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="39c3a-147">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="39c3a-148">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="39c3a-148">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="39c3a-149">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="39c3a-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="39c3a-150">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="39c3a-150">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="39c3a-151">Остановить-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="39c3a-151">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="39c3a-152">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="39c3a-152">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


