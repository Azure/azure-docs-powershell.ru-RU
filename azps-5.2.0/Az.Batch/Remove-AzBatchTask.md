---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
ms.openlocfilehash: e067eea86e3a4350d08c5c0f9ec34b4af65b07f8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401516"
---
# <span data-ttu-id="286fb-101">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="286fb-101">Remove-AzBatchTask</span></span>

## <span data-ttu-id="286fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="286fb-102">SYNOPSIS</span></span>
<span data-ttu-id="286fb-103">Удаляет пакетную задачу.</span><span class="sxs-lookup"><span data-stu-id="286fb-103">Deletes a Batch task.</span></span>

## <span data-ttu-id="286fb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="286fb-104">SYNTAX</span></span>

### <span data-ttu-id="286fb-105">ИД</span><span class="sxs-lookup"><span data-stu-id="286fb-105">Id</span></span>
```
Remove-AzBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="286fb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="286fb-106">InputObject</span></span>
```
Remove-AzBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="286fb-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="286fb-107">DESCRIPTION</span></span>
<span data-ttu-id="286fb-108">С **его использованием удаляется** задача пакета Azure.</span><span class="sxs-lookup"><span data-stu-id="286fb-108">The **Remove-AzBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="286fb-109">Этот cmdlet запросит подтверждение, если не указать параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="286fb-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="286fb-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="286fb-110">EXAMPLES</span></span>

### <span data-ttu-id="286fb-111">Пример 1. Удаление пакетной задачи по ИД</span><span class="sxs-lookup"><span data-stu-id="286fb-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="286fb-112">Эта команда удаляет задачу с ИД задачи23 для задания с заданием 0000001.</span><span class="sxs-lookup"><span data-stu-id="286fb-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="286fb-113">Команда запросит подтверждение.</span><span class="sxs-lookup"><span data-stu-id="286fb-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="286fb-114">Чтобы назначить контекст переменной $Context, используйте $Context **AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="286fb-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="286fb-115">Пример 2. Удаление задачи с пакетом с помощью конвейера без подтверждения</span><span class="sxs-lookup"><span data-stu-id="286fb-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="286fb-116">Эта команда получает задачу с пакетной задачей, которая имеет задачу "Код26" для задания с заданием 000001 с помощью командлета **Get-AzBatchTask.**</span><span class="sxs-lookup"><span data-stu-id="286fb-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzBatchTask** cmdlet.</span></span>
<span data-ttu-id="286fb-117">Эта команда передает эту задачу текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="286fb-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="286fb-118">Команда удалит задачу.</span><span class="sxs-lookup"><span data-stu-id="286fb-118">The command deletes that task.</span></span>
<span data-ttu-id="286fb-119">Эта команда определяет параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="286fb-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="286fb-120">Таким образом, команда не будет запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="286fb-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="286fb-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="286fb-121">PARAMETERS</span></span>

### <span data-ttu-id="286fb-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="286fb-122">-BatchContext</span></span>
<span data-ttu-id="286fb-123">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="286fb-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="286fb-124">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="286fb-124">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="286fb-125">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="286fb-125">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="286fb-126">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="286fb-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="286fb-127">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="286fb-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="286fb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="286fb-128">-DefaultProfile</span></span>
<span data-ttu-id="286fb-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="286fb-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="286fb-130">-Force</span><span class="sxs-lookup"><span data-stu-id="286fb-130">-Force</span></span>
<span data-ttu-id="286fb-131">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="286fb-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="286fb-132">-Id</span><span class="sxs-lookup"><span data-stu-id="286fb-132">-Id</span></span>
<span data-ttu-id="286fb-133">Определяет код задачи, удаляемой этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="286fb-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="286fb-134">Поддиавные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="286fb-134">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="286fb-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="286fb-135">-InputObject</span></span>
<span data-ttu-id="286fb-136">Задача, удаляемая этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="286fb-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="286fb-137">Чтобы получить объект **PSCloudTask,** используйте Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="286fb-137">To obtain a **PSCloudTask** object, use  the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="286fb-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="286fb-138">-JobId</span></span>
<span data-ttu-id="286fb-139">Определяет ИД задания, которое содержит задачу.</span><span class="sxs-lookup"><span data-stu-id="286fb-139">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="286fb-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="286fb-140">-Confirm</span></span>
<span data-ttu-id="286fb-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="286fb-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="286fb-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="286fb-142">-WhatIf</span></span>
<span data-ttu-id="286fb-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="286fb-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="286fb-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="286fb-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="286fb-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="286fb-145">CommonParameters</span></span>
<span data-ttu-id="286fb-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="286fb-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="286fb-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="286fb-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="286fb-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="286fb-148">INPUTS</span></span>

### <span data-ttu-id="286fb-149">System.String</span><span class="sxs-lookup"><span data-stu-id="286fb-149">System.String</span></span>

### <span data-ttu-id="286fb-150">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="286fb-150">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="286fb-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="286fb-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="286fb-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="286fb-152">OUTPUTS</span></span>

### <span data-ttu-id="286fb-153">System.Void</span><span class="sxs-lookup"><span data-stu-id="286fb-153">System.Void</span></span>

## <span data-ttu-id="286fb-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="286fb-154">NOTES</span></span>

## <span data-ttu-id="286fb-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="286fb-155">RELATED LINKS</span></span>

[<span data-ttu-id="286fb-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="286fb-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="286fb-157">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="286fb-157">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="286fb-158">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="286fb-158">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="286fb-159">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="286fb-159">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="286fb-160">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="286fb-160">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="286fb-161">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="286fb-161">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
