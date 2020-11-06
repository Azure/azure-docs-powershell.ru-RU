---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
ms.openlocfilehash: d28166ec0a9a339017aa11bc30c0c5f0394afe94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565691"
---
# <span data-ttu-id="eb141-101">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="eb141-101">Import-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="eb141-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb141-102">SYNOPSIS</span></span>
<span data-ttu-id="eb141-103">Импортирует Runbook автоматизации.</span><span class="sxs-lookup"><span data-stu-id="eb141-103">Imports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb141-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb141-104">SYNTAX</span></span>

```
Import-AzureRmAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb141-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb141-105">DESCRIPTION</span></span>
<span data-ttu-id="eb141-106">Командлет **Import-AzureRmAutomationRunbook** импортирует Runbook службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="eb141-106">The **Import-AzureRmAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="eb141-107">Укажите путь к файлу сценария wps_2 (PS1), который нужно импортировать для wps_2 и wps_2 runbooks рабочего процесса, или в графический файл Runbook (graphrunbook) для графических модулей Runbook.</span><span class="sxs-lookup"><span data-stu-id="eb141-107">Specify the path to a wps_2 script (.ps1 ) file to import for wps_2 and wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file for graphical runbooks.</span></span> <span data-ttu-id="eb141-108">Имя файла становится именем Runbook.</span><span class="sxs-lookup"><span data-stu-id="eb141-108">The name of the file becomes the name of the runbook.</span></span> <span data-ttu-id="eb141-109">Для wps_2 Runbook рабочего процесса этот сценарий должен содержать одно определение рабочего процесса wps_2, которое соответствует имени файла.</span><span class="sxs-lookup"><span data-stu-id="eb141-109">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="eb141-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb141-110">EXAMPLES</span></span>

### <span data-ttu-id="eb141-111">Пример 1: импорт модуля Runbook из файла</span><span class="sxs-lookup"><span data-stu-id="eb141-111">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzureRmAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="eb141-112">Первая команда присваивает переменной $Tags две пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="eb141-112">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="eb141-113">Вторая команда импортирует графический модуль Runbook, именуемый GraphicalRunbook06, в учетную запись автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="eb141-113">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="eb141-114">Команда также назначает теги, хранящиеся в $Tags.</span><span class="sxs-lookup"><span data-stu-id="eb141-114">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="eb141-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb141-115">PARAMETERS</span></span>

### <span data-ttu-id="eb141-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="eb141-116">-AutomationAccountName</span></span>
<span data-ttu-id="eb141-117">Указывает имя учетной записи автоматизации, на которую командлет импортирует Runbook.</span><span class="sxs-lookup"><span data-stu-id="eb141-117">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="eb141-118">-Описание</span><span class="sxs-lookup"><span data-stu-id="eb141-118">-Description</span></span>
<span data-ttu-id="eb141-119">Задает описание для импортированного Runbook.</span><span class="sxs-lookup"><span data-stu-id="eb141-119">Specifies a description for the imported runbook.</span></span>

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

### <span data-ttu-id="eb141-120">-Force</span><span class="sxs-lookup"><span data-stu-id="eb141-120">-Force</span></span>
<span data-ttu-id="eb141-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="eb141-121">ps_force</span></span>

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

### <span data-ttu-id="eb141-122">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="eb141-122">-LogProgress</span></span>
<span data-ttu-id="eb141-123">Указывает, будет ли Runbook регистрировать данные о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="eb141-123">Specifies whether the runbook logs progress information.</span></span>

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

### <span data-ttu-id="eb141-124">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="eb141-124">-LogVerbose</span></span>
<span data-ttu-id="eb141-125">Указывает, записывает ли Runbook подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="eb141-125">Specifies whether the runbook logs detailed information.</span></span>

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

### <span data-ttu-id="eb141-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eb141-126">-Name</span></span>
<span data-ttu-id="eb141-127">Указывает имя Runbook, который импортирует этот командлет.</span><span class="sxs-lookup"><span data-stu-id="eb141-127">Specifies the name of the runbook that this cmdlet imports.</span></span>

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

### <span data-ttu-id="eb141-128">-Path</span><span class="sxs-lookup"><span data-stu-id="eb141-128">-Path</span></span>
<span data-ttu-id="eb141-129">Задает путь к файлу PS1 или graphrunbook, который импортирует этот командлет.</span><span class="sxs-lookup"><span data-stu-id="eb141-129">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="eb141-130">-Опубликовано</span><span class="sxs-lookup"><span data-stu-id="eb141-130">-Published</span></span>
<span data-ttu-id="eb141-131">Указывает на то, что этот командлет публикует Runbook, который он импортирует.</span><span class="sxs-lookup"><span data-stu-id="eb141-131">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

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

### <span data-ttu-id="eb141-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb141-132">-ResourceGroupName</span></span>
<span data-ttu-id="eb141-133">Указывает имя группы ресурсов, для которой этот командлет импортирует Runbook.</span><span class="sxs-lookup"><span data-stu-id="eb141-133">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="eb141-134">-Теги</span><span class="sxs-lookup"><span data-stu-id="eb141-134">-Tags</span></span>
<span data-ttu-id="eb141-135">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="eb141-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="eb141-136">Например:</span><span class="sxs-lookup"><span data-stu-id="eb141-136">For example:</span></span>

<span data-ttu-id="eb141-137">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="eb141-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="eb141-138">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="eb141-138">-Type</span></span>
<span data-ttu-id="eb141-139">Указывает тип Runbook, создаваемый этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="eb141-139">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="eb141-140">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="eb141-140">Valid values are:</span></span>

- <span data-ttu-id="eb141-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="eb141-141">PowerShell</span></span>
- <span data-ttu-id="eb141-142">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="eb141-142">GraphicalPowerShell</span></span>
- <span data-ttu-id="eb141-143">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="eb141-143">PowerShellWorkflow</span></span>
- <span data-ttu-id="eb141-144">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="eb141-144">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="eb141-145">Виде</span><span class="sxs-lookup"><span data-stu-id="eb141-145">Graph</span></span>

<span data-ttu-id="eb141-146">Диаграмма значений устарела.</span><span class="sxs-lookup"><span data-stu-id="eb141-146">The value Graph is obsolete.</span></span>
<span data-ttu-id="eb141-147">Это эквивалентно GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="eb141-147">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb141-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb141-148">-Confirm</span></span>
<span data-ttu-id="eb141-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eb141-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb141-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb141-150">-WhatIf</span></span>
<span data-ttu-id="eb141-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eb141-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb141-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eb141-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb141-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb141-153">-DefaultProfile</span></span>
<span data-ttu-id="eb141-154">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eb141-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb141-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb141-155">CommonParameters</span></span>
<span data-ttu-id="eb141-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb141-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb141-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb141-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb141-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb141-158">INPUTS</span></span>

## <span data-ttu-id="eb141-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb141-159">OUTPUTS</span></span>

### <span data-ttu-id="eb141-160">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="eb141-160">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="eb141-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb141-161">NOTES</span></span>

## <span data-ttu-id="eb141-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb141-162">RELATED LINKS</span></span>

[<span data-ttu-id="eb141-163">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="eb141-163">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="eb141-164">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="eb141-164">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="eb141-165">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="eb141-165">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="eb141-166">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="eb141-166">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="eb141-167">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="eb141-167">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="eb141-168">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="eb141-168">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="eb141-169">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="eb141-169">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="eb141-170">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="eb141-170">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
