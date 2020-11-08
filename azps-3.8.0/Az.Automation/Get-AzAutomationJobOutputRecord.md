---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: e43cb76db410752aef0a0cffc72d3d5bb6f8e28f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072675"
---
# <span data-ttu-id="d2dcc-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="d2dcc-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="d2dcc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2dcc-102">SYNOPSIS</span></span>
<span data-ttu-id="d2dcc-103">Получает полный вывод записи выходных данных задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="d2dcc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2dcc-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2dcc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2dcc-105">DESCRIPTION</span></span>
<span data-ttu-id="d2dcc-106">Командлет **Get-AzAutomationJobOutputRecord** получает полный вывод записи выходных данных задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="d2dcc-107">Несмотря на то, что командлет **Get-AzAutomationJobOutput** содержит одну или несколько выходных записей задания, она возвращает только сводку из строки значения любой выходной записи.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="d2dcc-108">Оно не возвращает полную величину введенного значения из выходной записи в исходном типе.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="d2dcc-109">Кроме того, сводка имеет максимальную длину, которая может превысить полное значение, которое выводит этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>
<span data-ttu-id="d2dcc-110">В отличие от **Get-AzAutomationJobOutput** , этот командлет возвращает полное значение из первоначально выданного типа для значения, выводимого из записи.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-110">Unlike **Get-AzAutomationJobOutput** , this cmdlet returns the full value in its originally outputted type, for any output record's outputted value.</span></span>

## <span data-ttu-id="d2dcc-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2dcc-111">EXAMPLES</span></span>

### <span data-ttu-id="d2dcc-112">Пример 1: получение полного результата задания автоматизации</span><span class="sxs-lookup"><span data-stu-id="d2dcc-112">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="d2dcc-113">Эта команда получает полный вывод задания с указанным ИДЕНТИФИКАТОРом задания.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-113">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="d2dcc-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2dcc-114">PARAMETERS</span></span>

### <span data-ttu-id="d2dcc-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d2dcc-115">-AutomationAccountName</span></span>
<span data-ttu-id="d2dcc-116">Указывает имя учетной записи автоматизации, для которой этот командлет получает выходную запись о задании.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-116">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="d2dcc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2dcc-117">-DefaultProfile</span></span>
<span data-ttu-id="d2dcc-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d2dcc-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2dcc-119">-ID</span><span class="sxs-lookup"><span data-stu-id="d2dcc-119">-Id</span></span>
<span data-ttu-id="d2dcc-120">Указывает идентификатор записи выходных данных задания для этого командлета, который требуется извлечь.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-120">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

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

### <span data-ttu-id="d2dcc-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="d2dcc-121">-JobId</span></span>
<span data-ttu-id="d2dcc-122">Указывает идентификатор задания, для которого этот командлет получает выходную запись.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-122">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

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

### <span data-ttu-id="d2dcc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2dcc-123">-ResourceGroupName</span></span>
<span data-ttu-id="d2dcc-124">Указывает имя группы ресурсов, для которой этот командлет получает выходную запись задания.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-124">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="d2dcc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2dcc-125">CommonParameters</span></span>
<span data-ttu-id="d2dcc-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2dcc-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2dcc-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2dcc-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2dcc-128">INPUTS</span></span>

### <span data-ttu-id="d2dcc-129">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d2dcc-129">System.Guid</span></span>

### <span data-ttu-id="d2dcc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d2dcc-130">System.String</span></span>

## <span data-ttu-id="d2dcc-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2dcc-131">OUTPUTS</span></span>

### <span data-ttu-id="d2dcc-132">Microsoft. Azure. Commands. Automation. Model. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="d2dcc-132">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="d2dcc-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2dcc-133">NOTES</span></span>

## <span data-ttu-id="d2dcc-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2dcc-134">RELATED LINKS</span></span>

[<span data-ttu-id="d2dcc-135">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="d2dcc-135">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)


