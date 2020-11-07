---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 8742b9967720948118f132de23fd07dbfdcb5f0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731631"
---
# <span data-ttu-id="d7748-101">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="d7748-101">Get-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="d7748-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d7748-102">SYNOPSIS</span></span>
<span data-ttu-id="d7748-103">Возвращает задания компиляции DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="d7748-103">Gets DSC compilation jobs in Automation.</span></span>

## <span data-ttu-id="d7748-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d7748-104">SYNTAX</span></span>

### <span data-ttu-id="d7748-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d7748-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7748-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="d7748-106">ByJobId</span></span>
```
Get-AzAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7748-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d7748-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7748-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7748-108">DESCRIPTION</span></span>
<span data-ttu-id="d7748-109">Командлет **Get-AzAutomationDscCompilationJob** получает задания на компиляцию необходимой конфигурации (DSC) в Azure Automation (ТД).</span><span class="sxs-lookup"><span data-stu-id="d7748-109">The **Get-AzAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="d7748-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d7748-110">EXAMPLES</span></span>

### <span data-ttu-id="d7748-111">Пример 1: получение всех заданий компиляции DSC</span><span class="sxs-lookup"><span data-stu-id="d7748-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="d7748-112">Эта команда получает все задания компиляции в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d7748-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="d7748-113">Пример 2: получение заданий компиляции DSC для конфигурации</span><span class="sxs-lookup"><span data-stu-id="d7748-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="d7748-114">Эта команда получает все задания компиляции для конфигурации DSC с именем ContosoConfiguration в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d7748-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="d7748-115">Пример 3: получение определенного задания компиляции DSC</span><span class="sxs-lookup"><span data-stu-id="d7748-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="d7748-116">Эта команда получает задание компиляции с указанным ИДЕНТИФИКАТОРом в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d7748-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="d7748-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d7748-117">PARAMETERS</span></span>

### <span data-ttu-id="d7748-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d7748-118">-AutomationAccountName</span></span>
<span data-ttu-id="d7748-119">Указывает имя учетной записи автоматизации, содержащей задания компиляции DSC, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d7748-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d7748-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d7748-120">-ConfigurationName</span></span>
<span data-ttu-id="d7748-121">Указывает имя конфигурации DSC, для которой этот командлет получает задания компиляции.</span><span class="sxs-lookup"><span data-stu-id="d7748-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

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

### <span data-ttu-id="d7748-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7748-122">-DefaultProfile</span></span>
<span data-ttu-id="d7748-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d7748-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7748-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="d7748-124">-EndTime</span></span>
<span data-ttu-id="d7748-125">Указывает время окончания.</span><span class="sxs-lookup"><span data-stu-id="d7748-125">Specifies an end time.</span></span>
<span data-ttu-id="d7748-126">Этот командлет получает задания компиляции, запущенные до момента, когда этот параметр указывает.</span><span class="sxs-lookup"><span data-stu-id="d7748-126">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="d7748-127">-ID</span><span class="sxs-lookup"><span data-stu-id="d7748-127">-Id</span></span>
<span data-ttu-id="d7748-128">Указывает уникальный идентификатор задания компиляции DSC, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d7748-128">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d7748-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7748-129">-ResourceGroupName</span></span>
<span data-ttu-id="d7748-130">Указывает имя группы ресурсов, в которой этот командлет получает задания компиляции DSC.</span><span class="sxs-lookup"><span data-stu-id="d7748-130">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="d7748-131">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d7748-131">-StartTime</span></span>
<span data-ttu-id="d7748-132">Указывает время начала.</span><span class="sxs-lookup"><span data-stu-id="d7748-132">Specifies a start time.</span></span>
<span data-ttu-id="d7748-133">Этот командлет получает задания, которые начинаются с или после времени, указанном параметром.</span><span class="sxs-lookup"><span data-stu-id="d7748-133">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="d7748-134">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="d7748-134">-Status</span></span>
<span data-ttu-id="d7748-135">Указывает состояние заданий, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d7748-135">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="d7748-136">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="d7748-136">Valid values are:</span></span> 
- <span data-ttu-id="d7748-137">Completed</span><span class="sxs-lookup"><span data-stu-id="d7748-137">Completed</span></span> 
- <span data-ttu-id="d7748-138">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="d7748-138">Failed</span></span> 
- <span data-ttu-id="d7748-139">Очереди</span><span class="sxs-lookup"><span data-stu-id="d7748-139">Queued</span></span> 
- <span data-ttu-id="d7748-140">Начало</span><span class="sxs-lookup"><span data-stu-id="d7748-140">Starting</span></span> 
- <span data-ttu-id="d7748-141">Resuming</span><span class="sxs-lookup"><span data-stu-id="d7748-141">Resuming</span></span> 
- <span data-ttu-id="d7748-142">Использующ</span><span class="sxs-lookup"><span data-stu-id="d7748-142">Running</span></span> 
- <span data-ttu-id="d7748-143">Прекращена</span><span class="sxs-lookup"><span data-stu-id="d7748-143">Stopped</span></span> 
- <span data-ttu-id="d7748-144">Отключение</span><span class="sxs-lookup"><span data-stu-id="d7748-144">Stopping</span></span> 
- <span data-ttu-id="d7748-145">Остановить</span><span class="sxs-lookup"><span data-stu-id="d7748-145">Suspended</span></span> 
- <span data-ttu-id="d7748-146">Suspending</span><span class="sxs-lookup"><span data-stu-id="d7748-146">Suspending</span></span> 
- <span data-ttu-id="d7748-147">Сделать</span><span class="sxs-lookup"><span data-stu-id="d7748-147">Activating</span></span>
- <span data-ttu-id="d7748-148">Новые функции</span><span class="sxs-lookup"><span data-stu-id="d7748-148">New</span></span>

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

### <span data-ttu-id="d7748-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7748-149">CommonParameters</span></span>
<span data-ttu-id="d7748-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d7748-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7748-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7748-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7748-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d7748-152">INPUTS</span></span>

### <span data-ttu-id="d7748-153">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d7748-153">System.Guid</span></span>

### <span data-ttu-id="d7748-154">System. String</span><span class="sxs-lookup"><span data-stu-id="d7748-154">System.String</span></span>

## <span data-ttu-id="d7748-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7748-155">OUTPUTS</span></span>

### <span data-ttu-id="d7748-156">Microsoft. Azure. Commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="d7748-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="d7748-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="d7748-157">NOTES</span></span>

## <span data-ttu-id="d7748-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7748-158">RELATED LINKS</span></span>

[<span data-ttu-id="d7748-159">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="d7748-159">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="d7748-160">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="d7748-160">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


