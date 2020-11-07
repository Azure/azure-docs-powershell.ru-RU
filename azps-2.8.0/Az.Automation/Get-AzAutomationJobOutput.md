---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
ms.openlocfilehash: 60de6b852d516cd4742ed253d149ea031449548b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727841"
---
# <span data-ttu-id="3a6e6-101">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="3a6e6-101">Get-AzAutomationJobOutput</span></span>

## <span data-ttu-id="3a6e6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3a6e6-102">SYNOPSIS</span></span>
<span data-ttu-id="3a6e6-103">Получает выходные данные задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="3a6e6-103">Gets the output of an Automation job.</span></span>

## <span data-ttu-id="3a6e6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3a6e6-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a6e6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a6e6-105">DESCRIPTION</span></span>
<span data-ttu-id="3a6e6-106">Командлет **Get-AzAutomationJobOutput** получает выходные данные задания службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="3a6e6-106">The **Get-AzAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="3a6e6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3a6e6-107">EXAMPLES</span></span>

### <span data-ttu-id="3a6e6-108">Пример 1: получение выходных данных задания автоматизации</span><span class="sxs-lookup"><span data-stu-id="3a6e6-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="3a6e6-109">Эта команда получает все выходные данные задания с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="3a6e6-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="3a6e6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3a6e6-110">PARAMETERS</span></span>

### <span data-ttu-id="3a6e6-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3a6e6-111">-AutomationAccountName</span></span>
<span data-ttu-id="3a6e6-112">Указывает имя учетной записи автоматизации, для которой этот командлет получает выходные данные задания.</span><span class="sxs-lookup"><span data-stu-id="3a6e6-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="3a6e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a6e6-113">-DefaultProfile</span></span>
<span data-ttu-id="3a6e6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3a6e6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a6e6-115">-ID</span><span class="sxs-lookup"><span data-stu-id="3a6e6-115">-Id</span></span>
<span data-ttu-id="3a6e6-116">Указывает идентификатор задания, для которого этот командлет получает вывод.</span><span class="sxs-lookup"><span data-stu-id="3a6e6-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a6e6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a6e6-117">-ResourceGroupName</span></span>
<span data-ttu-id="3a6e6-118">Указывает имя группы ресурсов, для которой этот командлет получает выходные данные задания.</span><span class="sxs-lookup"><span data-stu-id="3a6e6-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="3a6e6-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3a6e6-119">-StartTime</span></span>
<span data-ttu-id="3a6e6-120">Задает время начала как объект **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="3a6e6-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="3a6e6-121">Вы можете указать строку, которую можно преобразовать в допустимый тип **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="3a6e6-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="3a6e6-122">Командлет извлекает выходные данные, созданные после этого времени.</span><span class="sxs-lookup"><span data-stu-id="3a6e6-122">The cmdlet retrieves output created after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a6e6-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="3a6e6-123">-Stream</span></span>
<span data-ttu-id="3a6e6-124">Указывает тип выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3a6e6-124">Specifies the type of output.</span></span>
<span data-ttu-id="3a6e6-125">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="3a6e6-125">Valid values are:</span></span> 
- <span data-ttu-id="3a6e6-126">Необходимые</span><span class="sxs-lookup"><span data-stu-id="3a6e6-126">Any</span></span>
- <span data-ttu-id="3a6e6-127">Приглашен</span><span class="sxs-lookup"><span data-stu-id="3a6e6-127">Debug</span></span>
- <span data-ttu-id="3a6e6-128">Ошибки</span><span class="sxs-lookup"><span data-stu-id="3a6e6-128">Error</span></span>
- <span data-ttu-id="3a6e6-129">Результата</span><span class="sxs-lookup"><span data-stu-id="3a6e6-129">Output</span></span>
- <span data-ttu-id="3a6e6-130">Последовательно</span><span class="sxs-lookup"><span data-stu-id="3a6e6-130">Progress</span></span>
- <span data-ttu-id="3a6e6-131">Подробный</span><span class="sxs-lookup"><span data-stu-id="3a6e6-131">Verbose</span></span>
- <span data-ttu-id="3a6e6-132">Об</span><span class="sxs-lookup"><span data-stu-id="3a6e6-132">Warning</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.StreamType
Parameter Sets: (All)
Aliases:
Accepted values: Any, Progress, Output, Warning, Error, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a6e6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a6e6-133">CommonParameters</span></span>
<span data-ttu-id="3a6e6-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3a6e6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a6e6-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a6e6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a6e6-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3a6e6-136">INPUTS</span></span>

### <span data-ttu-id="3a6e6-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="3a6e6-137">System.Guid</span></span>

### <span data-ttu-id="3a6e6-138">Microsoft. Azure. Commands. Automation. Common. StreamType</span><span class="sxs-lookup"><span data-stu-id="3a6e6-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="3a6e6-139">System. Nullable "1 [[System. DateTimeOffset, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3a6e6-139">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3a6e6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3a6e6-140">System.String</span></span>

## <span data-ttu-id="3a6e6-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a6e6-141">OUTPUTS</span></span>

### <span data-ttu-id="3a6e6-142">Microsoft. Azure. Commands. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="3a6e6-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="3a6e6-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="3a6e6-143">NOTES</span></span>

## <span data-ttu-id="3a6e6-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a6e6-144">RELATED LINKS</span></span>

[<span data-ttu-id="3a6e6-145">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3a6e6-145">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="3a6e6-146">Возобновить — AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3a6e6-146">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="3a6e6-147">Остановить-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3a6e6-147">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="3a6e6-148">Приостановить — AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3a6e6-148">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


