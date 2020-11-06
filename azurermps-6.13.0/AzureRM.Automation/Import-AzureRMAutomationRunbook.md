---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
ms.openlocfilehash: f6399c35316deb5590eada9eccd474ba7e47b116
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565958"
---
# <span data-ttu-id="903e8-101">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="903e8-101">Import-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="903e8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="903e8-102">SYNOPSIS</span></span>
<span data-ttu-id="903e8-103">Импортирует Runbook автоматизации.</span><span class="sxs-lookup"><span data-stu-id="903e8-103">Imports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="903e8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="903e8-104">SYNTAX</span></span>

```
Import-AzureRmAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="903e8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="903e8-105">DESCRIPTION</span></span>
<span data-ttu-id="903e8-106">Командлет **Import-AzureRmAutomationRunbook** импортирует Runbook службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="903e8-106">The **Import-AzureRmAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="903e8-107">Укажите путь к файлу сценария wps_2 (PS1), который нужно импортировать для wps_2 и wps_2 runbooks для рабочих процессов, (graphrunbook) для графических модулей runbooks или (файл. корректировки) для модулей Runbook 2.</span><span class="sxs-lookup"><span data-stu-id="903e8-107">Specify the path to a wps_2 script (.ps1) file to import for wps_2 and wps_2 Workflow runbooks, (.graphrunbook) file for graphical runbooks, or (.py) file for python 2 runbooks.</span></span> <span data-ttu-id="903e8-108">Для wps_2 Runbook рабочего процесса этот сценарий должен содержать одно определение рабочего процесса wps_2, которое соответствует имени файла.</span><span class="sxs-lookup"><span data-stu-id="903e8-108">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="903e8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="903e8-109">EXAMPLES</span></span>

### <span data-ttu-id="903e8-110">Пример 1: импорт модуля Runbook из файла</span><span class="sxs-lookup"><span data-stu-id="903e8-110">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzureRmAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="903e8-111">Первая команда присваивает переменной $Tags две пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="903e8-111">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="903e8-112">Вторая команда импортирует графический модуль Runbook, именуемый GraphicalRunbook06, в учетную запись автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="903e8-112">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="903e8-113">Команда также назначает теги, хранящиеся в $Tags.</span><span class="sxs-lookup"><span data-stu-id="903e8-113">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="903e8-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="903e8-114">PARAMETERS</span></span>

### <span data-ttu-id="903e8-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="903e8-115">-AutomationAccountName</span></span>
<span data-ttu-id="903e8-116">Указывает имя учетной записи автоматизации, на которую командлет импортирует Runbook.</span><span class="sxs-lookup"><span data-stu-id="903e8-116">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="903e8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="903e8-117">-DefaultProfile</span></span>
<span data-ttu-id="903e8-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="903e8-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="903e8-119">-Описание</span><span class="sxs-lookup"><span data-stu-id="903e8-119">-Description</span></span>
<span data-ttu-id="903e8-120">Задает описание для импортированного Runbook.</span><span class="sxs-lookup"><span data-stu-id="903e8-120">Specifies a description for the imported runbook.</span></span>

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

### <span data-ttu-id="903e8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="903e8-121">-Force</span></span>
<span data-ttu-id="903e8-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="903e8-122">ps_force</span></span>

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

### <span data-ttu-id="903e8-123">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="903e8-123">-LogProgress</span></span>
<span data-ttu-id="903e8-124">Указывает, будет ли Runbook регистрировать данные о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="903e8-124">Specifies whether the runbook logs progress information.</span></span>

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

### <span data-ttu-id="903e8-125">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="903e8-125">-LogVerbose</span></span>
<span data-ttu-id="903e8-126">Указывает, записывает ли Runbook подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="903e8-126">Specifies whether the runbook logs detailed information.</span></span>

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

### <span data-ttu-id="903e8-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="903e8-127">-Name</span></span>
<span data-ttu-id="903e8-128">Указывает имя Runbook, который импортирует этот командлет.</span><span class="sxs-lookup"><span data-stu-id="903e8-128">Specifies the name of the runbook that this cmdlet imports.</span></span>

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

### <span data-ttu-id="903e8-129">-Path</span><span class="sxs-lookup"><span data-stu-id="903e8-129">-Path</span></span>
<span data-ttu-id="903e8-130">Задает путь к файлу PS1 или graphrunbook, который импортирует этот командлет.</span><span class="sxs-lookup"><span data-stu-id="903e8-130">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="903e8-131">-Опубликовано</span><span class="sxs-lookup"><span data-stu-id="903e8-131">-Published</span></span>
<span data-ttu-id="903e8-132">Указывает на то, что этот командлет публикует Runbook, который он импортирует.</span><span class="sxs-lookup"><span data-stu-id="903e8-132">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

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

### <span data-ttu-id="903e8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="903e8-133">-ResourceGroupName</span></span>
<span data-ttu-id="903e8-134">Указывает имя группы ресурсов, для которой этот командлет импортирует Runbook.</span><span class="sxs-lookup"><span data-stu-id="903e8-134">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="903e8-135">-Теги</span><span class="sxs-lookup"><span data-stu-id="903e8-135">-Tags</span></span>
<span data-ttu-id="903e8-136">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="903e8-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="903e8-137">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="903e8-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="903e8-138">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="903e8-138">-Type</span></span>
<span data-ttu-id="903e8-139">Указывает тип Runbook, создаваемый этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="903e8-139">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="903e8-140">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="903e8-140">Valid values are:</span></span>
- <span data-ttu-id="903e8-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="903e8-141">PowerShell</span></span>
- <span data-ttu-id="903e8-142">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="903e8-142">GraphicalPowerShell</span></span>
- <span data-ttu-id="903e8-143">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="903e8-143">PowerShellWorkflow</span></span>
- <span data-ttu-id="903e8-144">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="903e8-144">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="903e8-145">Виде</span><span class="sxs-lookup"><span data-stu-id="903e8-145">Graph</span></span>
- <span data-ttu-id="903e8-146">Python2 значение графика устарело.</span><span class="sxs-lookup"><span data-stu-id="903e8-146">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="903e8-147">Это эквивалентно GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="903e8-147">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

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

### <span data-ttu-id="903e8-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="903e8-148">-Confirm</span></span>
<span data-ttu-id="903e8-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="903e8-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="903e8-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="903e8-150">-WhatIf</span></span>
<span data-ttu-id="903e8-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="903e8-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="903e8-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="903e8-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="903e8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="903e8-153">CommonParameters</span></span>
<span data-ttu-id="903e8-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="903e8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="903e8-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="903e8-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="903e8-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="903e8-156">INPUTS</span></span>

### <span data-ttu-id="903e8-157">System. String</span><span class="sxs-lookup"><span data-stu-id="903e8-157">System.String</span></span>

### <span data-ttu-id="903e8-158">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="903e8-158">System.Collections.IDictionary</span></span>

### <span data-ttu-id="903e8-159">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="903e8-159">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="903e8-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="903e8-160">OUTPUTS</span></span>

### <span data-ttu-id="903e8-161">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="903e8-161">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="903e8-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="903e8-162">NOTES</span></span>

## <span data-ttu-id="903e8-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="903e8-163">RELATED LINKS</span></span>

[<span data-ttu-id="903e8-164">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="903e8-164">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="903e8-165">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="903e8-165">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="903e8-166">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="903e8-166">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="903e8-167">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="903e8-167">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="903e8-168">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="903e8-168">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="903e8-169">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="903e8-169">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="903e8-170">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="903e8-170">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="903e8-171">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="903e8-171">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
