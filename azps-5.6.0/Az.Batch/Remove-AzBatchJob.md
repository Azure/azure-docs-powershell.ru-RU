---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
ms.openlocfilehash: e4f84e977e19dcd71731eb5ed09cae82dc5b3a0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975587"
---
# <span data-ttu-id="708bc-101">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="708bc-101">Remove-AzBatchJob</span></span>

## <span data-ttu-id="708bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="708bc-102">SYNOPSIS</span></span>
<span data-ttu-id="708bc-103">Удаляет задание пакета.</span><span class="sxs-lookup"><span data-stu-id="708bc-103">Deletes a Batch job.</span></span>

## <span data-ttu-id="708bc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="708bc-104">SYNTAX</span></span>

```
Remove-AzBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="708bc-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="708bc-105">DESCRIPTION</span></span>
<span data-ttu-id="708bc-106">С **его использованием** удаляется задание пакета Azure.</span><span class="sxs-lookup"><span data-stu-id="708bc-106">The **Remove-AzBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="708bc-107">Этот cmdlet запросит подтверждение перед удалением задания, если не указать параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="708bc-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="708bc-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="708bc-108">EXAMPLES</span></span>

### <span data-ttu-id="708bc-109">Пример 1. Удаление задания с пакетом</span><span class="sxs-lookup"><span data-stu-id="708bc-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="708bc-110">Эта команда удаляет задание с ИД-000001.</span><span class="sxs-lookup"><span data-stu-id="708bc-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="708bc-111">Перед удалением задания вам будет предложено подтвердить удаление.</span><span class="sxs-lookup"><span data-stu-id="708bc-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="708bc-112">Используйте Get-AzBatchAccountKey для назначения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="708bc-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="708bc-113">Пример 2. Удаление задания пакета без подтверждения с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="708bc-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="708bc-114">Эта команда получает задание с заданием для задания ИД-000002 с помощью Get-AzBatchJob командлета.</span><span class="sxs-lookup"><span data-stu-id="708bc-114">This command gets the job that has the ID Job-000002 by using the Get-AzBatchJob cmdlet.</span></span>
<span data-ttu-id="708bc-115">Эта команда передает это задание текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="708bc-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="708bc-116">Команда удалит задание.</span><span class="sxs-lookup"><span data-stu-id="708bc-116">The command deletes that job.</span></span>
<span data-ttu-id="708bc-117">Так как команда содержит параметр *Force,* запрос на подтверждение не выдан.</span><span class="sxs-lookup"><span data-stu-id="708bc-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="708bc-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="708bc-118">PARAMETERS</span></span>

### <span data-ttu-id="708bc-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="708bc-119">-BatchContext</span></span>
<span data-ttu-id="708bc-120">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="708bc-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="708bc-121">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="708bc-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="708bc-122">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="708bc-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="708bc-123">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="708bc-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="708bc-124">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="708bc-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="708bc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="708bc-125">-DefaultProfile</span></span>
<span data-ttu-id="708bc-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="708bc-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="708bc-127">-Force</span><span class="sxs-lookup"><span data-stu-id="708bc-127">-Force</span></span>
<span data-ttu-id="708bc-128">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="708bc-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="708bc-129">-Id</span><span class="sxs-lookup"><span data-stu-id="708bc-129">-Id</span></span>
<span data-ttu-id="708bc-130">Определяет код задания, которое этот cmdlet удаляет.</span><span class="sxs-lookup"><span data-stu-id="708bc-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="708bc-131">Поддиавные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="708bc-131">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="708bc-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="708bc-132">-Confirm</span></span>
<span data-ttu-id="708bc-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="708bc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="708bc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="708bc-134">-WhatIf</span></span>
<span data-ttu-id="708bc-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="708bc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="708bc-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="708bc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="708bc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="708bc-137">CommonParameters</span></span>
<span data-ttu-id="708bc-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="708bc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="708bc-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="708bc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="708bc-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="708bc-140">INPUTS</span></span>

### <span data-ttu-id="708bc-141">System.String</span><span class="sxs-lookup"><span data-stu-id="708bc-141">System.String</span></span>

### <span data-ttu-id="708bc-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="708bc-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="708bc-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="708bc-143">OUTPUTS</span></span>

### <span data-ttu-id="708bc-144">System.Void</span><span class="sxs-lookup"><span data-stu-id="708bc-144">System.Void</span></span>

## <span data-ttu-id="708bc-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="708bc-145">NOTES</span></span>

## <span data-ttu-id="708bc-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="708bc-146">RELATED LINKS</span></span>

[<span data-ttu-id="708bc-147">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="708bc-147">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="708bc-148">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="708bc-148">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="708bc-149">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="708bc-149">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="708bc-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="708bc-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="708bc-151">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="708bc-151">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="708bc-152">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="708bc-152">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="708bc-153">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="708bc-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
