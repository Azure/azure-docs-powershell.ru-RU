---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
ms.openlocfilehash: 247b2494e002ae6340f38aa626b9661dbf7722ac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079834"
---
# <span data-ttu-id="7044a-101">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7044a-101">Remove-AzBatchJobSchedule</span></span>

## <span data-ttu-id="7044a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7044a-102">SYNOPSIS</span></span>
<span data-ttu-id="7044a-103">Удаляет расписание пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="7044a-103">Removes a Batch job schedule.</span></span>

## <span data-ttu-id="7044a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7044a-104">SYNTAX</span></span>

```
Remove-AzBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7044a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7044a-105">DESCRIPTION</span></span>
<span data-ttu-id="7044a-106">Командлет **Remove-AzBatchJobSchedule** Удаляет расписание пакетного задания Azure.</span><span class="sxs-lookup"><span data-stu-id="7044a-106">The **Remove-AzBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="7044a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7044a-107">EXAMPLES</span></span>

### <span data-ttu-id="7044a-108">Пример 1: Удаление расписания пакетного задания</span><span class="sxs-lookup"><span data-stu-id="7044a-108">Example 1: Delete a Batch job schedule</span></span>
```
PS C:\>Remove-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
```

<span data-ttu-id="7044a-109">Эта команда удаляет расписание заданий с ИДЕНТИФИКАТОРом MyJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="7044a-109">This command deletes the job schedule that has the ID MyJobSchedule.</span></span>
<span data-ttu-id="7044a-110">Команда запрашивает подтверждение перед удалением задания.</span><span class="sxs-lookup"><span data-stu-id="7044a-110">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="7044a-111">Используйте командлет Get-AzBatchAccountKey для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="7044a-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="7044a-112">Пример 2: Удаление пакетного задания без подтверждения с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="7044a-112">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context | Remove-AzBatchJobSchedule -Force -BatchContext $Context
```

<span data-ttu-id="7044a-113">Эта команда получает расписание заданий с ИД MyJobSchedule с помощью командлета Get-AzBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="7044a-113">This command gets the job schedule that has the ID MyJobSchedule by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="7044a-114">Команда передает это расписание задания в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="7044a-114">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7044a-115">Команда удаляет это расписание задания.</span><span class="sxs-lookup"><span data-stu-id="7044a-115">The command deletes that job schedule.</span></span>
<span data-ttu-id="7044a-116">Так как команда включает параметр *Force* , она не предлагает подтверждения.</span><span class="sxs-lookup"><span data-stu-id="7044a-116">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7044a-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7044a-117">PARAMETERS</span></span>

### <span data-ttu-id="7044a-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7044a-118">-BatchContext</span></span>
<span data-ttu-id="7044a-119">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="7044a-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7044a-120">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="7044a-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7044a-121">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="7044a-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7044a-122">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="7044a-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7044a-123">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="7044a-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7044a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7044a-124">-DefaultProfile</span></span>
<span data-ttu-id="7044a-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7044a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7044a-126">-Force</span><span class="sxs-lookup"><span data-stu-id="7044a-126">-Force</span></span>
<span data-ttu-id="7044a-127">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="7044a-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7044a-128">-ID</span><span class="sxs-lookup"><span data-stu-id="7044a-128">-Id</span></span>
<span data-ttu-id="7044a-129">Указывает идентификатор расписания задания, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="7044a-129">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="7044a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7044a-130">-Confirm</span></span>
<span data-ttu-id="7044a-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7044a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7044a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7044a-132">-WhatIf</span></span>
<span data-ttu-id="7044a-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7044a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7044a-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7044a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7044a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7044a-135">CommonParameters</span></span>
<span data-ttu-id="7044a-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7044a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7044a-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7044a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7044a-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7044a-138">INPUTS</span></span>

### <span data-ttu-id="7044a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7044a-139">System.String</span></span>

### <span data-ttu-id="7044a-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7044a-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7044a-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7044a-141">OUTPUTS</span></span>

### <span data-ttu-id="7044a-142">System. void</span><span class="sxs-lookup"><span data-stu-id="7044a-142">System.Void</span></span>

## <span data-ttu-id="7044a-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="7044a-143">NOTES</span></span>

## <span data-ttu-id="7044a-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7044a-144">RELATED LINKS</span></span>

[<span data-ttu-id="7044a-145">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7044a-145">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="7044a-146">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7044a-146">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="7044a-147">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7044a-147">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="7044a-148">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7044a-148">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="7044a-149">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7044a-149">Set-AzBatchJobSchedule</span></span>](./Set-AzBatchJobSchedule.md)

[<span data-ttu-id="7044a-150">Остановить-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7044a-150">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


