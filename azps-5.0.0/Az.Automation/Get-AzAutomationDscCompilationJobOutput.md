---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
ms.openlocfilehash: 259f79e68b67726f78c96c46d62f8efbb2390d5a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246134"
---
# <span data-ttu-id="828b5-101">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="828b5-101">Get-AzAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="828b5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="828b5-102">SYNOPSIS</span></span>
<span data-ttu-id="828b5-103">Получает потоки ведения журнала для задания компиляции DSC Automation.</span><span class="sxs-lookup"><span data-stu-id="828b5-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

## <span data-ttu-id="828b5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="828b5-104">SYNTAX</span></span>

```
Get-AzAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="828b5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="828b5-105">DESCRIPTION</span></span>
<span data-ttu-id="828b5-106">Командлет **Get-AzAutomationDscCompilationJobOutput** получает записи потока для задания компиляции с требуемой конфигурацией AP (DSC) в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="828b5-106">The **Get-AzAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="828b5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="828b5-107">EXAMPLES</span></span>

### <span data-ttu-id="828b5-108">Пример 1: получение журналов для задания компиляции DSC</span><span class="sxs-lookup"><span data-stu-id="828b5-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="828b5-109">Первая команда получает задания компиляции в учетной записи автоматизации с именем Contoso17 с помощью командлета Get-AzAutomationDscCompilationJob.</span><span class="sxs-lookup"><span data-stu-id="828b5-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="828b5-110">Команда хранит эти объекты в переменной $Jobs.</span><span class="sxs-lookup"><span data-stu-id="828b5-110">The command stores those objects in the $Jobs variable.</span></span>
<span data-ttu-id="828b5-111">Вторая команда возвращает выходные данные задания компиляции для любого потока для первого элемента массива $Jobs.</span><span class="sxs-lookup"><span data-stu-id="828b5-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="828b5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="828b5-112">PARAMETERS</span></span>

### <span data-ttu-id="828b5-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="828b5-113">-AutomationAccountName</span></span>
<span data-ttu-id="828b5-114">Указывает имя учетной записи автоматизации, которая содержит задание компиляции DSC.</span><span class="sxs-lookup"><span data-stu-id="828b5-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="828b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="828b5-115">-DefaultProfile</span></span>
<span data-ttu-id="828b5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="828b5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="828b5-117">-ID</span><span class="sxs-lookup"><span data-stu-id="828b5-117">-Id</span></span>
<span data-ttu-id="828b5-118">Указывает уникальный идентификатор задания компиляции DSC, для которого этот командлет получает вывод.</span><span class="sxs-lookup"><span data-stu-id="828b5-118">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="828b5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="828b5-119">-ResourceGroupName</span></span>
<span data-ttu-id="828b5-120">Указывает имя группы ресурсов, которая содержит задание компиляции DSC, для которого этот командлет получает записи Streaming.</span><span class="sxs-lookup"><span data-stu-id="828b5-120">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="828b5-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="828b5-121">-StartTime</span></span>
<span data-ttu-id="828b5-122">Указывает время начала.</span><span class="sxs-lookup"><span data-stu-id="828b5-122">Specifies a start time.</span></span>
<span data-ttu-id="828b5-123">Этот командлет возвращает записи, выводимые заданием компиляции DSC после этого времени.</span><span class="sxs-lookup"><span data-stu-id="828b5-123">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

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

### <span data-ttu-id="828b5-124">-Stream</span><span class="sxs-lookup"><span data-stu-id="828b5-124">-Stream</span></span>
<span data-ttu-id="828b5-125">Указывает тип потока для вывода, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="828b5-125">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="828b5-126">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="828b5-126">Valid values are:</span></span> 
- <span data-ttu-id="828b5-127">Необходимые</span><span class="sxs-lookup"><span data-stu-id="828b5-127">Any</span></span> 
- <span data-ttu-id="828b5-128">Об</span><span class="sxs-lookup"><span data-stu-id="828b5-128">Warning</span></span> 
- <span data-ttu-id="828b5-129">Ошибки</span><span class="sxs-lookup"><span data-stu-id="828b5-129">Error</span></span> 
- <span data-ttu-id="828b5-130">Подробный</span><span class="sxs-lookup"><span data-stu-id="828b5-130">Verbose</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType
Parameter Sets: (All)
Aliases:
Accepted values: Warning, Error, Verbose, Any

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="828b5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="828b5-131">CommonParameters</span></span>
<span data-ttu-id="828b5-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="828b5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="828b5-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="828b5-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="828b5-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="828b5-134">INPUTS</span></span>

### <span data-ttu-id="828b5-135">System. GUID</span><span class="sxs-lookup"><span data-stu-id="828b5-135">System.Guid</span></span>

### <span data-ttu-id="828b5-136">Microsoft. Azure. Commands. Automation. Common. CompilationJobStreamType</span><span class="sxs-lookup"><span data-stu-id="828b5-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span></span>

### <span data-ttu-id="828b5-137">System. Nullable "1 [[System. DateTimeOffset, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="828b5-137">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="828b5-138">System. String</span><span class="sxs-lookup"><span data-stu-id="828b5-138">System.String</span></span>

## <span data-ttu-id="828b5-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="828b5-139">OUTPUTS</span></span>

### <span data-ttu-id="828b5-140">Microsoft. Azure. Commands. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="828b5-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="828b5-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="828b5-141">NOTES</span></span>

## <span data-ttu-id="828b5-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="828b5-142">RELATED LINKS</span></span>

[<span data-ttu-id="828b5-143">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="828b5-143">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="828b5-144">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="828b5-144">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


