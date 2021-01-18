---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: 7bece0fd2a9de822a5fa2a513fc06d4d20d96e4c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98510074"
---
# <span data-ttu-id="186d9-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="186d9-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="186d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="186d9-102">SYNOPSIS</span></span>
<span data-ttu-id="186d9-103">Возвращает полный результат записи выходных данных задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="186d9-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="186d9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="186d9-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="186d9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="186d9-105">DESCRIPTION</span></span>
<span data-ttu-id="186d9-106">Для получения полного результата записи выходных данных задания автоматизации возвращается все выходные данные для **get-AzAutomationJobOutputRecord.**</span><span class="sxs-lookup"><span data-stu-id="186d9-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="186d9-107">Хотя  с его учетом можно получить одну или несколько записей выходных данных задания, он возвращает только суммарную (строку) значение любой выходной записи.</span><span class="sxs-lookup"><span data-stu-id="186d9-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="186d9-108">Она не возвращает полное значение выводного значения записи исходного типа.</span><span class="sxs-lookup"><span data-stu-id="186d9-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="186d9-109">Кроме того, максимальная длина сводки может быть превышена при полном значении, выведемом этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="186d9-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>

## <span data-ttu-id="186d9-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="186d9-110">EXAMPLES</span></span>

### <span data-ttu-id="186d9-111">Пример 1. Полный выход задания автоматизации</span><span class="sxs-lookup"><span data-stu-id="186d9-111">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="186d9-112">Эта команда возвращает полный результат задания с указанным ид.</span><span class="sxs-lookup"><span data-stu-id="186d9-112">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="186d9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="186d9-113">PARAMETERS</span></span>

### <span data-ttu-id="186d9-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="186d9-114">-AutomationAccountName</span></span>
<span data-ttu-id="186d9-115">Указывает имя учетной записи автоматизации, для которой этот cmdlet получает запись вывода задания.</span><span class="sxs-lookup"><span data-stu-id="186d9-115">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="186d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="186d9-116">-DefaultProfile</span></span>
<span data-ttu-id="186d9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="186d9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="186d9-118">-Id</span><span class="sxs-lookup"><span data-stu-id="186d9-118">-Id</span></span>
<span data-ttu-id="186d9-119">Определяет код записи выходных данных задания для извлечения этим cmdletом.</span><span class="sxs-lookup"><span data-stu-id="186d9-119">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StreamRecordId

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="186d9-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="186d9-120">-JobId</span></span>
<span data-ttu-id="186d9-121">Определяет код задания, для которого этот cmdlet получает выходную запись.</span><span class="sxs-lookup"><span data-stu-id="186d9-121">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="186d9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="186d9-122">-ResourceGroupName</span></span>
<span data-ttu-id="186d9-123">Имя группы ресурсов, для которой этот cmdlet получает запись вывода задания.</span><span class="sxs-lookup"><span data-stu-id="186d9-123">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="186d9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="186d9-124">CommonParameters</span></span>
<span data-ttu-id="186d9-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="186d9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="186d9-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="186d9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="186d9-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="186d9-127">INPUTS</span></span>

### <span data-ttu-id="186d9-128">System.Guid</span><span class="sxs-lookup"><span data-stu-id="186d9-128">System.Guid</span></span>

### <span data-ttu-id="186d9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="186d9-129">System.String</span></span>

## <span data-ttu-id="186d9-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="186d9-130">OUTPUTS</span></span>

### <span data-ttu-id="186d9-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="186d9-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="186d9-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="186d9-132">NOTES</span></span>

## <span data-ttu-id="186d9-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="186d9-133">RELATED LINKS</span></span>

[<span data-ttu-id="186d9-134">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="186d9-134">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)


