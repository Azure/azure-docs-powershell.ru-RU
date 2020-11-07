---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: f5c6976ca1fa398c38f642cef757f0e7956f40c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727843"
---
# <span data-ttu-id="9b493-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="9b493-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="9b493-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b493-102">SYNOPSIS</span></span>
<span data-ttu-id="9b493-103">Получает полный вывод записи выходных данных задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="9b493-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="9b493-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b493-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b493-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b493-105">DESCRIPTION</span></span>
<span data-ttu-id="9b493-106">Командлет **Get-AzAutomationJobOutputRecord** получает полный вывод записи выходных данных задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="9b493-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="9b493-107">Несмотря на то, что командлет **Get-AzAutomationJobOutput** содержит одну или несколько выходных записей задания, она возвращает только сводку из строки значения любой выходной записи.</span><span class="sxs-lookup"><span data-stu-id="9b493-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="9b493-108">Оно не возвращает полную величину введенного значения из выходной записи в исходном типе.</span><span class="sxs-lookup"><span data-stu-id="9b493-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="9b493-109">Кроме того, сводка имеет максимальную длину, которая может превысить полное значение, которое выводит этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9b493-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>
<span data-ttu-id="9b493-110">В отличие от **Get-AzAutomationJobOutput** , этот командлет возвращает полное значение из первоначально выданного типа для значения, выводимого из записи.</span><span class="sxs-lookup"><span data-stu-id="9b493-110">Unlike **Get-AzAutomationJobOutput** , this cmdlet returns the full value in its originally outputted type, for any output record's outputted value.</span></span>

## <span data-ttu-id="9b493-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b493-111">EXAMPLES</span></span>

### <span data-ttu-id="9b493-112">Пример 1: получение полного результата задания автоматизации</span><span class="sxs-lookup"><span data-stu-id="9b493-112">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="9b493-113">Эта команда получает полный вывод задания с указанным ИДЕНТИФИКАТОРом задания.</span><span class="sxs-lookup"><span data-stu-id="9b493-113">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="9b493-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b493-114">PARAMETERS</span></span>

### <span data-ttu-id="9b493-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9b493-115">-AutomationAccountName</span></span>
<span data-ttu-id="9b493-116">Указывает имя учетной записи автоматизации, для которой этот командлет получает выходную запись о задании.</span><span class="sxs-lookup"><span data-stu-id="9b493-116">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="9b493-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b493-117">-DefaultProfile</span></span>
<span data-ttu-id="9b493-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9b493-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b493-119">-ID</span><span class="sxs-lookup"><span data-stu-id="9b493-119">-Id</span></span>
<span data-ttu-id="9b493-120">Указывает идентификатор записи выходных данных задания для этого командлета, который требуется извлечь.</span><span class="sxs-lookup"><span data-stu-id="9b493-120">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

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

### <span data-ttu-id="9b493-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="9b493-121">-JobId</span></span>
<span data-ttu-id="9b493-122">Указывает идентификатор задания, для которого этот командлет получает выходную запись.</span><span class="sxs-lookup"><span data-stu-id="9b493-122">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

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

### <span data-ttu-id="9b493-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b493-123">-ResourceGroupName</span></span>
<span data-ttu-id="9b493-124">Указывает имя группы ресурсов, для которой этот командлет получает выходную запись задания.</span><span class="sxs-lookup"><span data-stu-id="9b493-124">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="9b493-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b493-125">CommonParameters</span></span>
<span data-ttu-id="9b493-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b493-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b493-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b493-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b493-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b493-128">INPUTS</span></span>

### <span data-ttu-id="9b493-129">System. GUID</span><span class="sxs-lookup"><span data-stu-id="9b493-129">System.Guid</span></span>

### <span data-ttu-id="9b493-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9b493-130">System.String</span></span>

## <span data-ttu-id="9b493-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b493-131">OUTPUTS</span></span>

### <span data-ttu-id="9b493-132">Microsoft. Azure. Commands. Automation. Model. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="9b493-132">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="9b493-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b493-133">NOTES</span></span>

## <span data-ttu-id="9b493-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b493-134">RELATED LINKS</span></span>

[<span data-ttu-id="9b493-135">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="9b493-135">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)


