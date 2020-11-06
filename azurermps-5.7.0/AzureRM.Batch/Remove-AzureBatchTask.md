---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
ms.openlocfilehash: 775425b0da46ef6c2b22e1c28725b323b3071974
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568241"
---
# <span data-ttu-id="2f866-101">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2f866-101">Remove-AzureBatchTask</span></span>

## <span data-ttu-id="2f866-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f866-102">SYNOPSIS</span></span>
<span data-ttu-id="2f866-103">Удаляет пакетную задачу.</span><span class="sxs-lookup"><span data-stu-id="2f866-103">Deletes a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f866-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f866-104">SYNTAX</span></span>

### <span data-ttu-id="2f866-105">Номер</span><span class="sxs-lookup"><span data-stu-id="2f866-105">Id</span></span>
```
Remove-AzureBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f866-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2f866-106">InputObject</span></span>
```
Remove-AzureBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f866-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f866-107">DESCRIPTION</span></span>
<span data-ttu-id="2f866-108">Командлет **Remove-AzureBatchTask** удаляет пакетную задачу Azure.</span><span class="sxs-lookup"><span data-stu-id="2f866-108">The **Remove-AzureBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="2f866-109">Этот командлет запрашивает подтверждение, если не указан параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="2f866-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="2f866-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f866-110">EXAMPLES</span></span>

### <span data-ttu-id="2f866-111">Пример 1: удаление пакетной задачи по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="2f866-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="2f866-112">Эта команда удаляет задачу с ИДЕНТИФИКАТОРом Task23 под заданием с ИД задания 000001.</span><span class="sxs-lookup"><span data-stu-id="2f866-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="2f866-113">В командной строке появится запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="2f866-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="2f866-114">Используйте командлет **Get-AzureRmBatchAccountKeys** , чтобы назначить контекст переменной $context.</span><span class="sxs-lookup"><span data-stu-id="2f866-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="2f866-115">Пример 2: удаление пакетной задачи с помощью конвейера без подтверждения</span><span class="sxs-lookup"><span data-stu-id="2f866-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzureBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="2f866-116">Эта команда получает пакетную задачу с ИДЕНТИФИКАТОРом Task26 в задании с ИД задания 000001 с помощью командлета **Get-AzureBatchTask** .</span><span class="sxs-lookup"><span data-stu-id="2f866-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzureBatchTask** cmdlet.</span></span>
<span data-ttu-id="2f866-117">Команда передает эту задачу текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="2f866-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2f866-118">Команда удаляет эту задачу.</span><span class="sxs-lookup"><span data-stu-id="2f866-118">The command deletes that task.</span></span>
<span data-ttu-id="2f866-119">Эта команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="2f866-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="2f866-120">Таким образом, команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="2f866-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="2f866-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f866-121">PARAMETERS</span></span>

### <span data-ttu-id="2f866-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2f866-122">-BatchContext</span></span>
<span data-ttu-id="2f866-123">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="2f866-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2f866-124">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="2f866-124">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2f866-125">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="2f866-125">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2f866-126">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="2f866-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2f866-127">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="2f866-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2f866-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f866-128">-DefaultProfile</span></span>
<span data-ttu-id="2f866-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f866-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f866-130">-Force</span><span class="sxs-lookup"><span data-stu-id="2f866-130">-Force</span></span>
<span data-ttu-id="2f866-131">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="2f866-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2f866-132">-ID</span><span class="sxs-lookup"><span data-stu-id="2f866-132">-Id</span></span>
<span data-ttu-id="2f866-133">Указывает идентификатор задачи, которую этот командлет удаляет.</span><span class="sxs-lookup"><span data-stu-id="2f866-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="2f866-134">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="2f866-134">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="2f866-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f866-135">-InputObject</span></span>
<span data-ttu-id="2f866-136">Указывает задачу, которую этот командлет удаляет.</span><span class="sxs-lookup"><span data-stu-id="2f866-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="2f866-137">Чтобы получить объект **PSCloudTask** , используйте командлет Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="2f866-137">To obtain a **PSCloudTask** object, use  the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="2f866-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="2f866-138">-JobId</span></span>
<span data-ttu-id="2f866-139">Указывает идентификатор задания, содержащего задачу.</span><span class="sxs-lookup"><span data-stu-id="2f866-139">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="2f866-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f866-140">-Confirm</span></span>
<span data-ttu-id="2f866-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2f866-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f866-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f866-142">-WhatIf</span></span>
<span data-ttu-id="2f866-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2f866-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f866-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2f866-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f866-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f866-145">CommonParameters</span></span>
<span data-ttu-id="2f866-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f866-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f866-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f866-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f866-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f866-148">INPUTS</span></span>

### <span data-ttu-id="2f866-149">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2f866-149">BatchAccountContext</span></span>
<span data-ttu-id="2f866-150">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="2f866-150">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="2f866-151">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="2f866-151">PSCloudTask</span></span>
<span data-ttu-id="2f866-152">Параметр "InputObject" принимает значение типа "PSCloudTask" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="2f866-152">Parameter 'InputObject' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="2f866-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f866-153">OUTPUTS</span></span>

## <span data-ttu-id="2f866-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f866-154">NOTES</span></span>

## <span data-ttu-id="2f866-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f866-155">RELATED LINKS</span></span>

[<span data-ttu-id="2f866-156">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2f866-156">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="2f866-157">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2f866-157">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="2f866-158">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2f866-158">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="2f866-159">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2f866-159">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="2f866-160">Остановить-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2f866-160">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="2f866-161">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="2f866-161">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


