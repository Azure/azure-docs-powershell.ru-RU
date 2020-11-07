---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
ms.openlocfilehash: d46dd2e314aa8064b305adb0501ae20480a34418
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732177"
---
# <span data-ttu-id="e1d2e-101">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="e1d2e-101">Get-AzureRmAutomationJobOutput</span></span>

## <span data-ttu-id="e1d2e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e1d2e-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d2e-103">Получает выходные данные задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="e1d2e-103">Gets the output of an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1d2e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e1d2e-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1d2e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1d2e-105">DESCRIPTION</span></span>
<span data-ttu-id="e1d2e-106">Командлет **Get-AzureRmAutomationJobOutput** получает выходные данные задания службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="e1d2e-106">The **Get-AzureRmAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="e1d2e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e1d2e-107">EXAMPLES</span></span>

### <span data-ttu-id="e1d2e-108">Пример 1: получение выходных данных задания автоматизации</span><span class="sxs-lookup"><span data-stu-id="e1d2e-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="e1d2e-109">Эта команда получает все выходные данные задания с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="e1d2e-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="e1d2e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e1d2e-110">PARAMETERS</span></span>

### <span data-ttu-id="e1d2e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e1d2e-111">-AutomationAccountName</span></span>
<span data-ttu-id="e1d2e-112">Указывает имя учетной записи автоматизации, для которой этот командлет получает выходные данные задания.</span><span class="sxs-lookup"><span data-stu-id="e1d2e-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="e1d2e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d2e-113">-DefaultProfile</span></span>
<span data-ttu-id="e1d2e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e1d2e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1d2e-115">-ID</span><span class="sxs-lookup"><span data-stu-id="e1d2e-115">-Id</span></span>
<span data-ttu-id="e1d2e-116">Указывает идентификатор задания, для которого этот командлет получает вывод.</span><span class="sxs-lookup"><span data-stu-id="e1d2e-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d2e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1d2e-117">-ResourceGroupName</span></span>
<span data-ttu-id="e1d2e-118">Указывает имя группы ресурсов, для которой этот командлет получает выходные данные задания.</span><span class="sxs-lookup"><span data-stu-id="e1d2e-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="e1d2e-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e1d2e-119">-StartTime</span></span>
<span data-ttu-id="e1d2e-120">Задает время начала как объект **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="e1d2e-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="e1d2e-121">Вы можете указать строку, которую можно преобразовать в допустимый тип **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="e1d2e-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="e1d2e-122">Командлет извлекает выходные данные, созданные после этого времени.</span><span class="sxs-lookup"><span data-stu-id="e1d2e-122">The cmdlet retrieves output created after this time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d2e-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="e1d2e-123">-Stream</span></span>
<span data-ttu-id="e1d2e-124">Указывает тип выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e1d2e-124">Specifies the type of output.</span></span>
<span data-ttu-id="e1d2e-125">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="e1d2e-125">Valid values are:</span></span> 

- <span data-ttu-id="e1d2e-126">Необходимые</span><span class="sxs-lookup"><span data-stu-id="e1d2e-126">Any</span></span>
- <span data-ttu-id="e1d2e-127">Приглашен</span><span class="sxs-lookup"><span data-stu-id="e1d2e-127">Debug</span></span>
- <span data-ttu-id="e1d2e-128">Ошибки</span><span class="sxs-lookup"><span data-stu-id="e1d2e-128">Error</span></span>
- <span data-ttu-id="e1d2e-129">Результата</span><span class="sxs-lookup"><span data-stu-id="e1d2e-129">Output</span></span>
- <span data-ttu-id="e1d2e-130">Последовательно</span><span class="sxs-lookup"><span data-stu-id="e1d2e-130">Progress</span></span>
- <span data-ttu-id="e1d2e-131">Подробный</span><span class="sxs-lookup"><span data-stu-id="e1d2e-131">Verbose</span></span>
- <span data-ttu-id="e1d2e-132">Об</span><span class="sxs-lookup"><span data-stu-id="e1d2e-132">Warning</span></span>

```yaml
Type: StreamType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, Progress, Output, Warning, Error, Debug, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d2e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d2e-133">CommonParameters</span></span>
<span data-ttu-id="e1d2e-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e1d2e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d2e-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1d2e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d2e-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e1d2e-136">INPUTS</span></span>

### <span data-ttu-id="e1d2e-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="e1d2e-137">None</span></span>
<span data-ttu-id="e1d2e-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="e1d2e-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e1d2e-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1d2e-139">OUTPUTS</span></span>

### <span data-ttu-id="e1d2e-140">Microsoft. Azure. Commands. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="e1d2e-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="e1d2e-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="e1d2e-141">NOTES</span></span>

## <span data-ttu-id="e1d2e-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1d2e-142">RELATED LINKS</span></span>

[<span data-ttu-id="e1d2e-143">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="e1d2e-143">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="e1d2e-144">Возобновить — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="e1d2e-144">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="e1d2e-145">Остановить-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="e1d2e-145">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="e1d2e-146">Приостановить — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="e1d2e-146">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


