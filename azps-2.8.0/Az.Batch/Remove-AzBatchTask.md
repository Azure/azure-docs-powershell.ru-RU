---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
ms.openlocfilehash: c2b198359bbd793353c9b416a631d94cad0709fa
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93913154"
---
# <span data-ttu-id="4701f-101">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="4701f-101">Remove-AzBatchTask</span></span>

## <span data-ttu-id="4701f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4701f-102">SYNOPSIS</span></span>
<span data-ttu-id="4701f-103">Удаляет пакетную задачу.</span><span class="sxs-lookup"><span data-stu-id="4701f-103">Deletes a Batch task.</span></span>

## <span data-ttu-id="4701f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4701f-104">SYNTAX</span></span>

### <span data-ttu-id="4701f-105">Номер</span><span class="sxs-lookup"><span data-stu-id="4701f-105">Id</span></span>
```
Remove-AzBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4701f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4701f-106">InputObject</span></span>
```
Remove-AzBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4701f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4701f-107">DESCRIPTION</span></span>
<span data-ttu-id="4701f-108">Командлет **Remove-AzBatchTask** удаляет пакетную задачу Azure.</span><span class="sxs-lookup"><span data-stu-id="4701f-108">The **Remove-AzBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="4701f-109">Этот командлет запрашивает подтверждение, если не указан параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="4701f-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="4701f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4701f-110">EXAMPLES</span></span>

### <span data-ttu-id="4701f-111">Пример 1: удаление пакетной задачи по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="4701f-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="4701f-112">Эта команда удаляет задачу с ИДЕНТИФИКАТОРом Task23 под заданием с ИД задания 000001.</span><span class="sxs-lookup"><span data-stu-id="4701f-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="4701f-113">В командной строке появится запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4701f-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="4701f-114">Используйте командлет **Get-AzBatchAccountKeys** , чтобы назначить контекст переменной $context.</span><span class="sxs-lookup"><span data-stu-id="4701f-114">Use the **Get-AzBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="4701f-115">Пример 2: удаление пакетной задачи с помощью конвейера без подтверждения</span><span class="sxs-lookup"><span data-stu-id="4701f-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="4701f-116">Эта команда получает пакетную задачу с ИДЕНТИФИКАТОРом Task26 в задании с ИД задания 000001 с помощью командлета **Get-AzBatchTask** .</span><span class="sxs-lookup"><span data-stu-id="4701f-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzBatchTask** cmdlet.</span></span>
<span data-ttu-id="4701f-117">Команда передает эту задачу текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="4701f-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4701f-118">Команда удаляет эту задачу.</span><span class="sxs-lookup"><span data-stu-id="4701f-118">The command deletes that task.</span></span>
<span data-ttu-id="4701f-119">Эта команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="4701f-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="4701f-120">Таким образом, команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4701f-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="4701f-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4701f-121">PARAMETERS</span></span>

### <span data-ttu-id="4701f-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4701f-122">-BatchContext</span></span>
<span data-ttu-id="4701f-123">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="4701f-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4701f-124">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="4701f-124">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4701f-125">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="4701f-125">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4701f-126">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="4701f-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4701f-127">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4701f-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4701f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4701f-128">-DefaultProfile</span></span>
<span data-ttu-id="4701f-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4701f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4701f-130">-Force</span><span class="sxs-lookup"><span data-stu-id="4701f-130">-Force</span></span>
<span data-ttu-id="4701f-131">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="4701f-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4701f-132">-ID</span><span class="sxs-lookup"><span data-stu-id="4701f-132">-Id</span></span>
<span data-ttu-id="4701f-133">Указывает идентификатор задачи, которую этот командлет удаляет.</span><span class="sxs-lookup"><span data-stu-id="4701f-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="4701f-134">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="4701f-134">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="4701f-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4701f-135">-InputObject</span></span>
<span data-ttu-id="4701f-136">Указывает задачу, которую этот командлет удаляет.</span><span class="sxs-lookup"><span data-stu-id="4701f-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="4701f-137">Чтобы получить объект **PSCloudTask** , используйте командлет Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="4701f-137">To obtain a **PSCloudTask** object, use  the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="4701f-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="4701f-138">-JobId</span></span>
<span data-ttu-id="4701f-139">Указывает идентификатор задания, содержащего задачу.</span><span class="sxs-lookup"><span data-stu-id="4701f-139">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="4701f-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4701f-140">-Confirm</span></span>
<span data-ttu-id="4701f-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4701f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4701f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4701f-142">-WhatIf</span></span>
<span data-ttu-id="4701f-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4701f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4701f-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4701f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4701f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4701f-145">CommonParameters</span></span>
<span data-ttu-id="4701f-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4701f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4701f-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4701f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4701f-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4701f-148">INPUTS</span></span>

### <span data-ttu-id="4701f-149">System. String</span><span class="sxs-lookup"><span data-stu-id="4701f-149">System.String</span></span>

### <span data-ttu-id="4701f-150">Microsoft.Azure.Commands.BatCH. Models. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="4701f-150">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="4701f-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4701f-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4701f-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4701f-152">OUTPUTS</span></span>

### <span data-ttu-id="4701f-153">System. void</span><span class="sxs-lookup"><span data-stu-id="4701f-153">System.Void</span></span>

## <span data-ttu-id="4701f-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="4701f-154">NOTES</span></span>

## <span data-ttu-id="4701f-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4701f-155">RELATED LINKS</span></span>

[<span data-ttu-id="4701f-156">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="4701f-156">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="4701f-157">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="4701f-157">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="4701f-158">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="4701f-158">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="4701f-159">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="4701f-159">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="4701f-160">Остановить-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="4701f-160">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="4701f-161">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="4701f-161">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


