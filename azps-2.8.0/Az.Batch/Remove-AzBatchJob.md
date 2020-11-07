---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
ms.openlocfilehash: 4d15680902cb324561983877fef317d20ed94704
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93913143"
---
# <span data-ttu-id="ce6bf-101">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="ce6bf-101">Remove-AzBatchJob</span></span>

## <span data-ttu-id="ce6bf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ce6bf-102">SYNOPSIS</span></span>
<span data-ttu-id="ce6bf-103">Удаляет пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="ce6bf-103">Deletes a Batch job.</span></span>

## <span data-ttu-id="ce6bf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ce6bf-104">SYNTAX</span></span>

```
Remove-AzBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce6bf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce6bf-105">DESCRIPTION</span></span>
<span data-ttu-id="ce6bf-106">Командлет **Remove-AzBatchJob** удаляет пакетное задание Azure.</span><span class="sxs-lookup"><span data-stu-id="ce6bf-106">The **Remove-AzBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="ce6bf-107">Этот командлет запрашивает подтверждение перед удалением задания, если не указан параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="ce6bf-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="ce6bf-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ce6bf-108">EXAMPLES</span></span>

### <span data-ttu-id="ce6bf-109">Пример 1: Удаление пакетного задания</span><span class="sxs-lookup"><span data-stu-id="ce6bf-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="ce6bf-110">Эта команда удаляет задание с ИД задания-000001.</span><span class="sxs-lookup"><span data-stu-id="ce6bf-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="ce6bf-111">Команда запрашивает подтверждение перед удалением задания.</span><span class="sxs-lookup"><span data-stu-id="ce6bf-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="ce6bf-112">Используйте командлет Get-AzBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="ce6bf-112">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ce6bf-113">Пример 2: Удаление пакетного задания без подтверждения с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="ce6bf-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="ce6bf-114">Эта команда получает задание с ИДЕНТИФИКАТОРом Job 000002 с помощью командлета Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="ce6bf-114">This command gets the job that has the ID Job-000002 by using the Get-AzBatchJob cmdlet.</span></span>
<span data-ttu-id="ce6bf-115">Команда передает это задание текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="ce6bf-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ce6bf-116">Команда удаляет это задание.</span><span class="sxs-lookup"><span data-stu-id="ce6bf-116">The command deletes that job.</span></span>
<span data-ttu-id="ce6bf-117">Так как команда включает параметр *Force* , она не предлагает подтверждения.</span><span class="sxs-lookup"><span data-stu-id="ce6bf-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ce6bf-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ce6bf-118">PARAMETERS</span></span>

### <span data-ttu-id="ce6bf-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ce6bf-119">-BatchContext</span></span>
<span data-ttu-id="ce6bf-120">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="ce6bf-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ce6bf-121">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="ce6bf-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ce6bf-122">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="ce6bf-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ce6bf-123">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="ce6bf-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ce6bf-124">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ce6bf-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ce6bf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce6bf-125">-DefaultProfile</span></span>
<span data-ttu-id="ce6bf-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ce6bf-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce6bf-127">-Force</span><span class="sxs-lookup"><span data-stu-id="ce6bf-127">-Force</span></span>
<span data-ttu-id="ce6bf-128">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ce6bf-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ce6bf-129">-ID</span><span class="sxs-lookup"><span data-stu-id="ce6bf-129">-Id</span></span>
<span data-ttu-id="ce6bf-130">Указывает идентификатор задания, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ce6bf-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="ce6bf-131">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="ce6bf-131">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="ce6bf-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce6bf-132">-Confirm</span></span>
<span data-ttu-id="ce6bf-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ce6bf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce6bf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce6bf-134">-WhatIf</span></span>
<span data-ttu-id="ce6bf-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ce6bf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce6bf-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ce6bf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce6bf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce6bf-137">CommonParameters</span></span>
<span data-ttu-id="ce6bf-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ce6bf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce6bf-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce6bf-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce6bf-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ce6bf-140">INPUTS</span></span>

### <span data-ttu-id="ce6bf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ce6bf-141">System.String</span></span>

### <span data-ttu-id="ce6bf-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ce6bf-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ce6bf-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce6bf-143">OUTPUTS</span></span>

### <span data-ttu-id="ce6bf-144">System. void</span><span class="sxs-lookup"><span data-stu-id="ce6bf-144">System.Void</span></span>

## <span data-ttu-id="ce6bf-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="ce6bf-145">NOTES</span></span>

## <span data-ttu-id="ce6bf-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce6bf-146">RELATED LINKS</span></span>

[<span data-ttu-id="ce6bf-147">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="ce6bf-147">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="ce6bf-148">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="ce6bf-148">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="ce6bf-149">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="ce6bf-149">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="ce6bf-150">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ce6bf-150">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ce6bf-151">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="ce6bf-151">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="ce6bf-152">Остановить-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="ce6bf-152">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="ce6bf-153">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="ce6bf-153">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


