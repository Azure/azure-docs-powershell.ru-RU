---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 6527FF45-9C16-47E8-8E70-619A0581D2F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: c595779fa8c6b4c246f102a346290e931dc89379
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076369"
---
# <span data-ttu-id="43da2-101">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="43da2-101">Get-AzureAutomationJob</span></span>

## <span data-ttu-id="43da2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="43da2-102">SYNOPSIS</span></span>

<span data-ttu-id="43da2-103">Получает одно или несколько заданий Runbook службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="43da2-103">Gets one or more Azure Automation runbook jobs.</span></span>

## <span data-ttu-id="43da2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="43da2-104">SYNTAX</span></span>

### <span data-ttu-id="43da2-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="43da2-105">ByAll (Default)</span></span>
```
Get-AzureAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="43da2-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="43da2-106">ByJobId</span></span>
```
Get-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="43da2-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="43da2-107">ByRunbookName</span></span>
```
Get-AzureAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="43da2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43da2-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="43da2-109">Командлет **Get-AzureAutomationJob** получает одно или несколько заданий Runbook в службе автоматизации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="43da2-109">The **Get-AzureAutomationJob** cmdlet gets one or more runbook jobs in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="43da2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="43da2-110">EXAMPLES</span></span>

### <span data-ttu-id="43da2-111">Пример 1: получение определенного задания Runbook</span><span class="sxs-lookup"><span data-stu-id="43da2-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="43da2-112">Эта команда получает задание с указанным GUID.</span><span class="sxs-lookup"><span data-stu-id="43da2-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="43da2-113">Пример 2: получение всех заданий для Runbook</span><span class="sxs-lookup"><span data-stu-id="43da2-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -RunbookName "MyRunbook"
```

<span data-ttu-id="43da2-114">Эта команда возвращает все задания, связанные с модулем Runbook с именем MyRunbook.</span><span class="sxs-lookup"><span data-stu-id="43da2-114">This command gets all jobs associated with a runbook named MyRunbook.</span></span>

### <span data-ttu-id="43da2-115">Пример 2: получение всех выполняемых заданий</span><span class="sxs-lookup"><span data-stu-id="43da2-115">Example 2: Get all running jobs</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -Status "Running"
```

<span data-ttu-id="43da2-116">Эта команда получает все выполняемые задания в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="43da2-116">This command gets all running jobs in the automation account with the name Contoso17.</span></span>

## <span data-ttu-id="43da2-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="43da2-117">PARAMETERS</span></span>

### <span data-ttu-id="43da2-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="43da2-118">-AutomationAccountName</span></span>
<span data-ttu-id="43da2-119">Указывает имя учетной записи службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="43da2-119">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43da2-120">-EndTime</span><span class="sxs-lookup"><span data-stu-id="43da2-120">-EndTime</span></span>
<span data-ttu-id="43da2-121">Указывает время окончания для задания.</span><span class="sxs-lookup"><span data-stu-id="43da2-121">Specifies the end time for a job.</span></span>

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

### <span data-ttu-id="43da2-122">-ID</span><span class="sxs-lookup"><span data-stu-id="43da2-122">-Id</span></span>
<span data-ttu-id="43da2-123">Указывает идентификатор задания.</span><span class="sxs-lookup"><span data-stu-id="43da2-123">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="43da2-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="43da2-124">-Profile</span></span>
<span data-ttu-id="43da2-125">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="43da2-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="43da2-126">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="43da2-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43da2-127">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="43da2-127">-RunbookName</span></span>
<span data-ttu-id="43da2-128">Указывает имя Runbook.</span><span class="sxs-lookup"><span data-stu-id="43da2-128">Specifies the name of a runbook.</span></span>

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

### <span data-ttu-id="43da2-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="43da2-129">-StartTime</span></span>
<span data-ttu-id="43da2-130">Указывает время начала задания.</span><span class="sxs-lookup"><span data-stu-id="43da2-130">Specifies the start time of a job.</span></span>

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

### <span data-ttu-id="43da2-131">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="43da2-131">-Status</span></span>
<span data-ttu-id="43da2-132">Указывает состояние задания.</span><span class="sxs-lookup"><span data-stu-id="43da2-132">Specifies the status of a job.</span></span>
<span data-ttu-id="43da2-133">Этот командлет получает задания, которые имеют состояние, совпадающее с этим параметром.</span><span class="sxs-lookup"><span data-stu-id="43da2-133">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="43da2-134">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="43da2-134">Valid values are:</span></span> 

- <span data-ttu-id="43da2-135">Completed</span><span class="sxs-lookup"><span data-stu-id="43da2-135">Completed</span></span>
- <span data-ttu-id="43da2-136">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="43da2-136">Failed</span></span>
- <span data-ttu-id="43da2-137">Очереди</span><span class="sxs-lookup"><span data-stu-id="43da2-137">Queued</span></span>
- <span data-ttu-id="43da2-138">Начало</span><span class="sxs-lookup"><span data-stu-id="43da2-138">Starting</span></span>
- <span data-ttu-id="43da2-139">Resuming</span><span class="sxs-lookup"><span data-stu-id="43da2-139">Resuming</span></span>
- <span data-ttu-id="43da2-140">Использующ</span><span class="sxs-lookup"><span data-stu-id="43da2-140">Running</span></span>
- <span data-ttu-id="43da2-141">Прекращена</span><span class="sxs-lookup"><span data-stu-id="43da2-141">Stopped</span></span>
- <span data-ttu-id="43da2-142">Отключение</span><span class="sxs-lookup"><span data-stu-id="43da2-142">Stopping</span></span>
- <span data-ttu-id="43da2-143">Остановить</span><span class="sxs-lookup"><span data-stu-id="43da2-143">Suspended</span></span>
- <span data-ttu-id="43da2-144">Suspending</span><span class="sxs-lookup"><span data-stu-id="43da2-144">Suspending</span></span>
- <span data-ttu-id="43da2-145">Сделать</span><span class="sxs-lookup"><span data-stu-id="43da2-145">Activating</span></span>

```yaml
Type: String
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43da2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43da2-146">CommonParameters</span></span>
<span data-ttu-id="43da2-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="43da2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43da2-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43da2-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43da2-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="43da2-149">INPUTS</span></span>

## <span data-ttu-id="43da2-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="43da2-150">OUTPUTS</span></span>

### <span data-ttu-id="43da2-151">Microsoft. Azure. Commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="43da2-151">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="43da2-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="43da2-152">NOTES</span></span>

## <span data-ttu-id="43da2-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43da2-153">RELATED LINKS</span></span>

[<span data-ttu-id="43da2-154">Возобновить — AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="43da2-154">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="43da2-155">Остановить-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="43da2-155">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="43da2-156">Приостановить — AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="43da2-156">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


