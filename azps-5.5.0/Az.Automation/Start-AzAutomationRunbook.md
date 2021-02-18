---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
ms.openlocfilehash: 70d322b46f8aa9dc90696cbd813e576cc9dd9fbd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216161"
---
# <span data-ttu-id="43dce-101">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43dce-101">Start-AzAutomationRunbook</span></span>

## <span data-ttu-id="43dce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43dce-102">SYNOPSIS</span></span>
<span data-ttu-id="43dce-103">Запускает задание книги.</span><span class="sxs-lookup"><span data-stu-id="43dce-103">Starts a runbook job.</span></span>

## <span data-ttu-id="43dce-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="43dce-104">SYNTAX</span></span>

### <span data-ttu-id="43dce-105">ByAsynchronousReturnJob (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="43dce-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43dce-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="43dce-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43dce-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43dce-107">DESCRIPTION</span></span>
<span data-ttu-id="43dce-108">Для запуска задания книги автоматизации Azure запускается **cmdlet Start-AzAutomationRunbook.**</span><span class="sxs-lookup"><span data-stu-id="43dce-108">The **Start-AzAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="43dce-109">Укажите имя или ИД книги.</span><span class="sxs-lookup"><span data-stu-id="43dce-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="43dce-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="43dce-110">EXAMPLES</span></span>

### <span data-ttu-id="43dce-111">Пример 1. Запуск задания книги</span><span class="sxs-lookup"><span data-stu-id="43dce-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="43dce-112">Эта команда запускает задание книги Runbk01 в учетной записи автоматизации Azure Contoso17.</span><span class="sxs-lookup"><span data-stu-id="43dce-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="43dce-113">Пример 2. Запуск задания книги Python 2 с параметрами</span><span class="sxs-lookup"><span data-stu-id="43dce-113">Example 2: Start a Python 2 runbook job with parameters</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "RunbkPy01" -ResourceGroupName "ResourceGroup01" -Parameters @{"Key1"="ValueForPosition1";"Key2"="ValueForPosition2"}
```

<span data-ttu-id="43dce-114">Эта команда запускает задание книги Python 2 с именем RunbkPy01 в учетной записи автоматизации Azure с именем Contoso17 со значениемForPosition1 в качестве первого позиционного параметра, а для второго — с параметром ValueForPosition2.</span><span class="sxs-lookup"><span data-stu-id="43dce-114">This command starts a runbook job for the Python 2 runbook named RunbkPy01 in the Azure Automation account named Contoso17 with "ValueForPosition1" as the first positional parameter and "ValueForPosition2" for the second one.</span></span>

### <span data-ttu-id="43dce-115">Пример 3. Запуск задания и ожидание результатов</span><span class="sxs-lookup"><span data-stu-id="43dce-115">Example 3: Start a runbook job and wait for results</span></span>
```
Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="43dce-116">Эта команда запускает задание книги runbk01 в учетной записи автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="43dce-116">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="43dce-117">Эта команда определяет параметр _Wait._</span><span class="sxs-lookup"><span data-stu-id="43dce-117">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="43dce-118">Таким образом, она возвращает результаты после завершения задания.</span><span class="sxs-lookup"><span data-stu-id="43dce-118">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="43dce-119">Результат будет отсек 1000 секунд.</span><span class="sxs-lookup"><span data-stu-id="43dce-119">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="43dce-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43dce-120">PARAMETERS</span></span>

### <span data-ttu-id="43dce-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="43dce-121">-AutomationAccountName</span></span>
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

### <span data-ttu-id="43dce-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43dce-122">-DefaultProfile</span></span>
<span data-ttu-id="43dce-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="43dce-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43dce-124">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="43dce-124">-MaxWaitSeconds</span></span>
<span data-ttu-id="43dce-125">Определяет, сколько секунд этот cmdlet должен подождать завершения задания, прежде чем оно завершит работу.</span><span class="sxs-lookup"><span data-stu-id="43dce-125">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="43dce-126">Значение по умолчанию — 10800 или три часа.</span><span class="sxs-lookup"><span data-stu-id="43dce-126">The default value is 10800, or three hours.</span></span>

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

### <span data-ttu-id="43dce-127">-Name</span><span class="sxs-lookup"><span data-stu-id="43dce-127">-Name</span></span>
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

### <span data-ttu-id="43dce-128">-Parameters</span><span class="sxs-lookup"><span data-stu-id="43dce-128">-Parameters</span></span>
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

### <span data-ttu-id="43dce-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43dce-129">-ResourceGroupName</span></span>
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

### <span data-ttu-id="43dce-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="43dce-130">-RunOn</span></span>
<span data-ttu-id="43dce-131">Определяет гибридную группу рабочих, для которой нужно запустить книгу.</span><span class="sxs-lookup"><span data-stu-id="43dce-131">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

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

### <span data-ttu-id="43dce-132">-Wait</span><span class="sxs-lookup"><span data-stu-id="43dce-132">-Wait</span></span>
<span data-ttu-id="43dce-133">Указывает на то, что этот cmdlet ждет завершения задания, приостановки или сбой, а затем возвращает управление в Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="43dce-133">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

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

### <span data-ttu-id="43dce-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43dce-134">CommonParameters</span></span>
<span data-ttu-id="43dce-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43dce-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43dce-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43dce-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43dce-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43dce-137">INPUTS</span></span>

### <span data-ttu-id="43dce-138">System.String</span><span class="sxs-lookup"><span data-stu-id="43dce-138">System.String</span></span>

## <span data-ttu-id="43dce-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="43dce-139">OUTPUTS</span></span>

### <span data-ttu-id="43dce-140">Microsoft.Azure.Commands.Automation.Model.Job</span><span class="sxs-lookup"><span data-stu-id="43dce-140">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

### <span data-ttu-id="43dce-141">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="43dce-141">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="43dce-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="43dce-142">NOTES</span></span>

## <span data-ttu-id="43dce-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43dce-143">RELATED LINKS</span></span>

[<span data-ttu-id="43dce-144">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43dce-144">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="43dce-145">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43dce-145">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="43dce-146">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43dce-146">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="43dce-147">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43dce-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="43dce-148">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43dce-148">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="43dce-149">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43dce-149">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="43dce-150">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43dce-150">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="43dce-151">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43dce-151">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)
