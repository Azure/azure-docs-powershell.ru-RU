---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
ms.openlocfilehash: 3183720cbafc9a8feae5c9687dfb92ab325f8b04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557611"
---
# <span data-ttu-id="b8a87-101">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b8a87-101">Get-AzureRmAutomationJob</span></span>

## <span data-ttu-id="b8a87-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8a87-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a87-103">Получает задания Runbook Automation.</span><span class="sxs-lookup"><span data-stu-id="b8a87-103">Gets Automation runbook jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8a87-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8a87-104">SYNTAX</span></span>

### <span data-ttu-id="b8a87-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b8a87-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8a87-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="b8a87-106">ByJobId</span></span>
```
Get-AzureRmAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8a87-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="b8a87-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8a87-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8a87-108">DESCRIPTION</span></span>
<span data-ttu-id="b8a87-109">Командлет **Get-AzureRmAutomationJob** получает задания Runbook в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b8a87-109">The **Get-AzureRmAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="b8a87-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8a87-110">EXAMPLES</span></span>

### <span data-ttu-id="b8a87-111">Пример 1: получение определенного задания Runbook</span><span class="sxs-lookup"><span data-stu-id="b8a87-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="b8a87-112">Эта команда получает задание с указанным GUID.</span><span class="sxs-lookup"><span data-stu-id="b8a87-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="b8a87-113">Пример 2: получение всех заданий для Runbook</span><span class="sxs-lookup"><span data-stu-id="b8a87-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="b8a87-114">Эта команда возвращает все задания, связанные с модулем Runbook с именем Runbook02.</span><span class="sxs-lookup"><span data-stu-id="b8a87-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="b8a87-115">Пример 3: получение всех выполняемых заданий</span><span class="sxs-lookup"><span data-stu-id="b8a87-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="b8a87-116">Эта команда получает все выполняемые задания в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b8a87-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="b8a87-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8a87-117">PARAMETERS</span></span>

### <span data-ttu-id="b8a87-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b8a87-118">-AutomationAccountName</span></span>
<span data-ttu-id="b8a87-119">Указывает имя учетной записи автоматизации, для которой этот командлет получает задания.</span><span class="sxs-lookup"><span data-stu-id="b8a87-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a87-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8a87-120">-DefaultProfile</span></span>
<span data-ttu-id="b8a87-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b8a87-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8a87-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b8a87-122">-EndTime</span></span>
<span data-ttu-id="b8a87-123">Задает время окончания задания в качестве объекта **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="b8a87-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="b8a87-124">Вы можете указать строку, которую можно преобразовать в допустимый тип **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="b8a87-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="b8a87-125">Этот командлет получает задания, которые имеют время окончания до значения, указанного этим параметром, или до него.</span><span class="sxs-lookup"><span data-stu-id="b8a87-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a87-126">-ID</span><span class="sxs-lookup"><span data-stu-id="b8a87-126">-Id</span></span>
<span data-ttu-id="b8a87-127">Указывает идентификатор задания, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b8a87-127">Specifies the ID of a job that this cmdlet gets.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a87-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8a87-128">-ResourceGroupName</span></span>
<span data-ttu-id="b8a87-129">Указывает имя группы ресурсов, в которой этот командлет получает задания.</span><span class="sxs-lookup"><span data-stu-id="b8a87-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a87-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="b8a87-130">-RunbookName</span></span>
<span data-ttu-id="b8a87-131">Указывает имя Runbook, для которого этот командлет получает задания.</span><span class="sxs-lookup"><span data-stu-id="b8a87-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a87-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b8a87-132">-StartTime</span></span>
<span data-ttu-id="b8a87-133">Указывает время запуска задания как объект **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="b8a87-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="b8a87-134">Этот командлет получает задания, которые имеют время начала по отношению к значению, указанному в этом параметре, или после него.</span><span class="sxs-lookup"><span data-stu-id="b8a87-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a87-135">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="b8a87-135">-Status</span></span>
<span data-ttu-id="b8a87-136">Указывает состояние задания.</span><span class="sxs-lookup"><span data-stu-id="b8a87-136">Specifies the status of a job.</span></span>
<span data-ttu-id="b8a87-137">Этот командлет получает задания, которые имеют состояние, совпадающее с этим параметром.</span><span class="sxs-lookup"><span data-stu-id="b8a87-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="b8a87-138">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="b8a87-138">Valid values are:</span></span> 

- <span data-ttu-id="b8a87-139">Сделать</span><span class="sxs-lookup"><span data-stu-id="b8a87-139">Activating</span></span>
- <span data-ttu-id="b8a87-140">Completed</span><span class="sxs-lookup"><span data-stu-id="b8a87-140">Completed</span></span>
- <span data-ttu-id="b8a87-141">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="b8a87-141">Failed</span></span>
- <span data-ttu-id="b8a87-142">Очереди</span><span class="sxs-lookup"><span data-stu-id="b8a87-142">Queued</span></span>
- <span data-ttu-id="b8a87-143">Resuming</span><span class="sxs-lookup"><span data-stu-id="b8a87-143">Resuming</span></span>
- <span data-ttu-id="b8a87-144">Использующ</span><span class="sxs-lookup"><span data-stu-id="b8a87-144">Running</span></span>
- <span data-ttu-id="b8a87-145">Начало</span><span class="sxs-lookup"><span data-stu-id="b8a87-145">Starting</span></span>
- <span data-ttu-id="b8a87-146">Прекращена</span><span class="sxs-lookup"><span data-stu-id="b8a87-146">Stopped</span></span>
- <span data-ttu-id="b8a87-147">Отключение</span><span class="sxs-lookup"><span data-stu-id="b8a87-147">Stopping</span></span>
- <span data-ttu-id="b8a87-148">Остановить</span><span class="sxs-lookup"><span data-stu-id="b8a87-148">Suspended</span></span>
- <span data-ttu-id="b8a87-149">Suspending</span><span class="sxs-lookup"><span data-stu-id="b8a87-149">Suspending</span></span>

```yaml
Type: String
Parameter Sets: ByAll, ByRunbookName
Aliases: 
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a87-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a87-150">CommonParameters</span></span>
<span data-ttu-id="b8a87-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8a87-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a87-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8a87-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a87-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8a87-153">INPUTS</span></span>

### <span data-ttu-id="b8a87-154">Ничего</span><span class="sxs-lookup"><span data-stu-id="b8a87-154">None</span></span>
<span data-ttu-id="b8a87-155">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="b8a87-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b8a87-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8a87-156">OUTPUTS</span></span>

### <span data-ttu-id="b8a87-157">Microsoft. Azure. Commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="b8a87-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="b8a87-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8a87-158">NOTES</span></span>

## <span data-ttu-id="b8a87-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8a87-159">RELATED LINKS</span></span>

[<span data-ttu-id="b8a87-160">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="b8a87-160">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="b8a87-161">Возобновить — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b8a87-161">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="b8a87-162">Остановить-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b8a87-162">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="b8a87-163">Приостановить — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b8a87-163">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


