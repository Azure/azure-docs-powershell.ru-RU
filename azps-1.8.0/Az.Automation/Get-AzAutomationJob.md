---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
ms.openlocfilehash: ae638c693366568458a4194d1625d19eaac6af93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731613"
---
# <span data-ttu-id="546b1-101">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="546b1-101">Get-AzAutomationJob</span></span>

## <span data-ttu-id="546b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="546b1-102">SYNOPSIS</span></span>
<span data-ttu-id="546b1-103">Получает задания Runbook Automation.</span><span class="sxs-lookup"><span data-stu-id="546b1-103">Gets Automation runbook jobs.</span></span>

## <span data-ttu-id="546b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="546b1-104">SYNTAX</span></span>

### <span data-ttu-id="546b1-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="546b1-105">ByAll (Default)</span></span>
```
Get-AzAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="546b1-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="546b1-106">ByJobId</span></span>
```
Get-AzAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="546b1-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="546b1-107">ByRunbookName</span></span>
```
Get-AzAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="546b1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="546b1-108">DESCRIPTION</span></span>
<span data-ttu-id="546b1-109">Командлет **Get-AzAutomationJob** получает задания Runbook в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="546b1-109">The **Get-AzAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="546b1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="546b1-110">EXAMPLES</span></span>

### <span data-ttu-id="546b1-111">Пример 1: получение определенного задания Runbook</span><span class="sxs-lookup"><span data-stu-id="546b1-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="546b1-112">Эта команда получает задание с указанным GUID.</span><span class="sxs-lookup"><span data-stu-id="546b1-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="546b1-113">Пример 2: получение всех заданий для Runbook</span><span class="sxs-lookup"><span data-stu-id="546b1-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="546b1-114">Эта команда возвращает все задания, связанные с модулем Runbook с именем Runbook02.</span><span class="sxs-lookup"><span data-stu-id="546b1-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="546b1-115">Пример 3: получение всех выполняемых заданий</span><span class="sxs-lookup"><span data-stu-id="546b1-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="546b1-116">Эта команда получает все выполняемые задания в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="546b1-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="546b1-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="546b1-117">PARAMETERS</span></span>

### <span data-ttu-id="546b1-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="546b1-118">-AutomationAccountName</span></span>
<span data-ttu-id="546b1-119">Указывает имя учетной записи автоматизации, для которой этот командлет получает задания.</span><span class="sxs-lookup"><span data-stu-id="546b1-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546b1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="546b1-120">-DefaultProfile</span></span>
<span data-ttu-id="546b1-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="546b1-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="546b1-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="546b1-122">-EndTime</span></span>
<span data-ttu-id="546b1-123">Задает время окончания задания в качестве объекта **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="546b1-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="546b1-124">Вы можете указать строку, которую можно преобразовать в допустимый тип **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="546b1-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="546b1-125">Этот командлет получает задания, которые имеют время окончания до значения, указанного этим параметром, или до него.</span><span class="sxs-lookup"><span data-stu-id="546b1-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="546b1-126">-ID</span><span class="sxs-lookup"><span data-stu-id="546b1-126">-Id</span></span>
<span data-ttu-id="546b1-127">Указывает идентификатор задания, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="546b1-127">Specifies the ID of a job that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546b1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="546b1-128">-ResourceGroupName</span></span>
<span data-ttu-id="546b1-129">Указывает имя группы ресурсов, в которой этот командлет получает задания.</span><span class="sxs-lookup"><span data-stu-id="546b1-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="546b1-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="546b1-130">-RunbookName</span></span>
<span data-ttu-id="546b1-131">Указывает имя Runbook, для которого этот командлет получает задания.</span><span class="sxs-lookup"><span data-stu-id="546b1-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="546b1-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="546b1-132">-StartTime</span></span>
<span data-ttu-id="546b1-133">Указывает время запуска задания как объект **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="546b1-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="546b1-134">Этот командлет получает задания, которые имеют время начала по отношению к значению, указанному в этом параметре, или после него.</span><span class="sxs-lookup"><span data-stu-id="546b1-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="546b1-135">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="546b1-135">-Status</span></span>
<span data-ttu-id="546b1-136">Указывает состояние задания.</span><span class="sxs-lookup"><span data-stu-id="546b1-136">Specifies the status of a job.</span></span>
<span data-ttu-id="546b1-137">Этот командлет получает задания, которые имеют состояние, совпадающее с этим параметром.</span><span class="sxs-lookup"><span data-stu-id="546b1-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="546b1-138">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="546b1-138">Valid values are:</span></span> 
- <span data-ttu-id="546b1-139">Сделать</span><span class="sxs-lookup"><span data-stu-id="546b1-139">Activating</span></span>
- <span data-ttu-id="546b1-140">Completed</span><span class="sxs-lookup"><span data-stu-id="546b1-140">Completed</span></span>
- <span data-ttu-id="546b1-141">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="546b1-141">Failed</span></span>
- <span data-ttu-id="546b1-142">Очереди</span><span class="sxs-lookup"><span data-stu-id="546b1-142">Queued</span></span>
- <span data-ttu-id="546b1-143">Resuming</span><span class="sxs-lookup"><span data-stu-id="546b1-143">Resuming</span></span>
- <span data-ttu-id="546b1-144">Использующ</span><span class="sxs-lookup"><span data-stu-id="546b1-144">Running</span></span>
- <span data-ttu-id="546b1-145">Начало</span><span class="sxs-lookup"><span data-stu-id="546b1-145">Starting</span></span>
- <span data-ttu-id="546b1-146">Прекращена</span><span class="sxs-lookup"><span data-stu-id="546b1-146">Stopped</span></span>
- <span data-ttu-id="546b1-147">Отключение</span><span class="sxs-lookup"><span data-stu-id="546b1-147">Stopping</span></span>
- <span data-ttu-id="546b1-148">Остановить</span><span class="sxs-lookup"><span data-stu-id="546b1-148">Suspended</span></span>
- <span data-ttu-id="546b1-149">Suspending</span><span class="sxs-lookup"><span data-stu-id="546b1-149">Suspending</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByRunbookName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="546b1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="546b1-150">CommonParameters</span></span>
<span data-ttu-id="546b1-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="546b1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="546b1-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="546b1-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="546b1-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="546b1-153">INPUTS</span></span>

### <span data-ttu-id="546b1-154">System. GUID</span><span class="sxs-lookup"><span data-stu-id="546b1-154">System.Guid</span></span>

### <span data-ttu-id="546b1-155">System. String</span><span class="sxs-lookup"><span data-stu-id="546b1-155">System.String</span></span>

## <span data-ttu-id="546b1-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="546b1-156">OUTPUTS</span></span>

### <span data-ttu-id="546b1-157">Microsoft. Azure. Commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="546b1-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="546b1-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="546b1-158">NOTES</span></span>

## <span data-ttu-id="546b1-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="546b1-159">RELATED LINKS</span></span>

[<span data-ttu-id="546b1-160">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="546b1-160">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="546b1-161">Возобновить — AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="546b1-161">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="546b1-162">Остановить-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="546b1-162">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="546b1-163">Приостановить — AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="546b1-163">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


