---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
ms.openlocfilehash: 53ae09ba82de2a96bc9db17ad7ca538c48b23a47
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98510078"
---
# <span data-ttu-id="17605-101">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="17605-101">Get-AzAutomationJobOutput</span></span>

## <span data-ttu-id="17605-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17605-102">SYNOPSIS</span></span>
<span data-ttu-id="17605-103">Возвращает результат задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="17605-103">Gets the output of an Automation job.</span></span>

## <span data-ttu-id="17605-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="17605-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17605-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17605-105">DESCRIPTION</span></span>
<span data-ttu-id="17605-106">**Cmdlet Get-AzAutomationJobOutput** получает результат задания автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="17605-106">The **Get-AzAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="17605-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="17605-107">EXAMPLES</span></span>

### <span data-ttu-id="17605-108">Пример 1. Вывод задания автоматизации</span><span class="sxs-lookup"><span data-stu-id="17605-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="17605-109">Эта команда получает все выходные данные задания с указанным ИД.</span><span class="sxs-lookup"><span data-stu-id="17605-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="17605-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17605-110">PARAMETERS</span></span>

### <span data-ttu-id="17605-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="17605-111">-AutomationAccountName</span></span>
<span data-ttu-id="17605-112">Указывает имя учетной записи автоматизации, для которой этот cmdlet получает выходные данные задания.</span><span class="sxs-lookup"><span data-stu-id="17605-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="17605-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17605-113">-DefaultProfile</span></span>
<span data-ttu-id="17605-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="17605-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17605-115">-Id</span><span class="sxs-lookup"><span data-stu-id="17605-115">-Id</span></span>
<span data-ttu-id="17605-116">Определяет код задания, для которого этот cmdlet получает выходные данные.</span><span class="sxs-lookup"><span data-stu-id="17605-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="17605-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17605-117">-ResourceGroupName</span></span>
<span data-ttu-id="17605-118">Имя группы ресурсов, для которой этот cmdlet получает выходные данные задания.</span><span class="sxs-lookup"><span data-stu-id="17605-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="17605-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="17605-119">-StartTime</span></span>
<span data-ttu-id="17605-120">Время начала в качестве объекта **DateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="17605-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="17605-121">Вы можете указать строку, которую можно преобразовать в допустимый **набор DateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="17605-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="17605-122">С этого времени он извлекает выходные данные, созданные после этого.</span><span class="sxs-lookup"><span data-stu-id="17605-122">The cmdlet retrieves output created after this time.</span></span>

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

### <span data-ttu-id="17605-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="17605-123">-Stream</span></span>
<span data-ttu-id="17605-124">Определяет тип выходных данных.</span><span class="sxs-lookup"><span data-stu-id="17605-124">Specifies the type of output.</span></span>
<span data-ttu-id="17605-125">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="17605-125">Valid values are:</span></span> 
- <span data-ttu-id="17605-126">Любая</span><span class="sxs-lookup"><span data-stu-id="17605-126">Any</span></span>
- <span data-ttu-id="17605-127">Отлаг</span><span class="sxs-lookup"><span data-stu-id="17605-127">Debug</span></span>
- <span data-ttu-id="17605-128">Ошибка</span><span class="sxs-lookup"><span data-stu-id="17605-128">Error</span></span>
- <span data-ttu-id="17605-129">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="17605-129">Output</span></span>
- <span data-ttu-id="17605-130">Ход выполнения</span><span class="sxs-lookup"><span data-stu-id="17605-130">Progress</span></span>
- <span data-ttu-id="17605-131">Подробный</span><span class="sxs-lookup"><span data-stu-id="17605-131">Verbose</span></span>
- <span data-ttu-id="17605-132">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="17605-132">Warning</span></span>

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

### <span data-ttu-id="17605-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17605-133">CommonParameters</span></span>
<span data-ttu-id="17605-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17605-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17605-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17605-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17605-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17605-136">INPUTS</span></span>

### <span data-ttu-id="17605-137">System.Guid</span><span class="sxs-lookup"><span data-stu-id="17605-137">System.Guid</span></span>

### <span data-ttu-id="17605-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span><span class="sxs-lookup"><span data-stu-id="17605-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="17605-139">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="17605-139">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="17605-140">System.String</span><span class="sxs-lookup"><span data-stu-id="17605-140">System.String</span></span>

## <span data-ttu-id="17605-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="17605-141">OUTPUTS</span></span>

### <span data-ttu-id="17605-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span><span class="sxs-lookup"><span data-stu-id="17605-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="17605-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="17605-143">NOTES</span></span>

## <span data-ttu-id="17605-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17605-144">RELATED LINKS</span></span>

[<span data-ttu-id="17605-145">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="17605-145">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="17605-146">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="17605-146">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="17605-147">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="17605-147">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="17605-148">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="17605-148">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


