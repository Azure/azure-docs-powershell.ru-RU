---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationRunbook.md
ms.openlocfilehash: 15bd20e609c331c45a8b876f795869ded47ee056
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074975"
---
# <span data-ttu-id="9cf58-101">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9cf58-101">Import-AzAutomationRunbook</span></span>

## <span data-ttu-id="9cf58-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9cf58-102">SYNOPSIS</span></span>
<span data-ttu-id="9cf58-103">Импортирует Runbook автоматизации.</span><span class="sxs-lookup"><span data-stu-id="9cf58-103">Imports an Automation runbook.</span></span>

## <span data-ttu-id="9cf58-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9cf58-104">SYNTAX</span></span>

```
Import-AzAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cf58-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cf58-105">DESCRIPTION</span></span>
<span data-ttu-id="9cf58-106">Командлет **Import-AzAutomationRunbook** импортирует Runbook службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="9cf58-106">The **Import-AzAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="9cf58-107">Укажите путь к файлу сценария wps_2 (PS1), который нужно импортировать для wps_2 и wps_2 runbooks для рабочих процессов, (graphrunbook) для графических модулей runbooks или (файл. корректировки) для модулей Runbook 2.</span><span class="sxs-lookup"><span data-stu-id="9cf58-107">Specify the path to a wps_2 script (.ps1) file to import for wps_2 and wps_2 Workflow runbooks, (.graphrunbook) file for graphical runbooks, or (.py) file for python 2 runbooks.</span></span> <span data-ttu-id="9cf58-108">Для wps_2 Runbook рабочего процесса этот сценарий должен содержать одно определение рабочего процесса wps_2, которое соответствует имени файла.</span><span class="sxs-lookup"><span data-stu-id="9cf58-108">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="9cf58-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9cf58-109">EXAMPLES</span></span>

### <span data-ttu-id="9cf58-110">Пример 1: импорт модуля Runbook из файла</span><span class="sxs-lookup"><span data-stu-id="9cf58-110">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="9cf58-111">Первая команда присваивает переменной $Tags две пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="9cf58-111">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="9cf58-112">Вторая команда импортирует графический модуль Runbook, именуемый GraphicalRunbook06, в учетную запись автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="9cf58-112">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="9cf58-113">Команда также назначает теги, хранящиеся в $Tags.</span><span class="sxs-lookup"><span data-stu-id="9cf58-113">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="9cf58-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9cf58-114">PARAMETERS</span></span>

### <span data-ttu-id="9cf58-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9cf58-115">-AutomationAccountName</span></span>
<span data-ttu-id="9cf58-116">Указывает имя учетной записи автоматизации, на которую командлет импортирует Runbook.</span><span class="sxs-lookup"><span data-stu-id="9cf58-116">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="9cf58-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cf58-117">-DefaultProfile</span></span>
<span data-ttu-id="9cf58-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9cf58-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9cf58-119">-Описание</span><span class="sxs-lookup"><span data-stu-id="9cf58-119">-Description</span></span>
<span data-ttu-id="9cf58-120">Задает описание для импортированного Runbook.</span><span class="sxs-lookup"><span data-stu-id="9cf58-120">Specifies a description for the imported runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf58-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9cf58-121">-Force</span></span>
<span data-ttu-id="9cf58-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="9cf58-122">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf58-123">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="9cf58-123">-LogProgress</span></span>
<span data-ttu-id="9cf58-124">Указывает, будет ли Runbook регистрировать данные о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="9cf58-124">Specifies whether the runbook logs progress information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf58-125">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="9cf58-125">-LogVerbose</span></span>
<span data-ttu-id="9cf58-126">Указывает, записывает ли Runbook подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="9cf58-126">Specifies whether the runbook logs detailed information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf58-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9cf58-127">-Name</span></span>
<span data-ttu-id="9cf58-128">Указывает имя Runbook, который импортирует этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9cf58-128">Specifies the name of the runbook that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf58-129">-Path</span><span class="sxs-lookup"><span data-stu-id="9cf58-129">-Path</span></span>
<span data-ttu-id="9cf58-130">Задает путь к файлу PS1 или graphrunbook, который импортирует этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9cf58-130">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourcePath

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf58-131">-Опубликовано</span><span class="sxs-lookup"><span data-stu-id="9cf58-131">-Published</span></span>
<span data-ttu-id="9cf58-132">Указывает на то, что этот командлет публикует Runbook, который он импортирует.</span><span class="sxs-lookup"><span data-stu-id="9cf58-132">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf58-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cf58-133">-ResourceGroupName</span></span>
<span data-ttu-id="9cf58-134">Указывает имя группы ресурсов, для которой этот командлет импортирует Runbook.</span><span class="sxs-lookup"><span data-stu-id="9cf58-134">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="9cf58-135">-Теги</span><span class="sxs-lookup"><span data-stu-id="9cf58-135">-Tags</span></span>
<span data-ttu-id="9cf58-136">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="9cf58-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9cf58-137">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="9cf58-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf58-138">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="9cf58-138">-Type</span></span>
<span data-ttu-id="9cf58-139">Указывает тип Runbook, создаваемый этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="9cf58-139">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="9cf58-140">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="9cf58-140">Valid values are:</span></span>
- <span data-ttu-id="9cf58-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="9cf58-141">PowerShell</span></span>
- <span data-ttu-id="9cf58-142">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="9cf58-142">GraphicalPowerShell</span></span>
- <span data-ttu-id="9cf58-143">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="9cf58-143">PowerShellWorkflow</span></span>
- <span data-ttu-id="9cf58-144">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="9cf58-144">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="9cf58-145">Виде</span><span class="sxs-lookup"><span data-stu-id="9cf58-145">Graph</span></span>
- <span data-ttu-id="9cf58-146">Python2 значение графика устарело.</span><span class="sxs-lookup"><span data-stu-id="9cf58-146">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="9cf58-147">Это эквивалентно GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="9cf58-147">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph, Python2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf58-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9cf58-148">-Confirm</span></span>
<span data-ttu-id="9cf58-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9cf58-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf58-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cf58-150">-WhatIf</span></span>
<span data-ttu-id="9cf58-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9cf58-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cf58-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9cf58-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf58-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cf58-153">CommonParameters</span></span>
<span data-ttu-id="9cf58-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9cf58-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cf58-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cf58-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cf58-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9cf58-156">INPUTS</span></span>

### <span data-ttu-id="9cf58-157">System. String</span><span class="sxs-lookup"><span data-stu-id="9cf58-157">System.String</span></span>

### <span data-ttu-id="9cf58-158">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="9cf58-158">System.Collections.IDictionary</span></span>

### <span data-ttu-id="9cf58-159">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9cf58-159">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9cf58-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cf58-160">OUTPUTS</span></span>

### <span data-ttu-id="9cf58-161">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="9cf58-161">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="9cf58-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="9cf58-162">NOTES</span></span>

## <span data-ttu-id="9cf58-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9cf58-163">RELATED LINKS</span></span>

[<span data-ttu-id="9cf58-164">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9cf58-164">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="9cf58-165">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9cf58-165">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="9cf58-166">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9cf58-166">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="9cf58-167">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9cf58-167">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="9cf58-168">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9cf58-168">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="9cf58-169">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9cf58-169">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="9cf58-170">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9cf58-170">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)
