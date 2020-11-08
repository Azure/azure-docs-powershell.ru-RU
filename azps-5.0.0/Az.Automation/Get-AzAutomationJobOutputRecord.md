---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: 7bece0fd2a9de822a5fa2a513fc06d4d20d96e4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249116"
---
# <span data-ttu-id="9f001-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="9f001-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="9f001-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f001-102">SYNOPSIS</span></span>
<span data-ttu-id="9f001-103">Получает полный вывод записи выходных данных задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="9f001-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="9f001-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f001-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f001-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f001-105">DESCRIPTION</span></span>
<span data-ttu-id="9f001-106">Командлет **Get-AzAutomationJobOutputRecord** получает полный вывод записи выходных данных задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="9f001-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="9f001-107">Несмотря на то, что командлет **Get-AzAutomationJobOutput** содержит одну или несколько выходных записей задания, она возвращает только сводку из строки значения любой выходной записи.</span><span class="sxs-lookup"><span data-stu-id="9f001-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="9f001-108">Оно не возвращает полную величину введенного значения из выходной записи в исходном типе.</span><span class="sxs-lookup"><span data-stu-id="9f001-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="9f001-109">Кроме того, сводка имеет максимальную длину, которая может превысить полное значение, которое выводит этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9f001-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>

## <span data-ttu-id="9f001-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f001-110">EXAMPLES</span></span>

### <span data-ttu-id="9f001-111">Пример 1: получение полного результата задания автоматизации</span><span class="sxs-lookup"><span data-stu-id="9f001-111">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="9f001-112">Эта команда получает полный вывод задания с указанным ИДЕНТИФИКАТОРом задания.</span><span class="sxs-lookup"><span data-stu-id="9f001-112">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="9f001-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f001-113">PARAMETERS</span></span>

### <span data-ttu-id="9f001-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9f001-114">-AutomationAccountName</span></span>
<span data-ttu-id="9f001-115">Указывает имя учетной записи автоматизации, для которой этот командлет получает выходную запись о задании.</span><span class="sxs-lookup"><span data-stu-id="9f001-115">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="9f001-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f001-116">-DefaultProfile</span></span>
<span data-ttu-id="9f001-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9f001-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f001-118">-ID</span><span class="sxs-lookup"><span data-stu-id="9f001-118">-Id</span></span>
<span data-ttu-id="9f001-119">Указывает идентификатор записи выходных данных задания для этого командлета, который требуется извлечь.</span><span class="sxs-lookup"><span data-stu-id="9f001-119">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

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

### <span data-ttu-id="9f001-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="9f001-120">-JobId</span></span>
<span data-ttu-id="9f001-121">Указывает идентификатор задания, для которого этот командлет получает выходную запись.</span><span class="sxs-lookup"><span data-stu-id="9f001-121">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

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

### <span data-ttu-id="9f001-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f001-122">-ResourceGroupName</span></span>
<span data-ttu-id="9f001-123">Указывает имя группы ресурсов, для которой этот командлет получает выходную запись задания.</span><span class="sxs-lookup"><span data-stu-id="9f001-123">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="9f001-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f001-124">CommonParameters</span></span>
<span data-ttu-id="9f001-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f001-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f001-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f001-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f001-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f001-127">INPUTS</span></span>

### <span data-ttu-id="9f001-128">System. GUID</span><span class="sxs-lookup"><span data-stu-id="9f001-128">System.Guid</span></span>

### <span data-ttu-id="9f001-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9f001-129">System.String</span></span>

## <span data-ttu-id="9f001-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f001-130">OUTPUTS</span></span>

### <span data-ttu-id="9f001-131">Microsoft. Azure. Commands. Automation. Model. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="9f001-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="9f001-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f001-132">NOTES</span></span>

## <span data-ttu-id="9f001-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f001-133">RELATED LINKS</span></span>

[<span data-ttu-id="9f001-134">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="9f001-134">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)


