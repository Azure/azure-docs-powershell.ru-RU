---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
ms.openlocfilehash: 70d322b46f8aa9dc90696cbd813e576cc9dd9fbd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065040"
---
# <span data-ttu-id="7c4bd-101">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7c4bd-101">Start-AzAutomationRunbook</span></span>

## <span data-ttu-id="7c4bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7c4bd-102">SYNOPSIS</span></span>
<span data-ttu-id="7c4bd-103">Запускает задание Runbook.</span><span class="sxs-lookup"><span data-stu-id="7c4bd-103">Starts a runbook job.</span></span>

## <span data-ttu-id="7c4bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7c4bd-104">SYNTAX</span></span>

### <span data-ttu-id="7c4bd-105">ByAsynchronousReturnJob (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7c4bd-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c4bd-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="7c4bd-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c4bd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c4bd-107">DESCRIPTION</span></span>
<span data-ttu-id="7c4bd-108">Командлет **Start-AzAutomationRunbook** запускает задание Azure Automation Runbook.</span><span class="sxs-lookup"><span data-stu-id="7c4bd-108">The **Start-AzAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="7c4bd-109">Укажите идентификатор или имя Runbook.</span><span class="sxs-lookup"><span data-stu-id="7c4bd-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="7c4bd-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7c4bd-110">EXAMPLES</span></span>

### <span data-ttu-id="7c4bd-111">Пример 1: запуск задания Runbook</span><span class="sxs-lookup"><span data-stu-id="7c4bd-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7c4bd-112">Эта команда запускает задание Runbook для модуля Runbook с именем Runbk01 в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7c4bd-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="7c4bd-113">Пример 2: запуск задания Runbook для Python 2 с параметрами</span><span class="sxs-lookup"><span data-stu-id="7c4bd-113">Example 2: Start a Python 2 runbook job with parameters</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "RunbkPy01" -ResourceGroupName "ResourceGroup01" -Parameters @{"Key1"="ValueForPosition1";"Key2"="ValueForPosition2"}
```

<span data-ttu-id="7c4bd-114">Эта команда запускает задание Runbook для модуля Python 2 Runbook с именем RunbkPy01 в учетной записи службы автоматизации Azure с именем Contoso17 и "ValueForPosition1" в качестве первого позиционного параметра и "ValueForPosition2" для второго.</span><span class="sxs-lookup"><span data-stu-id="7c4bd-114">This command starts a runbook job for the Python 2 runbook named RunbkPy01 in the Azure Automation account named Contoso17 with "ValueForPosition1" as the first positional parameter and "ValueForPosition2" for the second one.</span></span>

### <span data-ttu-id="7c4bd-115">Пример 3: запуск задания Runbook и ожидание результатов</span><span class="sxs-lookup"><span data-stu-id="7c4bd-115">Example 3: Start a runbook job and wait for results</span></span>
```
Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="7c4bd-116">Эта команда запускает задание Runbook для модуля Runbook с именем Runbk01 в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7c4bd-116">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="7c4bd-117">Эта команда задает параметр _Wait_ .</span><span class="sxs-lookup"><span data-stu-id="7c4bd-117">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="7c4bd-118">Поэтому он возвращает результаты после завершения задания.</span><span class="sxs-lookup"><span data-stu-id="7c4bd-118">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="7c4bd-119">Командлет ожидает в течение 1000 секунд для результатов.</span><span class="sxs-lookup"><span data-stu-id="7c4bd-119">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="7c4bd-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7c4bd-120">PARAMETERS</span></span>

### <span data-ttu-id="7c4bd-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7c4bd-121">-AutomationAccountName</span></span>
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

### <span data-ttu-id="7c4bd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c4bd-122">-DefaultProfile</span></span>
<span data-ttu-id="7c4bd-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7c4bd-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c4bd-124">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="7c4bd-124">-MaxWaitSeconds</span></span>
<span data-ttu-id="7c4bd-125">Указывает количество секунд, в течение которых этот командлет ожидает завершения задания, прежде чем отказаться от него.</span><span class="sxs-lookup"><span data-stu-id="7c4bd-125">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="7c4bd-126">Значение по умолчанию — 10800 или три часа.</span><span class="sxs-lookup"><span data-stu-id="7c4bd-126">The default value is 10800, or three hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: BySynchronousReturnJobOutput
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c4bd-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7c4bd-127">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c4bd-128">-Parameters</span><span class="sxs-lookup"><span data-stu-id="7c4bd-128">-Parameters</span></span>
```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: JobParameters

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c4bd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c4bd-129">-ResourceGroupName</span></span>
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

### <span data-ttu-id="7c4bd-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="7c4bd-130">-RunOn</span></span>
<span data-ttu-id="7c4bd-131">Указывает группу гибридного рабочего процесса, в которой нужно запустить Runbook.</span><span class="sxs-lookup"><span data-stu-id="7c4bd-131">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c4bd-132">-Wait</span><span class="sxs-lookup"><span data-stu-id="7c4bd-132">-Wait</span></span>
<span data-ttu-id="7c4bd-133">Указывает на то, что этот командлет ожидает завершения, приостановки или сбоя задания, а затем возвращает управление в Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7c4bd-133">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySynchronousReturnJobOutput
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c4bd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c4bd-134">CommonParameters</span></span>
<span data-ttu-id="7c4bd-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7c4bd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c4bd-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c4bd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c4bd-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7c4bd-137">INPUTS</span></span>

### <span data-ttu-id="7c4bd-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7c4bd-138">System.String</span></span>

## <span data-ttu-id="7c4bd-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c4bd-139">OUTPUTS</span></span>

### <span data-ttu-id="7c4bd-140">Microsoft. Azure. Commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="7c4bd-140">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

### <span data-ttu-id="7c4bd-141">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="7c4bd-141">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7c4bd-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="7c4bd-142">NOTES</span></span>

## <span data-ttu-id="7c4bd-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c4bd-143">RELATED LINKS</span></span>

[<span data-ttu-id="7c4bd-144">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7c4bd-144">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="7c4bd-145">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7c4bd-145">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="7c4bd-146">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7c4bd-146">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="7c4bd-147">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7c4bd-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="7c4bd-148">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7c4bd-148">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="7c4bd-149">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7c4bd-149">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="7c4bd-150">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7c4bd-150">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="7c4bd-151">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7c4bd-151">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)
