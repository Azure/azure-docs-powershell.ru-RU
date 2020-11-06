---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
ms.openlocfilehash: 4509190a8417379c9d5bc9eae9d6d12609def4aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570147"
---
# <span data-ttu-id="a6da3-101">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a6da3-101">Get-AzureRmAutomationJob</span></span>

## <span data-ttu-id="a6da3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6da3-102">SYNOPSIS</span></span>
<span data-ttu-id="a6da3-103">Получает задания Runbook Automation.</span><span class="sxs-lookup"><span data-stu-id="a6da3-103">Gets Automation runbook jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6da3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6da3-104">SYNTAX</span></span>

### <span data-ttu-id="a6da3-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a6da3-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6da3-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="a6da3-106">ByJobId</span></span>
```
Get-AzureRmAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6da3-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="a6da3-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6da3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6da3-108">DESCRIPTION</span></span>
<span data-ttu-id="a6da3-109">Командлет **Get-AzureRmAutomationJob** получает задания Runbook в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a6da3-109">The **Get-AzureRmAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="a6da3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6da3-110">EXAMPLES</span></span>

### <span data-ttu-id="a6da3-111">Пример 1: получение определенного задания Runbook</span><span class="sxs-lookup"><span data-stu-id="a6da3-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="a6da3-112">Эта команда получает задание с указанным GUID.</span><span class="sxs-lookup"><span data-stu-id="a6da3-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="a6da3-113">Пример 2: получение всех заданий для Runbook</span><span class="sxs-lookup"><span data-stu-id="a6da3-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="a6da3-114">Эта команда возвращает все задания, связанные с модулем Runbook с именем Runbook02.</span><span class="sxs-lookup"><span data-stu-id="a6da3-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="a6da3-115">Пример 3: получение всех выполняемых заданий</span><span class="sxs-lookup"><span data-stu-id="a6da3-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="a6da3-116">Эта команда получает все выполняемые задания в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a6da3-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a6da3-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6da3-117">PARAMETERS</span></span>

### <span data-ttu-id="a6da3-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a6da3-118">-AutomationAccountName</span></span>
<span data-ttu-id="a6da3-119">Указывает имя учетной записи автоматизации, для которой этот командлет получает задания.</span><span class="sxs-lookup"><span data-stu-id="a6da3-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="a6da3-120">-EndTime</span><span class="sxs-lookup"><span data-stu-id="a6da3-120">-EndTime</span></span>
<span data-ttu-id="a6da3-121">Задает время окончания задания в качестве объекта **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="a6da3-121">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="a6da3-122">Вы можете указать строку, которую можно преобразовать в допустимый тип **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="a6da3-122">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="a6da3-123">Этот командлет получает задания, которые имеют время окончания до значения, указанного этим параметром, или до него.</span><span class="sxs-lookup"><span data-stu-id="a6da3-123">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="a6da3-124">-ID</span><span class="sxs-lookup"><span data-stu-id="a6da3-124">-Id</span></span>
<span data-ttu-id="a6da3-125">Указывает идентификатор задания, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a6da3-125">Specifies the ID of a job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a6da3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6da3-126">-ResourceGroupName</span></span>
<span data-ttu-id="a6da3-127">Указывает имя группы ресурсов, в которой этот командлет получает задания.</span><span class="sxs-lookup"><span data-stu-id="a6da3-127">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="a6da3-128">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="a6da3-128">-RunbookName</span></span>
<span data-ttu-id="a6da3-129">Указывает имя Runbook, для которого этот командлет получает задания.</span><span class="sxs-lookup"><span data-stu-id="a6da3-129">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="a6da3-130">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a6da3-130">-StartTime</span></span>
<span data-ttu-id="a6da3-131">Указывает время запуска задания как объект **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="a6da3-131">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="a6da3-132">Этот командлет получает задания, которые имеют время начала по отношению к значению, указанному в этом параметре, или после него.</span><span class="sxs-lookup"><span data-stu-id="a6da3-132">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="a6da3-133">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="a6da3-133">-Status</span></span>
<span data-ttu-id="a6da3-134">Указывает состояние задания.</span><span class="sxs-lookup"><span data-stu-id="a6da3-134">Specifies the status of a job.</span></span>
<span data-ttu-id="a6da3-135">Этот командлет получает задания, которые имеют состояние, совпадающее с этим параметром.</span><span class="sxs-lookup"><span data-stu-id="a6da3-135">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="a6da3-136">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="a6da3-136">Valid values are:</span></span> 

- <span data-ttu-id="a6da3-137">Сделать</span><span class="sxs-lookup"><span data-stu-id="a6da3-137">Activating</span></span>
- <span data-ttu-id="a6da3-138">Completed</span><span class="sxs-lookup"><span data-stu-id="a6da3-138">Completed</span></span>
- <span data-ttu-id="a6da3-139">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="a6da3-139">Failed</span></span>
- <span data-ttu-id="a6da3-140">Очереди</span><span class="sxs-lookup"><span data-stu-id="a6da3-140">Queued</span></span>
- <span data-ttu-id="a6da3-141">Resuming</span><span class="sxs-lookup"><span data-stu-id="a6da3-141">Resuming</span></span>
- <span data-ttu-id="a6da3-142">Использующ</span><span class="sxs-lookup"><span data-stu-id="a6da3-142">Running</span></span>
- <span data-ttu-id="a6da3-143">Начало</span><span class="sxs-lookup"><span data-stu-id="a6da3-143">Starting</span></span>
- <span data-ttu-id="a6da3-144">Прекращена</span><span class="sxs-lookup"><span data-stu-id="a6da3-144">Stopped</span></span>
- <span data-ttu-id="a6da3-145">Отключение</span><span class="sxs-lookup"><span data-stu-id="a6da3-145">Stopping</span></span>
- <span data-ttu-id="a6da3-146">Остановить</span><span class="sxs-lookup"><span data-stu-id="a6da3-146">Suspended</span></span>
- <span data-ttu-id="a6da3-147">Suspending</span><span class="sxs-lookup"><span data-stu-id="a6da3-147">Suspending</span></span>

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

### <span data-ttu-id="a6da3-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6da3-148">-DefaultProfile</span></span>
<span data-ttu-id="a6da3-149">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6da3-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6da3-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6da3-150">CommonParameters</span></span>
<span data-ttu-id="a6da3-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a6da3-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6da3-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6da3-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6da3-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6da3-153">INPUTS</span></span>

## <span data-ttu-id="a6da3-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6da3-154">OUTPUTS</span></span>

### <span data-ttu-id="a6da3-155">Microsoft. Azure. Commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="a6da3-155">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="a6da3-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6da3-156">NOTES</span></span>

## <span data-ttu-id="a6da3-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6da3-157">RELATED LINKS</span></span>

[<span data-ttu-id="a6da3-158">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="a6da3-158">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="a6da3-159">Возобновить — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a6da3-159">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="a6da3-160">Остановить-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a6da3-160">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="a6da3-161">Приостановить — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a6da3-161">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


