---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
ms.openlocfilehash: 83ac1df0259d39dd1db301e836479193b17f1dee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998945"
---
# <span data-ttu-id="81b06-101">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="81b06-101">Remove-AzBatchTask</span></span>

## <span data-ttu-id="81b06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81b06-102">SYNOPSIS</span></span>
<span data-ttu-id="81b06-103">Удаляет пакетную задачу.</span><span class="sxs-lookup"><span data-stu-id="81b06-103">Deletes a Batch task.</span></span>

## <span data-ttu-id="81b06-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="81b06-104">SYNTAX</span></span>

### <span data-ttu-id="81b06-105">ИД</span><span class="sxs-lookup"><span data-stu-id="81b06-105">Id</span></span>
```
Remove-AzBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81b06-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="81b06-106">InputObject</span></span>
```
Remove-AzBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81b06-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81b06-107">DESCRIPTION</span></span>
<span data-ttu-id="81b06-108">С **его использованием удаляется** задача пакета Azure.</span><span class="sxs-lookup"><span data-stu-id="81b06-108">The **Remove-AzBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="81b06-109">Этот cmdlet запросит подтверждение, если не указан параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="81b06-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="81b06-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="81b06-110">EXAMPLES</span></span>

### <span data-ttu-id="81b06-111">Пример 1. Удаление пакетной задачи по ИД</span><span class="sxs-lookup"><span data-stu-id="81b06-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="81b06-112">Эта команда удаляет задачу с ИД задачи23 для задания с ИД-0000001.</span><span class="sxs-lookup"><span data-stu-id="81b06-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="81b06-113">Команда запросит подтверждение.</span><span class="sxs-lookup"><span data-stu-id="81b06-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="81b06-114">Чтобы назначить контекст переменной $Context, используйте $Context **AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="81b06-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="81b06-115">Пример 2. Удаление задачи с пакетом с помощью конвейера без подтверждения</span><span class="sxs-lookup"><span data-stu-id="81b06-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="81b06-116">Эта команда получает задачу с пакетной задачей, которая имеет задачу "Код26" для задания с заданием 000001 с помощью командлета **Get-AzBatchTask.**</span><span class="sxs-lookup"><span data-stu-id="81b06-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzBatchTask** cmdlet.</span></span>
<span data-ttu-id="81b06-117">Эта команда передает эту задачу текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="81b06-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="81b06-118">Команда удалит задачу.</span><span class="sxs-lookup"><span data-stu-id="81b06-118">The command deletes that task.</span></span>
<span data-ttu-id="81b06-119">Эта команда определяет параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="81b06-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="81b06-120">Поэтому команда не будет запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="81b06-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="81b06-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81b06-121">PARAMETERS</span></span>

### <span data-ttu-id="81b06-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="81b06-122">-BatchContext</span></span>
<span data-ttu-id="81b06-123">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="81b06-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="81b06-124">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="81b06-124">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="81b06-125">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="81b06-125">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="81b06-126">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="81b06-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="81b06-127">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="81b06-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="81b06-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81b06-128">-DefaultProfile</span></span>
<span data-ttu-id="81b06-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="81b06-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81b06-130">-Force</span><span class="sxs-lookup"><span data-stu-id="81b06-130">-Force</span></span>
<span data-ttu-id="81b06-131">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="81b06-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="81b06-132">-Id</span><span class="sxs-lookup"><span data-stu-id="81b06-132">-Id</span></span>
<span data-ttu-id="81b06-133">Определяет код задачи, удаляемой этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81b06-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="81b06-134">Поддиавные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="81b06-134">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="81b06-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81b06-135">-InputObject</span></span>
<span data-ttu-id="81b06-136">Определяет задачу, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81b06-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="81b06-137">Чтобы получить объект **PSCloudTask,** используйте Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="81b06-137">To obtain a **PSCloudTask** object, use  the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="81b06-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="81b06-138">-JobId</span></span>
<span data-ttu-id="81b06-139">Определяет ИД задания, которое содержит задачу.</span><span class="sxs-lookup"><span data-stu-id="81b06-139">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="81b06-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81b06-140">-Confirm</span></span>
<span data-ttu-id="81b06-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81b06-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81b06-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81b06-142">-WhatIf</span></span>
<span data-ttu-id="81b06-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81b06-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81b06-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="81b06-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81b06-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81b06-145">CommonParameters</span></span>
<span data-ttu-id="81b06-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81b06-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81b06-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81b06-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81b06-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81b06-148">INPUTS</span></span>

### <span data-ttu-id="81b06-149">System.String</span><span class="sxs-lookup"><span data-stu-id="81b06-149">System.String</span></span>

### <span data-ttu-id="81b06-150">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="81b06-150">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="81b06-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="81b06-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="81b06-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="81b06-152">OUTPUTS</span></span>

### <span data-ttu-id="81b06-153">System.Void</span><span class="sxs-lookup"><span data-stu-id="81b06-153">System.Void</span></span>

## <span data-ttu-id="81b06-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="81b06-154">NOTES</span></span>

## <span data-ttu-id="81b06-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81b06-155">RELATED LINKS</span></span>

[<span data-ttu-id="81b06-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="81b06-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="81b06-157">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="81b06-157">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="81b06-158">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="81b06-158">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="81b06-159">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="81b06-159">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="81b06-160">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="81b06-160">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="81b06-161">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="81b06-161">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
