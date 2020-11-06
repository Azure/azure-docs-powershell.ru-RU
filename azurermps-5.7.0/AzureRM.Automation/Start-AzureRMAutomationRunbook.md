---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
ms.openlocfilehash: c3c59c8c4f503b090a77a93014f50dd7e2ce01dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561947"
---
# <span data-ttu-id="ad66d-101">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ad66d-101">Start-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="ad66d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad66d-102">SYNOPSIS</span></span>
<span data-ttu-id="ad66d-103">Запускает задание Runbook.</span><span class="sxs-lookup"><span data-stu-id="ad66d-103">Starts a runbook job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad66d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad66d-104">SYNTAX</span></span>

### <span data-ttu-id="ad66d-105">ByAsynchronousReturnJob (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ad66d-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad66d-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="ad66d-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad66d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad66d-107">DESCRIPTION</span></span>
<span data-ttu-id="ad66d-108">Командлет **Start-AzureRmAutomationRunbook** запускает задание Azure Automation Runbook.</span><span class="sxs-lookup"><span data-stu-id="ad66d-108">The **Start-AzureRmAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="ad66d-109">Укажите идентификатор или имя Runbook.</span><span class="sxs-lookup"><span data-stu-id="ad66d-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="ad66d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad66d-110">EXAMPLES</span></span>

### <span data-ttu-id="ad66d-111">Пример 1: запуск задания Runbook</span><span class="sxs-lookup"><span data-stu-id="ad66d-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ad66d-112">Эта команда запускает задание Runbook для модуля Runbook с именем Runbk01 в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ad66d-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="ad66d-113">Пример 2: запуск задания Runbook и ожидание результатов</span><span class="sxs-lookup"><span data-stu-id="ad66d-113">Example 2: Start a runbook job and wait for results</span></span>
```
Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="ad66d-114">Эта команда запускает задание Runbook для модуля Runbook с именем Runbk01 в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ad66d-114">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="ad66d-115">Эта команда задает параметр _Wait_ .</span><span class="sxs-lookup"><span data-stu-id="ad66d-115">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="ad66d-116">Поэтому он возвращает результаты после завершения задания.</span><span class="sxs-lookup"><span data-stu-id="ad66d-116">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="ad66d-117">Командлет ожидает в течение 1000 секунд для результатов.</span><span class="sxs-lookup"><span data-stu-id="ad66d-117">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="ad66d-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad66d-118">PARAMETERS</span></span>

### <span data-ttu-id="ad66d-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ad66d-119">-AutomationAccountName</span></span>
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

### <span data-ttu-id="ad66d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad66d-120">-DefaultProfile</span></span>
<span data-ttu-id="ad66d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ad66d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad66d-122">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="ad66d-122">-MaxWaitSeconds</span></span>
<span data-ttu-id="ad66d-123">Указывает количество секунд, в течение которых этот командлет ожидает завершения задания, прежде чем отказаться от него.</span><span class="sxs-lookup"><span data-stu-id="ad66d-123">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="ad66d-124">Значение по умолчанию — 10800 или три часа.</span><span class="sxs-lookup"><span data-stu-id="ad66d-124">The default value is 10800, or three hours.</span></span>

```yaml
Type: Int32
Parameter Sets: BySynchronousReturnJobOutput
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad66d-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ad66d-125">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad66d-126">-Parameters</span><span class="sxs-lookup"><span data-stu-id="ad66d-126">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad66d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad66d-127">-ResourceGroupName</span></span>
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

### <span data-ttu-id="ad66d-128">-RunOn</span><span class="sxs-lookup"><span data-stu-id="ad66d-128">-RunOn</span></span>
<span data-ttu-id="ad66d-129">Указывает группу гибридного рабочего процесса, в которой нужно запустить Runbook.</span><span class="sxs-lookup"><span data-stu-id="ad66d-129">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad66d-130">-Wait</span><span class="sxs-lookup"><span data-stu-id="ad66d-130">-Wait</span></span>
<span data-ttu-id="ad66d-131">Указывает на то, что этот командлет ожидает завершения, приостановки или сбоя задания, а затем возвращает управление в Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ad66d-131">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySynchronousReturnJobOutput
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad66d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad66d-132">CommonParameters</span></span>
<span data-ttu-id="ad66d-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad66d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad66d-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad66d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad66d-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad66d-135">INPUTS</span></span>

### <span data-ttu-id="ad66d-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="ad66d-136">None</span></span>
<span data-ttu-id="ad66d-137">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="ad66d-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ad66d-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad66d-138">OUTPUTS</span></span>

### <span data-ttu-id="ad66d-139">Microsoft. Azure. Commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="ad66d-139">Microsoft.Azure.Commands.Automation.Model.Job</span></span>
<span data-ttu-id="ad66d-140">Этот командлет возвращает объект **задания** , если не указан параметр _Wait_ .</span><span class="sxs-lookup"><span data-stu-id="ad66d-140">This cmdlet returns a **Job** object, unless you specify the _Wait_ parameter.</span></span>

<span data-ttu-id="ad66d-141">Если не указать _Wait_ , служба Azure PowerShell немедленно возвращает объект **задания** .</span><span class="sxs-lookup"><span data-stu-id="ad66d-141">If you do not specify _Wait_ , Azure PowerShell returns a **Job** object immediately.</span></span>
<span data-ttu-id="ad66d-142">Если вы задаете параметр _Wait_ , Azure PowerShell завершает выполнение задания и возвращает результат.</span><span class="sxs-lookup"><span data-stu-id="ad66d-142">If you specify _Wait_ , Azure PowerShell completes the job, and then returns the result.</span></span>
<span data-ttu-id="ad66d-143">Результат — это не объект **Job** .</span><span class="sxs-lookup"><span data-stu-id="ad66d-143">The result is not a **Job** object.</span></span>

## <span data-ttu-id="ad66d-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad66d-144">NOTES</span></span>

## <span data-ttu-id="ad66d-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad66d-145">RELATED LINKS</span></span>

[<span data-ttu-id="ad66d-146">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ad66d-146">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ad66d-147">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ad66d-147">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ad66d-148">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ad66d-148">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ad66d-149">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ad66d-149">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ad66d-150">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ad66d-150">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ad66d-151">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ad66d-151">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ad66d-152">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ad66d-152">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ad66d-153">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ad66d-153">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)
