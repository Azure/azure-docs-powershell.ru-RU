---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationRunbook.md
ms.openlocfilehash: e043496f421ec6602fea61018cbaa254192def10
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731577"
---
# <span data-ttu-id="d97a0-101">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d97a0-101">Import-AzAutomationRunbook</span></span>

## <span data-ttu-id="d97a0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d97a0-102">SYNOPSIS</span></span>
<span data-ttu-id="d97a0-103">Импортирует Runbook автоматизации.</span><span class="sxs-lookup"><span data-stu-id="d97a0-103">Imports an Automation runbook.</span></span>

## <span data-ttu-id="d97a0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d97a0-104">SYNTAX</span></span>

```
Import-AzAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d97a0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d97a0-105">DESCRIPTION</span></span>
<span data-ttu-id="d97a0-106">Командлет **Import-AzAutomationRunbook** импортирует Runbook службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="d97a0-106">The **Import-AzAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="d97a0-107">Укажите путь к файлу сценария wps_2 (PS1), который нужно импортировать для wps_2 и wps_2 runbooks для рабочих процессов, (graphrunbook) для графических модулей runbooks или (файл. корректировки) для модулей Runbook 2.</span><span class="sxs-lookup"><span data-stu-id="d97a0-107">Specify the path to a wps_2 script (.ps1) file to import for wps_2 and wps_2 Workflow runbooks, (.graphrunbook) file for graphical runbooks, or (.py) file for python 2 runbooks.</span></span> <span data-ttu-id="d97a0-108">Для wps_2 Runbook рабочего процесса этот сценарий должен содержать одно определение рабочего процесса wps_2, которое соответствует имени файла.</span><span class="sxs-lookup"><span data-stu-id="d97a0-108">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="d97a0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d97a0-109">EXAMPLES</span></span>

### <span data-ttu-id="d97a0-110">Пример 1: импорт модуля Runbook из файла</span><span class="sxs-lookup"><span data-stu-id="d97a0-110">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="d97a0-111">Первая команда присваивает переменной $Tags две пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="d97a0-111">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="d97a0-112">Вторая команда импортирует графический модуль Runbook, именуемый GraphicalRunbook06, в учетную запись автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="d97a0-112">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="d97a0-113">Команда также назначает теги, хранящиеся в $Tags.</span><span class="sxs-lookup"><span data-stu-id="d97a0-113">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="d97a0-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d97a0-114">PARAMETERS</span></span>

### <span data-ttu-id="d97a0-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d97a0-115">-AutomationAccountName</span></span>
<span data-ttu-id="d97a0-116">Указывает имя учетной записи автоматизации, на которую командлет импортирует Runbook.</span><span class="sxs-lookup"><span data-stu-id="d97a0-116">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="d97a0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d97a0-117">-DefaultProfile</span></span>
<span data-ttu-id="d97a0-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d97a0-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d97a0-119">-Описание</span><span class="sxs-lookup"><span data-stu-id="d97a0-119">-Description</span></span>
<span data-ttu-id="d97a0-120">Задает описание для импортированного Runbook.</span><span class="sxs-lookup"><span data-stu-id="d97a0-120">Specifies a description for the imported runbook.</span></span>

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

### <span data-ttu-id="d97a0-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d97a0-121">-Force</span></span>
<span data-ttu-id="d97a0-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="d97a0-122">ps_force</span></span>

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

### <span data-ttu-id="d97a0-123">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="d97a0-123">-LogProgress</span></span>
<span data-ttu-id="d97a0-124">Указывает, будет ли Runbook регистрировать данные о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="d97a0-124">Specifies whether the runbook logs progress information.</span></span>

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

### <span data-ttu-id="d97a0-125">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="d97a0-125">-LogVerbose</span></span>
<span data-ttu-id="d97a0-126">Указывает, записывает ли Runbook подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="d97a0-126">Specifies whether the runbook logs detailed information.</span></span>

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

### <span data-ttu-id="d97a0-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d97a0-127">-Name</span></span>
<span data-ttu-id="d97a0-128">Указывает имя Runbook, который импортирует этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d97a0-128">Specifies the name of the runbook that this cmdlet imports.</span></span>

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

### <span data-ttu-id="d97a0-129">-Path</span><span class="sxs-lookup"><span data-stu-id="d97a0-129">-Path</span></span>
<span data-ttu-id="d97a0-130">Задает путь к файлу PS1 или graphrunbook, который импортирует этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d97a0-130">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="d97a0-131">-Опубликовано</span><span class="sxs-lookup"><span data-stu-id="d97a0-131">-Published</span></span>
<span data-ttu-id="d97a0-132">Указывает на то, что этот командлет публикует Runbook, который он импортирует.</span><span class="sxs-lookup"><span data-stu-id="d97a0-132">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

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

### <span data-ttu-id="d97a0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d97a0-133">-ResourceGroupName</span></span>
<span data-ttu-id="d97a0-134">Указывает имя группы ресурсов, для которой этот командлет импортирует Runbook.</span><span class="sxs-lookup"><span data-stu-id="d97a0-134">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="d97a0-135">-Теги</span><span class="sxs-lookup"><span data-stu-id="d97a0-135">-Tags</span></span>
<span data-ttu-id="d97a0-136">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="d97a0-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d97a0-137">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="d97a0-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d97a0-138">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="d97a0-138">-Type</span></span>
<span data-ttu-id="d97a0-139">Указывает тип Runbook, создаваемый этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="d97a0-139">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="d97a0-140">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="d97a0-140">Valid values are:</span></span>
- <span data-ttu-id="d97a0-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="d97a0-141">PowerShell</span></span>
- <span data-ttu-id="d97a0-142">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="d97a0-142">GraphicalPowerShell</span></span>
- <span data-ttu-id="d97a0-143">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="d97a0-143">PowerShellWorkflow</span></span>
- <span data-ttu-id="d97a0-144">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="d97a0-144">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="d97a0-145">Виде</span><span class="sxs-lookup"><span data-stu-id="d97a0-145">Graph</span></span>
- <span data-ttu-id="d97a0-146">Python2 значение графика устарело.</span><span class="sxs-lookup"><span data-stu-id="d97a0-146">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="d97a0-147">Это эквивалентно GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="d97a0-147">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

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

### <span data-ttu-id="d97a0-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d97a0-148">-Confirm</span></span>
<span data-ttu-id="d97a0-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d97a0-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d97a0-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d97a0-150">-WhatIf</span></span>
<span data-ttu-id="d97a0-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d97a0-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d97a0-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d97a0-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d97a0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d97a0-153">CommonParameters</span></span>
<span data-ttu-id="d97a0-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d97a0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d97a0-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d97a0-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d97a0-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d97a0-156">INPUTS</span></span>

### <span data-ttu-id="d97a0-157">System. String</span><span class="sxs-lookup"><span data-stu-id="d97a0-157">System.String</span></span>

### <span data-ttu-id="d97a0-158">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="d97a0-158">System.Collections.IDictionary</span></span>

### <span data-ttu-id="d97a0-159">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d97a0-159">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d97a0-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d97a0-160">OUTPUTS</span></span>

### <span data-ttu-id="d97a0-161">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="d97a0-161">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="d97a0-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="d97a0-162">NOTES</span></span>

## <span data-ttu-id="d97a0-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d97a0-163">RELATED LINKS</span></span>

[<span data-ttu-id="d97a0-164">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d97a0-164">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="d97a0-165">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d97a0-165">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="d97a0-166">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d97a0-166">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="d97a0-167">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d97a0-167">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="d97a0-168">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d97a0-168">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="d97a0-169">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d97a0-169">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="d97a0-170">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d97a0-170">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="d97a0-171">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d97a0-171">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)
