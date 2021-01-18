---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
ms.openlocfilehash: 247b2494e002ae6340f38aa626b9661dbf7722ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519788"
---
# <span data-ttu-id="9b6ae-101">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9b6ae-101">Remove-AzBatchJobSchedule</span></span>

## <span data-ttu-id="9b6ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b6ae-102">SYNOPSIS</span></span>
<span data-ttu-id="9b6ae-103">Удаляет расписание пакетных рабочих мест.</span><span class="sxs-lookup"><span data-stu-id="9b6ae-103">Removes a Batch job schedule.</span></span>

## <span data-ttu-id="9b6ae-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9b6ae-104">SYNTAX</span></span>

```
Remove-AzBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b6ae-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b6ae-105">DESCRIPTION</span></span>
<span data-ttu-id="9b6ae-106">С **его использованием удаляется** расписание рабочих мест Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="9b6ae-106">The **Remove-AzBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="9b6ae-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9b6ae-107">EXAMPLES</span></span>

### <span data-ttu-id="9b6ae-108">Пример 1. Удаление графика пакетных задания</span><span class="sxs-lookup"><span data-stu-id="9b6ae-108">Example 1: Delete a Batch job schedule</span></span>
```
PS C:\>Remove-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
```

<span data-ttu-id="9b6ae-109">Эта команда удаляет расписание задания с календарем ID MyJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="9b6ae-109">This command deletes the job schedule that has the ID MyJobSchedule.</span></span>
<span data-ttu-id="9b6ae-110">Перед удалением задания вам будет предложено подтвердить удаление.</span><span class="sxs-lookup"><span data-stu-id="9b6ae-110">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="9b6ae-111">Используйте Get-AzBatchAccountKey для назначения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="9b6ae-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="9b6ae-112">Пример 2. Удаление пакетного задания без подтверждения с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="9b6ae-112">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context | Remove-AzBatchJobSchedule -Force -BatchContext $Context
```

<span data-ttu-id="9b6ae-113">Эта команда получает расписание задания, которое использует ID MyJobSchedule, с помощью Get-AzBatchJobSchedule командлета.</span><span class="sxs-lookup"><span data-stu-id="9b6ae-113">This command gets the job schedule that has the ID MyJobSchedule by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="9b6ae-114">Эта команда передает расписание задания текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="9b6ae-114">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9b6ae-115">Команда удаляет это расписание задания.</span><span class="sxs-lookup"><span data-stu-id="9b6ae-115">The command deletes that job schedule.</span></span>
<span data-ttu-id="9b6ae-116">Так как команда содержит параметр *Force,* запрос на подтверждение не выдан.</span><span class="sxs-lookup"><span data-stu-id="9b6ae-116">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="9b6ae-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b6ae-117">PARAMETERS</span></span>

### <span data-ttu-id="9b6ae-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9b6ae-118">-BatchContext</span></span>
<span data-ttu-id="9b6ae-119">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="9b6ae-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9b6ae-120">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9b6ae-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9b6ae-121">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="9b6ae-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9b6ae-122">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9b6ae-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9b6ae-123">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="9b6ae-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9b6ae-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b6ae-124">-DefaultProfile</span></span>
<span data-ttu-id="9b6ae-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b6ae-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b6ae-126">-Force</span><span class="sxs-lookup"><span data-stu-id="9b6ae-126">-Force</span></span>
<span data-ttu-id="9b6ae-127">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="9b6ae-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9b6ae-128">-Id</span><span class="sxs-lookup"><span data-stu-id="9b6ae-128">-Id</span></span>
<span data-ttu-id="9b6ae-129">Определяет ИД удаляемого расписания задания.</span><span class="sxs-lookup"><span data-stu-id="9b6ae-129">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="9b6ae-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b6ae-130">-Confirm</span></span>
<span data-ttu-id="9b6ae-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9b6ae-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b6ae-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b6ae-132">-WhatIf</span></span>
<span data-ttu-id="9b6ae-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b6ae-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b6ae-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9b6ae-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b6ae-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b6ae-135">CommonParameters</span></span>
<span data-ttu-id="9b6ae-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b6ae-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b6ae-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b6ae-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b6ae-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b6ae-138">INPUTS</span></span>

### <span data-ttu-id="9b6ae-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9b6ae-139">System.String</span></span>

### <span data-ttu-id="9b6ae-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9b6ae-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9b6ae-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9b6ae-141">OUTPUTS</span></span>

### <span data-ttu-id="9b6ae-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="9b6ae-142">System.Void</span></span>

## <span data-ttu-id="9b6ae-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9b6ae-143">NOTES</span></span>

## <span data-ttu-id="9b6ae-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b6ae-144">RELATED LINKS</span></span>

[<span data-ttu-id="9b6ae-145">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9b6ae-145">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="9b6ae-146">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9b6ae-146">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="9b6ae-147">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9b6ae-147">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="9b6ae-148">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9b6ae-148">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="9b6ae-149">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9b6ae-149">Set-AzBatchJobSchedule</span></span>](./Set-AzBatchJobSchedule.md)

[<span data-ttu-id="9b6ae-150">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9b6ae-150">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


