---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
ms.openlocfilehash: dd80c745c99c98d6ea5b551ab454661d4370cebd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735069"
---
# <span data-ttu-id="ada79-101">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="ada79-101">Get-AzureRmAutomationJobOutput</span></span>

## <span data-ttu-id="ada79-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ada79-102">SYNOPSIS</span></span>
<span data-ttu-id="ada79-103">Получает выходные данные задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="ada79-103">Gets the output of an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ada79-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ada79-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ada79-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ada79-105">DESCRIPTION</span></span>
<span data-ttu-id="ada79-106">Командлет **Get-AzureRmAutomationJobOutput** получает выходные данные задания службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="ada79-106">The **Get-AzureRmAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="ada79-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ada79-107">EXAMPLES</span></span>

### <span data-ttu-id="ada79-108">Пример 1: получение выходных данных задания автоматизации</span><span class="sxs-lookup"><span data-stu-id="ada79-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="ada79-109">Эта команда получает все выходные данные задания с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="ada79-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="ada79-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ada79-110">PARAMETERS</span></span>

### <span data-ttu-id="ada79-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ada79-111">-AutomationAccountName</span></span>
<span data-ttu-id="ada79-112">Указывает имя учетной записи автоматизации, для которой этот командлет получает выходные данные задания.</span><span class="sxs-lookup"><span data-stu-id="ada79-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="ada79-113">-ID</span><span class="sxs-lookup"><span data-stu-id="ada79-113">-Id</span></span>
<span data-ttu-id="ada79-114">Указывает идентификатор задания, для которого этот командлет получает вывод.</span><span class="sxs-lookup"><span data-stu-id="ada79-114">Specifies the ID of a job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="ada79-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ada79-115">-ResourceGroupName</span></span>
<span data-ttu-id="ada79-116">Указывает имя группы ресурсов, для которой этот командлет получает выходные данные задания.</span><span class="sxs-lookup"><span data-stu-id="ada79-116">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="ada79-117">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ada79-117">-StartTime</span></span>
<span data-ttu-id="ada79-118">Задает время начала как объект **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="ada79-118">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="ada79-119">Вы можете указать строку, которую можно преобразовать в допустимый тип **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="ada79-119">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="ada79-120">Командлет извлекает выходные данные, созданные после этого времени.</span><span class="sxs-lookup"><span data-stu-id="ada79-120">The cmdlet retrieves output created after this time.</span></span>

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

### <span data-ttu-id="ada79-121">-Stream</span><span class="sxs-lookup"><span data-stu-id="ada79-121">-Stream</span></span>
<span data-ttu-id="ada79-122">Указывает тип выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ada79-122">Specifies the type of output.</span></span>
<span data-ttu-id="ada79-123">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="ada79-123">Valid values are:</span></span> 

- <span data-ttu-id="ada79-124">Необходимые</span><span class="sxs-lookup"><span data-stu-id="ada79-124">Any</span></span>
- <span data-ttu-id="ada79-125">Приглашен</span><span class="sxs-lookup"><span data-stu-id="ada79-125">Debug</span></span>
- <span data-ttu-id="ada79-126">Ошибки</span><span class="sxs-lookup"><span data-stu-id="ada79-126">Error</span></span>
- <span data-ttu-id="ada79-127">Результата</span><span class="sxs-lookup"><span data-stu-id="ada79-127">Output</span></span>
- <span data-ttu-id="ada79-128">Последовательно</span><span class="sxs-lookup"><span data-stu-id="ada79-128">Progress</span></span>
- <span data-ttu-id="ada79-129">Подробный</span><span class="sxs-lookup"><span data-stu-id="ada79-129">Verbose</span></span>
- <span data-ttu-id="ada79-130">Об</span><span class="sxs-lookup"><span data-stu-id="ada79-130">Warning</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.StreamType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, Progress, Output, Warning, Error, Debug, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ada79-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ada79-131">-DefaultProfile</span></span>
<span data-ttu-id="ada79-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ada79-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ada79-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ada79-133">CommonParameters</span></span>
<span data-ttu-id="ada79-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ada79-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ada79-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ada79-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ada79-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ada79-136">INPUTS</span></span>

## <span data-ttu-id="ada79-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ada79-137">OUTPUTS</span></span>

### <span data-ttu-id="ada79-138">Microsoft. Azure. Commands. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="ada79-138">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="ada79-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="ada79-139">NOTES</span></span>

## <span data-ttu-id="ada79-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ada79-140">RELATED LINKS</span></span>

[<span data-ttu-id="ada79-141">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ada79-141">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="ada79-142">Возобновить — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ada79-142">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="ada79-143">Остановить-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ada79-143">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="ada79-144">Приостановить — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ada79-144">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


