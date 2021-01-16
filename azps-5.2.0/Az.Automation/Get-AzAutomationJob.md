---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
ms.openlocfilehash: 31390ccb19574b6b88c26828bf504dbc8ac5d924
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418700"
---
# <span data-ttu-id="a9da5-101">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a9da5-101">Get-AzAutomationJob</span></span>

## <span data-ttu-id="a9da5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9da5-102">SYNOPSIS</span></span>
<span data-ttu-id="a9da5-103">Возвращает задания запуска автоматизации.</span><span class="sxs-lookup"><span data-stu-id="a9da5-103">Gets Automation runbook jobs.</span></span>

## <span data-ttu-id="a9da5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a9da5-104">SYNTAX</span></span>

### <span data-ttu-id="a9da5-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a9da5-105">ByAll (Default)</span></span>
```
Get-AzAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9da5-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="a9da5-106">ByJobId</span></span>
```
Get-AzAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9da5-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="a9da5-107">ByRunbookName</span></span>
```
Get-AzAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9da5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9da5-108">DESCRIPTION</span></span>
<span data-ttu-id="a9da5-109">Для работы с рабочими книгами в автоматизации Azure возвращается набор заданий для **get-AzAutomationJob.**</span><span class="sxs-lookup"><span data-stu-id="a9da5-109">The **Get-AzAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="a9da5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a9da5-110">EXAMPLES</span></span>

### <span data-ttu-id="a9da5-111">Пример 1. Получить задание для запуска</span><span class="sxs-lookup"><span data-stu-id="a9da5-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="a9da5-112">Эта команда возвращает задание с указанным GUID.</span><span class="sxs-lookup"><span data-stu-id="a9da5-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="a9da5-113">Пример 2. Получить все задания для книги</span><span class="sxs-lookup"><span data-stu-id="a9da5-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="a9da5-114">Эта команда получает все задания, связанные с книгой Runbook02.</span><span class="sxs-lookup"><span data-stu-id="a9da5-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="a9da5-115">Пример 3. Работа со всеми заданиями</span><span class="sxs-lookup"><span data-stu-id="a9da5-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="a9da5-116">Эта команда получает все задания в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a9da5-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a9da5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9da5-117">PARAMETERS</span></span>

### <span data-ttu-id="a9da5-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a9da5-118">-AutomationAccountName</span></span>
<span data-ttu-id="a9da5-119">Указывает имя учетной записи автоматизации, для которой этот cmdlet получает задания.</span><span class="sxs-lookup"><span data-stu-id="a9da5-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="a9da5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9da5-120">-DefaultProfile</span></span>
<span data-ttu-id="a9da5-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a9da5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9da5-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="a9da5-122">-EndTime</span></span>
<span data-ttu-id="a9da5-123">Время окончания задания в качестве объекта **DateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="a9da5-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="a9da5-124">Вы можете указать строку, которую можно преобразовать в допустимый **набор DateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="a9da5-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="a9da5-125">Этот cmdlet получает задания, у которые есть время окончания в или раньше значения, указанного для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="a9da5-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="a9da5-126">-Id</span><span class="sxs-lookup"><span data-stu-id="a9da5-126">-Id</span></span>
<span data-ttu-id="a9da5-127">Определяет код задания, которое получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9da5-127">Specifies the ID of a job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a9da5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9da5-128">-ResourceGroupName</span></span>
<span data-ttu-id="a9da5-129">Указывает имя группы ресурсов, в которой этот cmdlet получает задания.</span><span class="sxs-lookup"><span data-stu-id="a9da5-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="a9da5-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="a9da5-130">-RunbookName</span></span>
<span data-ttu-id="a9da5-131">Определяет имя книги, для которой этот cmdlet получает задания.</span><span class="sxs-lookup"><span data-stu-id="a9da5-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="a9da5-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a9da5-132">-StartTime</span></span>
<span data-ttu-id="a9da5-133">Время начала задания в качестве объекта **DateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="a9da5-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="a9da5-134">Этот cmdlet возвращает задания, время начала в течение или после значений, указанных этим параметром.</span><span class="sxs-lookup"><span data-stu-id="a9da5-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="a9da5-135">-Status</span><span class="sxs-lookup"><span data-stu-id="a9da5-135">-Status</span></span>
<span data-ttu-id="a9da5-136">Определяет состояние задания.</span><span class="sxs-lookup"><span data-stu-id="a9da5-136">Specifies the status of a job.</span></span>
<span data-ttu-id="a9da5-137">Этот командлет возвращает задания с состоянием, которое соответствует этому параметру.</span><span class="sxs-lookup"><span data-stu-id="a9da5-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="a9da5-138">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="a9da5-138">Valid values are:</span></span> 
- <span data-ttu-id="a9da5-139">Активация</span><span class="sxs-lookup"><span data-stu-id="a9da5-139">Activating</span></span>
- <span data-ttu-id="a9da5-140">Завершено</span><span class="sxs-lookup"><span data-stu-id="a9da5-140">Completed</span></span>
- <span data-ttu-id="a9da5-141">Сбой</span><span class="sxs-lookup"><span data-stu-id="a9da5-141">Failed</span></span>
- <span data-ttu-id="a9da5-142">В очереди</span><span class="sxs-lookup"><span data-stu-id="a9da5-142">Queued</span></span>
- <span data-ttu-id="a9da5-143">Резюме</span><span class="sxs-lookup"><span data-stu-id="a9da5-143">Resuming</span></span>
- <span data-ttu-id="a9da5-144">Запущена</span><span class="sxs-lookup"><span data-stu-id="a9da5-144">Running</span></span>
- <span data-ttu-id="a9da5-145">Запуск</span><span class="sxs-lookup"><span data-stu-id="a9da5-145">Starting</span></span>
- <span data-ttu-id="a9da5-146">Остановлено</span><span class="sxs-lookup"><span data-stu-id="a9da5-146">Stopped</span></span>
- <span data-ttu-id="a9da5-147">Остановка</span><span class="sxs-lookup"><span data-stu-id="a9da5-147">Stopping</span></span>
- <span data-ttu-id="a9da5-148">Приостановлено</span><span class="sxs-lookup"><span data-stu-id="a9da5-148">Suspended</span></span>
- <span data-ttu-id="a9da5-149">Приостановка</span><span class="sxs-lookup"><span data-stu-id="a9da5-149">Suspending</span></span>

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

### <span data-ttu-id="a9da5-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9da5-150">CommonParameters</span></span>
<span data-ttu-id="a9da5-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9da5-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9da5-152">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9da5-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9da5-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9da5-153">INPUTS</span></span>

### <span data-ttu-id="a9da5-154">System.Guid</span><span class="sxs-lookup"><span data-stu-id="a9da5-154">System.Guid</span></span>

### <span data-ttu-id="a9da5-155">System.String</span><span class="sxs-lookup"><span data-stu-id="a9da5-155">System.String</span></span>

## <span data-ttu-id="a9da5-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a9da5-156">OUTPUTS</span></span>

### <span data-ttu-id="a9da5-157">Microsoft.Azure.Commands.Automation.Model.Job</span><span class="sxs-lookup"><span data-stu-id="a9da5-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="a9da5-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a9da5-158">NOTES</span></span>

## <span data-ttu-id="a9da5-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9da5-159">RELATED LINKS</span></span>

[<span data-ttu-id="a9da5-160">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="a9da5-160">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="a9da5-161">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a9da5-161">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="a9da5-162">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a9da5-162">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="a9da5-163">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a9da5-163">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


