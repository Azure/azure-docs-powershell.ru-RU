---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
ms.openlocfilehash: 59263dab3037e050229bab2a69c43559c2c1827b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567182"
---
# <span data-ttu-id="dba9c-101">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="dba9c-101">Get-AzureRmAutomationDscCompilationJob</span></span>

## <span data-ttu-id="dba9c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dba9c-102">SYNOPSIS</span></span>
<span data-ttu-id="dba9c-103">Возвращает задания компиляции DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="dba9c-103">Gets DSC compilation jobs in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dba9c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dba9c-104">SYNTAX</span></span>

### <span data-ttu-id="dba9c-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dba9c-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dba9c-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="dba9c-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dba9c-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="dba9c-107">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>]
 [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dba9c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dba9c-108">DESCRIPTION</span></span>
<span data-ttu-id="dba9c-109">Командлет **Get-AzureRmAutomationDscCompilationJob** получает задания на компиляцию необходимой конфигурации (DSC) в Azure Automation (ТД).</span><span class="sxs-lookup"><span data-stu-id="dba9c-109">The **Get-AzureRmAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="dba9c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dba9c-110">EXAMPLES</span></span>

### <span data-ttu-id="dba9c-111">Пример 1: получение всех заданий компиляции DSC</span><span class="sxs-lookup"><span data-stu-id="dba9c-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="dba9c-112">Эта команда получает все задания компиляции в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="dba9c-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="dba9c-113">Пример 2: получение заданий компиляции DSC для конфигурации</span><span class="sxs-lookup"><span data-stu-id="dba9c-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="dba9c-114">Эта команда получает все задания компиляции для конфигурации DSC с именем ContosoConfiguration в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="dba9c-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="dba9c-115">Пример 3: получение определенного задания компиляции DSC</span><span class="sxs-lookup"><span data-stu-id="dba9c-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="dba9c-116">Эта команда получает задание компиляции с указанным ИДЕНТИФИКАТОРом в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="dba9c-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="dba9c-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dba9c-117">PARAMETERS</span></span>

### <span data-ttu-id="dba9c-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dba9c-118">-AutomationAccountName</span></span>
<span data-ttu-id="dba9c-119">Указывает имя учетной записи автоматизации, содержащей задания компиляции DSC, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="dba9c-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="dba9c-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="dba9c-120">-ConfigurationName</span></span>
<span data-ttu-id="dba9c-121">Указывает имя конфигурации DSC, для которой этот командлет получает задания компиляции.</span><span class="sxs-lookup"><span data-stu-id="dba9c-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

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

### <span data-ttu-id="dba9c-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="dba9c-122">-EndTime</span></span>
<span data-ttu-id="dba9c-123">Указывает время окончания.</span><span class="sxs-lookup"><span data-stu-id="dba9c-123">Specifies an end time.</span></span>
<span data-ttu-id="dba9c-124">Этот командлет получает задания компиляции, запущенные до момента, когда этот параметр указывает.</span><span class="sxs-lookup"><span data-stu-id="dba9c-124">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="dba9c-125">-ID</span><span class="sxs-lookup"><span data-stu-id="dba9c-125">-Id</span></span>
<span data-ttu-id="dba9c-126">Указывает уникальный идентификатор задания компиляции DSC, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="dba9c-126">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="dba9c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dba9c-127">-ResourceGroupName</span></span>
<span data-ttu-id="dba9c-128">Указывает имя группы ресурсов, в которой этот командлет получает задания компиляции DSC.</span><span class="sxs-lookup"><span data-stu-id="dba9c-128">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="dba9c-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="dba9c-129">-StartTime</span></span>
<span data-ttu-id="dba9c-130">Указывает время начала.</span><span class="sxs-lookup"><span data-stu-id="dba9c-130">Specifies a start time.</span></span>
<span data-ttu-id="dba9c-131">Этот командлет получает задания, которые начинаются с или после времени, указанном параметром.</span><span class="sxs-lookup"><span data-stu-id="dba9c-131">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="dba9c-132">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="dba9c-132">-Status</span></span>
<span data-ttu-id="dba9c-133">Указывает состояние заданий, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="dba9c-133">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="dba9c-134">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="dba9c-134">Valid values are:</span></span> 

- <span data-ttu-id="dba9c-135">Completed</span><span class="sxs-lookup"><span data-stu-id="dba9c-135">Completed</span></span> 
- <span data-ttu-id="dba9c-136">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="dba9c-136">Failed</span></span> 
- <span data-ttu-id="dba9c-137">Очереди</span><span class="sxs-lookup"><span data-stu-id="dba9c-137">Queued</span></span> 
- <span data-ttu-id="dba9c-138">Начало</span><span class="sxs-lookup"><span data-stu-id="dba9c-138">Starting</span></span> 
- <span data-ttu-id="dba9c-139">Resuming</span><span class="sxs-lookup"><span data-stu-id="dba9c-139">Resuming</span></span> 
- <span data-ttu-id="dba9c-140">Использующ</span><span class="sxs-lookup"><span data-stu-id="dba9c-140">Running</span></span> 
- <span data-ttu-id="dba9c-141">Прекращена</span><span class="sxs-lookup"><span data-stu-id="dba9c-141">Stopped</span></span> 
- <span data-ttu-id="dba9c-142">Отключение</span><span class="sxs-lookup"><span data-stu-id="dba9c-142">Stopping</span></span> 
- <span data-ttu-id="dba9c-143">Остановить</span><span class="sxs-lookup"><span data-stu-id="dba9c-143">Suspended</span></span> 
- <span data-ttu-id="dba9c-144">Suspending</span><span class="sxs-lookup"><span data-stu-id="dba9c-144">Suspending</span></span> 
- <span data-ttu-id="dba9c-145">Сделать</span><span class="sxs-lookup"><span data-stu-id="dba9c-145">Activating</span></span>
- <span data-ttu-id="dba9c-146">Новые функции</span><span class="sxs-lookup"><span data-stu-id="dba9c-146">New</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases: 
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dba9c-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dba9c-147">-DefaultProfile</span></span>
<span data-ttu-id="dba9c-148">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dba9c-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dba9c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dba9c-149">CommonParameters</span></span>
<span data-ttu-id="dba9c-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dba9c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dba9c-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dba9c-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dba9c-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dba9c-152">INPUTS</span></span>

## <span data-ttu-id="dba9c-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dba9c-153">OUTPUTS</span></span>

### <span data-ttu-id="dba9c-154">Microsoft. Azure. Commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="dba9c-154">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="dba9c-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="dba9c-155">NOTES</span></span>

## <span data-ttu-id="dba9c-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dba9c-156">RELATED LINKS</span></span>

[<span data-ttu-id="dba9c-157">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="dba9c-157">Get-AzureRmAutomationDscCompilationJobOutput</span></span>](./Get-AzureRmAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="dba9c-158">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="dba9c-158">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)


