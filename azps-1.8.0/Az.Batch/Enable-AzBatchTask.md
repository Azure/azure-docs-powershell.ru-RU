---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
ms.openlocfilehash: 1eef03db73e6b1afcb2c9ca92f507e8b0f3ff0ae
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93731900"
---
# <span data-ttu-id="79f48-101">Enable-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="79f48-101">Enable-AzBatchTask</span></span>

## <span data-ttu-id="79f48-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79f48-102">SYNOPSIS</span></span>
<span data-ttu-id="79f48-103">Повторная активация задачи.</span><span class="sxs-lookup"><span data-stu-id="79f48-103">Reactivates a task.</span></span>

## <span data-ttu-id="79f48-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79f48-104">SYNTAX</span></span>

### <span data-ttu-id="79f48-105">Номер</span><span class="sxs-lookup"><span data-stu-id="79f48-105">Id</span></span>
```
Enable-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79f48-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="79f48-106">InputObject</span></span>
```
Enable-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79f48-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79f48-107">DESCRIPTION</span></span>
<span data-ttu-id="79f48-108">Командлет **Enable-AzBatchTask** повторно активирует задачу.</span><span class="sxs-lookup"><span data-stu-id="79f48-108">The **Enable-AzBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="79f48-109">Если в задаче исчерпано количество повторных попыток, этот командлет, тем не менее, позволяет ему выполняться.</span><span class="sxs-lookup"><span data-stu-id="79f48-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="79f48-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79f48-110">EXAMPLES</span></span>

### <span data-ttu-id="79f48-111">Пример 1: повторная активация задачи</span><span class="sxs-lookup"><span data-stu-id="79f48-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="79f48-112">Эта команда повторно активирует Task2 задачи в задании Job7.</span><span class="sxs-lookup"><span data-stu-id="79f48-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="79f48-113">Пример 2: повторная активация задачи с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="79f48-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="79f48-114">Эта команда возвращает пакетную задачу с ИДЕНТИФИКАТОРом Task3 в задании с ИД Job8 с помощью командлета Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="79f48-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="79f48-115">Команда передает эту задачу текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="79f48-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="79f48-116">Эта команда активирует эту задачу повторно.</span><span class="sxs-lookup"><span data-stu-id="79f48-116">The command reactivates that task.</span></span>

## <span data-ttu-id="79f48-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79f48-117">PARAMETERS</span></span>

### <span data-ttu-id="79f48-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="79f48-118">-BatchContext</span></span>
<span data-ttu-id="79f48-119">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="79f48-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="79f48-120">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="79f48-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="79f48-121">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="79f48-121">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="79f48-122">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="79f48-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="79f48-123">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="79f48-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="79f48-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79f48-124">-DefaultProfile</span></span>
<span data-ttu-id="79f48-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79f48-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79f48-126">-ID</span><span class="sxs-lookup"><span data-stu-id="79f48-126">-Id</span></span>
<span data-ttu-id="79f48-127">Указывает идентификатор задачи, которую нужно повторно активировать.</span><span class="sxs-lookup"><span data-stu-id="79f48-127">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="79f48-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="79f48-128">-JobId</span></span>
<span data-ttu-id="79f48-129">Указывает идентификатор задания, содержащего задачу.</span><span class="sxs-lookup"><span data-stu-id="79f48-129">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="79f48-130">-Задача</span><span class="sxs-lookup"><span data-stu-id="79f48-130">-Task</span></span>
<span data-ttu-id="79f48-131">Указывает задачу, которую повторно активировал этот командлет.</span><span class="sxs-lookup"><span data-stu-id="79f48-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="79f48-132">Чтобы получить объект **PSCloudTask** , используйте командлет Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="79f48-132">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="79f48-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79f48-133">-Confirm</span></span>
<span data-ttu-id="79f48-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="79f48-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79f48-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79f48-135">-WhatIf</span></span>
<span data-ttu-id="79f48-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="79f48-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79f48-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="79f48-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79f48-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79f48-138">CommonParameters</span></span>
<span data-ttu-id="79f48-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79f48-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79f48-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79f48-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79f48-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79f48-141">INPUTS</span></span>

### <span data-ttu-id="79f48-142">System. String</span><span class="sxs-lookup"><span data-stu-id="79f48-142">System.String</span></span>

### <span data-ttu-id="79f48-143">Microsoft.Azure.Commands.BatCH. Models. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="79f48-143">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="79f48-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="79f48-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="79f48-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79f48-145">OUTPUTS</span></span>

### <span data-ttu-id="79f48-146">System. void</span><span class="sxs-lookup"><span data-stu-id="79f48-146">System.Void</span></span>

## <span data-ttu-id="79f48-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="79f48-147">NOTES</span></span>

## <span data-ttu-id="79f48-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79f48-148">RELATED LINKS</span></span>

[<span data-ttu-id="79f48-149">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="79f48-149">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="79f48-150">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="79f48-150">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="79f48-151">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="79f48-151">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="79f48-152">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="79f48-152">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="79f48-153">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="79f48-153">Set-AzBatchTask</span></span>](./Set-AzBatchTask.md)

[<span data-ttu-id="79f48-154">Остановить-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="79f48-154">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)


