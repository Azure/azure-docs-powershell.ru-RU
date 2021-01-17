---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 5b2c8685596771cd7986d8cfa071808daa63435c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399431"
---
# <span data-ttu-id="5eaeb-101">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="5eaeb-101">Get-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="5eaeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5eaeb-102">SYNOPSIS</span></span>
<span data-ttu-id="5eaeb-103">Получает задания компиляции DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-103">Gets DSC compilation jobs in Automation.</span></span>

## <span data-ttu-id="5eaeb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5eaeb-104">SYNTAX</span></span>

### <span data-ttu-id="5eaeb-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5eaeb-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5eaeb-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="5eaeb-106">ByJobId</span></span>
```
Get-AzAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5eaeb-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="5eaeb-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5eaeb-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5eaeb-108">DESCRIPTION</span></span>
<span data-ttu-id="5eaeb-109">Для получения заданий компиляции APS в автоматизации Azure можно получить задания компиляции **APS-AzAutomationDscCompilationJob.**</span><span class="sxs-lookup"><span data-stu-id="5eaeb-109">The **Get-AzAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="5eaeb-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5eaeb-110">EXAMPLES</span></span>

### <span data-ttu-id="5eaeb-111">Пример 1. Все задания компиляции DSC</span><span class="sxs-lookup"><span data-stu-id="5eaeb-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="5eaeb-112">Эта команда получает все задания компиляции в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="5eaeb-113">Пример 2. Задания компиляции DSC для конфигурации</span><span class="sxs-lookup"><span data-stu-id="5eaeb-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="5eaeb-114">Эта команда получает все задания компиляции для конфигурации DSC ContosoConfiguration в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="5eaeb-115">Пример 3. Задание компиляции DSC</span><span class="sxs-lookup"><span data-stu-id="5eaeb-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="5eaeb-116">Эта команда получает задание компиляции с указанным именем в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="5eaeb-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5eaeb-117">PARAMETERS</span></span>

### <span data-ttu-id="5eaeb-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5eaeb-118">-AutomationAccountName</span></span>
<span data-ttu-id="5eaeb-119">Указывает имя учетной записи автоматизации, которая содержит задания компиляции DSC, которые получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5eaeb-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="5eaeb-120">-ConfigurationName</span></span>
<span data-ttu-id="5eaeb-121">Указывает имя конфигурации DSC, для которой этот cmdlet получает задания компиляции.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eaeb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eaeb-122">-DefaultProfile</span></span>
<span data-ttu-id="5eaeb-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5eaeb-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5eaeb-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="5eaeb-124">-EndTime</span></span>
<span data-ttu-id="5eaeb-125">Время окончания.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-125">Specifies an end time.</span></span>
<span data-ttu-id="5eaeb-126">Этот cmdlet получает задания компиляции, которые начали работу до времени, указанного для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-126">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eaeb-127">-Id</span><span class="sxs-lookup"><span data-stu-id="5eaeb-127">-Id</span></span>
<span data-ttu-id="5eaeb-128">Указывает уникальный код задания компиляции DSC, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-128">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5eaeb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eaeb-129">-ResourceGroupName</span></span>
<span data-ttu-id="5eaeb-130">Указывает имя группы ресурсов, в которой этот cmdlet получает задания компиляции DSC.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-130">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="5eaeb-131">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5eaeb-131">-StartTime</span></span>
<span data-ttu-id="5eaeb-132">Время начала.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-132">Specifies a start time.</span></span>
<span data-ttu-id="5eaeb-133">Этот cmdlet получает задания, которые начинаются с указанного параметра или после него.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-133">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eaeb-134">-Status</span><span class="sxs-lookup"><span data-stu-id="5eaeb-134">-Status</span></span>
<span data-ttu-id="5eaeb-135">Определяет состояние заданий, которые получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-135">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="5eaeb-136">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="5eaeb-136">Valid values are:</span></span> 
- <span data-ttu-id="5eaeb-137">Завершено</span><span class="sxs-lookup"><span data-stu-id="5eaeb-137">Completed</span></span> 
- <span data-ttu-id="5eaeb-138">Сбой</span><span class="sxs-lookup"><span data-stu-id="5eaeb-138">Failed</span></span> 
- <span data-ttu-id="5eaeb-139">В очереди</span><span class="sxs-lookup"><span data-stu-id="5eaeb-139">Queued</span></span> 
- <span data-ttu-id="5eaeb-140">Запуск</span><span class="sxs-lookup"><span data-stu-id="5eaeb-140">Starting</span></span> 
- <span data-ttu-id="5eaeb-141">Резюме</span><span class="sxs-lookup"><span data-stu-id="5eaeb-141">Resuming</span></span> 
- <span data-ttu-id="5eaeb-142">Запущена</span><span class="sxs-lookup"><span data-stu-id="5eaeb-142">Running</span></span> 
- <span data-ttu-id="5eaeb-143">Остановлено</span><span class="sxs-lookup"><span data-stu-id="5eaeb-143">Stopped</span></span> 
- <span data-ttu-id="5eaeb-144">Остановка</span><span class="sxs-lookup"><span data-stu-id="5eaeb-144">Stopping</span></span> 
- <span data-ttu-id="5eaeb-145">Приостановлено</span><span class="sxs-lookup"><span data-stu-id="5eaeb-145">Suspended</span></span> 
- <span data-ttu-id="5eaeb-146">Приостановка</span><span class="sxs-lookup"><span data-stu-id="5eaeb-146">Suspending</span></span> 
- <span data-ttu-id="5eaeb-147">Активация</span><span class="sxs-lookup"><span data-stu-id="5eaeb-147">Activating</span></span>
- <span data-ttu-id="5eaeb-148">Новые функции</span><span class="sxs-lookup"><span data-stu-id="5eaeb-148">New</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating, New

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eaeb-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eaeb-149">CommonParameters</span></span>
<span data-ttu-id="5eaeb-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eaeb-151">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5eaeb-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eaeb-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5eaeb-152">INPUTS</span></span>

### <span data-ttu-id="5eaeb-153">System.Guid</span><span class="sxs-lookup"><span data-stu-id="5eaeb-153">System.Guid</span></span>

### <span data-ttu-id="5eaeb-154">System.String</span><span class="sxs-lookup"><span data-stu-id="5eaeb-154">System.String</span></span>

## <span data-ttu-id="5eaeb-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5eaeb-155">OUTPUTS</span></span>

### <span data-ttu-id="5eaeb-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span><span class="sxs-lookup"><span data-stu-id="5eaeb-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="5eaeb-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5eaeb-157">NOTES</span></span>

## <span data-ttu-id="5eaeb-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5eaeb-158">RELATED LINKS</span></span>

[<span data-ttu-id="5eaeb-159">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="5eaeb-159">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="5eaeb-160">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="5eaeb-160">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


