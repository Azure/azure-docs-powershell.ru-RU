---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
ms.openlocfilehash: 1da8d90ca336d2886f7633e646583bc61529fcee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993009"
---
# <span data-ttu-id="d64ff-101">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="d64ff-101">Get-AzAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="d64ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d64ff-102">SYNOPSIS</span></span>
<span data-ttu-id="d64ff-103">Возвращает потоки ведения журнала в задание компиляции DSC автоматизации.</span><span class="sxs-lookup"><span data-stu-id="d64ff-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

## <span data-ttu-id="d64ff-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d64ff-104">SYNTAX</span></span>

```
Get-AzAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d64ff-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d64ff-105">DESCRIPTION</span></span>
<span data-ttu-id="d64ff-106">**Cmdlet Get-AzAutomationDscCompilationJobOutput** возвращает записи потока задания компиляции APS в автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="d64ff-106">The **Get-AzAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="d64ff-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d64ff-107">EXAMPLES</span></span>

### <span data-ttu-id="d64ff-108">Пример 1. Просмотр журналов для задания компиляции DSC</span><span class="sxs-lookup"><span data-stu-id="d64ff-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="d64ff-109">Первая команда получает задания компиляции в учетной записи автоматизации Contoso17 с помощью Get-AzAutomationDscCompilationJob командлета.</span><span class="sxs-lookup"><span data-stu-id="d64ff-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="d64ff-110">Команда сохраняет эти объекты в переменной $Jobs.</span><span class="sxs-lookup"><span data-stu-id="d64ff-110">The command stores those objects in the $Jobs variable.</span></span>
<span data-ttu-id="d64ff-111">Вторая команда получает результаты задания компиляции для любого потока для первого $Jobs массива.</span><span class="sxs-lookup"><span data-stu-id="d64ff-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="d64ff-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d64ff-112">PARAMETERS</span></span>

### <span data-ttu-id="d64ff-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d64ff-113">-AutomationAccountName</span></span>
<span data-ttu-id="d64ff-114">Указывает имя учетной записи автоматизации, которая содержит задание компиляции DSC.</span><span class="sxs-lookup"><span data-stu-id="d64ff-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="d64ff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d64ff-115">-DefaultProfile</span></span>
<span data-ttu-id="d64ff-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d64ff-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d64ff-117">-Id</span><span class="sxs-lookup"><span data-stu-id="d64ff-117">-Id</span></span>
<span data-ttu-id="d64ff-118">Указывает уникальный код задания компиляции DSC, для которого этот cmdlet получает выходные данные.</span><span class="sxs-lookup"><span data-stu-id="d64ff-118">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="d64ff-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d64ff-119">-ResourceGroupName</span></span>
<span data-ttu-id="d64ff-120">Указывает имя группы ресурсов, которая содержит задание компиляции DSC, для которого этот cmdlet получает записи потоков.</span><span class="sxs-lookup"><span data-stu-id="d64ff-120">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="d64ff-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d64ff-121">-StartTime</span></span>
<span data-ttu-id="d64ff-122">Время начала.</span><span class="sxs-lookup"><span data-stu-id="d64ff-122">Specifies a start time.</span></span>
<span data-ttu-id="d64ff-123">Этот cmdlet получает потоковую запись, которую после этого времени выдвоает задание компиляции DSC.</span><span class="sxs-lookup"><span data-stu-id="d64ff-123">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

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

### <span data-ttu-id="d64ff-124">-Stream</span><span class="sxs-lookup"><span data-stu-id="d64ff-124">-Stream</span></span>
<span data-ttu-id="d64ff-125">Определяет тип потока для выходных данных, которые получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d64ff-125">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="d64ff-126">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="d64ff-126">Valid values are:</span></span> 
- <span data-ttu-id="d64ff-127">Любая</span><span class="sxs-lookup"><span data-stu-id="d64ff-127">Any</span></span> 
- <span data-ttu-id="d64ff-128">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="d64ff-128">Warning</span></span> 
- <span data-ttu-id="d64ff-129">Ошибка</span><span class="sxs-lookup"><span data-stu-id="d64ff-129">Error</span></span> 
- <span data-ttu-id="d64ff-130">Подробный</span><span class="sxs-lookup"><span data-stu-id="d64ff-130">Verbose</span></span>

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

### <span data-ttu-id="d64ff-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d64ff-131">CommonParameters</span></span>
<span data-ttu-id="d64ff-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d64ff-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d64ff-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d64ff-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d64ff-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d64ff-134">INPUTS</span></span>

### <span data-ttu-id="d64ff-135">System.Guid</span><span class="sxs-lookup"><span data-stu-id="d64ff-135">System.Guid</span></span>

### <span data-ttu-id="d64ff-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span><span class="sxs-lookup"><span data-stu-id="d64ff-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span></span>

### <span data-ttu-id="d64ff-137">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d64ff-137">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d64ff-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d64ff-138">System.String</span></span>

## <span data-ttu-id="d64ff-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d64ff-139">OUTPUTS</span></span>

### <span data-ttu-id="d64ff-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span><span class="sxs-lookup"><span data-stu-id="d64ff-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="d64ff-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d64ff-141">NOTES</span></span>

## <span data-ttu-id="d64ff-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d64ff-142">RELATED LINKS</span></span>

[<span data-ttu-id="d64ff-143">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="d64ff-143">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="d64ff-144">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="d64ff-144">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


