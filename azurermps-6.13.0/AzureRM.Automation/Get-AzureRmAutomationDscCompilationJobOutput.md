---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
ms.openlocfilehash: a7ddc25fa7c6bc52acbe9369c569db060cf63a06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556887"
---
# <span data-ttu-id="1a32d-101">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="1a32d-101">Get-AzureRmAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="1a32d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1a32d-102">SYNOPSIS</span></span>
<span data-ttu-id="1a32d-103">Получает потоки ведения журнала для задания компиляции DSC Automation.</span><span class="sxs-lookup"><span data-stu-id="1a32d-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a32d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1a32d-104">SYNTAX</span></span>

```
Get-AzureRmAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a32d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a32d-105">DESCRIPTION</span></span>
<span data-ttu-id="1a32d-106">Командлет **Get-AzureRmAutomationDscCompilationJobOutput** получает записи потока для задания компиляции с требуемой конфигурацией AP (DSC) в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="1a32d-106">The **Get-AzureRmAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="1a32d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1a32d-107">EXAMPLES</span></span>

### <span data-ttu-id="1a32d-108">Пример 1: получение журналов для задания компиляции DSC</span><span class="sxs-lookup"><span data-stu-id="1a32d-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzureRmAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="1a32d-109">Первая команда получает задания компиляции в учетной записи автоматизации с именем Contoso17 с помощью командлета Get-AzureRmAutomationDscCompilationJob.</span><span class="sxs-lookup"><span data-stu-id="1a32d-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzureRmAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="1a32d-110">Команда хранит эти объекты в переменной $Jobs.</span><span class="sxs-lookup"><span data-stu-id="1a32d-110">The command stores those objects in the $Jobs variable.</span></span>
<span data-ttu-id="1a32d-111">Вторая команда возвращает выходные данные задания компиляции для любого потока для первого элемента массива $Jobs.</span><span class="sxs-lookup"><span data-stu-id="1a32d-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="1a32d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1a32d-112">PARAMETERS</span></span>

### <span data-ttu-id="1a32d-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1a32d-113">-AutomationAccountName</span></span>
<span data-ttu-id="1a32d-114">Указывает имя учетной записи автоматизации, которая содержит задание компиляции DSC.</span><span class="sxs-lookup"><span data-stu-id="1a32d-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="1a32d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a32d-115">-DefaultProfile</span></span>
<span data-ttu-id="1a32d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1a32d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a32d-117">-ID</span><span class="sxs-lookup"><span data-stu-id="1a32d-117">-Id</span></span>
<span data-ttu-id="1a32d-118">Указывает уникальный идентификатор задания компиляции DSC, для которого этот командлет получает вывод.</span><span class="sxs-lookup"><span data-stu-id="1a32d-118">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="1a32d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a32d-119">-ResourceGroupName</span></span>
<span data-ttu-id="1a32d-120">Указывает имя группы ресурсов, которая содержит задание компиляции DSC, для которого этот командлет получает записи Streaming.</span><span class="sxs-lookup"><span data-stu-id="1a32d-120">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="1a32d-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1a32d-121">-StartTime</span></span>
<span data-ttu-id="1a32d-122">Указывает время начала.</span><span class="sxs-lookup"><span data-stu-id="1a32d-122">Specifies a start time.</span></span>
<span data-ttu-id="1a32d-123">Этот командлет возвращает записи, выводимые заданием компиляции DSC после этого времени.</span><span class="sxs-lookup"><span data-stu-id="1a32d-123">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

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

### <span data-ttu-id="1a32d-124">-Stream</span><span class="sxs-lookup"><span data-stu-id="1a32d-124">-Stream</span></span>
<span data-ttu-id="1a32d-125">Указывает тип потока для вывода, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1a32d-125">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="1a32d-126">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="1a32d-126">Valid values are:</span></span> 
- <span data-ttu-id="1a32d-127">Необходимые</span><span class="sxs-lookup"><span data-stu-id="1a32d-127">Any</span></span> 
- <span data-ttu-id="1a32d-128">Об</span><span class="sxs-lookup"><span data-stu-id="1a32d-128">Warning</span></span> 
- <span data-ttu-id="1a32d-129">Ошибки</span><span class="sxs-lookup"><span data-stu-id="1a32d-129">Error</span></span> 
- <span data-ttu-id="1a32d-130">Подробный</span><span class="sxs-lookup"><span data-stu-id="1a32d-130">Verbose</span></span>

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

### <span data-ttu-id="1a32d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a32d-131">CommonParameters</span></span>
<span data-ttu-id="1a32d-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1a32d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a32d-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a32d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a32d-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1a32d-134">INPUTS</span></span>

### <span data-ttu-id="1a32d-135">System. GUID</span><span class="sxs-lookup"><span data-stu-id="1a32d-135">System.Guid</span></span>

### <span data-ttu-id="1a32d-136">Microsoft. Azure. Commands. Automation. Common. CompilationJobStreamType</span><span class="sxs-lookup"><span data-stu-id="1a32d-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span></span>

### <span data-ttu-id="1a32d-137">System. Nullable "1 [[System. DateTimeOffset, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="1a32d-137">System.Nullable\`1[[System.DateTimeOffset, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="1a32d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1a32d-138">System.String</span></span>

## <span data-ttu-id="1a32d-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a32d-139">OUTPUTS</span></span>

### <span data-ttu-id="1a32d-140">Microsoft. Azure. Commands. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="1a32d-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="1a32d-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="1a32d-141">NOTES</span></span>

## <span data-ttu-id="1a32d-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a32d-142">RELATED LINKS</span></span>

[<span data-ttu-id="1a32d-143">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="1a32d-143">Get-AzureRmAutomationDscCompilationJob</span></span>](./Get-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="1a32d-144">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="1a32d-144">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)


