---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/powershell/module/az.batch/enable-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
ms.openlocfilehash: 902c7ab5f6125716e03e846a4f1ebc3925aae43f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988504"
---
# <span data-ttu-id="0901c-101">Enable-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0901c-101">Enable-AzBatchTask</span></span>

## <span data-ttu-id="0901c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0901c-102">SYNOPSIS</span></span>
<span data-ttu-id="0901c-103">Повторно активирует задачу.</span><span class="sxs-lookup"><span data-stu-id="0901c-103">Reactivates a task.</span></span>

## <span data-ttu-id="0901c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0901c-104">SYNTAX</span></span>

### <span data-ttu-id="0901c-105">ИД</span><span class="sxs-lookup"><span data-stu-id="0901c-105">Id</span></span>
```
Enable-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0901c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0901c-106">InputObject</span></span>
```
Enable-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0901c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0901c-107">DESCRIPTION</span></span>
<span data-ttu-id="0901c-108">С **помощью cmdlet Enable-AzBatchTask** можно повторно активировать задачу.</span><span class="sxs-lookup"><span data-stu-id="0901c-108">The **Enable-AzBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="0901c-109">Если у задачи уже есть возможность повторить попытку, этот cmdlet не даст возможности выполнить его.</span><span class="sxs-lookup"><span data-stu-id="0901c-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="0901c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0901c-110">EXAMPLES</span></span>

### <span data-ttu-id="0901c-111">Пример 1. Повторное отключение задачи</span><span class="sxs-lookup"><span data-stu-id="0901c-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="0901c-112">Эта команда повторно активирует задачу "Задача2" в заданиях7.</span><span class="sxs-lookup"><span data-stu-id="0901c-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="0901c-113">Пример 2. Повторно активировать задачу с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="0901c-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="0901c-114">Эта команда получает задачу с пакетной задачей, которая имеет код задачи3 в задаче, которая имеет задание 8, с помощью Get-AzBatchTask командлета.</span><span class="sxs-lookup"><span data-stu-id="0901c-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="0901c-115">Эта команда передает эту задачу текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="0901c-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0901c-116">Эта команда повторно активирует задачу.</span><span class="sxs-lookup"><span data-stu-id="0901c-116">The command reactivates that task.</span></span>

## <span data-ttu-id="0901c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0901c-117">PARAMETERS</span></span>

### <span data-ttu-id="0901c-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0901c-118">-BatchContext</span></span>
<span data-ttu-id="0901c-119">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="0901c-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0901c-120">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0901c-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0901c-121">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="0901c-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0901c-122">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0901c-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0901c-123">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="0901c-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0901c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0901c-124">-DefaultProfile</span></span>
<span data-ttu-id="0901c-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0901c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0901c-126">-Id</span><span class="sxs-lookup"><span data-stu-id="0901c-126">-Id</span></span>
<span data-ttu-id="0901c-127">Определяет ИД задачи, которую нужно активировать повторно.</span><span class="sxs-lookup"><span data-stu-id="0901c-127">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="0901c-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="0901c-128">-JobId</span></span>
<span data-ttu-id="0901c-129">Определяет ИД задания, которое содержит задачу.</span><span class="sxs-lookup"><span data-stu-id="0901c-129">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="0901c-130">-Задача</span><span class="sxs-lookup"><span data-stu-id="0901c-130">-Task</span></span>
<span data-ttu-id="0901c-131">Указывает задачу, которая повторно активирована этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0901c-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="0901c-132">Чтобы получить объект **PSCloudTask,** используйте Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="0901c-132">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="0901c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0901c-133">-Confirm</span></span>
<span data-ttu-id="0901c-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0901c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0901c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0901c-135">-WhatIf</span></span>
<span data-ttu-id="0901c-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0901c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0901c-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0901c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0901c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0901c-138">CommonParameters</span></span>
<span data-ttu-id="0901c-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0901c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0901c-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0901c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0901c-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0901c-141">INPUTS</span></span>

### <span data-ttu-id="0901c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="0901c-142">System.String</span></span>

### <span data-ttu-id="0901c-143">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="0901c-143">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="0901c-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0901c-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0901c-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0901c-145">OUTPUTS</span></span>

### <span data-ttu-id="0901c-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="0901c-146">System.Void</span></span>

## <span data-ttu-id="0901c-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0901c-147">NOTES</span></span>

## <span data-ttu-id="0901c-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0901c-148">RELATED LINKS</span></span>

[<span data-ttu-id="0901c-149">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="0901c-149">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="0901c-150">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0901c-150">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="0901c-151">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0901c-151">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="0901c-152">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0901c-152">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="0901c-153">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0901c-153">Set-AzBatchTask</span></span>](./Set-AzBatchTask.md)

[<span data-ttu-id="0901c-154">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0901c-154">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)


