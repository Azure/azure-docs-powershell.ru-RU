---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
ms.openlocfilehash: 9979a0fa16b8cfbe59eb8412a76cbbebcb2fca4a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410012"
---
# <span data-ttu-id="94709-101">Enable-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="94709-101">Enable-AzBatchTask</span></span>

## <span data-ttu-id="94709-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94709-102">SYNOPSIS</span></span>
<span data-ttu-id="94709-103">Повторно активирует задачу.</span><span class="sxs-lookup"><span data-stu-id="94709-103">Reactivates a task.</span></span>

## <span data-ttu-id="94709-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="94709-104">SYNTAX</span></span>

### <span data-ttu-id="94709-105">ИД</span><span class="sxs-lookup"><span data-stu-id="94709-105">Id</span></span>
```
Enable-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94709-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="94709-106">InputObject</span></span>
```
Enable-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94709-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94709-107">DESCRIPTION</span></span>
<span data-ttu-id="94709-108">С **помощью cmdlet Enable-AzBatchTask** можно повторно активировать задачу.</span><span class="sxs-lookup"><span data-stu-id="94709-108">The **Enable-AzBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="94709-109">Если задача посчиталась повторной, этот cmdlet не позволяет выполнить ее.</span><span class="sxs-lookup"><span data-stu-id="94709-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="94709-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="94709-110">EXAMPLES</span></span>

### <span data-ttu-id="94709-111">Пример 1. Повторное отключение задачи</span><span class="sxs-lookup"><span data-stu-id="94709-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="94709-112">Эта команда повторно активирует задачу "Задача2" в заданиях7.</span><span class="sxs-lookup"><span data-stu-id="94709-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="94709-113">Пример 2. Повторно активировать задачу с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="94709-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="94709-114">Эта команда получает задачу с пакетной задачей, которая имеет код задачи3 в задаче, которая имеет задание 8, с помощью Get-AzBatchTask командлета.</span><span class="sxs-lookup"><span data-stu-id="94709-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="94709-115">Эта команда передает эту задачу текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="94709-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="94709-116">Эта команда повторно активирует задачу.</span><span class="sxs-lookup"><span data-stu-id="94709-116">The command reactivates that task.</span></span>

## <span data-ttu-id="94709-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94709-117">PARAMETERS</span></span>

### <span data-ttu-id="94709-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="94709-118">-BatchContext</span></span>
<span data-ttu-id="94709-119">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="94709-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="94709-120">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="94709-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="94709-121">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="94709-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="94709-122">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="94709-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="94709-123">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="94709-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="94709-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94709-124">-DefaultProfile</span></span>
<span data-ttu-id="94709-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94709-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94709-126">-Id</span><span class="sxs-lookup"><span data-stu-id="94709-126">-Id</span></span>
<span data-ttu-id="94709-127">Определяет ИД задачи, которую нужно активировать повторно.</span><span class="sxs-lookup"><span data-stu-id="94709-127">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="94709-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="94709-128">-JobId</span></span>
<span data-ttu-id="94709-129">Определяет ИД задания, которое содержит задачу.</span><span class="sxs-lookup"><span data-stu-id="94709-129">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="94709-130">-Задача</span><span class="sxs-lookup"><span data-stu-id="94709-130">-Task</span></span>
<span data-ttu-id="94709-131">Указывает задачу, которая повторно активирована этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94709-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="94709-132">Чтобы получить объект **PSCloudTask,** используйте Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="94709-132">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="94709-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94709-133">-Confirm</span></span>
<span data-ttu-id="94709-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94709-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94709-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94709-135">-WhatIf</span></span>
<span data-ttu-id="94709-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94709-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94709-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="94709-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94709-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94709-138">CommonParameters</span></span>
<span data-ttu-id="94709-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94709-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94709-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94709-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94709-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94709-141">INPUTS</span></span>

### <span data-ttu-id="94709-142">System.String</span><span class="sxs-lookup"><span data-stu-id="94709-142">System.String</span></span>

### <span data-ttu-id="94709-143">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="94709-143">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="94709-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="94709-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="94709-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="94709-145">OUTPUTS</span></span>

### <span data-ttu-id="94709-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="94709-146">System.Void</span></span>

## <span data-ttu-id="94709-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="94709-147">NOTES</span></span>

## <span data-ttu-id="94709-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94709-148">RELATED LINKS</span></span>

[<span data-ttu-id="94709-149">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="94709-149">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="94709-150">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="94709-150">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="94709-151">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="94709-151">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="94709-152">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="94709-152">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="94709-153">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="94709-153">Set-AzBatchTask</span></span>](./Set-AzBatchTask.md)

[<span data-ttu-id="94709-154">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="94709-154">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)


