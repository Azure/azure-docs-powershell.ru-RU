---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
ms.openlocfilehash: c84410a38cb803eab9dbe4866c7a9426c9c3a21d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560532"
---
# <span data-ttu-id="ff418-101">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ff418-101">Start-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="ff418-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff418-102">SYNOPSIS</span></span>
<span data-ttu-id="ff418-103">Запускает задание Runbook.</span><span class="sxs-lookup"><span data-stu-id="ff418-103">Starts a runbook job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff418-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff418-104">SYNTAX</span></span>

### <span data-ttu-id="ff418-105">ByAsynchronousReturnJob (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ff418-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ff418-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="ff418-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff418-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff418-107">DESCRIPTION</span></span>
<span data-ttu-id="ff418-108">Командлет **Start-AzureRmAutomationRunbook** запускает задание Azure Automation Runbook.</span><span class="sxs-lookup"><span data-stu-id="ff418-108">The **Start-AzureRmAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="ff418-109">Укажите идентификатор или имя Runbook.</span><span class="sxs-lookup"><span data-stu-id="ff418-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="ff418-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff418-110">EXAMPLES</span></span>

### <span data-ttu-id="ff418-111">Пример 1: запуск задания Runbook</span><span class="sxs-lookup"><span data-stu-id="ff418-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ff418-112">Эта команда запускает задание Runbook для модуля Runbook с именем Runbk01 в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ff418-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="ff418-113">Пример 2: запуск задания Runbook и ожидание результатов</span><span class="sxs-lookup"><span data-stu-id="ff418-113">Example 2: Start a runbook job and wait for results</span></span>
```
Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="ff418-114">Эта команда запускает задание Runbook для модуля Runbook с именем Runbk01 в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ff418-114">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="ff418-115">Эта команда задает параметр _Wait_ .</span><span class="sxs-lookup"><span data-stu-id="ff418-115">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="ff418-116">Поэтому он возвращает результаты после завершения задания.</span><span class="sxs-lookup"><span data-stu-id="ff418-116">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="ff418-117">Командлет ожидает в течение 1000 секунд для результатов.</span><span class="sxs-lookup"><span data-stu-id="ff418-117">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="ff418-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff418-118">PARAMETERS</span></span>

### <span data-ttu-id="ff418-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ff418-119">-AutomationAccountName</span></span>
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

### <span data-ttu-id="ff418-120">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="ff418-120">-MaxWaitSeconds</span></span>
<span data-ttu-id="ff418-121">Указывает количество секунд, в течение которых этот командлет ожидает завершения задания, прежде чем отказаться от него.</span><span class="sxs-lookup"><span data-stu-id="ff418-121">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="ff418-122">Значение по умолчанию — 10800 или три часа.</span><span class="sxs-lookup"><span data-stu-id="ff418-122">The default value is 10800, or three hours.</span></span>

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

### <span data-ttu-id="ff418-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ff418-123">-Name</span></span>
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

### <span data-ttu-id="ff418-124">-Parameters</span><span class="sxs-lookup"><span data-stu-id="ff418-124">-Parameters</span></span>
```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff418-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff418-125">-ResourceGroupName</span></span>
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

### <span data-ttu-id="ff418-126">-RunOn</span><span class="sxs-lookup"><span data-stu-id="ff418-126">-RunOn</span></span>
<span data-ttu-id="ff418-127">Указывает группу гибридного рабочего процесса, в которой нужно запустить Runbook.</span><span class="sxs-lookup"><span data-stu-id="ff418-127">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

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

### <span data-ttu-id="ff418-128">-Wait</span><span class="sxs-lookup"><span data-stu-id="ff418-128">-Wait</span></span>
<span data-ttu-id="ff418-129">Указывает на то, что этот командлет ожидает завершения, приостановки или сбоя задания, а затем возвращает управление в Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ff418-129">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

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

### <span data-ttu-id="ff418-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff418-130">-DefaultProfile</span></span>
<span data-ttu-id="ff418-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff418-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff418-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff418-132">CommonParameters</span></span>
<span data-ttu-id="ff418-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff418-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff418-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff418-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff418-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff418-135">INPUTS</span></span>

## <span data-ttu-id="ff418-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff418-136">OUTPUTS</span></span>

### <span data-ttu-id="ff418-137">Microsoft. Azure. Commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="ff418-137">Microsoft.Azure.Commands.Automation.Model.Job</span></span>
<span data-ttu-id="ff418-138">Этот командлет возвращает объект **задания** , если не указан параметр _Wait_ .</span><span class="sxs-lookup"><span data-stu-id="ff418-138">This cmdlet returns a **Job** object, unless you specify the _Wait_ parameter.</span></span>

<span data-ttu-id="ff418-139">Если не указать _Wait_ , служба Azure PowerShell немедленно возвращает объект **задания** .</span><span class="sxs-lookup"><span data-stu-id="ff418-139">If you do not specify _Wait_ , Azure PowerShell returns a **Job** object immediately.</span></span>
<span data-ttu-id="ff418-140">Если вы задаете параметр _Wait_ , Azure PowerShell завершает выполнение задания и возвращает результат.</span><span class="sxs-lookup"><span data-stu-id="ff418-140">If you specify _Wait_ , Azure PowerShell completes the job, and then returns the result.</span></span>
<span data-ttu-id="ff418-141">Результат — это не объект **Job** .</span><span class="sxs-lookup"><span data-stu-id="ff418-141">The result is not a **Job** object.</span></span>

## <span data-ttu-id="ff418-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff418-142">NOTES</span></span>

## <span data-ttu-id="ff418-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff418-143">RELATED LINKS</span></span>

[<span data-ttu-id="ff418-144">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ff418-144">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ff418-145">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ff418-145">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ff418-146">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ff418-146">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ff418-147">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ff418-147">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ff418-148">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ff418-148">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ff418-149">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ff418-149">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ff418-150">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ff418-150">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ff418-151">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ff418-151">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)
